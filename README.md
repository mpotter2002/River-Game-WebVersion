# Chicago River Clean Up — Web Version

Browser (WebGL) build of the River Game capstone project.
Live site: https://mpotter2002.github.io/River-Game-WebVersion/

This folder is both the Unity build output and the git repo for the site —
there is no separate copy anywhere else.

## Files

- `index.html` — self-contained player page (loading screen, pause, fullscreen)
- `Build/` — Unity WebGL output (`Web.loader.js`, `Web.framework.js`, `Web.wasm`, `Web.data`)
- `StreamingAssets/river-film.mp4` — intro film streamed by the game
- `icons.js`, `LUCIDE-LICENSE` — toolbar icons and their license
- `.nojekyll` — keeps GitHub Pages from processing the Unity files

## Run locally

Serve this folder over HTTP (Unity WebGL builds do not run from `file://`):

```sh
npx serve .
```

Then open the printed local address.

## Updating the live site

1. In the Unity Editor (project: `River Game Web Version Copy`, Unity
   6000.0.66f2), choose **River Game → Build Browser Version**.
   The build replaces this folder's game files; the git repo files are
   stashed and restored automatically by the build script.
2. From this folder, publish the update:

```sh
git add -A
git commit -m "Update web build"
git push
```

GitHub Pages redeploys automatically a minute or two after the push.
