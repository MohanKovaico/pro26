---
title: Feedback
internalDescription: Reader voting and comments, how to read them, and turning them into work.
tags:
  - readers
  - writer
labels:
  - sample-content
seo:
  title: Reader feedback in a Document360 knowledge base
  description: What readers can tell you, and what to do with it.
display:
  toc: true
  outline: true
---

Readers can tell you a page helped or did not. It is a small signal, and it is the only one that
comes from the person the page was written for.

## Voting

Each article can show a helpful / not helpful control, configured per article with `feedback.voting`
in front matter.

> [!NOTE]
> **Voting is on by default, so you will not usually see the key written**
>
> Front matter records booleans only where they differ from the stored default. An article with no
> `feedback` block has voting enabled; a file that says `voting: false` has had it deliberately
> switched off.

## Reading a score honestly

[d360]: # 'table border="all" striped="true"'

| What you see | What it probably means |
| :--- | :--- |
| High score, many votes | The page works. Leave it alone |
| Low score, many votes | Fix this first — it is failing the most people |
| Low score, few votes | Possibly a bad page, possibly three annoyed readers |
| No votes at all | Nobody is reading it, or nobody cares enough to vote |

[d360]: # "/table"

> [!IMPORTANT]
> **A score tells you where to look, never what to change**
>
> "Not helpful" from forty readers says the page is failing and nothing about why. The comments, what
> support hears about the same subject, and reading the page yourself as though you had the problem —
> those tell you why.

## Comments

Where comments are enabled, readers can say what was wrong in their own words, which is worth more
than any amount of voting.

[d360]: # 'callout kind="success"'

> **A reader who writes a comment has done you a favour at their own expense**
>
> They were trying to get something done and stopped to tell you the documentation failed. Treat the
> comment as a bug report, and answer it — people who get an answer report again.

[d360]: # "/callout"

## Turning feedback into work

[d360]: # 'multi-level-list styles="decimal,lower-alpha"'

1. Read the comment and the page together, in that order.
2. Decide what kind of failure it is.
   1. **Wrong** — the page says something untrue. Fix it today.
   2. **Missing** — the page does not cover the case. Add it.
   3. **Unfindable** — the answer was there and they did not see it. A structure or title problem.
   4. **Not a documentation problem** — the product is confusing. Tell whoever owns the product.
3. Make the change as an ordinary reviewed change.
4. Where somebody left contact details and the fix is theirs, tell them.

[d360]: # "/multi-level-list"

> [!CAUTION]
> **The fourth category is the one that gets mislabelled**
>
> A page that has to explain a confusing screen will always score badly, however well written. Some
> documentation failures are product failures wearing a documentation costume, and rewriting the page
> for a third time will not fix them.

## What not to do with feedback

| Do not | Because |
| :--- | :--- |
| Target a feedback score | The fastest way to raise one is to stop asking |
| Switch voting off on a badly-scoring page | You lose the signal and the page stays bad |
| Rewrite on a single "not helpful" | One reader is not a pattern |
| Ignore a comment because the tone is sharp | An annoyed reader is still usually right about the facts |

[d360]: # 'callout kind="error"'

> **Never argue with a reader in a public comment**
>
> Even when they are wrong about the facts. Fix what is fixable, answer plainly, and move the
> disagreement somewhere it is not published beneath your documentation.

[d360]: # "/callout"

## A quarterly habit

[d360]: # 'divider style="dashed"'

---

- [ ] Every page with a falling score, read as a reader would.
- [ ] Every comment from the quarter, triaged into the four categories above.
- [ ] The questions support answered that a page should have.
- [ ] Anything carrying `status.expiresAt` in the next quarter.

[d360]: # 'snippet name="deleteMe"'
