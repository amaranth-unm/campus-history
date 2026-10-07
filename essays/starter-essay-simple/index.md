---
title: Starter Essay Simple
author: Your Name
layout: essay
date: 2026-11-12
header-title: Your Campus Topic
category: Starter Essay
popup-teaser: Replace this with one clear sentence that makes readers want to know more.
card-description: Replace this with two sentences that summarize the story your essay tells and why it matters.
card-image: /essays/starter-essay-simple/images/sample-archive-photo.jpg
header-image: images/sample-archive-photo.jpg
header-caption: Replace with a short source note for the header image. Plain text only here, no links.
start: 1950
---

This first paragraph should give readers a quick way into your topic. Start with a scene, a question, a surprising fact, or a problem your essay will explain. You do not need to summarize everything here. Help the reader understand why this campus place, person, organization, object, or event deserves attention.

Keep the above lead paragraph first. Do not put an image, a heading, or any other component above it.

## Main Story

Use this section to tell the most important part of the history. Keep paragraphs short enough for online reading. A good paragraph usually develops one idea, source, moment, or change over time.

Use specific evidence from the archive. Name dates, people, places, decisions, conflicts, renovations, controversies, or missing records when they matter. The goal is not just to list facts. The goal is to explain what those facts reveal about UNM and its history.

<!-- Full-width figure. This is the default for any landscape photo wider than about 700px. -->

{% include images/figure.html
  class="img-center"
  width="100%"
  caption="Replace this caption. Say why the image matters, not just what it shows, then cite where you found it: [Center for Southwest Research](https://econtent.unm.edu/), collection and box number."
  image-path="images/sample-archive-photo.jpg"
%}

Every image needs a caption, including this one. A caption should explain what the reader should notice and where the image came from. Captions accept Markdown, so use `[source](https://example.com/)` to link to a digital collection whenever the image has an online home.

## What Changed

Use this section to explain change over time. What did your topic used to be? How did people use it, describe it, fund it, argue about it, rename it, neglect it, preserve it, or forget it?

This is a good place to connect your specific topic to a larger campus pattern: enrollment growth, architecture, student life, race, gender, labor, protest, public memory, administration, technology, or access.

<!-- Carousel: use when you have three or more images that belong together but do not
     each need their own paragraph. Images are split on commas, captions on the | character.
     Carousel captions are plain text: Markdown links will NOT work here, so write out
     the collection name and box number instead of linking. -->

{% assign images =
"images/sample-archive-photo.jpg,
images/sample-second-photo.jpg,
images/sample-primary-source.jpg" | split: ','
%}

{% assign headers =
"Replace with a short slide title,
Replace with a short slide title,
Replace with a short slide title" | split: ','
%}

{% assign captions =
"Replace this caption. Explain what this slide shows and why it matters. Center for Southwest Research, collection name, box number.|
Replace this caption. Every slide needs one. Center for Southwest Research, collection name, box number.|
Replace this caption. Plain text only in carousels, so spell out the source instead of linking. Center for Southwest Research, collection name, box number." | split: '|'
%}

{% include images/carousel.html
  images=images
  headers=headers
  captions=captions
%}

Delete the carousel if you do not have a set of images that works this way. Three related photographs, a series of floor plans, or a run of newspaper clippings are all good candidates. Two images that need to be compared directly are usually better as a pair than as a carousel.

## Evidence

Use this section to show readers a document, not just a photograph. Scanned letters, meeting minutes, ledgers, clippings, and blueprints all reward close looking, and they prove you spent time in the boxes.

<!-- Portrait documents are the exception to the full-width rule. A tall scan at 100%
     is over 1200px tall and swallows the screen, so center it and leave it near 55%.
     Keep it centered, not floated. -->

{% include images/figure.html
  class="img-center"
  width="55%"
  caption="Replace this caption. Tell readers what to notice in the document and why it changes how they should understand your topic. Cite the collection, box, and folder."
  image-path="images/sample-primary-source.jpg"
%}

Explain what the document says, what it does not say, and how it fits the story. A source you actually read and explain is worth more than three you only mention.

## Why This History Matters

End by returning to the present. How should readers see this campus place, person, organization, object, or event differently after reading your essay? Point to continued use, memory, loss, gaps in the archive, or campus change rather than announcing a conclusion.

{% capture bibliography %}
- Replace this with your first source. Include enough detail that someone else could find it: collection name, box, and folder for archival material.
- Replace this with your second source.
- Replace this with your third source.
{% endcapture %}

{% include typography/bibliography.html
  title="Bibliography"
  content=bibliography
%}
