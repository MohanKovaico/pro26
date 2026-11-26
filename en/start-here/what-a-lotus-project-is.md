---
title: What a Document360 Lotus project is2
internalDescription: The product-type distinction, what Git being the source of truth means in practice.
tags:
  - getting-started
  - git
  - writer
labels:
  - sample-content
seo:
  title: What a Document360 Lotus project is2
  description: Git as the source of truth, and what that changes for a writer.
display:
  toc: true
  outline: true
---

Document360 has two product types. This project is the Git-backed one.

| | <span data-variable="productType">{{variable.productType}}</span> | <span data-variable="siblingType">{{variable.siblingType}}</span> |
| :--- | :--- | :--- |
| Source of truth | A Git repository | Document360 |
| An article is | A Markdown file | A record in Document360 |
| Order of pages | A manifest file in the repository | Arranged in the portal |
| Reuse objects | Files under `.document360/` | Records in the portal |
| Editing | <span data-variable="editorName">{{variable.editorName}}</span>, or any editor you like | <span data-variable="editorName">{{variable.editorName}}</span> |

Both are supported, and neither is a migration path to the other.

## What "source of truth" actually means

Three consequences, and they are the whole of it:

[d360]: # 'multi-level-list styles="decimal,lower-alpha"'

1. **The files are the content.** Not a copy of it, not an export of it. If you clone the repository
   you have the documentation.
2. **The history is Git's history.** Who changed what, and when, is a commit log — the same log your
   engineers already know how to read.
3. **Anything that can edit a text file can edit your documentation.** The portal, your own editor, a
   script, or a colleague's pull request.

[d360]: # "/multi-level-list"

> [!NOTE]
> **Markdown is the stored form, not an export**
>
> The file on disk is what Document360 reads and writes. There is no separate database copy that the
> Markdown is generated from, which is what makes the repository trustworthy as a source of truth.

## Who this suits

[d360]: # 'table border="all" striped="true"'

| This product type suits you if | The other one may suit you better if |
| :--- | :--- |
| Your docs sit beside code that changes with them | Your writers never want to see a repository |
| Engineers contribute, or should | Content is written entirely by a docs team |
| You want review to look like code review | You want approval to look like a workflow state |
| You already have CI you want docs to run through | You have no Git practice to build on |

[d360]: # "/table"

## What it does not change

[d360]: # 'callout kind="success"'

> **You still get a knowledge base site, search, categories, tags and feedback**
>
> Being Git-backed changes where content is stored. It does not reduce what readers get — the
> reader-facing product is the same one. See [Your readers](../your-readers/README.md).

[d360]: # "/callout"

## The honest trade-off

A repository introduces concepts a writer did not previously need: branches, merges, and the
occasional conflict. Document360 hides most of that for people who want it hidden, and the rest of
this section is about the parts that do reach you.

> [!CAUTION]
> **A Git-backed project has one genuinely new failure mode**
>
> Two people editing the same page in different places, which in an editor-first product cannot
> happen. [When two people edit](../review-and-publishing/when-two-people-edit.md) is the page about
> that, and it is worth reading before it happens rather than afterwards.

[d360]: # 'snippet name="deleteMe"'
