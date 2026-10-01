# Comment Mentions — Users and User Groups

**Live prototype:** https://mariaarcevich.github.io/LPD-107439-Comment-Mentions/

Prototype for mentioning users and user groups in asset comments (CMS, CMP, DSR).

- Epic: [LPD-104086 — Mention users and user groups in asset comments](https://liferay.atlassian.net/browse/LPD-104086)
- Discovery: [LPD-107439 — Mention specific users or user groups in a comment](https://liferay.atlassian.net/browse/LPD-107439)
- Comments panel design: [Figma — Side Panel / Comments](https://www.figma.com/design/ghOut4w1bJlQ06qiMZrE0U/LPD-55596-EPIC-Extend-sidebar-fragment-for-building-custom-experiences-in-content-edition?node-id=1-28407)

## What it shows

- Comments side panel (280px) with composer, threaded replies, likes / dislikes, and the vertical bar.
- Typing `@` in the composer opens the mention list (behaviour modelled on the CKEditor 5 Mention plugin): type to filter, ↑/↓ to move, Enter/Tab to insert, Esc to close.
- **Users:** avatar + name + `@screenname`. Only users who can view the asset are listed.
- **User groups:** primary square sticker with the group initials + the number of users who will be notified. The count only includes members with View permission on the asset; groups where nobody can view it are not offered.
- Inserted mentions render in primary text (no background). Saving adds the comment to the top of the thread.

> The composer is a simulated editor (contenteditable + JS), not the real CKEditor 5.

Built with [Lexicon Vanilla](https://github.com/liferay-design/lexicon-vanilla) — plain HTML + CSS, no build step.
