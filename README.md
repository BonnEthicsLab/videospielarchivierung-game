# World of Videospielarchivierungsethik

A browser-playable Godot game, published using GitHub Pages. [Click Here](https://bonnethicslab.github.io/videospielarchivierung-game/)

## Live game

Once GitHub Pages is enabled, open:

`https://YOUR-ORGANIZATION.github.io/YOUR-REPOSITORY/`

## Deploy

This repository contains a **ready-to-run Godot Web export**, not the editable Godot source project.

1. Create a **public** repository in your GitHub organization.
2. Clone the repository onto your computer and copy every file in this folder into the repository root, including the hidden `.nojekyll` file.
3. Commit and push your files using Git. The `index.wasm` file exceeds GitHub's 25 MiB *browser* upload limit, so do **not** upload through GitHub's web interface.
4. In the repository: **Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save**.
5. Visit the published `github.io` URL shown on the Pages settings page.

To update the game, replace all exported Godot Web files with a fresh *single-threaded* Web export, retaining `index.html` and matching asset names. Commit and push again. (The `.nojekyll` and this README may remain.)

## Browser requirements

Requires JavaScript, WebAssembly, and WebGL 2.0. GitHub Pages serves the exported static assets and does not require a backend. Large `.wasm` downloads may increase first-load time.

## Important

The game export uses `GODOT_THREADS_ENABLED = false`, avoiding the cross-origin isolation requirement of threaded Godot 4 Web exports. This is a compiled/distributed version; obtain the `.godot` project separately for editing the game.
