# 6. Handwriting and notebooks

[← The calendar](05-calendar.md) · [Next: Design and Glass →](07-design-and-glass.md)

Handwriting is the reason NorthStar exists, so it got more of my time than anything else. It's also where I changed my mind the most.

## Two ink engines, then one

Remember the setup screen from the prototype that asked which handwriting you want? For the first weeks NorthStar had two ink engines. On iPad and iPhone there was Apple ink, Apple's own drawing framework, with the best pen feel. And there was "works everywhere" ink, my own Flutter stroke engine, which you could edit on every device.

It sounded like the best of both. It turned out to be the worst of both. An Apple page was stored as Apple's own drawing data plus a picture, so on the web, on Android and on Windows it was just an image. My mum could write a note on the iPad and then not edit it on her laptop. On top of that I had to build every feature twice: lasso, pictures, tables, page turns.

On 6 September I removed the Apple engine. Apple Pencil support stayed, of course, with pressure, tilt, palm rejection and the Pencil squeeze. But all ink is now one format, drawn by one engine, and you can edit it on every device.

Taking it out was not just a delete. People already had pages written in the old format, so it needed a careful migration.

## Making the pen feel right

The goal from [chapter 1](01-the-question.md) never went away. The line has to follow the pen with no lag you can see. It took many releases to get there.

A stroke is drawn the instant the pen moves and only tidied when you lift it. The page you are writing on is never redrawn as a whole while you write. Pictures of pages get rendered at quiet moments and not on every autosave. If you hold the pen still for a moment, a line straightens or a scribble turns into a clean shape. And since 1.3.22 black ink turns white in dark mode, everywhere, at once.

The note for release 1.3.17 (26 October) says it shortest: *"Writing feels instant."* I was proud of that one.

## The tools grow up

In early October the notebook got a floating pen palette, a page menu and a lasso to move writing around.

| Floating pen palette | Lasso selection | Page and paper menu |
|---|---|---|
| ![Floating pen palette](../../assets/notebooks/2026-10-02-floating-pen-palette.webp) | ![Lasso selection around ink](../../assets/notebooks/2026-10-02-lasso-selection.webp) | ![Page menu with paper types](../../assets/notebooks/2026-10-02-page-menu-paper.webp) |

Later came an Apple-style pen toolbar with real-looking pens, pens and colours you can customize (2.3.0), a laser pointer for presenting (3.1.0) and a highlighter (3.4.0).

| Notebook with tabs | Customize pens | Laser pointer |
|---|---|---|
| ![A notebook with the pen toolbar and tabs](../../assets/features/2026-11-05-notebook-tabs.webp) | ![Customize pens settings](../../assets/features/2026-11-05-customize-pens.webp) | ![Laser pointer colours](../../assets/features/2026-11-05-laser-pointer.webp) |

## Notebooks, papers, covers

Notebooks have covers and a lot of papers: lines, wide and narrow lines, dots, grid, blank, and school papers like maths squares, a music staff and notes-with-summary. You can import a PDF as a notebook, bring in notebooks from other notebook apps, add tables, and export as PDF, image or a NorthStar file.

| Covers | New notebook | Export |
|---|---|---|
| ![Notebook covers in the Documents folder](../../assets/features/2026-11-05-notebook-covers.webp) | ![New notebook: cover, direction and paper](../../assets/features/2026-11-05-new-notebook-papers.webp) | ![Export sheet: NorthStar, Image, PDF](../../assets/features/2026-11-05-export-sheet.webp) |

| A table in a notebook | One big whiteboard | Page overview |
|---|---|---|
| ![A table on a notebook page](../../assets/notebooks/notebook-table.webp) | ![A mind map on the whiteboard](../../assets/notebooks/whiteboard-mind-map.webp) | ![Page overview strip beside a page](../../assets/notebooks/page-overview.webp) |

There is also handwriting correction, still in beta. You write a sample notebook in your best handwriting, and the app gently nudges new writing towards it. Your writing stays yours.

![Handwriting correction (beta) settings](../../assets/notebooks/handwriting-correction-beta.webp)

## The page curl story

No feature had more versions than turning a page.

On 2 September my rule was "no page curl". My own early design rules banned fake paper effects completely. No curl, no binder, no texture. Pages just slid.

