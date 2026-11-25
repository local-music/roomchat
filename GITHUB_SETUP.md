# Putting RoomCode Chat on GitHub

I can't create the GitHub repo or push to it myself (no GitHub account access from here), but
everything needed is in this folder. Here's exactly what to do.

## 1. Create the repo
1. On github.com, click **New repository**. Name it whatever you like (e.g. `roomcode-chat`).
   Public, so Pages can serve it for free.
2. Clone it locally, or just use GitHub's "Upload files" button in the browser.

## 2. Add the files
Copy these into the repo root:
- `index.html` (the landing page)
- `README.txt` → rename to `README.md` if you want it to render nicely on the repo's main page
  (GitHub shows `README.md` automatically; `.txt` won't get the same formatting)
- the extension source, e.g. in a `/extension` folder (the "-source" zip you have is the
  readable version; keep the "-release" zip's contents as what you actually hand out, since
  it's the same thing minified)

## 3. Turn on GitHub Pages
1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment", set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Save. GitHub gives you a URL like `https://YOUR_USERNAME.github.io/roomcode-chat/` within a minute or two.

## 4. Publish the zip as a Release (so the Download button works)
1. In the repo, go to **Releases → Create a new release**.
2. Tag it, e.g. `v11.4`.
3. Drag in the release zip and name the uploaded asset exactly `room-chat-extension.zip`
   (the page's download button points at that exact filename).
4. Publish the release.

## 5. Fix the two placeholders in index.html
Open `index.html` and replace `REPLACE_OWNER` and `REPLACE_REPO` (appears 3 times) with your
actual GitHub username and repo name. Commit and push — Pages rebuilds automatically.

That's it — your landing page is live, and the download button pulls directly from your
latest GitHub Release, so pushing a new release later just means re-doing step 4.
