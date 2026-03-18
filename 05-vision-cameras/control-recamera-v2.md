# reCamera Web API Skill

[English](control-recamera-v2.md) | [中文](control-recamera-v2-zh.md)

This project is a Skill for reCamera V2 (RV1126B) devices. It helps agents correctly use the device's HTTP/WebSocket APIs and the related [SenseCraft AI](https://sensecraft.seeed.cc/) cloud APIs during development, integration, and troubleshooting.

Its focus is not just listing endpoints, but packaging real executable workflows together, such as logging in to obtain a token, using the read-before-write pattern for configuration APIs, discovering devices on a local network, accessing recording storage via relay, and handling model inference and cloud conversion flows.


- GitHub：<https://github.com/mjq2020/reCamera_skill>
- YouTube：<https://www.youtube.com/watch?v=eh7HKjYU2SI>
- ClawHub：<https://clawhub.ai/mjq2020/recamera>


## Core Capabilities

- Authentication flow: call `/system/key` first, then log in and capture the `token` from `Set-Cookie`
- Authorized request requirements: all subsequent requests must reuse `Cookie: token=<jwt>`
- Configuration update pattern: for APIs that support GET/POST or GET/PUT, follow the "read before write" approach
- Device discovery workflow: identify whether a device on the local network is a reCamera through `/cgi-bin/entry.cgi/system/key`
- Image tuning workflow: enter scene edit mode, modify parameters, and send the save command
- Storage relay workflow: create a relay, list directories, download files, and handle timeouts
- AI capabilities: model upload, inference configuration, notification output, and SenseCraft cloud model conversion



## File Overview
- `SKILL.md`: the main Skill entry file, defining trigger conditions, workflows, and key constraints
- `API_REFERENCE.md`: a more complete API reference, organized by module
- `scripts/discover_recamera.py`: a LAN scanning script used to discover reCamera devices within the subnet

## Quick Start

- You can install the Skill already published to `clawhub` using the following method:

```bash
# Install the clawhub CLI, skip if already installed
npm i -g clawhub
# Or
pnpm add -g clawhub

# Install the Skill via CLI
clawhub install recamera

# Update the Skill
clawhub install recamera
```

## References

- [Agent Skills Specification](https://agentskills.io/home)
- [OpenClaw Documentation](https://docs.openclaw.ai/)
