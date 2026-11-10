---
title: Submitting Your Essay
layout: essay
date: 2026-11-09
permalink: /submitting-your-essay/
---

# Submitting Your Essay

This is Part 3 of the [student guide](../student-guide/). Use it when your essay is finished, as described in [Part 2](../working-on-your-essay/). You will check your essay against a list, then send it to the main Campus History site with a pull request. A pull request is how you ask the project to add your work to the public site. Your instructor reviews it and merges it.

Your course schedule gives the deadline. Open **one** pull request, when your essay is ready.

## The Checklist

Open your website, `https://YOUR-USERNAME.github.io/campus-history/essays/your-folder-name/`, in one tab and your essay's `index.md` in the editor in another. Go through every item, ticking each box as you go. Fix what fails, commit, and check the Actions tab for a green check mark before you move on (see [Commit a Change and Check It](../working-on-your-essay/#commit-a-change-and-check-it)).

<style>
  .task-list { list-style: none; padding-left: 0; }
  .task-list-item { padding-left: 1.9em; text-indent: -1.9em; }
  .task-list-item-checkbox { margin-right: 0.7em; }
</style>

### Folders and Files

- [ ] Your essay folder is inside `essays`, and its name is all lowercase, with hyphens instead of spaces: `mesa-vista-hall-1970s`, not `Mesa Vista Hall` or `mesa vista hall copy`.
- [ ] No other essay has the same folder name, and you did not change any other essay's folder or `starter-essay-simple` itself.
- [ ] Your folder holds `index.md` and your own images, and nothing else.
- [ ] The three sample images (`sample-archive-photo.jpg`, `sample-second-photo.jpg`, `sample-primary-source.jpg`) are gone.
- [ ] Every image filename is lowercase, with hyphens and an extension (`.jpg` or `.png`).
- [ ] Every `image-path`, and your `header-image`, matches a filename in your folder exactly, letter for letter.

### Metadata at the Top

- [ ] `title` and `author` are right, and `author` is your name.
- [ ] `category` is one from the [list of categories](../setting-up-your-site-and-essay/#categories), typed exactly. It is no longer `Starter Essay`.
- [ ] `header-image` shows at the top of your page, and `header-caption` says where it came from.
- [ ] `card-description` is two sentences about your essay, not the starter's placeholder.
- [ ] `start` is a year.
- [ ] Your essay's card appears on your website's Essays page, `/directory/`, with your picture and your description.

### Writing

- [ ] The first thing after the header image is a lead paragraph, with no image, heading, or pull quote above it.
- [ ] The lead paragraph opens with a scene, question, or specific fact, not with `This essay will`.
- [ ] Each section has a `##` heading that says what the section is about.
- [ ] Paragraphs are short, usually two to five sentences, with one idea each.
- [ ] No placeholder text is left. Search your `index.md` for `Replace`, `Your`, and `starter`.
- [ ] You have read your essay aloud once and fixed the sentences you stumbled over.
- [ ] Your essay includes everything your assignment requires. Check the assignment page for your course.

### Images and Captions

- [ ] Every image appears on the page, and none is blurry. Each is at least about 800 pixels wide.
- [ ] Every image has a caption, including each carousel slide and each image in a grid.
- [ ] Each caption says why the image matters, not just what it shows.
- [ ] Each caption names the source: collection, box, and folder, or a link.
- [ ] No caption or title contains a double quotation mark.
- [ ] Any pull quote has at least two sentences of your own text between it and the heading above it.

### Links and Sources

- [ ] You clicked every link in your essay, and each goes where you expect.
- [ ] Your bibliography is at the end of the essay, one source per line.
- [ ] Each source has enough detail for someone else to find it.
- [ ] Footnotes, if you used any, show up at the bottom and match their numbers.

### The Final Check

- [ ] Source Control in the editor shows no uncommitted changes.
- [ ] The Actions tab shows a green check mark for your latest commit.
- [ ] You reloaded your website and looked at the whole essay, top to bottom, after your last change.

## Open the Pull Request

Do this only after every box above is checked.

1. **Go to your repository** on GitHub: `https://github.com/YOUR-USERNAME/campus-history`. Check that the address has your username, not `amaranth-unm`.
2. **Click `Contribute`,** just above the list of files, then click `Open pull request`. If you do not see `Contribute`, click the `Pull requests` tab, then `New pull request`.
3. **Check the two sides at the top.** The left side (the base) should be `amaranth-unm/campus-history` and `master`. The right side (the head) should be your own repository, `YOUR-USERNAME/campus-history`.
4. **Check the changed files.** Below the title and description boxes, click the `Files changed` tab. Every file listed should be inside `essays/your-folder-name/`. If any file is outside your folder, **do not submit.** Ask your instructor first.
5. **Add a title and a note.** Use a title such as `Essay: Mesa Vista Hall`. In the description box, write your name, your course, and your topic, such as `Your Name, your course, Mesa Vista Hall`. Add your website address too.
6. **Click `Create pull request`.**

That is it. Your pull request now appears on the main repository's `Pull requests` page, and your instructor will review it.

### If Your Instructor Asks for Changes

Do not open a new pull request. Make the changes in the editor and commit them to your repository, as you have been doing. Your open pull request updates by itself with each commit. Then add a short comment on the pull request saying you have made the changes.

### After Your Essay Is Merged

Once your instructor merges your pull request, your essay is on the public site. If you need to fix something after that, go to your repository on GitHub first and click `Sync fork`, then `Update branch`. Otherwise your next pull request carries your old changes along with the new ones, and the two versions of your essay conflict.

[Back to Part 2: Working on Your Essay](../working-on-your-essay/)

<script>
  // Make the checklist boxes clickable, and remember them on this device.
  (function () {
    var boxes = document.querySelectorAll('.task-list-item-checkbox');
    var key = 'submit-checklist';
    var saved = [];
    try { saved = JSON.parse(localStorage.getItem(key)) || []; } catch (e) {}
    boxes.forEach(function (box, i) {
      box.disabled = false;
      box.checked = !!saved[i];
      box.addEventListener('change', function () {
        var state = Array.prototype.map.call(boxes, function (b) { return b.checked; });
        try { localStorage.setItem(key, JSON.stringify(state)); } catch (e) {}
      });
    });
  })();
</script>
