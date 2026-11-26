---
type: page
title: Writing
icon: ✍️
tags:
  - editor
  - writer
labels:
  - sample-content
seo:
  title: Writing in a Document360 Lotus project
  description: The editor, the blocks available to you, and how to reuse content.
display:
  toc: true
---

| Page | Covers |
| :--- | :--- |
| [The editor](the-editor.md) | <span data-variable="editorName">{{variable.editorName}}</span>, and what it writes to disk |
| [Blocks](blocks.md) | Every block you can add, and what each becomes in Markdown |
| [Reuse](reuse.md) | Snippets, variables and glossary terms |

## One thing worth knowing before you start

Your article is a Markdown file, and the blocks you insert are written into that file in a specific
form. You do not have to think about it — but when you look at a diff, or edit a file outside the
portal, it helps to know that the form is deliberate and that keeping it is what stops the editor
rewriting your file later.

> [!NOTE]
> **Write in the editor, read the Markdown when you are curious**
>
> Nobody needs to learn the syntax to use this product. The reason these pages show it at all is
> that in a Git-backed project you will eventually see a diff, and an unexplained diff is unsettling.

## The shape of an article

Every article is front matter, then content:

```markdown
---
title: The article's title
tags:
  - writer
---

Content starts here.
```

Front matter carries the metadata — title, tags, SEO, display options. See
Front matter for the full set of keys.

[d360]: # 'snippet name="deleteMe"'
