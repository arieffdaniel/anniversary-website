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

The photo sections render local images directly. Chapter 04 adds six random videos from a public Google Drive folder to the scrapbook. Each card uses a short romantic caption instead of an unreliable Drive date or filename and autoplays as a muted, looping preview; tapping one opens it fullscreen with sound and native controls. Visitors can also shuffle to a new random selection. Configure the videos and editable caption list in `index.html`.

```js
driveVideos: {
  visibleCount: 6,
  folderId: "YOUR_GOOGLE_DRIVE_FOLDER_ID",
  apiKey: "YOUR_RESTRICTED_BROWSER_API_KEY",
  captions: [
    "a little piece of us",
    "one for the memories",
    "ordinary days, favourite moments",
  ],
},
```

Share the folder and each video as **Anyone with the link — Viewer**. Enable the Google Drive API in Google Cloud, and restrict the browser key to the website's HTTP referrer and the Google Drive API. Remember that a browser API key is visible in a static website's source.

## Video size

For local files, keep videos compressed for faster page loading. GitHub rejects individual files larger than 100 MB, and smaller web videos generally provide a better mobile experience. MP4 using H.264 video and AAC audio has the widest browser support.
