---
title: Search
internalDescription: How readers find content, what writers control, and reading the failed-search report.
tags:
  - readers
  - writer
labels:
  - sample-content
seo:
  title: Search in a Document360 knowledge base
  description: What makes a page findable, and what to do about searches that find nothing.
display:
  toc: true
  outline: true
---

Most readers do not browse your navigation. They search, read one page, and leave. Writing for that
reader is a different discipline from writing a manual to be read in order.

## What a writer controls

[d360]: # 'table border="all" striped="true"'

| Lever | Where | Effect |
| :--- | :--- | :--- |
| Title | `title` in front matter | The strongest signal there is |
| Headings | The article body | Nearly as strong, and how a reader scans |
| SEO title and description | `seo` in front matter | What a search engine shows |
| Tags | `tags` in front matter | Grouping and filtering |
| Exclusion | `search.exclude` | Keeps a page out of results |
| AI exclusion | `search.excludeAi` | Keeps a page out of AI answers |
| External exclusion | `search.excludeExternal` | Keeps a page out of external search |

[d360]: # "/table"

> [!IMPORTANT]
> **Title the page with the words the reader has, not the words you have**
>
> They search "can't sign in", not "authentication troubleshooting". They search "invoice", not
> "billing statement reconciliation". Your internal vocabulary is the thing standing between them and
> the page you already wrote.

## Writing a page that answers

Four habits, and they cost nothing:

[d360]: # 'multi-level-list styles="decimal,lower-alpha"'

1. **Answer in the first paragraph.** The reader arrived mid-problem; the background can wait.
2. **Make each section stand alone.**
   1. A reader arriving at a heading from search has not read the one above it.
   2. Which is why "as explained above" is a phrase worth deleting on sight.
3. **Say the thing, then explain it.** Not the other way round.
4. **Name what the page does not cover**, and link to what does.

[d360]: # "/multi-level-list"

> [!TIP]
> **Write the heading as the question somebody would type**
>
> "Why is my import failing?" is findable. "Import subsystem error handling" is not, however accurate
> it is.

## What is in the index

Search covers the current workspace, as it is live on the tracked branch. Nothing else.

| In the index | Not in the index |
| :--- | :--- |
| Published content on the tracked branch | Anything on a working branch |
| | Branch saves |
| | Unpublished drafts |
| | Another workspace's content |

Content reaches the index in one of two ways: you publish it, or it arrives in an import from the
tracked branch. There is no third route, which is why a page that exists and cannot be found is
nearly always a page that is not published yet.

> [!IMPORTANT]
> **A branch is invisible to search on purpose**
>
> It is what makes a working branch safe for an unannounced feature. It also means you cannot check
> findability until the change is live — so check the wording before you merge, not after.

## Questions that found nothing

The list of questions readers asked and got nothing for is the most useful editorial input there is:
each one is a question in a reader's own words, with a count attached.

| What it means | What to do |
| :--- | :--- |
| No page exists | Write it |
| A page exists under a different word | Change the title, or add the reader's word to it |
| The question is unanswerable | Ignore it |
| It is a question for a different team | Send it to them |

[d360]: # 'callout kind="success"'

> **Collect those questions deliberately, because nothing here collects them for you**
>
> The Analytics module is not part of this product type in the MVP release, so the list has to come
> from where your team already meets readers — the support queue above all. Half an hour a month on
> it replaces every argument about what to document next.

[d360]: # "/callout"

## Excluding a page

`search.exclude` keeps a page out of results while leaving it reachable by link. Legitimate uses are
narrow:

- [x] A page that exists for one audience who always arrive by link.
- [x] A deprecated page kept only so an old address resolves.
- [ ] Not for hiding something you would rather readers did not find — if it should not be read, it
      should not be published.

> [!CAUTION]
> **An excluded page is still public**
>
> It is not findable; it is not protected. Anybody with the URL reads it, and URLs travel.

<details>
<summary>Does content inside an accordion get indexed?</summary>

Yes. Collapsed content is indexed and matched, and a reader arriving from search sees it open.
Putting something in an accordion hides it from the page, not from search.

</details>

<details>
<summary>Why does my new page not appear in search?</summary>

Check in this order: it is published on the tracked branch rather than sitting on a working branch or
as a draft; you are searching the workspace it belongs to; it is not `hidden`; it does not carry
`search.exclude`; and enough time has passed for the index to refresh. The first check catches most
of them.

</details>

[d360]: # 'snippet name="deleteMe"'
