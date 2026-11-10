---
title: Working on Your Essay
layout: essay
date: 2026-11-09
permalink: /working-on-your-essay/
---

# Working on Your Essay

This is Part 2 of the [student guide](../student-guide/). In [Part 1](../setting-up-your-site-and-essay/) you made your own copy of the site and started your essay folder. This page is where you turn the starter's placeholder text into a finished essay.

<div class="alert alert-info" markdown="1">

#### Your Two Addresses
{: .alert-heading}

Keep these open in two browser tabs while you work. Replace `YOUR-USERNAME` with your GitHub username.

- **Your repository** (where your files live and where you save changes): `https://github.com/YOUR-USERNAME/campus-history`
- **Your website** (where you see your changes): `https://YOUR-USERNAME.github.io/campus-history/`

Your essay is at the website address plus `essays/your-folder-name/`.

</div>

## What a Finished Essay Has

The starter already has a place for everything below. Your job is to replace each placeholder with your own work.

- A **lead paragraph** that opens the essay, with nothing above it.
- Three to five **sections**, each with its own `##` heading.
- **Short paragraphs** built on specific evidence.
- Several **images**, each with a caption that says why it matters and where it came from.
- One or more **pull quotes**.
- A **bibliography** at the end.
- **No placeholder text** and no sample images left over.

Work through the sections of this page in order. Commit and check your work after each one.

## Commit a Change and Check It

You will do this over and over, so learn it first. The editor saves your typing automatically, but only in your browser. Nothing you change reaches your repository or your website until you commit and push.

1. **Open the editor.** Go to your repository, then change `github.com` in the address bar to `github.dev`, so it reads `https://github.dev/YOUR-USERNAME/campus-history`, and press `Enter`. Your essay is in `essays`, in the folder you named.
2. **Make your change.**
3. **Look at your changes.** Click the Source Control icon in the bar on the far left. Under `Changes` you should see only files in your own essay folder. If you see files from anywhere else, stop and ask your instructor.
4. **Commit.** Type a short message, such as `Write my lead paragraph`, in the `Message` box and click `Commit & Push`.
5. **Watch the Actions tab.** On github.com, go to your repository and click `Actions` in the row of tabs at the top. The newest line at the top is your change. A yellow circle means GitHub is still rebuilding your site. A **green check mark** means it worked. A **red ✗** means the site failed to build, so click that line to see the error.
6. **Preview your website.** Once the check mark is green, open your website tab and reload the page. To force a fresh copy, press `Cmd+Shift+R` on a Mac or `Ctrl+Shift+R` on Windows. A rebuild takes about a minute or two.

If you see a red ✗, the cause is almost always one of these:

- A **double quotation mark** inside a caption or title. Use single quotation marks instead.
- A missing or damaged `---` line at the top of `index.md`.
- A typo inside one of the `{% raw %}{% include ... %}{% endraw %}` blocks, such as a missing `%}` at the end.

Fix it, then commit again. If you cannot find the problem, ask your instructor.

## Finish the Metadata

In Part 1 you set `title`, `author`, `category`, `header-image`, and `header-caption`. Now fill in the rest. The directory, the homepage cards, and the page header all use the metadata, so fill it out carefully. Filled in, it looks like this:

```markdown
---
title: Mesa Vista Hall
author: Your Name
category: Dormitory
header-image: mesa-vista-hall-today.jpg
header-caption: Photograph by Your Name, October 2026.
card-description: Two sentences that summarize the story your essay tells and why it matters.
start: 1950
layout: essay
---
```

**Do these now:**

1. Replace `card-description` with two sentences that sum up your essay's story and why it matters. This is the text on your essay's card in the directory and on the homepage.
2. Set `start` to the year your story begins, such as `1950`. The map shows it next to your title.
3. Delete the `#` comments once their lines are filled in. The comments never show on the site, so this is optional.

What each line does:

