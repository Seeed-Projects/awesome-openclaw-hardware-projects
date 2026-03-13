
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

- [nanobot](https://github.com/HKUDS/nanobot) - ultra-lightweight personal AI assistant inspired by OpenClaw.
- [Seeed's SBC Benchmark for OpenClaw](01-single-board-computers/seeed-sbc-benchmark-en.md) - A comprehensive benchmark of Seeed's single-board computers running OpenClaw, including performance metrics and hardware recommendations.

</details>

<details open>
<summary><h3 style="display:inline">Microcontrollers</h3></summary>

Lightweight embedded implementations for MCU platforms, and hardware boards proved to run OpenClaw or agent-like workloads.

- [mimiclaw](https://github.com/memovai/mimiclaw) - Pocket AI Assistant on a $5 Chip.
- [espclaw](02-microcontrollers/espclaw.md) - ESP32-based OpenClaw implementation with MQTT channel and more native tools. @wangtianrui
- [mimiclaw on XIAO ESP32-S3](02-microcontrollers/mimiclaw-on-xiao-esp32s3.md) - mimiclaw ported to Seeed Studio XIAO ESP32S3.
</details>

<details open>
<summary><h3 style="display:inline">Local LLM</h3></summary>

OpenClaw driven by local LLM backends on edge devices.

- [nanobot + reComputer RK + Local LLM](03-local-llm/nanobot-recomputer-rk-local-llm.md) - todo. @jiahao


</details>

<details open>
<summary><h3 style="display:inline">Voice & Audio</h3></summary>

Add voice input/output capabilities to OpenClaw agents.

- [MimiClaw x reSpeaker](04-voice-audio/mimiclaw-x-respeaker.md) - Voice-enabled AI assistant with reSpeaker (XVF3800) + ESP32S3.
</details>

<details open>
<summary><h3 style="display:inline">Vision & Cameras</h3></summary>

Computer vision, AI cameras, and visual perception systems.

- [reCamera Intellisense](05-vision-cameras/recamera-intellisense.md) - Agent-friendly CLI/SDK for reCamera v2 with multi-camera support.
- [openclaw with reCamera Gimbal](05-vision-cameras/openclaw-recamera-gimbal.md) - todo. @wuxinrui
- [openclaw with SenseCap Watcher](05-vision-cameras/openclaw-sensecap-watcher.md) - todo. @jerry
- [Control reCamera v2 with OpenClaw](05-vision-cameras/control-recamera-v2.md) - todo. @daqing
</details>

<details open>
<summary><h3 style="display:inline">Home Automation & IoT</h3></summary>

OpenClaw interact with smart home protocols, and IoT devices.

- [nanobot + reComputer RK + Local LLM](06-home-automation-iot/nanobot-recomputer-rk-iot.md) - todo @jiahao

</details>

<details open>
<summary><h3 style="display:inline">Robotics</h3></summary>

Motor control, robot arms, and physical agent systems.

- [Control SOArm 101 with OpenClaw](07-robotics/control-soarm101.md) - OpenClaw controlling SOArm 101 robotic arm with Nvidia Jetson.
- [Reachy Mini](07-robotics/reachy-mini.md) - todo. @suhe

</details>

<details open>
<summary><h3 style="display:inline">Displays & HMI</h3></summary>

E-ink screens, LCD displays, and HMI devices.

- [OpenClaw with e-ink Displays](08-displays-hmi/openclaw-eink-displays.md) - Give e-ink displays the most powerful content generation engine - OpenClaw.

</details>

<details open>
<summary><h3 style="display:inline">Wireless Communication</h3></summary>

OpenClaw communication with the physical world through wireless protocols.

- [MeshClaw](09-wireless-communication/meshclaw.md) - Meshtastic integration for off-grid AI communication.

</details>

---

## Contributing

Contributions welcome! Please read our [contributing guidelines](./CONTRIBUTING.md) before submitting PRs.

- Add only projects you've verified work
- Include clear descriptions
- Categorize appropriately
- Link to official docs/github repository when available

---

## Related Awesome Lists

- [awesome-openclaw](https://github.com/rohitg00/awesome-openclaw) — Main OpenClaw resource list
- [awesome-openclaw-usecases](https://github.com/hesamsheikh/awesome-openclaw-usecases) — Real-world use cases
- [awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) — 5,400+ community skills

---

## Stargazers

[![Stargazers over time](https://starcharts.vercel.app/seeed-projects.svg)](https://github.com/seeed-projects/awesome-openclaw-hardware-projects/stargazers)

---

## License

[![License: CC0](https://img.shields.io/badge/License-CC0-lightgrey?style=flat&style=flat)](LICENSE)

To the extent possible under law, contributors have waived all copyright and related rights to this work.
