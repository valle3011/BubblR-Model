# BubblR Model

Hosts the latest trained **BubblR** object-detection model (YOLO). BubblR Trainer
and BubblR Model Trainer download it directly from here — no manual copying.

## How the apps find it
The newest model is published as a GitHub **release asset** named
`bubblr-model.pt`, so this URL always points at the latest one:

```
https://github.com/valle3011/BubblR-Model/releases/latest/download/bubblr-model.pt
```

Metadata (version, task, class names) lives in [`model.json`](model.json).

## Publishing a new model
After training in BubblR Model Trainer, take the `best.pt` and create a release
whose asset is named `bubblr-model.pt`, e.g.:

```
gh release create v1 "runs/<name>/weights/best.pt#bubblr-model.pt" \
  -R valle3011/BubblR-Model --title "BubblR model v1"
```

Then bump `"version"` in `model.json`. The apps show a "new model available"
note when that version is higher than the one you last downloaded.