- `title` names your essay over the header image, in the directory, and in the browser tab.
- `author` is your name, shown under the title as a byline.
- `category` sorts your essay in the directory and appears just above the title. Use one from the [list of categories](../setting-up-your-site-and-essay/#categories).
- `header-image` is the filename of the large image at the top of the page. It also stands for your essay in the directory, on the map, and on the homepage.
- `header-caption` says where the header image came from. Plain text only: links do not work here.
- `card-description` is the two sentences on your essay's card.
- `start` is the year your story begins.
- `layout` tells the site to build an essay page. Leave it as `essay`.

The same rules from Part 1 still apply: change only the text after a colon, leave one space after it, do not type another colon or a `#` in these lines, and keep both `---` lines.

A few optional lines, all shown in `starter-essay-advanced`: `header-title` puts a different title over the header image than `title`, `header-subtitle` adds a short phrase under it, `popup-teaser` is a single sentence for the map and homepage, and `card-image` is a different picture for your card.

Your essay appears on the campus map once an outline of its location is added to `assets/kml/` under your folder name, such as `assets/kml/mesa-vista-hall.kml`. You will do that later.

**Commit and check** (see [Commit a Change and Check It](#commit-a-change-and-check-it)), then look at your essay's card on your website's Essays page, `https://YOUR-USERNAME.github.io/campus-history/directory/`.

## Write the Lead Paragraph

The lead paragraph is the first thing after the header image. It is a short scene, question, surprising fact, or problem that makes readers want to keep going.

- **Nothing goes above it.** No image, heading, pull quote, or carousel.
- **Start with a specific moment or detail,** not a summary. Open with the day a building opened, a complaint someone wrote, or a question the archive raised.
- **Skip announcements.** Cut phrases such as `This essay will` and `The purpose of this page is`. Say what happened.
- **Keep it short.** Three to five sentences is plenty. The rest of the essay does the explaining.

Replace the starter's first paragraph, the one that begins `This first paragraph should give readers a quick way into your topic`. Commit and check.

## Write the Sections

After the lead paragraph, the essay is a series of sections. Replace the starter's placeholder sections (`Main Story`, `What Changed`, `Evidence`, `Why This History Matters`) with sections that fit your story, or keep the ones that do.

- **Start each section with a `##` heading** that says what the section is about. `The 1950 Housing Shortage` tells readers more than `Main Story`. Do not use a single `#`: your title already appears over the header image.
- **Keep paragraphs short.** Usually two to five sentences, built around one idea, source, or moment. Start a new paragraph when the date, person, source, or example changes.
- **Be specific.** Name dates, people, places, decisions, and costs. Explain what each fact shows about UNM and its history.
- **Explain your sources.** When you mention a document, say what it says, what it does not say, and how it fits the story.
- **End on why it matters.** Point to how the place is used today, what has been lost or forgotten, or what the archive does not tell us. Do not write `In conclusion`.
- **Put an image after the heading it belongs to,** not directly before the next heading.

Commit and check after each section.

## Add Images

Your images go in your essay folder, right next to `index.md`. Add them the same way you added your header image: in the web editor, drag them onto your essay folder, or right-click the folder and choose `Upload...`. Then commit.

**Name each file** in lowercase, with hyphens instead of spaces, and keep its extension: `mvh-construction-1950.jpg`, not `MVH Construction (1).JPG`. Rename files on your computer before you upload them. Your folder should look like this:

```text
essays/mesa-vista-hall/index.md
essays/mesa-vista-hall/mvh-construction-1950.jpg
essays/mesa-vista-hall/mvh-today.jpg
```

**Make sure your images are large enough.** This is the one thing about image size you need to check. Download the largest version the archive offers, and aim for **at least 800 pixels wide**. The text column is 768 pixels wide, so a smaller image gets stretched and looks blurry. To check a file's size on a Mac, select it in Finder and press `Cmd+I`, then look for `Dimensions` under `More Info`. On Windows, right-click the file, choose `Properties`, and open the `Details` tab. If the best copy you can find is narrower than 800 pixels, ask your instructor before you use it.

**Do not resize or compress images yourself.** The site has a tool that shrinks oversized files, so a big file is never a problem. A small one is.

**Delete the starter's sample images** (`sample-archive-photo.jpg`, `sample-second-photo.jpg`, and `sample-primary-source.jpg`) once your own images replace them. Right-click each file in the editor and choose `Delete`.

### The Image Code

Use this code for every image, in place of regular Markdown image syntax. Copy it, paste it on its own line between two paragraphs, and change the filename and caption:

{% raw %}
```markdown
{% include images/figure.html
  class="img-center"
  width="100%"
  caption="Construction of Mesa Vista Hall in 1950. This photograph shows the building as a rushed solution to postwar enrollment growth. Source: [Center for Southwest Research](https://econtent.unm.edu/), collection name, box number."
  image-path="mvh-construction-1950.jpg"
%}
```
{% endraw %}

That code produces this:

{% include images/figure.html
  class="img-center"
  width="100%"
  caption="Example caption. Construction of a campus building, with the walls up and the roof not yet on. Say what the reader should notice, then name the source: [Center for Southwest Research](https://econtent.unm.edu/), collection name, box number."
  image-path="/essays/starter-essay-simple/sample-archive-photo.jpg"
%}

What to change, and what to leave alone:

- `image-path` is the image's filename, with no folder in front of it. It must match the file exactly, including capitalization and extension. `mvh.jpg`, `MVH.jpg`, and `mvh.jpeg` are three different files.
- `caption` must say **why the image matters**, not just what it shows, and **where it came from**: the collection, box, and folder, or a link. Every image needs one.
- **Do not use double quotation marks inside the caption.** They end the code early and break the page. Single quotation marks are fine.
- Leave `class="img-center"` and `width="100%"` as they are for any wide photograph. For a tall document, such as a letter or clipping, use `width="55%"` so it does not fill the whole screen. Do not try other widths: the site will not make a picture smaller than about two-thirds of the column anyway.

## Add a Pull Quote

A pull quote lifts one vivid sentence out of your essay, or out of a primary source, and sets it in large type. Use one to three in the whole essay, and only for a sentence that deserves a second look.

{% raw %}
```markdown
{% include typography/aside.html
  class="center"
  text="The dormitory had been built in a hurry, and everyone who lived there knew it. (Daily Lobo, 1953)"
%}
```
{% endraw %}

That code produces this:

{% include typography/aside.html
  class="center"
  text="The dormitory had been built in a hurry, and everyone who lived there knew it. (Daily Lobo, 1953)"
%}

(That sentence is made up, so do not copy it.) Rules for pull quotes:

- `class` can be `left`, `right`, or `center`. `left` and `right` tuck the quote beside the text. `center` runs across the column.
- Put **at least two sentences of your own text** between a `##` heading and a pull quote. A pull quote should never be the first thing under a heading.
- If the quote comes from a source, name the source in the text itself, in parentheses, as in the example.
- A pull quote repeats a sentence that is also in your text. It does not replace explaining your point in your own words.
- Do not use double quotation marks inside the `text`. Use single ones.

To quote a document at more length, use a Markdown blockquote with a footnote instead. `starter-essay-advanced` shows how.

## More Components, and Rules for Using Them

Copy components out of a starter essay rather than inventing your own HTML. `starter-essay-simple` and `starter-essay-advanced` are real pages built along with the rest of the site, so the snippets in them work. `starter-essay-advanced` has one example of each of these, with a comment explaining when to use it:

- image grids, for two or three images that belong side by side
- carousels, for three or more related images
- before/after image sliders
- footnotes and blockquotes
- banner images
- full-screen scrollstory sections

Delete every component you do not use. A clean essay with four well-chosen images beats a cluttered one that uses everything. Whichever you use:

- **Every image needs a caption,** including each carousel slide and each image in a grid.
- **Two images that belong side by side go in an image grid,** not in two half-width figures. Half-width figures cannot sit next to each other and will stack.
- **Carousel captions are plain text.** Links do not work there, so write out the collection name and box number.
- **Before/after sliders need two images of the same shape,** such as two landscape photographs. A tall document paired with a wide photograph gets cut off.
- **Do not float images left or right** unless your sentence actually says `the image at right`.
- **Keep both `---` lines** around the metadata at the top of the file, each on its own line.

## Add Your Sources

End your essay with a bibliography. Put each source on its own line starting with `-`, in a collapsible drawer. Copy this code and replace the sources:

{% raw %}
```markdown
{% capture bibliography %}
- Center for Southwest Research, collection name, box number, folder title.
- Author, [Title of article](https://example.com/), publication, date.
- Source three.
{% endcapture %}

{% include typography/bibliography.html
  title="Bibliography"
  content=bibliography
%}
```
{% endraw %}

- Give enough detail that someone else could find each source: collection, box, and folder for archival material, and a link for anything online.
- One source per line. Do not run several sources together in one paragraph.
- Put the bibliography last, and keep any concluding paragraph of your own outside the drawer.

## Clean Up

Before you move on to [Part 3](../submitting-your-essay/), clean up the starter:

1. **Search for leftover placeholder text.** In the editor, open your `index.md` and press `Cmd+F` (Mac) or `Ctrl+F` (Windows). Search for `Replace`, then `Your`, then `starter`. Fix every match that is leftover starter text.
2. **Delete any starter component you did not use,** such as the carousel.
3. **Read your essay aloud once, on your website,** not in the editor. You will hear the long sentences and the paragraphs that run on.
4. **Look at it on a phone** if you can. Most readers will.

## If Something Looks Wrong

- **Your page is not updating.** Look at the Actions tab. A red ✗ means the build failed: see [Commit a Change and Check It](#commit-a-change-and-check-it). If the check mark is green, reload with `Cmd+Shift+R` or `Ctrl+Shift+R`.
- **An image is missing or broken.** The filename in `image-path` does not match the file exactly. Compare them letter by letter, including capitalization and the extension.
- **The header image, title, and category have disappeared.** One of the metadata rules is broken. Check the lines at the top of `index.md`.
- **A caption or include shows up as plain text on the page.** There is probably a double quotation mark inside it, or the closing `%}` is missing.
- **The text beside a figure is squeezed into a narrow column.** You floated the image. Change its `class` to `img-center`.

## Next

When your essay is finished, continue to [Part 3: Submitting Your Essay](../submitting-your-essay/).
