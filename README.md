# Sangrahalaya · संग्रहालय

**Live:** https://dtensor.github.io/sangrahalaya/

Two walkable 3D museums that run in any browser (three.js). Both are generated
from live records, not maintained by hand.

## Yantra Sangrahalaya: the museum of apps → [`/yantra/`](https://dtensor.github.io/sangrahalaya/yantra/)

Every app in the estate catalogue gets its own 3D exhibit. The shape of each
exhibit comes from the app's own data:

| On the exhibit | Comes from |
|---|---|
| Coloured ports on the left | what the app takes in (text, image, audio, data…) |
| The core's shape | how it runs: ring = service, crystal + clock = scheduled, books = reference, planet = remote, screen = desktop |
| Cones on the right | what it produces |
| Beads orbiting in the glass case | what it can do |
| The band's colour and a pulse | its health when the museum was built |
| Beams to other exhibits | apps it works with |

The halls sit around a domed rotunda with an oculus. At its centre an orb of
points (one per app, coloured by hall) marks the collection.

| Hall | What's inside |
|---|---|
| Studio of Making | image, video, design, visual tools |
| Hall of Voice | speech, song, transcription, audio |
| Library of Inquiry | knowledge bases, research, learning |
| Watchtower | defence intelligence, markets, signals |
| Engine Room | development tools, reasoning agents |
| Keep | infrastructure, security, plumbing |
| Everyday Arcade | utilities, wellbeing, daily helpers |

A newly registered app appears on the next build. An app from a category with no
hall yet goes to the Annex.

## Sangrahalaya: the museum of made things → [`/prints/`](https://dtensor.github.io/sangrahalaya/prints/)

Four wings of work, each with its status:

* **Built:** finished products, with their seal verdicts.
* **Conceived:** designs taken from idea to dossier.
* **Forged:** 3D parts, some shown as models on pedestals.
* **Qualified:** capabilities that have been registered.

## Getting around

* **Move:** WASD or the arrow keys (Shift to run). Drag to look.
* **Walls:** you slide along them instead of stopping.
* **Glide:** click the floor to glide there, or click an exhibit to walk up to it.
* **Browse:** N/P steps between exhibits, and the hall buttons and minimap teleport you.
* **Find:** search or the catalogue view.
* **Link:** `yantra/#<app-id>` links straight to one exhibit.
* **Phones:** works with the on-screen pad.

## Privacy

This is the **public edition**. It is built with `--web`, which removes local
folder paths, private and tailnet addresses, launch commands and local links
before anything is written. The publisher then scans every file and refuses to
push if it finds anything private. Search engines are asked not to index the
site (`robots.txt` and `noindex`).

The owner's private copy, served on their own machine, keeps full launch access.

## How it's made

Built by `tools/sangrahalaya/` in the owner's workspace:
* `apps_museum.py` and `apps_hall.html` build Yantra.
* `sangrahalaya.py` and `hall.html` build the prints museum.
* `webscrub.py` does the redaction and the leak check.
* `publish_web.py` builds, checks and pushes the site.
