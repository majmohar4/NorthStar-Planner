# 1. The question: a blank page

[Next: Mum's idea →](02-mums-idea.md) · [Back to README](../../README.md)

Before there was a planner, there was a blank page.

The whole idea depended on one thing: **writing on a screen with an Apple Pencil has to feel good**. If the ink trails behind the pen tip, nobody will use it, no matter how clever the rest of the app is. So before planning a single screen, I wanted to know how much latency each way of building the app would give me.

## The experiment

I built the same thing three times: an empty page you can write on with an Apple Pencil.

1. **A native iPad page**, using Apple's own drawing framework.
2. **A Flutter page**, with my own stroke drawing on a canvas.
3. **A web page**, drawing into a browser canvas.

Then I wrote on all three, again and again, and compared how far the line lagged behind the Pencil.

## The result, and how it changed

The first answer was clear: **native was the obvious winner.** So the first versions of NorthStar used Apple's native ink on iPad and iPhone, with a Flutter whiteboard for everything else.

That did not last. When I started adding **notebooks**, with pages, paper types, pictures, a lasso and page turns, the native ink surface was not usable enough for what a notebook needs, and it only worked on Apple devices. So I gradually moved everything to the Flutter whiteboard and finally removed the native ink option on **6 September** (the story is in [chapter 6](06-handwriting-and-notebooks.md)).

After that the work was on the Flutter side: making the whiteboard faster and smoother, release after release, until writing in NorthStar felt really close to Apple's own Notes app, which was always the benchmark.

## What I learned

- **Measure first.** The blank-page test gave a clear answer on latency before any real code existed.
- **The best component is not always the best fit.** Native ink had the best latency on a blank page, but a notebook needs much more than a blank page.
- **One engine you can improve beats two you have to keep in sync.** Most of the pen feel was won later, by optimising the one engine NorthStar kept.

[Next: Mum's idea →](02-mums-idea.md)
