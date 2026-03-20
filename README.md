<img width="1000" height="329" alt="awesome-openclaw-hardware-projects" src="https://github.com/user-attachments/assets/c54b5aa8-1fe6-4d56-98c2-b978f77ff558" />

[![awesome](https://cdn.jsdelivr.net/gh/sindresorhus/awesome@main/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![License: CC0](https://img.shields.io/badge/License-CC0-lightgrey?style=flat&style=flat)](LICENSE)

# Awesome OpenClaw Hardware Projects

> A community collection of OpenClaw hardware projects — enabling AI agents to interact with the physical world.

[OpenClaw](https://github.com/openclaw/openclaw) has transformed office automation and content creation, but its connection to the physical world remains underdeveloped. Unlike interacting with internet APIs, hardware integration lacks standardized interfaces and protocols. This field is still in its infancy — but as hardware becomes more accessible and agent-to-physical-world protocols mature, OpenClaw will increasingly power perception and control of the real world.

This repository aggregates projects, skills, and tutorials that bring OpenClaw into the physical realm.

---

## Table of Contents

| | | |
|---|---|---|
| [Single Board Computers](#single-board-computers) | [Microcontrollers](#microcontrollers) | [Local LLM](#local-llm) | [Voice \& Audio](#voice--audio) |
| [Vision \& Cameras](#vision--cameras) | [Home Automation \& IoT](#home-automation--iot) | [Robotics](#robotics) |
| [Displays \& HMI](#displays--hmi) | [Wireless Communication](#wireless-communication) | |

---

<details open>
<summary><h3 style="display:inline">Single Board Computers</h3></summary>

Running OpenClaw natively on single-board computers.

| Project Name | Related Hardware | Description |
|---|---|---|
| [nanobot](https://github.com/HKUDS/nanobot) | — | Ultra-lightweight personal AI assistant inspired by OpenClaw. |
| [Seeed's SBC Benchmark for OpenClaw](01-single-board-computers/seeed-sbc-benchmark-en.md) | • [reComputer R Series](https://wiki.seeedstudio.com/recomputer_r/)<br>• [reComputer J Series](https://wiki.seeedstudio.com/reComputer_Jetson_Series_Introduction/) | A comprehensive benchmark of Seeed's single-board computers running OpenClaw, including performance metrics and hardware recommendations. |

</details>

<details open>
<summary><h3 style="display:inline">Microcontrollers</h3></summary>

Lightweight embedded implementations for MCU platforms, and hardware boards proved to run OpenClaw or agent-like workloads.

| Project Name | Related Hardware | Description |
|---|---|---|
| [mimiclaw](https://github.com/memovai/mimiclaw) | • [XIAO ESP32S3](https://wiki.seeedstudio.com/xiao_esp32s3_getting_started/) | Pocket AI Assistant on a $5 Chip. |
| [espclaw](02-microcontrollers/espclaw.md) | • [XIAO ESP32C3](https://wiki.seeedstudio.com/XIAO_ESP32C3_Getting_Started/)<br>• [XIAO ESP32S3](https://wiki.seeedstudio.com/xiao_esp32s3_getting_started/) | ESP32-based OpenClaw implementation with MQTT channel and more native tools. |
| [mimiclaw on XIAO ESP32-S3](https://github.com/luoluoter/mimiclaw) | • [XIAO ESP32S3](https://wiki.seeedstudio.com/xiao_esp32s3_getting_started/) | mimiclaw ported to Seeed Studio XIAO ESP32S3. |

</details>

<details open>
<summary><h3 style="display:inline">Local LLM</h3></summary>

OpenClaw driven by local LLM backends on edge devices.

| Project Name | Related Hardware | Description |
|---|---|---|
| [nanobot + reComputer RK + Local LLM](03-local-llm/nanobot-recomputer-rk-local-llm.md) | • [reComputer RK Series](https://wiki.seeedstudio.com/object_detection_with_yolov11_on_recomputer_rk/) | A complete guide to installing and using the USB Relay Control and Light Sensor Reader skills with Nanobot on reComputer RK (featuring the RK1826 accelerator) alongside a local LLM. |

</details>

<details open>
<summary><h3 style="display:inline">Voice & Audio</h3></summary>

Add voice input/output capabilities to OpenClaw agents.

| Project Name | Related Hardware | Description |
|---|---|---|
| [reSpeaker-claw](04-voice-audio/respeaker-claw.md) | • [reSpeaker XVF3800](https://wiki.seeedstudio.com/respeaker_xvf3800_introduction/)<br>• [XIAO ESP32S3](https://wiki.seeedstudio.com/xiao_esp32s3_getting_started/) | Voice-first AI agent on ESP32-S3 with local VAD, pluggable STT/TTS,multi-channel messaging, and persistent memory. |
| [reSpeaker + OpenClaw Lark Meeting Card Push](04-voice-audio/respeaker-openclaw-lark-card-push.md) | • [reSpeaker XVF3800](https://wiki.seeedstudio.com/respeaker_xvf3800_introduction/) | Voice-input and skill-development tutorial for sending smart location and interactive meeting cards to Lark/Feishu groups with OpenClaw. |
| [openclaw with SenseCAP Watcher](https://github.com/luoluoter/watcher-OI) | • [SenseCAP Watcher](https://wiki.seeedstudio.com/getting_started_with_watcher/) | Give OpenClaw Ears and a Voice |

</details>

<details open>
<summary><h3 style="display:inline">Vision & Cameras</h3></summary>

Computer vision, AI cameras, and visual perception systems.

| Project Name | Related Hardware | Description |
|---|---|---|
| [reCamera Intellisense](05-vision-cameras/recamera-intellisense.md) | • [reCamera (v2, pending relaese)](https://wiki.seeedstudio.com) | A skill for multi-camera capable intelligent object detection, media capturing, GPIO controls. |
| [openclaw with reCamera Gimbal](https://github.com/Seeed-Projects/reCamera_Gimbal-OpenClaw/blob/main/README.md) | • [reCamera Gimbal](https://wiki.seeedstudio.com/recamera_gimbal_getting_started/) | Use OpenClaw to control the motor, speaker, microphone, LED, and camera of the reCamera Gimbal. |
| [reCamera v2 fleet management with OpenClaw](05-vision-cameras/control-recamera-v2.md) | • [reCamera (v2, pending relaese)](https://wiki.seeedstudio.com) | OpenClaw skill to manage a fleet of reCamera v2 devices, including discovery, configuration and control. |

</details>

<details open>
<summary><h3 style="display:inline">Home Automation & IoT</h3></summary>

OpenClaw interact with smart home protocols, and IoT devices.

| Project Name | Related Hardware | Description |
|---|---|---|
| [nanobot + reComputer RK + IoT](06-home-automation-iot/nanobot-recomputer-rk-iot.md) | • [reComputer RK Series](https://wiki.seeedstudio.com/object_detection_with_yolov11_on_recomputer_rk/) | A complete guide to installing and using the USB Relay Control and Light Sensor Reader skills with Nanobot on reComputer RK (featuring the RK1826 accelerator) alongside a local LLM. |

</details>

<details open>
<summary><h3 style="display:inline">Robotics</h3></summary>

Motor control, robot arms, and physical agent systems.

| Project Name | Related Hardware | Description |
|---|---|---|
| [Control SOArm 101 with OpenClaw](07-robotics/control-soarm101.md) | • [SO-ARM101](https://wiki.seeedstudio.com/lerobot_so100m_new/)<br>• [reComputer J Series (Jetson)](https://wiki.seeedstudio.com/reComputer_Jetson_Series_Introduction/) | OpenClaw controlling SOArm 101 robotic arm with Nvidia Jetson. |
| [Reachy Mini](07-robotics/reachy-mini.md) | • [Reachy Mini](https://huggingface.co/reachy-mini) | A fully local desktop AI robot with sub-second voice interaction, emotional motion, face tracking, and OpenClaw-powered workflows. |

</details>

<details open>
<summary><h3 style="display:inline">Displays & HMI</h3></summary>

E-ink screens, LCD displays, and HMI devices.

| Project Name | Related Hardware | Description |
|---|---|---|
| [OpenClaw with e-ink Displays](08-displays-hmi/openclaw-eink-displays.md) | • [reTerminal E series](https://wiki.seeedstudio.com/reterminal_e10xx_main_page/)<br>• [ePaper Driver Boards](https://wiki.seeedstudio.com/xiao_epaper_display_board_overview/) | Give e-ink displays the most powerful content generation engine - OpenClaw. |

</details>

<details open>
<summary><h3 style="display:inline">Wireless Communication</h3></summary>

OpenClaw communication with the physical world through wireless protocols.

| Project Name | Related Hardware | Description |
|---|---|---|
| [MeshClaw](https://github.com/Seeed-Solution/MeshClaw) | • [SenseCAP Card Tracker T1000](https://wiki.seeedstudio.com/SenseCAP_T1000_tracker/Introduction/) | Meshtastic integration for off-grid AI communication. |

</details>

---

## Contributing

Contributions welcome! Please read our [contributing guidelines](./CONTRIBUTING.md) before submitting PRs.

- Add only projects you've verified work
- Include clear descriptions
- Categorize appropriately
- Link to official docs/github repository when available, if you need a landing page aggregating skills/videos/docs for your project, you can create a markdown file in the relevant category and link to it from the README.

---

## Related Awesome Lists

- [awesome-openclaw](https://github.com/rohitg00/awesome-openclaw) — Main OpenClaw resource list
- [awesome-openclaw-usecases](https://github.com/hesamsheikh/awesome-openclaw-usecases) — Real-world use cases
- [awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) — 5,400+ community skills

---

## Star History

[![Star History Chart](https://api.star-history.com/image?repos=seeed-projects/awesome-openclaw-hardware-projects&type=date&legend=top-left)](https://www.star-history.com/?repos=seeed-projects%2Fawesome-openclaw-hardware-projects&type=date&legend=top-left)

---

## License

[![License: CC0](https://img.shields.io/badge/License-CC0-lightgrey?style=flat&style=flat)](LICENSE)

To the extent possible under law, contributors have waived all copyright and related rights to this work.
