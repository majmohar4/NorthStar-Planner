# 2. Mum's idea

[← The question](01-the-question.md) · [Next: The first prototype →](03-first-prototype.md)

My mum is a teacher. Her week is a timetable: lessons, class periods, meetings, parents' evenings. All of that sits in the school's Outlook calendar. Her notes were everywhere else. A paper planner, a notes app, a notebook app on the iPad, loose PDFs, sticky notes.

What she asked for was simple. An app with her timetable that she can draw on, kept in sync with her Google and Outlook calendars.

Then it grew. While I was building it I kept getting new ideas, and I kept finding out they were actually possible. Notebooks, a whiteboard, tasks, widgets, more platforms. Her first wish stayed in the middle of it all, and I turned it into a few rules for myself.

The app shows the calendar she already has. Outlook came first, through a published calendar link, and Google and other calendar links later. She should never have to type an event in twice.

Notes sit next to the calendar and never inside it. A note about a lesson is hers. It doesn't belong to the school's calendar. So notes are stored in NorthStar and never written back to Outlook. I never changed this rule.

Handwriting comes first. Apple Pencil on the iPad is the main way in, and typing is the fallback.

It has to be on every device. iPad first, then iPhone, then the web on her Windows laptop. Android, Mac and Windows apps came later.

And it has to keep working when the internet doesn't. School Wi-Fi is not always kind. The app works offline and catches up later, and it must never lose what she wrote.

## Planning before building

For the first two days (21 and 22 August 2026) I only planned. No app code at all, on purpose. I wrote a product brief (what it is, who it's for, and a "v1 works" test), a data design for days, events, notes, notebooks and tasks, and a sync contract that says how devices and the server talk and what happens when things go wrong. I also wrote milestones, M1 to M8, and a design spec with strict rules: paper colours, one accent colour, real typography, no gimmicks.

The "v1 works" test was one sentence. I still like it:

> She plans a full school week on iPad with ink, sees it on her phone and laptop, the server goes down for a day, and nothing is lost or blocked.

For the look I collected paper planners, a handwritten week grid with Slovenian day names (PON, TOR, SRE, ČET, PET), minimal to-do apps, and classic daily planners with an hour grid on the left and Top 3, to-do and notes on the right. That last layout became the Day view. It has been the heart of the app ever since.

![The Day view layout from the first weeks: timetable on the left, Top 3, to-do and notes on the right](../../assets/prototype/2026-09-02-day-view-ipad-light.webp)

*Almost all screenshots in this repository use invented demo data: a made-up school week, made-up names and made-up notes. The few exceptions are marked.*

[Next: The first prototype →](03-first-prototype.md)
