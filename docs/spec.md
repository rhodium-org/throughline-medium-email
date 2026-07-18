# Medium — Email — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates
it in CI. The prose headings are hand-owned — everything between `tl:*` markers is
injected from the YAML items, so the published spec can never drift from the graph.

This source is the **medium axis** for one channel: an **email**, read in a crowded
inbox, often on a phone in a narrow preview pane, skimmed rather than read, judged from
its From name and subject line before it is opened, carrying live links and possibly read
with images turned off. It governs how delivery is *shaped for that channel* — structure,
length, navigation, framing and presentation — not universal readability, spelling,
punctuation, register, purpose or audience, each of which is its own throughline source.
Email sits between its siblings: like a **letter** it is addressed correspondence with a
greeting and a sign-off, but like a **web** page it carries live links and one call to
action, and unlike a postal letter it has no address block. Channels are mutually
exclusive: **email**, **web**, **letter**, **SMS** and **print** are sibling sources and
a consumer composes exactly one under the `medium` namespace. Every principle is a
`user_requirement`; every rule is a `system_requirement` that `implements` its principle.
The throughline UIDs are this source's own and immutable — a consumer cites a rule as
`medium:SR-0001`.

It carries
<!-- tl:count type == 'user_requirement' -->
5
<!-- tl:end --> principles and
<!-- tl:count type == 'system_requirement' -->
10
<!-- tl:end --> rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — Text is delivered as an email** — `intent`, status `approved`

> An email lands in a crowded inbox, is often read on a phone in a narrow preview pane, and is judged from its From name and subject line before it is opened. The reader skims it, may read it with images turned off, can click links and expects a greeting and a sign-off but no postal address block. This axis governs how delivery is shaped for that channel — structure, length, navigation, framing and presentation — not universal readability, spelling, register, purpose or audience, each of which is a separate source. Channels are mutually exclusive: a consumer composes exactly one of the web, letter, email, SMS or print sibling sources.

**source_ref**: TBS Medium — Email
<!-- tl:end -->

## 1. Structure the email so the point survives a skim

<!-- tl:item UR-0001 -->
**UR-0001 — Structure the email so the point survives a skim** — `user_requirement`, status `approved`

> An email is skimmed in a crowded inbox, often in a narrow preview pane; lead with the point and let the rest follow so it reads top to bottom.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Email — Structure for the channel
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0001' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Put the main point and any action in the first line |
| SR-0002 | system_requirement | approved | Order the email as a single top-to-bottom read |
<!-- tl:end -->

## 2. Keep the email short and to a single purpose

<!-- tl:item UR-0002 -->
**UR-0002 — Keep the email short and to a single purpose** — `user_requirement`, status `approved`

> An email competes with a full inbox and is read quickly, so keep it brief, focused on one purpose, and easy to skim.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Email — Length and density
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0002' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0003 | system_requirement | approved | Keep the email to a single purpose |
| SR-0004 | system_requirement | approved | Keep it short and skimmable with brief paragraphs |
<!-- tl:end -->

## 3. Point and prompt with the inbox's live affordances

<!-- tl:item UR-0003 -->
**UR-0003 — Point and prompt with the inbox's live affordances** — `user_requirement`, status `approved`

> An email can carry links and a button but may be read with images off; give one clear call to action as a descriptive text link.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Email — Navigation and actions
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0003' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0005 | system_requirement | approved | Offer one clear call to action as a text link |
| SR-0006 | system_requirement | approved | Do not rely on an image or button alone for the action |
<!-- tl:end -->

## 4. Frame the email with its subject, greeting and sign-off

<!-- tl:item UR-0004 -->
**UR-0004 — Frame the email with its subject, greeting and sign-off** — `user_requirement`, status `approved`

> An email is framed by a From name, a subject line, a greeting and a sign-off, but no postal address block; give it that framing so it reads as addressed correspondence.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Email — Opening and closing
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0004' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0007 | system_requirement | approved | Write a specific, informative subject line |
| SR-0008 | system_requirement | approved | Open with a greeting and close with a sign-off, without an address block |
<!-- tl:end -->

## 5. Present the email to render everywhere

<!-- tl:item UR-0005 -->
**UR-0005 — Present the email to render everywhere** — `user_requirement`, status `approved`

> Email clients render inconsistently and may block images, so keep the layout simple and robust and do not depend on images or rich formatting.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Email — Presentation and formatting
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0005' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0009 | system_requirement | approved | Make sure the email still makes sense with images off |
| SR-0010 | system_requirement | approved | Keep formatting simple so it renders across clients |
<!-- tl:end -->
