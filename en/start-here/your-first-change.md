---
title: Your first change
internalDescription: Edit a page and get it to readers, from the portal and from a clone.
tags:
  - getting-started
  - git
  - writer
labels:
  - sample-content
seo:
  title: Make your first change in a Document360 Lotus project
  description: Edit this page, review the change, and publish it.
display:
  toc: true
  outline: true
---

The best way to understand this project is to change something in it. This page is a safe thing to
change, because it is sample content and nobody is relying on it.

## From the portal

[d360]: # 'multi-level-list styles="decimal,lower-alpha"'

1. Open this article in <span data-variable="editorName">{{variable.editorName}}</span>.
2. Change a sentence. Add your name to the end of this one, for instance.
3. Save, then Save to branch.
   1. Save keeps a draft in Document360. Save to branch commits the Markdown file to the branch.
   2. The branch you are working on is shown while you edit.
4. Take the change through review, then publish it.

[d360]: # "/multi-level-list"

> [!IMPORTANT]
> **Saving to a branch writes a file; publishing is a separate act**
>
> In an editor-first product those two are often the same moment. Here they are not: Save to branch
> commits your work to a branch, and readers see nothing until the change is published. That gap is the point
> of the product.

## From a clone, if you prefer

```bash
git clone <your repository>
cd docs/en/start-here
# edit your-first-change.md in whatever you use
git commit -am "Docs: first change"
git push
```

Document360 reads the change and the article updates. Nothing about editing in your own editor is
second-class — the file you edited is the article.

> [!TIP]
> **Both routes write the same file**
>
> A page edited in the portal and a page edited in Vim produce the same Markdown. There is no
> "portal format" and no conversion step, which is what makes mixed teams workable.

## What a change looks like in Git

```diff
-The best way to understand this project is to read about it.
+The best way to understand this project is to change something in it.
```

A one-sentence edit is a one-line diff. This is the main practical reason the canonical Markdown
matters: a reviewer sees the sentence that changed, not a reformatted file.

> [!CAUTION]
> **Avoid reflowing paragraphs you have not edited**
>
> Re-wrapping a paragraph to a different line length turns a one-word fix into a diff nobody can
> read. If your editor reformats on save, turn that off for Markdown.

## Things to try next

- [ ] Change a sentence and watch the diff.
- [ ] Add a callout, using the block menu rather than typing the syntax.
- [ ] Move this article above its siblings — note that this edits `d360.json`, not the file.
- [ ] Delete this article. It is sample content, and deleting it is a legitimate first change.

[d360]: # 'callout kind="success"'

> **If you can do those four, you can run this project**
>
> Everything else in this documentation is detail on top of edit, review, publish.

[d360]: # "/callout"

## Where to go next

[Writing](../writing/README.md) if you want to get on with writing;
Structure if you would rather understand how the tree is put together
first. Both are written to be read in either order.

[d360]: # 'snippet name="deleteMe"'