By 9 September I had to admit that sliding felt cheap on an iPad. *"Turning a page is smooth now, and you can see the edge of the paper as it goes."* That was a first, simple page edge.

On 26 October a real page curl became the default turn in Book mode. I narrowed the early rule: a curl is allowed, but only as a visual effect, never over your writing.

A day later, on 27 October, my mum noticed something. While you dragged, the next page was not under the curl. It only appeared after you let go. I fixed it by preparing the real neighbouring pages in advance, and the curl got proper 3D perspective and a shadow.

5 November brought Open book. Two pages side by side, and the leaf curls across the spine and shows the next page on its back.

12 November was the bad day. During the Glass redesign the curl changed its look as a side effect of other work. Nobody asked for that, and I was not happy. The curl went back exactly as it was, and since then there is a rule that the page curl look is never changed by accident.

On 16 November there was one more bug. Adding a new page with a curl could briefly blank the page or double the ruled lines at the end of the animation. That got fixed and tested frame by frame:

![Test frames of the page curl, checked one by one](../../assets/notebooks/2026-11-16-page-curl-test-frames.webp)

![The page curl today](../../assets/notebooks/page-curl.webp)

With things people feel, like a page turn or a pen stroke, tiny changes matter a lot. So I protect what works, and I check it with my own eyes. A passing test is not enough here.

## More notebook history

Pictures from the What's new screens of earlier versions, and two bugs from November.

| 1.3: page menu | 1.3: copy pages | 1.3.5: picture tools |
|---|---|---|
| <img src="../../assets/history/1.3-page-menu.webp" alt="1.3: page menu" width="300"> | <img src="../../assets/history/1.3-copy-pages.webp" alt="1.3: copy pages" width="300"> | <img src="../../assets/history/1.3.5-picture-tools.webp" alt="1.3.5: picture tools" width="300"> |
| **1.3.6: handwriting correction** | **1.3.12: neat writing** | **2.0.4: Scroll, Book, Open book** |
| <img src="../../assets/history/1.3.6-handwriting-correction.webp" alt="1.3.6: handwriting correction" width="300"> | <img src="../../assets/history/1.3.12-neat-writing.webp" alt="1.3.12: neat writing" width="300"> | <img src="../../assets/history/2.0.4-page-flow-setting.webp" alt="2.0.4: Scroll, Book, Open book" width="300"> |
| **2.1: planner, blue binder** | **2.1: planner, leather** | **2.1: planner, month tabs** |
| <img src="../../assets/history/2.1-planner-blue-binder.webp" alt="2.1: planner, blue binder" width="300"> | <img src="../../assets/history/2.1-planner-leather.webp" alt="2.1: planner, leather" width="300"> | <img src="../../assets/history/2.1-planner-month-tabs.webp" alt="2.1: planner, month tabs" width="300"> |
| **2.1: spiral planner, page curl** | **Bug: Open book blank leaf (16 Nov)** | **Highlighter before the fix (17 Nov)** |
| <img src="../../assets/history/2.1-planner-spiral-curl.webp" alt="2.1: spiral planner, page curl" width="300"> | <img src="../../assets/notebooks/2026-11-16-open-book-bug.webp" alt="Bug: Open book blank leaf (16 Nov)" width="300"> | <img src="../../assets/notebooks/2026-11-17-highlighter-before-fix.webp" alt="Highlighter before the fix (17 Nov)" width="300"> |
| **3.1: everyday stickers** | | |
| <img src="../../assets/features/2026-11-05-stickers.webp" alt="3.1: everyday stickers" width="300"> | | |

## Notebook bugs from my own iPad

Real test pages from November, with my own scribbles.

| Day note before Glass round 5 | Day note with the page rail | Page shifted by the pen toolbar (name hidden) |
|---|---|---|
| <img src="../../assets/notebooks/2026-11-12-day-note-before-round-5.webp" alt="Day note before Glass round 5" width="300"> | <img src="../../assets/notebooks/2026-11-12-day-note-page-rail.webp" alt="Day note with the page rail" width="300"> | <img src="../../assets/notebooks/2026-11-17-page-shifted-by-toolbar.webp" alt="Page shifted by the pen toolbar (name hidden)" width="300"> |

[Next: Design and Glass →](07-design-and-glass.md)
