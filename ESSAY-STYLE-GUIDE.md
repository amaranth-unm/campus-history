# Campus History Essay Style Guide

This guide is for light editorial normalization of student essay pages. The goal is to make the collection feel cohesive and readable while preserving student authorship, argument, and voice.

## Core Principle

Keep the student work recognizably student-authored. Improve the container, formatting, and readability; do not rewrite the essay into a new voice.

All essay content should be written in Markdown or use established Xanthan framework includes and patterns. Avoid raw HTML unless the project already provides a Xanthan include or layout pattern that requires it.

## Allowed Changes

- Fix Markdown formatting.
- Break up very long paragraphs into shorter units appropriate for online reading, using the student's existing transitions and topic shifts.
- Normalize heading levels, usually `##` for major sections and `###` for subsections.
- Normalize bibliography, works cited, references, or further reading headings.
- Convert bibliography-style source lists into the collapsible `typography/bibliography.html` include when the section is mostly citations rather than substantive prose.
- Convert footnotes to the site's Littlefoot-compatible Markdown footnote format when the intended citation is clear.
- Convert bare URLs into Markdown links when helpful.
- Fix obvious typos, repeated words, spacing problems, and broken punctuation.
- Remove duplicate blank lines or inconsistent whitespace.
- Standardize image includes, captions, and nearby spacing when the intended image/caption is clear.
- Move a top-level `#` heading that appears directly under the page header into the front matter `header-title` field, then remove that body `#` heading so the title displays on the hero image instead of repeating below it.
- Add or normalize a front matter `category` field so the page-header eyebrow identifies the type of campus place, such as `Dormitory`, `Classroom Building`, `Student Resource`, `Landscape`, or `Public Art`.
- Ensure the first content after the page header is a clear introductory lead paragraph: a short vignette or scene-setting entry point that orients the reader before section headings, images, pullquotes, or other components appear.
- Add a neutral opening `##` section heading when an essay starts directly with body text after the page header.
- Preserve front matter unless a formatting error prevents the page from working.

## Common Student Formatting Issues To Fix

- Bibliography, works cited, references, or further reading sections should be formatted as Markdown lists, with each source as its own bullet point.
- Bibliography-style source lists should usually be placed in a collapsible bibliography drawer using `typography/bibliography.html`. Preserve the source text and use the drawer title `Sources`, `Bibliography`, `Works Cited`, or `References` to match the original section.
- Long bibliography entries should remain one bullet point per source, even if the line wraps visually.
- Visible URLs in bibliography entries should be folded into the preceding citation text as regular Markdown links when the destination is clear, rather than left as raw URLs.
- Multiple sources run together in one paragraph should be split into separate bullet points.
- Long paragraphs should be divided where the student shifts evidence, example, chronology, place, or subtopic. Do not rewrite the prose just to make shorter paragraphs.
- Section headings should use Markdown heading syntax, not bold text standing in for a heading.
- Essays should not use a body-level `#` heading immediately under the page header. Put that text in `image-title` in the YAML front matter so it appears over the header image.
- Essays with a hero image should include a `category` in front matter. This category is used as the page-header eyebrow, replacing generic site text like `Campus History`.
- Essays should begin with one lead paragraph immediately after the page header. This paragraph should offer a quick vignette, scene, question, or orientation to the essay's historical stakes. Do not place images, carousels, pullquotes, raw HTML components, or section headings before this lead paragraph.
- After the lead paragraph, essays may move into `##` section headings. If the essay previously started directly with a heading or image, move or draft a restrained lead from the student's existing opening material without inventing a new argument.
- Remove `<br>` tags immediately before headings; use normal Markdown spacing instead.
- Lists should use Markdown bullets or numbered lists, not manually typed numbers in paragraphs.
- Image placement should follow Xanthan image includes or existing project patterns, not ad hoc HTML.
- Image include widths should not be smaller than `50%` on essay pages. If an existing figure uses `width="33%"`, `width="40%"`, or another smaller value, raise it to at least `50%` unless there is a clear visual reason to ask first.
- Wide horizontal images should default to `width="100%"`, especially maps, plans, newspaper clippings, architectural drawings, construction photos, panoramas, and other visual evidence readers may need to inspect. Treat a strong landscape ratio, roughly `1.6:1` or wider, as a signal that the image should span the full content width.
- Only keep a wide image below `100%` when there is a detectable reason: the source file is too small or blurry at full width, the image is decorative rather than evidentiary, the important detail is already legible at a smaller size, or the image is intentionally paired with adjacent prose or another image. In those cases, use at least `50%` and place text beside it only when the surrounding paragraph directly discusses the image.
- Do not preserve a `48%`, `50%`, or `60%` width just because it already exists. If the image is wide and evidentiary, make it full width unless one of the exceptions above applies.
- Use the `images/image-grid.html` include when two or three related images should be read together as one visual evidence set, such as matching clippings, paired invitations, before/after documents, or two images that were previously floated at `48%` only to appear side by side.
- Use individual `images/figure.html` includes with `img-left` or `img-right` when an image is meant to sit beside and support a specific paragraph of prose. Do not use side-by-side floated figures just to create a gallery; use `image-grid` or `carousel` instead.
- Captions should be kept close to the image they describe and formatted consistently.
- URLs in image captions should be encapsulated as a `[source](URL)` link in the caption.
- Image paths should resolve from the essay page directory. For essay-local files, use paths like `images/example.jpg`, not duplicated folder paths such as `popejoy-hall/example.jpg` or `essays/popejoy-hall/images/example.jpg`.
- Check that every `image-path` value points to an existing file with the exact same spelling, extension, capitalization, spaces, and punctuation. Broken images are often caused by small path mismatches rather than missing files.
- Images should not appear immediately before a heading; move the image to after the heading so the section title introduces the visual material.
- `##` section headings should always come before any image include that belongs to that section. If an image include is immediately followed by an `##` heading, reverse the order unless the image is intentionally ending the previous section.
- Carousel includes must be checked in the browser after standardization. Confirm that all carousel images render, arrows/pagination work, captions appear with the correct slide, and multiple carousels on the same page use unique `id` values.
- Legacy raw carousel markup must be converted to the standard include. Replace blocks like `<div class="carousel"><div><img src="..."></div>...</div>` with `{% include images/carousel.html %}` using assigned `images`, optional `headers`, optional `captions`, and a unique `id` when more than one carousel appears on the page. Do not rely on hidden JavaScript fixes for old carousel markup.
- Pullquotes should not be the first thing after a heading. Keep at least two sentences of body text between a heading and a pullquote so the section has enough typographic breathing room.
- Footnotes should use the site's Littlefoot-compatible Markdown footnote format, with an inline marker such as `[^1]` and a matching footnote definition such as `[^1]: Source text`.
- Footnote markers should stay attached to the paragraph or sentence they support, not sit alone on a separate line.
- Extra blank lines, inconsistent indentation, and trailing spaces should be cleaned up.
- Object or essay links should use Markdown links or established Xanthan include patterns.
- Do not use raw HTML for layout, spacing, images, captions, or lists when Markdown or a Xanthan include can do the job.
- Do not hide substantive concluding prose in the bibliography drawer; only collapse source lists and citation material.

