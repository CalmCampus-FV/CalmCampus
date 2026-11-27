# CalmCampus research and design archive

This repo is the archive: `ml/` (on-device reframing model research), `spike/` (iOS feasibility spike) and `design/` (early mockups, app icon, palette). Product work does not happen here:

- iOS app: [CalmCampus-FV/CalmApp](https://github.com/CalmCampus-FV/CalmApp)
- Website (cc.braunf.com) and forms: [CalmCampus-FV/CalmWeb](https://github.com/CalmCampus-FV/CalmWeb)
- University demos and the reviewer preview web app (formerly `web/` here): [CalmCampus-FV/CalmUni](https://github.com/CalmCampus-FV/CalmUni)
- Company demos: [CalmCampus-FV/CalmBiz](https://github.com/CalmCampus-FV/CalmBiz)

`ios/` and `web/` were removed after the moves; their history stays in git. The branches `epfl-web-demo`, `quivr-web-demo` and `unil-web-demo` here are frozen references: change those demos in CalmUni.

## Layout

- `ml/` - fine-tuned on-device reframing model (data, MLX training, eval, `MODEL_CARD.md`). See `ml/README.md`. Weights live on Hugging Face ([CalmCampus](https://huggingface.co/CalmCampus)), not in git; `ml/publish_hf.py` publishes them. Sending user text to any inference API (including Hugging Face's) is not allowed.
- `spike/` - throwaway iOS feasibility spike (what sensor data iOS actually gives). See `spike/README.md`. `.xcodeproj` files are generated from `project.yml` (XcodeGen) and gitignored.
- `design/mockups/` - HTML mockups of early app screens; `design/brand/` - app icon, palette.

## Commands

```bash
python3 -m py_compile ml/*.py ml/data/*.py     # what CI checks
cd spike && xcodegen generate && open -a Xcode CalmCampusSpike.xcodeproj
python3 -m http.server 3399 --directory design/mockups
```

CI (`.github/workflows/ci.yml`) compiles the Python in `ml/` and checks the README wording. `.github/workflows/claude.yml` is the Claude Code action (write access, triggered by `@claude`).

## Wording rules (all CalmCampus copy)

- Never claim pilots, results, partnerships or detection. No "early signs", no "stop burnout", no claim that CalmCampus finds burnout or gets students to seek help. Wellness wording only ("supports").
- Full disclaimer: we are students, not medical professionals; CalmCampus does not diagnose or treat; we strongly suggest a doctor or student support.
- The check-in takes less than a minute. Data stays on the phone.
- No em dashes in user-facing copy. Names: Florian Braùn (with the ù) and Hélène David.
