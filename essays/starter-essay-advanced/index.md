---
title: Starter Essay Advanced
author: Your Name
layout: essay
date: 2026-11-12
header-title: Your Campus Topic
header-subtitle: Replace this with a short phrase if your essay needs one
category: Starter Essay
popup-teaser: Replace this with one clear sentence that makes readers want to know more.
card-description: Replace this with two sentences that summarize the story your essay tells and why it matters.
card-image: /essays/starter-essay-advanced/images/sample-archive-photo.jpg
header-image: images/sample-archive-photo.jpg
header-caption: Replace with a short source note for the header image. Plain text only here, no links.
header-position: center center
start: 1950
---

This advanced starter contains one working example of every component the site offers. It is a parts catalog, not a model essay. **Delete every component you do not need.** A clean essay with four well-chosen images beats a cluttered one that uses all of these at once.

Keep this lead paragraph first, before any heading or component. Open with a scene, a question, or a problem, and give readers a reason to care about your topic.

## Opening Historical Problem

Use this section to set up the historical problem your essay investigates. What seems obvious about your topic today? What does the archive reveal that complicates that first impression?

<!-- Pullquote. Keep at least two sentences of body text between a heading and a pullquote.
     class can be left, right, or center. -->

{% include typography/aside.html
  class="right"
  text="Replace this pullquote with one vivid sentence from your essay or from a primary source."
%}

Your prose should still carry the main argument. Pullquotes are highlights, not substitutes for explanation. Use them sparingly when a phrase or source deserves extra attention.

When you are quoting a historical source at more length, use a Markdown blockquote instead, and attach a footnote to the end of it:

> Replace this with a quotation from a document, letter, newspaper, or oral history that is worth reading in full. Blockquotes work best when the language itself is the evidence.[^quotesource]

## Archival Evidence

Use this section to show readers the evidence behind your interpretation. Explain what you found, where you found it, and how it changed what you thought you knew.

<!-- Full-width figure: the default for any landscape image wider than about 700px. -->

{% include images/figure.html
  class="img-center"
  width="100%"
  caption="Replace this caption. Explain why the image matters, then cite it: [Center for Southwest Research](https://econtent.unm.edu/), collection and box number."
  image-path="images/sample-archive-photo.jpg"
%}

<!-- Portrait documents are the exception to the full-width rule. A tall scan at 100%
     renders over 1200px tall. Center it near 55%. Keep it centered, never floated. -->

{% include images/figure.html
  class="img-center"
  width="55%"
  caption="Replace this caption. Tall documents like ledgers, letters, and clippings belong at about 55%, centered."
  image-path="images/sample-primary-source.jpg"
%}

<!-- Image grid: two or three images that should be read together as one evidence set.
     Use images of the same shape. Matched portrait scans work best. Do not mix a wide
     photo and a tall document in the same grid; stack those at 100% instead. -->

{% assign evidence_images =
"images/sample-archive-photo.jpg,
images/sample-second-photo.jpg" | split: ','
%}

