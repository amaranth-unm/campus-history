---
title: Student Publishing Guide
layout: essay
date: 2026-08-04
permalink: /student-guide/
---

# Student Publishing Guide

This page explains how to turn a course assignment into a working page on the Campus History site. Your course syllabus explains the assignment, grading, due dates, and reflection requirements. This guide only covers the site workflow: making a page, adding images, checking metadata, and submitting your work for publication.

<div class="alert alert-warning" markdown="1">

#### Due Tuesday: Your Own Working Copy of the Site
{: .alert-heading}

By Tuesday, do these five things. Each step links to its section of this guide.

1. **Make your own copy of the site.** [Fork the repository](#fork-the-repository).
2. **Get your copy working as a website.** [Turn on GitHub Pages](#preview-your-work) and open your preview site.
3. **Duplicate the starter folder.** [Copy `starter-essay-simple`](#copy-the-starter-folder) and rename the copy with [your folder name](#choose-a-folder-name). This becomes your essay folder.
4. **Add an image of your building.** [Find a picture of your building](#find-a-header-image) and upload it into your essay folder.
5. **Point the metadata at your image.** In the metadata at the top of your `index.md` (sometimes called the YAML header), set `header-image:` to your image's exact filename and fill in the other marked lines, including a `category:` from the [list of categories](#categories). See [Change the Top of `index.md`](#change-the-top-of-indexmd).

You are done when your essay shows up on your preview site's Essays page, `https://YOUR-USERNAME.github.io/campus-history/directory/`, with your building's picture on its card. Stop there. The rest of this guide covers writing and submitting the essay, which comes later.

</div>

## Before You Start

- Create or sign in to a [GitHub](https://github.com/) account.
- Choose a topic according to your course assignment.
- Check with your instructor before duplicating a topic already claimed by another student.
- Open the [Campus History repository](https://github.com/amaranth-unm/campus-history).

## Fork the Repository
In GitHub, a "fork" (like a fork in the road) is your own copy of the Campus History repository. You can edit your own copy without changing the "official" site until you are ready.

1. Go to the [Campus History repository](https://github.com/amaranth-unm/campus-history).
2. Click `Fork` in the upper-right corner.
3. Keep the default settings and click `Create fork`.
4. After GitHub creates the fork, make sure the URL includes your GitHub username.

Bookmark two pages:

- Your repository: `https://github.com/YOUR-USERNAME/campus-history`
- Your preview site, once GitHub Pages is enabled: `https://YOUR-USERNAME.github.io/campus-history`

## Preview Your Work

Your fork can generate its own preview version of the website. Use that preview to check page content, links, images, and formatting before submitting. Fork previews can behave a little differently from the public Campus History site because they live under your GitHub username, so do not change `_config.yml` or site-wide settings unless your instructor specifically tells you to.

1. In your fork, click `Settings`.
2. Click `Pages` in the left sidebar.
3. Under `Build and deployment`, choose `Deploy from a branch`.
4. Select the `master` branch and the `/ (root)` folder.
5. Click `Save`.
6. Wait a minute or two, then return to `Settings` > `Pages` and open the published site link.

GitHub Pages takes about a minute to rebuild your site and show your latest changes. 


## Start From a Starter Essay

All essays live in the `essays` folder. Each essay has its own folder and an `index.md` file inside that folder. The easiest way to begin is to copy one of the starter essay folders and rename it for your topic.

Use one of these:

- `starter-essay-simple` — best for most essays. It already contains everything a finished essay needs: a lead paragraph, subheadings, captioned images, a carousel, and a bibliography. Replace the placeholder text and images and you have a complete page.
- `starter-essay-advanced` — a parts catalog containing one working example of every component the site offers, including pullquotes, image grids, before/after sliders, footnotes, banner images, and full-screen scrollstory sections. Start here only if you want the fuller set, and delete every component you do not use.

### Choose a Folder Name

Pick your folder name before you copy anything. It becomes part of your essay's web address, as in `/essays/mesa-vista-hall/`.

Folder names must be:

- all lowercase
- hyphenated instead of spaced
- short but recognizable
- new: no folder in `essays` can already have that name
- exactly the same wherever you refer to them

The folders already in `essays` show the pattern: `duck-pond`, `maxwell-museum`, `sara-raynolds-hall`. Check that list before you name yours. If your topic already has a folder, add a word that sets yours apart, such as `duck-pond-1970s`. Even `mesa-vista-hall`, the example on this page, is taken by the site's demo essay. Two essays in the same folder would overwrite each other.

### Copy the Starter Folder

**Do not edit the starter folder itself.** Duplicate it, then rename the copy. 

You will do this in GitHub's web editor, which runs in your browser. Use a laptop or desktop computer: the editor depends on right-clicking and does not work well on a phone or tablet (many tablets are fine, but quite hard to use if you're not used to this sort of thing). On a Mac trackpad, right-click by clicking with two fingers, or by holding `Control` while you click.

1. **Open your fork.** Go to `https://github.com/YOUR-USERNAME/campus-history`. Check that the address shows your username, not `amaranth-unm`. If it shows `amaranth-unm`, you are in the main repository, and you cannot save changes there.
2. **Open the editor.** In your browser's address bar, change `github.com` to `github.dev` so the address reads `https://github.dev/YOUR-USERNAME/campus-history`, then press `Enter`. Sign in if GitHub asks. The editor opens with a list of files down the left side.
3. **Open the `essays` folder.** Click `essays` in the file list. It expands into a list of folders, one for each essay, in alphabetical order. Find `starter-essay-simple` under S.
4. **Copy the starter.** Right-click `starter-essay-simple` and choose `Copy`. Nothing visible happens. That is normal.
5. **Paste it into `essays`.** Scroll up and right-click the word `essays` itself, not any folder inside it, and choose `Paste`. A new folder called `starter-essay-simple copy` appears in the list under `essays`. If it does not, the copy went somewhere else: see the fixes below.
6. **Rename the copy.** Right-click `starter-essay-simple copy`, the one with `copy` in its name, and choose `Rename`. Delete the whole name, type your folder name, and press `Enter`.
7. **Check the folder list.** `essays` should now contain both `starter-essay-simple` and your new folder. Click your folder to open it. It should hold `index.md` and three sample images. `index.md` is your essay, so keep that filename.
8. **Check the list of changes.** Click the Source Control icon in the bar on the far left, the one showing a small number. Under `Changes` you should see four files: `index.md` and the three sample images, each with your folder name in gray beside it. If any of them shows `starter-essay-simple` instead, or has a `D` beside it, stop and use the fixes below.
9. **Save to GitHub.** Type `Start my essay` in the `Message` box above the list of changes, then click `Commit & Push`.
10. **Confirm it worked.** Go back to your fork on github.com and open the `essays` folder. Your folder should be there. After a minute or two, your preview site shows your page at `/essays/your-folder-name/`.

Nothing you change in the editor reaches your fork or your preview site until you commit. Repeat steps 8 and 9 each time you finish a round of changes.

### If Something Goes Wrong

If you have not committed yet, the easiest fix is to start over. In Source Control, hover over the word `Changes` and click the curved-arrow icon, `Discard All Changes`, then confirm. Everything goes back to how it was at your last commit, and you can start again from step 4.

- **The copy landed inside `starter-essay-simple` or another essay's folder.** You right-clicked a folder other than `essays` when you pasted. Discard your changes, copy again, and this time right-click the word `essays` to paste.
- **`Paste` is grayed out or missing.** You right-clicked blank space, or the copy did not take. Right-click `starter-essay-simple`, choose `Copy` again, and then right-click `essays`.
- **`starter-essay-simple` has disappeared.** You renamed the starter instead of the copy. Discard your changes and start again from step 4.
- **Your folder name still contains a space or the word `copy`.** Right-click it, choose `Rename`, and fix it.
- **You already committed a mistake.** Fix it in the editor so the folders look right again, then commit again. Your pull request only shows how things end up, not every step along the way. If you are not sure how to put things back, ask your instructor before you go further.

## Make the Page Yours

Your copy is still the starter, with its sample pictures and placeholder text. The first round of work replaces the top of the page: your title, your name, a category, and one image of your topic. Leave the rest of the placeholder text for now.

### Find a Header Image

Your header image stretches across the top of your page, and it stands for your essay everywhere else on the site: the directory, the map, and the homepage. Pick one picture of your topic:

- **A photo you take yourself.** Hold your phone sideways, so the picture is wider than it is tall, and get the whole building or place in the frame.
- **A historical photo** from the [New Mexico Digital Archive](https://econtent.unm.edu/). Search for your topic, open the image, and download the largest size offered.

Then get the file ready:

- It must be a `.jpg` or `.png` file. Browsers cannot show `.heic`, the format many iPhones use. If your file ends in `.heic`, open it in Preview on a Mac and choose `File` > `Export`, with `JPEG` as the format.
- Rename it in lowercase with hyphens, keeping the extension: `mesa-vista-hall-today.jpg`.
- Write down where it came from. For your own photo, that is `Photograph by Your Name, October 2026.` For an archive image, it is the collection name and the item's title or number.

### Change the Top of `index.md`

1. **Upload your image.** In the web editor, drag the file from your computer onto your folder in the file list, or right-click your folder and choose `Upload...`. The image should appear inside your folder, next to `index.md`.
2. **Open your essay.** Click `index.md` in your folder. The lines between the two `---` lines at the top are the metadata. The starter marks the five lines to change now.
3. **Change the five lines.** Replace only the text after each colon:
   - `title:` your topic, such as `Mesa Vista Hall`
   - `author:` your name
   - `category:` one from the [list of categories](#categories), typed exactly
   - `header-image:` your image's filename, exactly as it appears in the file list
   - `header-caption:` where your image came from
4. **Commit.** Open Source Control. The changes should be your image and `index.md`. Type a message such as `Add my header image` and click `Commit & Push`.
5. **Check your preview.** Wait a minute or two, then open `https://YOUR-USERNAME.github.io/campus-history/essays/your-folder-name/` and reload the page. Your image should fill the top of the page, with your title over it, your category just above the title, and your name below it.

That is a working page of your own. Below the header, it still shows the starter's placeholder text and sample images until you replace them.

The metadata is easy to break. Keep these rules:

- Do not change anything to the left of a colon, and leave one space after each colon.
- Do not type another colon or a `#` in these lines. Use a comma or a dash instead: `Mesa Vista Hall, the 400-Man Dorm`.
- Do not delete either `---` line.

If your page loads but its header image, title, and category have disappeared, one of these rules is broken. Look over the lines at the top of `index.md`, fix the one that breaks a rule, and commit again.

If your page has not changed at all after five minutes, open your fork on github.com and look beside your latest commit. A red ✗, instead of a green check mark, means the site failed to build. Undo your last change, commit again, and ask your instructor if it still fails.

<div class="alert alert-warning" markdown="1">

#### Check Everything Works and Stop
{: .alert-heading}

Open your preview site's Essays page, `https://YOUR-USERNAME.github.io/campus-history/directory/`. Your essay should be listed under its category, with your building's picture on its card. If it is, you have finished the work due Tuesday. Stop here.

- **Your essay is not listed.** Your `category:` line is still `Starter Essay`, or it does not match one of the [categories](#categories) exactly.
- **Your essay is listed, but its picture is missing, broken, or still the starter's.** Your `header-image:` line does not match your image's filename exactly. Compare the two letter by letter, including capitalization and the extension, such as `.jpg`.

</div>




## Customize the Metadata

Every essay begins with metadata between two lines of three hyphens. The directory, homepage cards, and page header use this metadata, so fill it out carefully.

The starters include every line an essay needs, with comments marking which ones to change first. A comment starts with `#` and never appears on the site; you can delete the comments once the lines are filled in. Filled in, the metadata looks like this:

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

What each line does:

- `title` names your essay over the header image, in the directory, in the essay lists, and in the browser tab.
- `author` is your name, shown under your title as a byline.
- `category` sorts your essay in the directory, and appears just above your title. The starter's category is `Starter Essay`, which keeps a page out of the directory and the arrows between essays, so change it to one from the [list below](#categories).
- `header-image` is the filename of the large image at the top of your page, such as `mesa-vista-hall-today.jpg`. The same image also stands for your essay in the directory, on the map, and on the homepage.
- `header-caption` says where the header image came from. Plain text only: links do not work here.
- `card-description` is the two sentences on your essay's card in the directory and on the homepage.
- `start` is the year your story begins. The map shows it next to your title.
- `layout` tells the site to build an essay page. Leave it as `essay`.

A few optional lines, all shown in `starter-essay-advanced`:

- `header-title` puts a different title over the header image, if it should not match `title`.
- `header-subtitle` adds a short phrase under the title over the header image.
- `popup-teaser` is a single sentence for the map and homepage, used there instead of `card-description`.
- `card-image` is the filename of a different picture for your essay's card in the directory, on the map, and on the homepage.

Your essay appears on the campus map once an outline of its location is added to `assets/kml/` under your folder name, such as `assets/kml/mesa-vista-hall.kml`. We will get to this much later.

### Categories

Use one of these categories, typed exactly as shown. An essay with any other category does not appear in the directory, so if none fits, ask your instructor.

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

The current Campus History directory is generated from essay metadata. 


## Add Images

Your images go in your essay folder, right next to `index.md`. The starter essay came with three sample images there; delete them once your own images have replaced them.

Add them the same way as your header image: in the web editor, drag them onto your essay folder or right-click the folder and choose `Upload...`, then commit. You can also upload on github.com: open your essay folder, choose `Add file` > `Upload files`, and click `Commit changes`. If you do, close the web editor first and reopen it afterward, so it picks up the new files.

Name each file in lowercase, with hyphens instead of spaces, and keep its extension: `mvh-construction-1950.jpg`, not `MVH Construction (1).JPG`. Rename files on your computer before you upload them, because renaming one later means fixing every place your essay mentions it.

Your folder should look like this:

```text
essays/mesa-vista-hall/index.md
essays/mesa-vista-hall/mvh-construction-1950.jpg
essays/mesa-vista-hall/mvh-today.jpg
```

In your essay, refer to an image by its filename alone, with no folder in front of it: `image-path="mvh-today.jpg"`. The filename must match exactly, including capitalization and extension. `mvh.jpg`, `MVH.jpg`, and `mvh.jpeg` are three different files.

### How big should images be?

Save images **at least 768 pixels wide**, and closer to **1500 pixels** if the archive gives you the option. The text column is 768 pixels, so anything narrower gets stretched to fit and looks blurry on the page. Downloading the largest version a digital collection offers is almost always the right move — the site will scale it down cleanly, but it cannot invent detail that is not in the file.

Before/after sliders are stricter. Both images should be at least 768 pixels wide **and roughly the same shape**, because the slider is sized from the first image and crops the second one to match. Two landscape photographs work well; a tall document paired with a wide photograph will get its top and bottom cut off.


Use the Campus History image include instead of regular Markdown image syntax:

{% raw %}
```markdown
{% include images/figure.html
  class="img-center"
  width="100%"
  caption="Construction of Mesa Vista Hall in 1950. This image shows how the building was originally framed as a residential solution for postwar enrollment growth. Source: Center for Southwest Research, collection and box information."
  image-path="mvh-construction-1950.jpg"
%}
```
{% endraw %}

Captions should explain why the image matters, not just identify what is in the picture. Include a source, box number, collection name, or link whenever possible.

## Use Site Components

Copy components out of a starter essay rather than inventing your own HTML. The starters are real pages that get built along with the rest of the site, so the snippets in them are guaranteed to work.

`starter-essay-advanced` has a working example of each one, with a comment above it explaining when to use it:

- figures, at full width and at the smaller width for tall documents
- image grids
- carousels
- before/after image sliders
- pullquotes and blockquotes
- footnotes
- banner (jumbotron) images
- full-screen scrollstory sections
- bibliography drawers

A few rules the snippets cannot enforce on their own:

- **Every image needs a caption**, including carousel slides and grid cells. A caption should say why the image matters and where you found it.
- **Do not use double quotation marks inside a caption or title.** They end the snippet early and break the page. Single quotation marks are fine.
- **Do not change figure widths to fine-tune the layout.** The text column is 768px and the stylesheet puts a floor under every figure, so `33%`, `40%`, and `50%` all come out the same size. Use `width="100%"` with `class="img-center"` for anything landscape, and about `55%` for tall documents like letters and clippings. Do not float images left or right unless your sentence actually says "the image at right."
- **Two images that belong side by side need an image grid**, not two half-width figures. Floated figures cannot fit next to each other and will stack instead.
- **Carousel captions are plain text.** Markdown links will not render there, so write out the collection name and box number.
- **Keep your three hyphens** `---` above and below the metadata at the top of the file, each on its own line.

## Check Your Page

Before submitting, open your preview site and check:

- Your essay page loads at `/essays/your-folder-name/`.
- The page title, author, card description, and category are correct.
- Your header image appears at the top of your page, and on your essay's card on the preview site's Essays page (`/directory/`).
- Every image in the essay appears.
- Captions are informative and include source information.
- Links go where you expect.
- The bibliography is readable.
- The essay has subheadings and is easy to skim.
- The first paragraph gives readers a clear entry point into the story.

## Submit a Pull Request

When your page is ready, send your work back to the main Campus History repository with a pull request.

1. Go to your fork on GitHub.
2. Click `Contribute` or `Pull requests`.
3. Click `Open pull request` or `New pull request`.
4. Review the list of changed files.
5. Make sure every changed file is inside your essay folder unless your instructor told you otherwise.
6. Click `Create pull request`.
7. Add a short note with your name, course, and topic.

After that, your instructor can review the page and merge it into the public Campus History site.

Open a single pull request once your essay is finished. If you need to change your essay after it has been merged, first go to your fork on GitHub and click `Sync fork` > `Update branch`. Otherwise your next pull request carries your old changes along with the new ones, and the two versions of your essay conflict.
