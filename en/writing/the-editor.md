---
title: The editor
internalDescription: Editor V3 in a Lotus project — what it writes, and why the saved form matters.
tags:
  - editor
  - writer
labels:
  - sample-content
seo:
  title: Editor V3 in a Document360 Lotus project
  description: How the editor and the Markdown file relate to each other.
display:
  toc: true
  outline: true
---

<span data-variable="editorName">{{variable.editorName}}</span> is a block editor. You write
paragraphs, insert blocks from a menu, and what reaches your repository is a Markdown file.

## The two things worth understanding

1. **What you see is not what is stored.** The editor shows you a rendered callout; the file holds
   Markdown that describes one. Both are correct — they are the same content in two forms.
2. **The stored form is canonical.** There is one way the editor writes each block, and it writes it
   that way every time. That is what makes diffs readable and round-trips safe.

> [!IMPORTANT]
> **A file written by hand in an older syntax will be rewritten on first save**
>
> Document360's Markdown accepts a legacy fence form for blocks as *input*, and migrates it to the
> canonical form when the article is next saved. In a Git-backed project that migration is a commit —
> on content nobody edited. If you write Markdown by hand, write it the way the editor writes it, and
> nothing is rewritten behind you.

## How blocks look on disk

A block is delimited by a pair of marker lines, which are Markdown comments and so are invisible to
any other Markdown renderer:

```markdown
> [!NOTE]
> **The title**
>
> The body of the callout.
```

> [!CAUTION]
> **The blank lines around those markers carry meaning**
>
> They are not formatting. A marker without a blank line before and after it is not recognised as a
> marker, and the block becomes literal text. If you edit files by hand, leave those lines alone.

## Collapsibles are plain HTML

Accordions, tabs and FAQ items are built from `<details>` and `<summary>`, so they still work when
somebody reads the file on GitHub rather than in your knowledge base:

```markdown
<details>
<summary>The visible label</summary>

The content, with a blank line above it and below it.

</details>
```

> [!NOTE]
> **Those blank lines matter too**
>
> A `<details>` whose content starts on the line immediately after `</summary>` renders as literal
> text in some Markdown renderers. The editor writes them correctly; hand-editing is where they get
> lost.

## Writing outside the portal

Any editor works. What the project needs from your file is:

- [x] Front matter at the top, with the keys in the canonical order.
- [x] Blocks in the marker form shown above.
- [x] The blank lines around markers and inside `<details>`.
- [ ] Nothing else. There is no build step and no lint gate you must satisfy by hand.

> [!TIP]
> **The fastest way to learn the syntax is to insert a block and read the file**
>
> Add a tabbed block in the editor, save it to a branch, and look at what appeared in the repository. Five minutes
> of that beats any syntax reference, including this one.

## Two things the editor will not let you do

| Construct | Why |
| :--- | :--- |
| Conditional content aimed at an audience | No reader surface enforces the audience, so the content would be visible to everyone — the validator rejects it rather than letting you believe otherwise |
| Related-article links without a stable id | The link needs an identity to point at, and an article that has not been imported yet does not have one |

[d360]: # 'snippet name="deleteMe"'
