# BubblR Model

Hosts the latest trained **BubblR** object-detection model (YOLO). BubblR Trainer
and BubblR Model Trainer download it directly from here — no manual copying.

## How the apps find it
The newest model is published as a GitHub **release asset** named
`bubblr-model.pt`, so this URL always points at the latest one:

```
https://github.com/valle3011/BubblR-Model/releases/latest/download/bubblr-model.pt
```

Metadata (version, task, class names, score) lives in
[`model.json`](model.json). Models here are published only by the maintainer.
