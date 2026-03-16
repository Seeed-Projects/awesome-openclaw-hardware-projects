# reCamera Intellisense

AI-powered monitoring and control skill for reCamera (v2) — manage devices, configure object detection, capture images/video, and stream events, all with the tiny stdlib-only reCamera Python SDK integrated.

## Features

- **Multi-camera management** — register and control multiple reCamera devices from a single host; deploy remotely (PC / Cloud) or locally on the camera (e.g. ZeroClaw).
- **Real-time image & video capture** — on-demand JPG/RAW snapshots and MP4 video recording, independent of the detection pipeline.
- **Intelligent detection monitoring** — configurable AI models, timed schedules, multi-category label filters, region-based rules, and debounce thresholds for precise event triggering.
- **Event correlation & reporting** — the on-device monitor merges rule triggers with captured files in real-time, queryable by time range via HTTP API.
- **Agent-friendly CLI / SDK** — every operation is a single CLI command accepting JSON, or a Python function call, designed for seamless AI-agent integration (Claw, LangChain, etc.).

For detailed API signatures and CLI schemas, see [API Reference](skills/recamera-intellisense/REFERENCE.md).

## Installation

**Note: requires an unreleased reCamera (v2) hardware with an experimental firmware, stay tuned for the public release!**

### Option A — ClawHub (recommended)

If you use the [ClawHub](https://clawhub.ai) agent framework, install the skill directly:

```bash
npx clawhub@latest install recamera-intellisense
```

### Option B — Shell script (macOS or Linux)

```bash
curl -fsSL https://raw.githubusercontent.com/iChizer0/reCamera-Intellisense/main/scripts/install-skill.sh | bash
```

The installer will prompt you to choose an installation directory (current workspace, a detected Claw directory, or a custom path).