## Light Prose Edits

Use light prose edits to make essays easier to read online while keeping the student's voice, argument, and level of certainty intact. Edit the sentence's path, not its destination.

- Preserve vivid, personal, funny, or distinctive student phrasing when it helps the essay feel authored. Fix the mechanics around it, but do not sand down personality just to make the collection sound uniform.
- Remove assignment scaffolding when it is not doing meaningful work. Phrases such as `this essay will`, `the purpose of this page is`, `in this article`, or `in conclusion` can usually be cut or replaced with a direct statement about the place, object, source, or historical stakes.
- Keep first person when it reveals research process, archival surprise, interpretive humility, or a meaningful encounter with evidence. Trim first person when it only narrates ordinary workflow or delays the historical point.
- Break long paragraphs at natural turns: a new date or period, a new source, a new person, a new building use, a new example, or a shift from evidence to interpretation.
- Split overloaded sentences that stack several clauses with `which`, `while`, `causing`, `because`, or repeated commas. Prefer two clear student-authored sentences over one tangled sentence.
- Prefer concrete subjects and verbs. When a sentence begins with `there is`, `there are`, `it is important`, or `this shows`, revise only as much as needed to name the actor, source, building, event, or consequence.
- Replace vague intensifiers and filler when the meaning is clear. Words such as `very`, `really`, `a lot`, `things`, `stuff`, `interesting`, `important`, and `unique` should usually point to specific evidence: enrollment growth, funding, architecture, activism, controversy, preservation, demolition, or archival absence.
- Normalize time language. Prefer specific dates, decades, or periods over vague phrases such as `today`, `currently`, `back then`, `at this time`, or `nowadays` when a more precise reference is available.
- Clarify chronology when the prose jumps between periods. Add or preserve light transition phrases such as `By 1949`, `In the early 1970s`, `After the renovation`, or `Decades later` when they help readers follow the sequence.
- Keep hedging when the archive is genuinely incomplete. Do not convert `seems`, `suggests`, `may have`, or `more research is needed` into certainty unless the evidence clearly supports the stronger claim.
- Make conclusions land on stakes rather than summary. A closing paragraph can point to continued use, memory, loss, archival gaps, campus change, or the building's present-day meaning without announcing `in conclusion`.
- Correct typos, repeated words, apostrophes, capitalization, and grammar when the intended meaning is clear. Flag sentences where the fix would change the claim, interpretation, or tone.

