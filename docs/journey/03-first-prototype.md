# 3. The first prototype (with all its bugs)

[← Mum's idea](02-mums-idea.md) · [Next: Sync and the server →](04-sync-and-the-server.md)

Building started on 22 August 2026. The first milestone was small on purpose: a header, the Month / Week / Day switch, swiping between days, pinch zoom that keeps the spot under your fingers, and a settings page for theme, accent colour, weekends and school hours.

Within a week the app had a timetable you could write on, a Top 3, a to-do list, a server, sign-in and a first web build. Version **0.6.0** shipped to my mum's iPad on **28 August**, one week after the first planning commit.

## What it looked like

The first look was dark, calm and quite bare. Events were grey rows on a lesson grid, the right side held Top 3, short notes, to-do and a notes area.

| Day, 28 August | Month, 28 August |
|---|---|
| ![First Day view, dark](../../assets/prototype/2026-08-28-day-view-dark.webp) | ![First Month view, dark](../../assets/prototype/2026-08-28-month-view-dark.webp) |

Four days later the panels got frames, numbered Top 3 rows (01, 02, 03), a "day 258 / 365" counter and a coloured date stamp:

| Day, 1 September | Month, 2 September |
|---|---|
| ![Day view with framed panels](../../assets/prototype/2026-09-01-day-view-dark-cards.webp) | ![Month view with event chips](../../assets/prototype/2026-09-02-month-view-dark.webp) |

And there was a light "paper" theme, which slowly became the main look:

![Week view, early September](../../assets/prototype/2026-09-02-week-view-ipad-light.webp)

The phone got its own layout with a bottom bar:

<img src="../../assets/prototype/2026-09-02-day-view-phone-dark.webp" alt="Day view on a phone, early September" width="320">

The first whiteboard and the first task lists were very plain:

| First whiteboard | First tasks |
|---|---|
| ![First whiteboard with a simple pen bar](../../assets/prototype/2026-09-02-first-whiteboard.webp) | ![First task lists](../../assets/prototype/2026-09-02-first-tasks.webp) |

## The first setup

A first-run setup asked for the calendar link and, at that time, **which handwriting engine** to use: Apple's native ink, or "works everywhere" ink. Keep that second screen in mind, it comes back in chapter 6.

| Add your calendar | Choose your handwriting |
|---|---|
| <img src="../../assets/prototype/2026-09-02-setup-add-calendar.webp" alt="Setup: add your calendar" width="300"> | <img src="../../assets/prototype/2026-09-02-setup-two-handwriting-engines.webp" alt="Setup: Apple Pencil ink or ink that works everywhere" width="300"> |

## The bugs

The prototype worked, mostly. The release notes from those weeks read like a bug diary:

- **0.6.0:** "Settings stopped forgetting your theme, and sync no longer gets stuck."
- **0.8.0:** "Handwriting fixes for both kinds of handwriting, and the web app can save again."
- **0.11.0:** "Fixes for what you reported in 0.10.0."
- **0.12.0:** "Fixes for what you reported, and for things that were quietly broken."
- **0.15.0:** "Ink can no longer land on the wrong page."
- **0.16.0:** "The web app no longer loses the last thing you did."

Some favourites from that time:

- **Ink on the wrong page.** Turn a page quickly while the pen is still down and the stroke would land on the next page.
- **The web app opened blank.** The web build shipped with a stock start page that showed nothing until everything had loaded. On a slow connection that looked like a dead app.
- **Settings did not sync**, because of two separate bugs that each failed silently.
- **A real school week almost went public.** The very first landing page screenshots had been taken on a build connected to a real calendar. It was caught before anything was published, and from then on every public picture had to come from an invented demo week. That rule is why almost every screenshot here shows "Mathematics 7.B" and a made-up staff meeting. The only exceptions are a few shots of the very first build below, kept in on purpose because they show day one.

When the app could not open its local data after an update, it at least said so honestly instead of pretending to save:

<img src="../../assets/prototype/2026-09-21-error-cannot-open-data.webp" alt="Error screen: NorthStar cannot open your data on this device" width="480">

### What I learned

- **Ship early to the one real user.** My mum found things in a day that no test found in a week.
- **Silent failures are the worst kind.** A crash gets reported. A setting that quietly does not sync just makes someone stop trusting the app. From here on, the rule was: if something did not save, the app has to say so.

## More from the first weeks

The very first build on 22 August was an empty month. A few days later came the first web build, test renders with placeholder fonts, and in September a full first-run setup.

| First build, 22 Aug | First web build, 27 Aug | Placeholder-font test render |
|---|---|---|
| <img src="../../assets/prototype/2026-08-22-first-build-month.webp" alt="First build, 22 Aug" width="300"> | <img src="../../assets/prototype/2026-08-27-web-app-empty.webp" alt="First web build, 27 Aug" width="300"> | <img src="../../assets/prototype/2026-08-27-font-loading-placeholder.webp" alt="Placeholder-font test render" width="300"> |
| **Setup: choose a look** | **Setup: draw on the timetable** | **Setup: school hours** |
| <img src="../../assets/prototype/2026-09-21-setup-theme.webp" alt="Setup: choose a look" width="300"> | <img src="../../assets/prototype/2026-09-21-setup-timetableInk.webp" alt="Setup: draw on the timetable" width="300"> | <img src="../../assets/prototype/2026-09-21-setup-schoolHours.webp" alt="Setup: school hours" width="300"> |
| **Setup: where your notes live** | **Setup: what it costs (later dropped)** | **Phone, no calendar yet** |
| <img src="../../assets/prototype/2026-09-21-setup-plan.webp" alt="Setup: where your notes live" width="300"> | <img src="../../assets/prototype/2026-09-04-setup-what-it-costs.webp" alt="Setup: what it costs (later dropped)" width="300"> | <img src="../../assets/prototype/2026-09-04-phone-no-calendar.webp" alt="Phone, no calendar yet" width="300"> |

## The very first build, with the real calendar

On 22 August the first build ran on the iPad simulator against my mum's real school calendar link. This is what the app looked like on day one, before any design work.

| Day, 22 Aug | Month, 22 Aug | Week, 22 Aug |
|---|---|---|
| <img src="../../assets/prototype/2026-08-22-first-build-day-real-calendar.webp" alt="Day, 22 Aug" width="300"> | <img src="../../assets/prototype/2026-08-22-first-build-month-real-calendar.webp" alt="Month, 22 Aug" width="300"> | <img src="../../assets/prototype/2026-08-22-first-build-week-real-calendar.webp" alt="Week, 22 Aug" width="300"> |
| **Welcome email (address hidden)** | **My admin page (details hidden)** | |
| <img src="../../assets/prototype/2026-09-21-welcome-email.webp" alt="Welcome email (address hidden)" width="300"> | <img src="../../assets/prototype/2026-09-04-admin-page.webp" alt="My admin page (details hidden)" width="300"> | |

[Next: Sync and the server →](04-sync-and-the-server.md)