{% assign evidence_captions =
"Replace this with a caption for the first image, including source information.|
Replace this with a caption for the second image. Grid captions accept [Markdown links](https://econtent.unm.edu/)." | split: '|'
%}

{% include images/image-grid.html
  images=evidence_images
  captions=evidence_captions
  columns=2
%}

## Change Over Time

Use this section to explain chronology. What changed, when, and why? What stayed the same? Which people or institutions had the power to shape what happened?

<!-- Before/after slider. Both images must be roughly the same shape, because the slider
     is sized from the first image and crops the second one to match. -->

{% include images/juxtapose.html
  image1="images/sample-archive-photo.jpg"
  image2="images/sample-second-photo.jpg"
  caption="Replace this with a caption that explains what readers should notice in the comparison, and cite both images."
%}

<!-- Carousel: three or more images that belong together but do not each need a paragraph.
     Captions are plain text here: Markdown links will NOT render, so spell out the source. -->

{% assign carousel_images =
"images/sample-archive-photo.jpg,
images/sample-second-photo.jpg,
images/sample-primary-source.jpg" | split: ','
%}

{% assign carousel_headers =
"Replace with a short slide title,
Replace with a short slide title,
Replace with a short slide title" | split: ','
%}

{% assign carousel_captions =
"Replace this caption. Every slide needs one. Center for Southwest Research, collection name, box number.|
Replace this caption. Explain what this slide adds to the story. Collection name, box number.|
Replace this caption. Plain text only, so write the source out instead of linking. Collection name, box number." | split: '|'
%}

{% include images/carousel.html
  images=carousel_images
  headers=carousel_headers
  captions=carousel_captions
%}

## ScrollStory Components

These components break out of the text column and take over the screen. They are dramatic, and they are easy to overuse. One scrollstory section in an essay is usually plenty, and it should carry a moment that deserves the emphasis: a building going up, a protest, a demolition, a plan that was never built.

Background images cannot carry a caption the way a figure does, so put the source note in the surrounding prose or in the text box itself.

<!-- Single background image with a text box scrolling over it. Self-contained: no closing
     include needed. Pass height and pre-box-space WITH units. -->

{% include scrollybox/bg.html
  height="220vh"
  image-url="images/sample-archive-photo.jpg"
  position="center center"
  pre-box-space="100vh"
  font-size="200%"
  line-height="150%"
  box-content="Replace this with one or two sentences worth reading against a full-screen image. Keep it short. Long paragraphs do not work at this size."
%}

Back in the normal text column. Explain what the reader just saw and why you gave it a whole screen.

The next component is different: it holds one background image while several screens of text scroll over it, and the image **switches** partway through. It opens a container that stays open until you close it, so the closing include is required.

<!-- SCROLLY BOX WITH IMAGE SWITCHING
     bg-multi-long opens a container that MUST be closed with bg-multi-long-close.
     Everything between them scrolls over the background image.
     pre-box-space here is a bare number (no units), unlike bg.html above. -->

{% include scrollybox/bg-multi-long.html
  bg-id="bg1"
  image-url="images/sample-archive-photo.jpg"
  pre-box-space="0"
  font-size="150%"
  line-height="120%"
%}

Replace this with the text that should scroll over the first background image. Write in short paragraphs. Text set at this size fills the screen quickly, so a few sentences go a long way.

This is the place for narrative momentum rather than dense citation. Save the box numbers for your captions and bibliography.

{% include scrollybox/bg-switch.html
  bg-id="bg1"
  switch-id="switch1"
  image-url="images/sample-second-photo.jpg"
%}

Replace this with the text that should scroll over the second image. The switch happens where the include sits, so put it at the moment your story actually turns.

Add another `bg-switch` include for a third image if your story needs one. Give each switch a unique `switch-id` and keep the same `bg-id`.

{% include scrollybox/bg-multi-long-close.html %}

Back in the normal text column again. If your page suddenly looks broken from this point down, you almost certainly deleted or lost the `bg-multi-long-close` include above.

<!-- Jumbotron: a full-bleed banner image with optional text over it.
     Pass height WITH units. -->

{% include images/jumbotron.html
  height="55vh"
  image-path="images/sample-second-photo.jpg"
  box-align="left"
  title="Replace this title"
  text="Replace this with a sentence that belongs over a full-width banner, or delete both title and text for a plain banner image."
  caption="Replace this with a source note for the banner image."
%}

## Why This History Matters

End by returning to the present. How should readers see this campus place, person, organization, object, or event differently after reading your essay?[^archivegap]

Footnotes are optional but useful when a specific claim needs a specific source and the bibliography is too blunt an instrument. Every footnote has two halves: a marker like `[^archivegap]` where the claim appears, and a matching definition at the bottom of the file. The numbering happens automatically.

[^quotesource]: Replace this with the source for the blockquote above: collection name, box, folder, and a link if the item is digitized.
[^archivegap]: Replace this with a footnote. These definitions live at the bottom of the file no matter where their markers appear.

{% capture bibliography %}
- Replace this with a book, article, archival collection, or digital source. Include enough detail that someone else could find it.
- Replace this with another source.
- Replace this with another source.
{% endcapture %}

{% include typography/bibliography.html
  title="Bibliography"
  content=bibliography
%}