## Avoid

- Do not rewrite thesis statements or major claims.
- Do not add new evidence, interpretation, or scholarly framing.
- Do not substantially reorder the argument.
- Do not polish every awkward phrase just to make the essays sound uniform.
- Do not remove student tone, uncertainty, or stylistic variation unless it creates a readability or formatting problem.
- Do not change citations or bibliography entries beyond formatting unless the source information is clearly broken.

## Flag Or Ask First

Ask before making a change when you encounter a nonstandard, unusual, or ambiguous issue. This includes:

- A factual claim that seems wrong but is not simply a typo.
- A citation that is missing, incomplete, or difficult to match to a source.
- A paragraph or section whose meaning is unclear.
- A quotation that may be inaccurate or missing attribution.
- An image, object, or essay link that seems mismatched.
- A section that appears duplicated but may have been intentional.
- A major structure problem that would require moving sections around.
- Any change that would alter the student's argument, evidence, or interpretive emphasis.

When in doubt, preserve the original text and leave a note or ask for direction.

## Checklist For Each Essay

- Front matter is intact and valid.
- Front matter includes a `header-title` when the page has a hero image; this should contain the essay/building title that displays over the image.
- Front matter includes a normalized `category` for the page-header eyebrow.
- Any body-level `#` heading immediately below the page header has been converted to `header-title` and removed from the body.
- The first body element after the page header is a clear lead paragraph, not an image, carousel, pullquote, raw HTML block, or heading.
- Title, author, object links, and metadata are preserved.
- Paragraphs are sized for online reading without changing the student's argument, sequence, or voice.
- Heading levels are consistent.
- The lead paragraph provides a quick vignette or scene-setting introduction and receives the site's special first-paragraph typography.
- Section headings begin after the lead paragraph, not before it.
- Images and captions are formatted consistently.
- All `image-path` values resolve to existing files, with no duplicated essay folder segments or capitalization/extension mismatches.
- Figure include widths are `50%` or larger, except for explicit full-width/mobile behavior or an unusual case that has been flagged.
- Wide horizontal images, roughly `1.6:1` or wider, are set to `width="100%"` unless there is a detectable reason to keep them smaller, such as low resolution, blur, decorative use, or a direct text-and-image pairing.
- Related side-by-side images use `images/image-grid.html` instead of separate floated `48%` figures when they function as one evidence set.
- No image include appears immediately before an `##` heading unless it clearly belongs to the previous section and has been flagged as intentional.
- Carousel images have been verified in the browser, including image loading, controls, captions, and unique IDs when more than one carousel appears on the page.
- No legacy raw `<div class="carousel">` image blocks remain; all carousels use the standard `images/carousel.html` include.
- Pullquotes are introduced by at least two sentences after a heading.
- Footnotes, citations, and bibliography sections are readable and consistent.
- Footnotes use the site's Littlefoot-compatible Markdown footnote format.
- Footnote markers are attached to their relevant paragraph or sentence, not isolated on separate lines.
- Bibliography-style sections use one Markdown bullet point per source.
- Bibliography-style source lists are collapsed with `typography/bibliography.html` unless there is a reason to keep them visible.
- Content uses Markdown or established Xanthan framework patterns, not ad hoc HTML.
- Visible bibliography URLs are folded into the preceding citation text as Markdown links where appropriate.
- No new claims, sources, or interpretations have been added.
- Any unusual or ambiguous issue has been flagged instead of silently changed.

## Page Header Categories

Use a short, readable category in front matter to identify the type of campus place. The category should orient readers without overexplaining the essay.

Preferred categories:

- `Academic Building`
- `Administration`
- `Arts Venue`
- `Athletics`
- `Campus Services`
- `Classroom Building`
- `Dining`
- `Dormitory`
- `Historic Building`
- `Landscape`
- `Museum`
- `Office`
- `Public Art`
- `Student Resource`

When standardizing an essay, choose the closest category from this list. If none fits, use a concise title-case category and flag it for review rather than inventing several near-duplicates. For example, prefer `Dormitory` over separate variants like `Dorm`, `Residence Hall`, or `Student Housing` unless the project later decides to expand the vocabulary.

## Bibliography Drawer Pattern

Use this pattern to collapse source lists without asking students to write custom HTML:

```liquid
{% capture bibliography %}
- Source one.
- Source two.
- Source three.
{% endcapture %}

{% include typography/bibliography.html
  title="Sources"
  content=bibliography
%}
```

Use `title="Bibliography"`, `title="Works Cited"`, or `title="References"` when that better matches the original essay. Keep one Markdown bullet per source. If the section includes reflective prose, acknowledgments, or a conclusion, leave that prose outside the drawer.
