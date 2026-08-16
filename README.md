# Do Robots Need All Tactile Signals?

Project page for **"Do Robots Need All Tactile Signals? Evaluating Tactile Field
Selection in Contact-rich Imitation Learning"** — Tao Liu, Ningquan Gu and
Mitsuhiro Hayashibe, Neuro-Robotics Laboratory, Department of Robotics, Tohoku
University.

**→ https://theotaoliu.github.io/act-tactile-page/**

The page carries the abstract, the approach and task figures, the full
per-configuration results for both real-robot tasks, and two deployment videos:

| Video | Task | Tactile field the policy consumes |
|---|---|---|
| `assets/video/task_t1.mp4` | Task 1 — hidden-property pick-and-place, three episodes (cubes A, B, C) | `force_norm`, left-arm sensors, overlaid top-right in real time |
| `assets/video/task_t2.mp4` | Task 2 — pressure-regulated wiping, five episodes (one per board height) | `marker2d`, right-arm sensor, overlaid top-right in real time |

`assets/pdf/` holds the paper, the poster and the two-page preprint.

## Layout

Plain static site — no build step, no dependencies. `index.html` inlines all of
its CSS; edit it and reload. `.github/workflows/pages.yml` publishes the
repository root to GitHub Pages on every push to `main`.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Serve it over HTTP rather than opening `index.html` directly — browsers block
video loading over `file://`.

## Source

This repository holds only the published page. It is generated from
`paper/website/` in the (private) research repository; figures are exported from
the paper's LaTeX sources and the videos are H.264 transcodes of the original
recordings.

Code, dataset manifests, checksums and the episode split are available on
request: <liu.tao.p1@dc.tohoku.ac.jp>.

Page content is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
