# Boundary — Mining Header Animations

Six standalone header-animation builds for client review. Each page is self-contained (illustration linework inlined); background videos are served from `/assets`.

## Pages (paired by name)

| Version    | Wide                      | Vertical (mobile)             |
|------------|---------------------------|-------------------------------|
| Blue Wave  | `blue-wave-wide.html`     | `blue-wave-vertical.html`     |
| Pattern    | `pattern-wide.html`       | `pattern-vertical.html`       |
| Cinematic  | `cinematic-wide.html`     | `cinematic-vertical.html`     |

With `vercel.json` (`cleanUrls`), each is reachable without the `.html`, e.g.
`https://<project>.vercel.app/blue-wave-wide`.

## Deploy (Vercel + this repo)

1. Push this folder to the repo (see below).
2. On [vercel.com/new](https://vercel.com/new) → **Import Git Repository** → select this repo → **Deploy**.
3. Every future `git push` auto-redeploys.

## Pushing the files

From the unzipped folder on your machine:

```
git init
git add .
git commit -m "Initial header animation builds"
git branch -M main
git remote add origin https://github.com/almostdougal/boundary_mining_animations.git
git push -u origin main
```

(Or drag the files into the repo via GitHub's web "Add file → Upload files".)

## Notes

- Background videos autoplay muted + looped at 0.4× speed.
- Keep `/assets` next to the HTML files — pages reference `assets/<video>.mp4` by relative path.
- The animation: a scan bar sweeps across (wide: left→right, vertical: top→bottom) revealing each illustration at full opacity through a feathered band while the previous one wipes away, over a 25% floor layer. Cycles through all five illustrations and loops.
