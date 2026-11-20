# 1. The question: a blank page

[Next: Mum's idea →](02-mums-idea.md) · [Back to README](../../README.md)

Before I planned a single screen, I had one worry. Writing with an Apple Pencil has to feel good. If the line drags behind the tip of the pen, my mum won't use the app, and it doesn't matter how clever everything else is.

So I didn't start with a planner. I started with a blank page.

## The test

I built the same thing three times: an empty page you can write on with an Apple Pencil. Once as a native iPad page with Apple's own drawing framework. Once in Flutter, with my own stroke drawing on a canvas. And once as a web page, drawing into a browser canvas.

Then I sat there and scribbled on all three, again and again, watching how far the line fell behind the Pencil.

## What came out of it

Native won, and it wasn't close. So the first versions of NorthStar used Apple's native ink on iPad and iPhone, and a Flutter whiteboard for everything else.

That didn't survive notebooks. Once I started adding pages, paper types, pictures, a lasso and page turns, native ink was not usable enough for what a notebook needs. It also only worked on Apple devices. I moved things over to the Flutter whiteboard bit by bit and removed the native ink option on 6 September. [Chapter 6](06-handwriting-and-notebooks.md) has the full story.

From then on all the work went into the Flutter side. Release after release I made the whiteboard faster and smoother, until writing in NorthStar felt very close to Apple's own Notes app. Notes was always the thing I compared against.

I'm still glad I tested before building anything. The blank page gave me a clear answer about latency before any real code existed. It just wasn't the whole answer, because a notebook is a lot more than a blank page. And most of the pen feel came later anyway, from tuning the one engine I kept.

[Next: Mum's idea →](02-mums-idea.md)
