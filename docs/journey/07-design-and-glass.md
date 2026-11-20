# 7. Design: from Classic paper to Glass

[← Handwriting and notebooks](06-handwriting-and-notebooks.md) · [Next: Widgets and everywhere →](08-widgets-and-everywhere.md)

## The first rules

The design spec from the planning days was strict. Stubborn, even. Warm off-white paper colours, ink-black text and exactly one accent blue. A serif font for dates and titles and a calm humanist sans for everything else. Hairline rules instead of boxes inside boxes.

It also had a list of banned things: gradients, glowing blobs, emoji as icons, neon, and specifically "glassmorphism or frosted blur".

Keep that last one in mind.

The paper look grew through September and October. The dark theme stayed close to the first prototype. Tabs were added on top once several notebooks could be open at the same time (2.6.0).

| Dark, with tabs | Paper, with a writing area in the day |
|---|---|
| ![Dark Day view with notebook tabs](../../assets/features/demo-day-view-tabs-dark.webp) | ![Light Day view with the writing area open](../../assets/notebooks/2026-10-02-day-view-writing-area.webp) |

## Why Glass

By November the app did a lot, and you could see it. Bars, panels, borders, more bars. It felt heavy, especially on a big iPad screen. Meanwhile Apple's own apps had moved to translucent, layered "glass" surfaces, and NorthStar started to look old next to them.

So I threw out my own rule from August. I don't think the rule was wrong back then. The app had simply changed. The new idea was this:

> The **controls** float on glass over a background. **Your pages stay paper.**

Your notes, timetable and notebooks never become see-through. Only the bars, menus and panels do.

## Eight rounds in five days

Glass became the new default on 10 November, with Classic kept as an option. Then came round after round of fixes.

Rounds 2 and 3 were dialogs, the pen sheet, typed notes, one pen toolbar everywhere and glass popups. Round 4 made glass work over any background, added a notebook "desk" and put the page curl back (see [chapter 6](06-handwriting-and-notebooks.md#the-page-curl-story)). Round 5 was about Classic. It had to look exactly like Classic again, and for a while it looked like Glass with the glass turned off. Rounds 6 and 7 brought transparent backgrounds, full-bleed documents and a live glass slider from 0 to 100. Round 8 finally gave me real frosted glass, like the preview I had picked, with one shared wallpaper.

Version 3.3.0 shipped it on 14 November: *"New appearance: Glass design, shared backgrounds, adjustable frost and palette-matched planner pages."*

| Classic | Glass |
|---|---|
| ![Month view in the Classic design](../../assets/glass/2026-11-14-classic-month.webp) | ![Month view in the Glass design](../../assets/glass/2026-11-14-glass-month.webp) |

| Glass, dark | Glass Day view |
|---|---|
| ![Glass Month view in dark mode](../../assets/glass/2026-11-14-glass-month-dark.webp) | ![Glass Day view](../../assets/glass/2026-11-14-glass-day.webp) |

| Glass tasks | Appearance settings |
|---|---|
| ![Glass Tasks with smart lists](../../assets/glass/2026-11-14-glass-tasks.webp) | ![Appearance settings: Classic or Glass, glass amount, frost](../../assets/glass/2026-11-14-glass-appearance-settings.webp) |

In a Glass notebook the page sits on the desk and the controls float above it.

| Notebook with page strip | Selection on a page |
|---|---|
| ![Glass notebook with the page strip](../../assets/glass/2026-11-14-glass-notebook-sideways.webp) | ![Lasso selection with the glass selection bar](../../assets/glass/2026-11-14-glass-notebook-selection.webp) |

## Glass without the cost

Frosted blur is expensive to draw. An iPad that draws a blur behind every bar while you write would ruin the pen latency from [chapter 1](01-the-question.md). So the app blurs the background once and keeps it, and every glass surface samples that saved blur. Nothing is blurred live, and there is never a blur inside a blur. The Day and Month views ended up with no live blurs at all.

## Accessibility

Reduce Transparency in the iOS settings turns the bars solid. The glass amount slider goes from 0 (solid, like Classic) to 100. I checked the layouts with text sizes from 100 % to 200 % and with every app font, down to a narrow phone.

What I'd tell myself in August: write down why each design rule exists. When things change, you then know which rule can go.

## From Classic to Glass, step by step

Settings in 1.1, the 3.0 look with the new tab bar, the design targets the Glass rounds were measured against, and real-device shots from the rounds after 3.3.

| 1.1: appearance settings | 3.0: Day with the tab bar | 3.0: Month with spirals |
|---|---|---|
| <img src="../../assets/history/1.1-settings-appearance.webp" alt="1.1: appearance settings" width="300"> | <img src="../../assets/history/3.0-day.webp" alt="3.0: Day with the tab bar" width="300"> | <img src="../../assets/history/3.0-month-spiral.webp" alt="3.0: Month with spirals" width="300"> |
| **3.0: documents with covers** | **Glass target: Month** | **Glass target: notebook** |
| <img src="../../assets/history/3.0-documents.webp" alt="3.0: documents with covers" width="300"> | <img src="../../assets/glass/2026-11-12-design-target-month.webp" alt="Glass target: Month" width="300"> | <img src="../../assets/glass/2026-11-12-design-target-notebook.webp" alt="Glass target: notebook" width="300"> |
| **Glass target: tasks** | **Glass target: typed note** | **Tasks before round 9** |
| <img src="../../assets/glass/2026-11-12-design-target-tasks.webp" alt="Glass target: tasks" width="300"> | <img src="../../assets/glass/2026-11-12-design-target-typed-note.webp" alt="Glass target: typed note" width="300"> | <img src="../../assets/glass/2026-11-15-tasks-before-round-9.webp" alt="Tasks before round 9" width="300"> |
| **Documents before round 9** | **Spiral month on a real iPad** | **A curtain that got removed** |
| <img src="../../assets/glass/2026-11-15-documents-before-round-9.webp" alt="Documents before round 9" width="300"> | <img src="../../assets/glass/2026-11-16-ipad-spiral-month.webp" alt="Spiral month on a real iPad" width="300"> | <img src="../../assets/glass/2026-11-17-pull-curtain-removed.webp" alt="A curtain that got removed" width="300"> |

## The Glass rounds on a real iPad

Before-shots from the rounds: what the screens looked like before round 4, an edit sheet from round 8, and a bug where glass amount 0 still was not solid.

| Month before round 4 | Documents before round 4 | Tasks before round 4 |
|---|---|---|
| <img src="../../assets/glass/2026-11-12-month-before-round-4.webp" alt="Month before round 4" width="300"> | <img src="../../assets/glass/2026-11-12-documents-before-round-4.webp" alt="Documents before round 4" width="300"> | <img src="../../assets/glass/2026-11-12-tasks-before-round-4.webp" alt="Tasks before round 4" width="300"> |
| **Stickers before round 4** | **Edit event, round 8** | **Glass amount 0 bug (email hidden)** |
| <img src="../../assets/glass/2026-11-12-stickers-before-round-4.webp" alt="Stickers before round 4" width="300"> | <img src="../../assets/glass/2026-11-14-edit-event-round-8.webp" alt="Edit event, round 8" width="300"> | <img src="../../assets/glass/2026-11-16-glass-amount-zero-bug.webp" alt="Glass amount 0 bug (email hidden)" width="300"> |

[Next: Widgets and everywhere →](08-widgets-and-everywhere.md)
