# reSpeaker-claw

> Voice-first AI agent for reSpeaker XVF3800 and XIAO ESP32S3.

- **Status:** Linked
- **Linked Project:** [Seeed-Projects/reSpeaker-claw](https://github.com/Seeed-Projects/reSpeaker-claw)
- **Hardware:** [reSpeaker XVF3800 USB 4 Mic Array with XIAO ESP32S3](https://wiki.seeedstudio.com/respeaker_xvf3800_xiao_getting_started/)
- **Framework:** ESP-IDF v5.5+
- **Language:** C

## Overview

**reSpeaker-claw** turns a reSpeaker XVF3800 based device into a voice-native OpenClaw-style agent. It captures microphone input over I2S, performs on-device VAD, sends utterances to STT services, runs an embedded agent loop, and plays TTS responses back through an I2S speaker path.
Compared with Linux-centric voice assistant stacks, this project keeps the system small and embedded-friendly: pure C firmware, ESP32-S3 target, USB power, and persistent local storage for memory and automation data.

![reSpeaker-claw Demo](https://github.com/Seeed-Projects/reSpeaker-claw/raw/main/assets/respeaker-claw.png)

Watch the latest demo videos:
- [X / reSpeaker-claw demo](https://x.com/seeedstudio/status/2032358691299869022)
- [LinkedIn / reSpeaker-claw demo](https://www.linkedin.com/feed/update/urn:li:activity:7438123175634173952)

## Highlights

- **Voice pipeline built in** - microphone PCM -> VAD -> STT -> agent loop -> TTS -> speaker playback.
- **Multi-channel interaction** - supports voice plus Telegram, Feishu, and WebSocket channels.
- **Persistent memory** - stores persona, user profile, long-term memory, sessions, and scheduled jobs in SPIFFS.
- **Configurable backends** - works with OpenAI-compatible or Anthropic-compatible LLM endpoints, plus custom STT/TTS services.
- **Runtime configuration** - Wi-Fi, provider, model, proxy, and tokens can be updated from the serial CLI without recompiling for every change.
- **Automation ready** - includes heartbeat tasks, cron-style scheduling, tool calling, and reboot-persistent state.

## Hardware Setup

The reference project targets:

- reSpeaker XVF3800 USB 4 Mic Array with XIAO ESP32S3
- An external speaker, DAC, or amplifier on the I2S output path
- USB for flashing and serial monitoring
- Wi-Fi connectivity for LLM, STT, and TTS services

Before building the firmware, the XVF3800 I2S firmware should be flashed by following the Seeed guide:

- [reSpeaker XVF3800 introduction and firmware guide](https://wiki.seeedstudio.com/respeaker_xvf3800_introduction/#flash-firmware)

## Software and Service Requirements

- ESP-IDF v5.5 or newer
- One LLM API key for an OpenAI-compatible or Anthropic-compatible endpoint
- One STT service and one TTS service for full voice mode
- Optional Telegram bot token or Feishu app credentials for extra channels

## Quick Start

1. Clone the upstream project:

```bash
git clone https://github.com/Seeed-Projects/reSpeaker-claw
cd reSpeaker-claw
idf.py set-target esp32s3
```

2. Copy the secrets template:

```bash
cp "main/mimi_secrets.h.example" "main/mimi_secrets.h"
```

3. Configure Wi-Fi, LLM, STT, TTS, and the XVF3800 I2S pin map in `main/mimi_secrets.h`.

4. Build and flash:

```bash
idf.py fullclean
idf.py build
idf.py -p PORT flash monitor
```

## Why It Matters Here

This project is a strong fit for the **Voice & Audio** section of this list because it shows a practical path to running an always-on voice agent on low-power hardware without a full Linux stack. It also demonstrates how OpenClaw-like interaction can be extended into the physical world with real microphones, speakers, local memory, and hardware-friendly runtime control.

## Useful Links

- [reSpeaker-claw](https://github.com/Seeed-Projects/reSpeaker-claw)
- [ESP-IDF installation guide](https://docs.espressif.com/projects/esp-idf/en/v5.5.3/esp32s3/get-started/)
- [reSpeaker XVF3800 wiki](https://wiki.seeedstudio.com/respeaker_xvf3800_introduction/)
