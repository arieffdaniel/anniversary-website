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

The photo sections render local images directly. Chapter 04 adds six random videos from a public Google Drive folder to the scrapbook. Every video receives its own stable archive-wide number, such as **Memory 001** or **Memory 247**, based on its order in the complete Drive collection; Shuffle keeps that video's number instead of resetting the visible cards to 01–06. Cards autoplay as muted, looping previews, and tapping one opens it fullscreen with sound and native controls. Configure the videos in `index.html`.

```js
driveVideos: {
  visibleCount: 6,
  folderId: "YOUR_GOOGLE_DRIVE_FOLDER_ID",
  apiKey: "YOUR_RESTRICTED_BROWSER_API_KEY",
},
```

Share the folder and each video as **Anyone with the link — Viewer**. Enable the Google Drive API in Google Cloud, and restrict the browser key to the website's HTTP referrer and the Google Drive API. Remember that a browser API key is visible in a static website's source.

## Video size

For local files, keep videos compressed for faster page loading. GitHub rejects individual files larger than 100 MB, and smaller web videos generally provide a better mobile experience. MP4 using H.264 video and AAC audio has the widest browser support.
