# CalmCampus research and design archive

[![CI](https://github.com/CalmCampus-FV/CalmCampus/actions/workflows/ci.yml/badge.svg)](https://github.com/CalmCampus-FV/CalmCampus/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

[**cc.braunf.com**](https://cc.braunf.com/)

This repository is the research and design archive of **CalmCampus**, a student project by Florian Braùn and Hélène David: a weekly wellbeing check-in that takes less than a minute and keeps every answer on the phone. It holds the early research work and design material. The product itself now lives in separate repositories (below).

> We are students, not medical professionals. CalmCampus does not diagnose or treat. If you need help, we strongly suggest a doctor or your student support service. If you are in crisis, contact your local emergency number or a crisis line.

## Where things live now

| Repository | What it holds |
|---|---|
| [CalmApp](https://github.com/CalmCampus-FV/CalmApp) | The iOS app |
| [CalmWeb](https://github.com/CalmCampus-FV/CalmWeb) | The website at [cc.braunf.com](https://cc.braunf.com/) and the forms platform |
| [CalmUni](https://github.com/CalmCampus-FV/CalmUni) | University demos and prototypes: the reviewer preview web app (formerly `web/` here, with its history and per-university branches) |
| [CalmBiz](https://github.com/CalmCampus-FV/CalmBiz) | Company demos and prototypes |
| CalmCampus (this repo) | Research and design archive |

`ios/` and `web/` were removed from this repo after they moved to CalmApp and CalmUni. Their full history is still here in git; the old university branches (`epfl-web-demo`, `quivr-web-demo`, `unil-web-demo`) are kept for reference, but new work happens in CalmUni. The earlier Flutter prototype is preserved at git tag [`flutter-final`](https://github.com/CalmCampus-FV/CalmCampus/tree/flutter-final).

## What's in the archive

```
ml/       On-device thought-reframing language model: data, training, evaluation, model card (v0.1 research preview)
spike/    iOS feasibility spike: which phone signals iOS actually provides (XcodeGen project)
design/   HTML mockups of early app screens, app icon and colour palette
```

- **`ml/`**: a research preview, not part of any shipped app. See [`ml/README.md`](ml/README.md) and [`ml/MODEL_CARD.md`](ml/MODEL_CARD.md) for its evaluation and limitations. Weights and data are on [Hugging Face](https://huggingface.co/CalmCampus), not in git. It is not a crisis or safety tool.
- **`spike/`**: a throwaway experiment, see [`spike/README.md`](spike/README.md). It needs macOS with Xcode and [XcodeGen](https://github.com/yonaskolb/XcodeGen).
- **`design/`**: the mockups show early design ideas, not the current app. Open `design/mockups/*.html` in a browser.

## Principles that carried over

- **All data stays on-device.** No cloud storage, analytics or accounts.
- **On-device AI only.** User text is never sent to a cloud API.
- **Wellness wording, not medical claims.** CalmCampus "supports"; it does not detect, diagnose or treat anything.
- **Light-touch check-ins.** A small question budget, every question skippable, no clinical screeners or self-harm items.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) and the [Code of Conduct](CODE_OF_CONDUCT.md). To report a security or privacy problem, see [SECURITY.md](SECURITY.md).

## Team

- **Florian Braùn**: Engineering Technology
- **Hélène David**: Economics and Business

## License

[MIT](LICENSE) © 2026 Florian Braùn, Hélène David. The fine-tuned model in `ml/` is derived from Qwen3-1.7B (Apache-2.0), see its [model card](ml/MODEL_CARD.md).
