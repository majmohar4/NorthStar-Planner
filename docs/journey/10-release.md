# 10. Release: stores, landing page, promo video

[← Polish and feedback rounds](09-polish-and-feedback-rounds.md) · [Next: What's next →](11-whats-next.md)

For most of its life NorthStar was installed by hand: on my mum's iPad and iPhone, on my own devices, as a web app and as an Android APK. Going public meant stores, a landing page, store pictures, privacy texts, and review.

## The landing page

The landing page at [northstar.majmohar.eu](https://northstar.majmohar.eu) is generated from one content file, in English and Slovenian, and it went through its own journey:

- **August:** a first spec: warm paper colours like the app, one clear hero, screenshots from the demo week.
- **2 October:** a redesign with a live Day view you can draw on in the browser, and short silent films of the app (writing on a lesson, the Top 3, the pen palette).
- **5 November:** a *New in 3.0* gallery and download buttons, plus a clear section on what NorthStar does with Google data, needed for Google's verification of calendar access.
- **9 November:** five pages (home, features, download, pricing, story). Pricing is simple: the app is free, donations are optional.
- **16 November:** redone in the Glass look.

![The landing page in October, with a live Day view you can write on](../../assets/release/2026-10-02-first-landing-page.webp)

## Store pictures

All store screenshots are made from the same invented demo week, rendered at exact store sizes, with a short headline on each.

| | | |
|---|---|---|
| ![Store picture: Your calendar. Your handwriting.](../../assets/release/store-ipad-01-notebook.webp) | ![Store picture: Your whole week at a glance.](../../assets/release/store-ipad-03-week.webp) | ![Store picture: The month ahead, planned in one view.](../../assets/release/store-ipad-04-month.webp) |
| ![Store picture: To-dos that never slip.](../../assets/release/store-ipad-05-tasks.webp) | ![Store picture: Every notebook in one place.](../../assets/release/store-ipad-06-documents.webp) | |

![Store banner with iPad and iPhone](../../assets/release/store-universal-banner.webp)

## App Store

The App Store listing covers iPhone, iPad and Mac. Review did not go through on the first try. App Review sent the submission back with a request for more information, including **a screen recording of the full user flow**, which I had not provided. So I recorded it myself on a MacBook: open the app, sign in, walk through the calendar, notes, handwriting, notebooks and tasks, sign out, and a second clip showing how to delete an account. Together with a written explanation of what the app is for and which services it relies on, it went back to review.

**Learned:** reviewers can only judge what they can see. Make it easy for them: a ready demo account with a sample timetable, a short recording, and plain answers.

[App Store link](https://apps.apple.com/app/id6831786463)

## Google Play

Google Play had its own surprises:

- The very first upload was **rejected because it was signed with a debug certificate**. It was rebuilt with a proper upload key.
- A personal developer account must run a **closed test with at least 12 testers for 14 days** before the app can go public. So NorthStar is in closed testing on Google Play right now. [Ask to join](https://play.google.com/store/apps/details?id=eu.majmohar.northstar).

Until then, the Android APK on the [Releases page](https://github.com/majmohar4/NorthStar-Planner/releases) works on any Android device and updates itself.

## Web, Windows, Mac and Linux

- The **web app** at [app-northstar.majmohar.eu](https://app-northstar.majmohar.eu) is always the newest version.
- **Windows** and a direct **macOS** download go to [Releases](https://github.com/majmohar4/NorthStar-Planner/releases). They are not code-signed, see the [install notes](../../README.md#install-notes). A **Linux** build is coming soon.

## Promo video

*Coming soon.* A short promo video of NorthStar is in the works and will be linked here when it is final. A still from the current cut:

![Promo video poster, work in progress](../../assets/release/promo-v3-poster.webp)

## Earlier store and landing pictures

The app icon barely changed, it only got sharper. The first store set (3.1, November) used the Classic look. The landing page's Day picture was re-shot for every big version.

| App icon, August | App icon, November | Google Play feature graphic |
|---|---|---|
| <img src="../../assets/history/icon-2026-08.webp" alt="App icon, August" width="300"> | <img src="../../assets/history/icon-2026-11.webp" alt="App icon, November" width="300"> | <img src="../../assets/release/play-feature-graphic.webp" alt="Google Play feature graphic" width="300"> |
| **3.1 store set: Day** | **3.1 store set: Month** | **3.1 store set: notebooks** |
| <img src="../../assets/history/3.1-store-day.webp" alt="3.1 store set: Day" width="300"> | <img src="../../assets/history/3.1-store-month.webp" alt="3.1 store set: Month" width="300"> | <img src="../../assets/history/3.1-store-notebooks.webp" alt="3.1 store set: notebooks" width="300"> |
| **Landing Day, October** | **Landing Day, November** | **Landing film poster, October** |
| <img src="../../assets/history/landing-day-2026-10.webp" alt="Landing Day, October" width="300"> | <img src="../../assets/history/landing-day-2026-11.webp" alt="Landing Day, November" width="300"> | <img src="../../assets/release/2026-10-02-landing-film-poster.webp" alt="Landing film poster, October" width="300"> |
| **Store: iPad day (3.4)** | **Store: iPhone Top 3** | **Store: iPhone day** |
| <img src="../../assets/release/store-ipad-02-day.webp" alt="Store: iPad day (3.4)" width="300"> | <img src="../../assets/release/store-iphone-top3.webp" alt="Store: iPhone Top 3" width="300"> | <img src="../../assets/release/store-iphone-day.webp" alt="Store: iPhone day" width="300"> |
| **Store: iPhone notebook** | | |
| <img src="../../assets/release/store-iphone-notebook.webp" alt="Store: iPhone notebook" width="300"> | | |

[Next: What's next →](11-whats-next.md)
