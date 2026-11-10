---
title: Setting Up Your Site and Essay
layout: essay
date: 2026-08-04
permalink: /setting-up-your-site-and-essay/
---

# Setting Up Your Site and Essay

This is Part 1 of the [student guide](../student-guide/) to publishing on the Campus History site. Your course syllabus explains the assignment, grading, due dates, and reflection requirements. The guide only covers the site workflow, in three parts:

1. **Setting up your site and essay** (this page): make your own copy of the site, start your essay folder, and add your header image.
2. **[Working on your essay](../working-on-your-essay/):** finish the metadata, write, add images and pull quotes, and check your work.
3. **[Submitting your essay](../submitting-your-essay/):** go through the checklist and open a pull request.

<div class="alert alert-warning" markdown="1">

#### Due Tuesday: Your Own Working Copy of the Site
{: .alert-heading}

By Tuesday, do these five things. Each step links to its section of this guide.

1. **Make your own copy of the site.** [Fork the repository](#fork-the-repository).
2. **Get your copy working as a website.** [Turn on GitHub Pages](#preview-your-work) and open your preview site.
3. **Duplicate the starter folder.** [Copy `starter-essay-simple`](#copy-the-starter-folder) and rename the copy with [your folder name](#choose-a-folder-name). This becomes your essay folder.
4. **Add an image of your building.** [Find a picture of your building](#find-a-header-image) and upload it into your essay folder.
5. **Point the metadata at your image.** In the metadata at the top of your `index.md` (sometimes called the YAML header), set `header-image:` to your image's exact filename and fill in the other marked lines, including a `category:` from the [list of categories](#categories). See [Change the Top of `index.md`](#change-the-top-of-indexmd).

You are done when your essay shows up on your preview site's Essays page, `https://YOUR-USERNAME.github.io/campus-history/directory/`, with your building's picture on its card. Stop there. Parts 2 and 3 of this guide cover writing and submitting the essay, which come later.

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

   {% include images/guide-shot.html image="fork-button.png" width="340px" alt="The Notifications, Fork, and Star buttons at the top right of the repository page, with Fork outlined in red." caption="The `Fork` button, near the top right of the page." %}

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

   {% include images/guide-shot.html image="check-essay-header.jpg" alt="The top of a finished essay page: a photo of the Anthropology Building fills the screen, with the category Academic Building, the title Anthropology Building, and By Maxine Porter written over it." caption="You should see something like this, with your own picture, category, title, and name." %}

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

{% include images/guide-shot.html image="check-essays-page-card.jpg" alt="The Academic Building section of the Essays page, showing four essay cards, each with a photo, a title, and a short description." caption="Your essay's card should look something like these, under your category's heading." %}

- **Your essay is not listed.** Your `category:` line is still `Starter Essay`, or it does not match one of the [categories](#categories) exactly.
- **Your essay is listed, but its picture is missing, broken, or still the starter's.** Your `header-image:` line does not match your image's filename exactly. Compare the two letter by letter, including capitalization and the extension, such as `.jpg`.

</div>

## Next

When your instructor tells you to start writing, continue to [Part 2: Working on Your Essay](../working-on-your-essay/).
