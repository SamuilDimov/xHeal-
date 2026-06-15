# xHeal

A personalized daily health routine app. Single-file, dependency-free front end: onboarding
(welcome → goals → conditions → intensity → tone) flows into a daily routine screen with tasks,
a progress mascot, task detail/logging, completion overlays, and more.

The entire app lives in `index.html` (inline CSS + JS). External runtime dependencies are loaded
from CDNs (Lucide icons, Manrope font); the only local assets are the PWA manifest, icons, and
mascot images.

## Run locally

No build step. Serve the folder with any static server:

```bash
python3 -m http.server 8765
```

Then open <http://localhost:8765/index.html>.

## Project structure

```
index.html        # the whole app (CSS + JS inline)
manifest.json     # PWA manifest
icon-192.png      # app icon
icon-512.png      # app icon
mascots/          # mood-based mascot images
```

## Mascot images

The `mascots/*.png` files are currently **placeholders** (simple colored faces) so nothing
appears broken. Replace them with the real artwork using these exact filenames:

```
curious.png   encouraging.png   resting.png   happy.png   proud.png   default.png
Anxious.png   Frustrated.png    Overwhelmed.png   Uneasy.png   tujen.png
```

Note: `gentle` reuses `Anxious.png`. Filenames are case-sensitive — keep the capitalized ones
exactly as shown. No code changes are needed; the new files just overwrite the placeholders.
