---
# Change these five lines as soon as you copy this starter.
title: Mitchell Hall
author: Alex Roberson
category: Public Art                  # change to a category from the student guide
header-image: mitchell-hall2.jpg   # the filename of your own image
header-caption: New Mexico's Digital Collection
# Fill these in later, once your research is under way.
card-description: Mitchell Hall stands as one of the institution’s oldest, most heavily utilized general-education classroom facilities. Over its seventy-five-year existence, the building has served as a rite of passage for generations of undergraduate students navigating core academic prerequisites.
start:                                   # the year your story begins, shown on the map

# Leave this line as it is.
layout: essay
---

## Main Story

Located on the central campus of the University of New Mexico (UNM) in Albuquerque, Mitchell Hall stands as one of the institution’s oldest, most heavily utilized general-education classroom facilities. Over its seventy-five-year existence, the building has served as a rite of passage for generations of undergraduate students navigating core academic prerequisites. Its creation and subsequent modernization mirror the university's broader mid-century post-war growth and its late-2000s transition toward sustainable, technologically advanced infrastructure.

Design, Naming, and Mid-Century Construction (1950–1951)

Mitchell Hall was constructed in 1950 and opened for widespread campus use during the 1951 academic year to meet the educational needs of a booming student body. The facility was named in honor of Dean Lynn B. Mitchell, a prominent institutional pioneer who originally joined the university in 1912. Mitchell was a dedicated professor of Latin and Greek languages, earning the campus nickname "The Old Roman," and served as a foundational academic dean during the university's formative decades.
Architecturally, the building represents a crucial evolutionary phase in the career of legendary regional architect John Gaw Meem, who partnered with the firm Zehner, Holien and Associates to execute the project. Unlike Meem's more heavily ornamented, highly romantic Spanish-Pueblo Revival masterpieces from the 1930s (such as the nearby Zimmerman Library), Mitchell Hall emerged as a streamlined, two-story concrete block structure. While it retained Meem’s signature earthy color palette, solid massing, and flat-roofed profile, it leaned heavily toward functional, institutional simplicity—a programmatic necessity dictated by tight post-war budgets and the immediate demand for multi-department classrooms.

Decades of General Education and Spatial Shifts (1950s–1970s)

Upon its completion, Mitchell Hall was celebrated as one of the most modern instructional venues on campus, outfitted with contemporary audio-visual and lecturing tools captured in mid-century promotional postcards. For decades, it remained the focal point of UNM's foundational curriculum, hosting key TA sessions, introductory lectures, and iconic courses like the history of math taught by popular educators like Dr. Merle Mitchell.
The physical environment surrounding Mitchell Hall shifted dramatically during the mid-1970s. Prior to 1974, a bustling student parking lot sat directly adjacent to the building, and Yale Boulevard openly cut through the center of campus, running south straight past the alleyway behind Mitchell Hall. In the fall of 1974, university planners officially closed this section of Yale Boulevard and the surrounding parking lots to clear room for the construction of the iconic UNM Duck Pond. This major development effectively transitioned Mitchell Hall's surrounding environment from a vehicle-dominated thoroughfare into a pedestrian-friendly campus core.

The 21st-Century Sustainable Renewal (2008–2009)

By the turn of the century, Mitchell Hall suffered heavily from structural stagnation. Having received no major renovations since its 1950 construction, the 54,000-square-foot facility had become notoriously energy-inefficient. Its 60-year-old, single-pane, steel-framed windows leaked conditioned air, and the interior was widely criticized by students and faculty for its rigid, dark corridors, poor ventilation, and lack of collaboration spaces.
To salvage the historic building, UNM launched a sweeping modernization project that began late in 2008 and wrapped up in 2009. The university commissioned the Hartman + Majewski Design Group (with architectural work led by Eric Haskins) to revitalize the space. The design team stripped down the rigid layout, maximizing the flow of natural daylight and introducing advanced ventilation, smart boards, and flexible seating. The $9.1 million remodel successfully brought the mid-century building into the modern era, achieving LEED Silver Certification while carefully preserving Meem's historic exterior facade

<!-- Full-width figure. This is the default for any landscape photo wider than about 700px.
     image-path is just the filename: upload your images into this essay's folder,
     next to index.md. -->

{% include images/figure.html
  class="img-center"
  width="100%"
  caption="Replace this caption. Say why the image matters, not just what it shows, then cite where you found it: [Center for Southwest Research](https://econtent.unm.edu/), collection and box number."
  image-path="sample-archive-photo.jpg"
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
"sample-archive-photo.jpg,
sample-second-photo.jpg,
sample-primary-source.jpg" | split: ','
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
  image-path="sample-primary-source.jpg"
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
