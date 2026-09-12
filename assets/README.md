# Website assets

Store local media for the anniversary website in these folders:

- `images/` — photos and artwork (`.jpg`, `.jpeg`, `.png`, `.webp`, `.gif`)
- `videos/` — video clips (`.mp4`, `.webm`)

Use simple lowercase filenames without spaces, for example:

```text
assets/images/first-date.jpg
assets/images/family-photo.webp
assets/videos/our-memories.mp4
```

Then reference an image from `index.html` like this:

```js
image: "assets/images/first-date.jpg",
```

or:

```js
hero: "assets/images/where-we-met.jpg",
```

The current photo sections render images. Files placed in `videos/` are stored and ready, but a video must be connected to a section in `index.html` before it will appear on the website.

## Video size

Keep videos compressed for faster page loading. GitHub rejects individual files larger than 100 MB, and smaller web videos generally provide a better mobile experience.
