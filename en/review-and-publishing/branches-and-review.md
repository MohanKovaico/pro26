---
title: Branches and review
internalDescription: What a branch is for a writer, how review works, and who can approve.
tags:
  - git
  - publishing
  - writer
labels:
  - sample-content
seo:
  title: Branches and review in a Document360 Lotus project
  description: Where your work lives before it is published, and how it gets approved.
display:
  toc: true
  outline: true
---

## A branch, for a writer

A branch is a copy of the documentation that only your work affects. You write on it, save as often
as you like, and nothing you save is visible to readers.

[d360]: # 'table border="all" striped="true"'

| | On a branch | Published |
| :--- | :--- | :--- |
| Who sees it | You, and anybody who looks at the branch | Readers |
| How often you save | As often as you like | — |
| Half-finished work | Fine | Not fine |
| Reversible | Yes, entirely | Only by publishing again |

[d360]: # "/table"

> [!IMPORTANT]
> **Every role sees the branch they are working on**
>
> This was once hidden from writers on the theory that they would rather not know. It is shown
> instead, because a writer who does not know where their work lives cannot tell whether it is safe,
> and that uncertainty costs more than the concept does.

## The controls on a branch

Save to branch is the main button; Create pull request, Ready to merge, Merge and publish and Sync
are under **More branch actions**. Knowing which does what is most of working on a branch.

[d360]: # 'table border="all" striped="true"'

| | Does |
| :--- | :--- |
| **Save** | Keeps a draft in Document360 only. Nothing reaches Git |
| **Save to branch** | Commits all your drafts on that branch as one commit. Never publishes, never indexes, never opens a pull request |
| **Create pull request** | Opens a draft pull request, after a first save |
| **Ready to merge** | Turns the draft into an open pull request |
| **Merge and publish** | Merges into the tracked branch and publishes |

[d360]: # "/table"

> [!IMPORTANT]
> **Save and Save to branch are different buttons and the difference matters**
>
> Save leaves your work in Document360 where nobody else's checkout can see it. Save to branch is the
> one that puts it in Git. A writer who only ever uses Save has work that exists in one place, and
> will be surprised the day somebody asks why the branch is empty.

## Review as a pull request

The change becomes a pull request in GitHub, reviewed where your engineers already review code. The
menu shows its number and status, and links to it.

The sync action is labelled with the tracked branch's name: **Sync with main**, for instance. It is
offered when the branch is behind the tracked branch, when it conflicts with it, and while a conflict
is being resolved. It saves
your unsaved drafts first, brings the tracked branch's changes in, and opens any overlaps in the
conflict review.

**Merge and publish** is disabled with a visible reason when it cannot run: still a draft, needs a
sync with main, a required review or check has not passed, or you do not have permission to publish.

> [!NOTE]
> **Document360 never works around your GitHub review process**
>
> If the tracked branch requires a pull-request review, editing on it is blocked and you are offered
> a branch instead. If your repository requires checks, Merge and publish waits for them. The rules
> your engineers set for code apply to documentation unchanged.

[d360]: # 'callout kind="success"'

> **Both can be true at once**
>
> An approval inside Document360 that materialises as a pull request is the combination this product
> type exists to offer. A writer gets a review experience built for writing; an engineering
> organisation gets a pull request in the place it expects one.

[d360]: # "/callout"

## What a reviewer should actually check

[d360]: # 'multi-level-list styles="decimal,lower-alpha"'

1. **Is it true?** The only question that cannot be automated.
2. **Is it in the right place?** A correct article in the wrong category is hard to find.
3. **Does it belong to somebody?** An article with no owner is an article nobody will update.
4. **What else does it change?**
   1. A snippet edit changes every article that uses it.
   2. A manifest edit changes the navigation.
   3. A rename changes addresses readers already hold.

[d360]: # "/multi-level-list"

> [!CAUTION]
> **A small diff is not the same as a small change**
>
> One line in a snippet is twenty pages. One reordered node is your whole navigation. Read what the
> diff *does*, not how long it is.

## Keeping a branch short-lived

> [!WARNING]
> **A branch open for a month is a merge conflict with a date attached**
>
> The longer a branch runs, the more the published content moves underneath it. Small changes
> reviewed quickly are easier for everybody than a fortnight of work arriving at once — and that is
> as true of documentation as it is of code.

## Attribution

Changes you make are attributed to you. Where Document360 knows your Git identity, the commit is
attributed to that identity; where it does not, the change is still attributed to you inside
Document360 and the commit carries the project's identity instead.

> [!NOTE]
> **Link your Git identity if you want your name on the commits**
>
> It costs one step and it means the repository's history reads correctly — which matters to the
> engineers reviewing it, and to anybody later asking who wrote something.

[d360]: # 'snippet name="deleteMe"'
