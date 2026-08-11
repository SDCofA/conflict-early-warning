# Conflict Early Warning System

[![Pages](https://github.com/SDCofA/conflict-early-warning/actions/workflows/pipeline.yml/badge.svg)](https://github.com/SDCofA/conflict-early-warning/actions/workflows/pipeline.yml)

Open-source indicators for monitoring changes in conflict risk.

**Live dashboard:** https://sdcofa.github.io/conflict-early-warning/

## Run locally

```bash
python -m pip install -r requirements.txt
python pipeline/conflict_early_warning_pipeline.py
python -m http.server 8000
```

Open `http://localhost:8000`. Direct `file://` access cannot fetch `data/output.json` in modern browsers.

## Automation

GitHub Actions refreshes public data every six hours and deploys the static dashboard to GitHub Pages. AI briefs are optional: configure `OPENROUTER_API_KEY` as a repository Actions secret. Without it, core collection and dashboard deployment remain available.

## Data notice

Source availability varies. The dashboard identifies its generation time and operating mode in `data/output.json`. Treat indicators as decision-support signals, not verified ground truth.

## Brand

Published by SDCofA, the endorsed analytical unit of Monarch Castle Technologies. See [BRAND.md](BRAND.md) for approved asset use.
