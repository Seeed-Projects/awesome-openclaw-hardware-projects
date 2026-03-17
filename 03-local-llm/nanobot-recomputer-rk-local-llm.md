# nanobot + reComputer RK + Local LLM

A complete guide to installing and using the USB Relay Control and Light Sensor Reader skills with Nanobot on reComputer RK (featuring the RK1826 accelerator) alongside a local LLM.

---

## Prerequisites

### Hardware Requirements

| Device | RAM |
|--------|-------------|
| reComputer RK | 8GB |
| RK1826 | \ |

| Device | Port | Description |
|--------|------|-------------|
| USB Relay | `/dev/ttyUSB1` | 1-channel or multi-channel relay module |
| USB Light Sensor | `/dev/ttyUSB0` | BH1750 or similar lux sensor |


### System Requirements

- **OS:** Linux (Ubuntu, Debian, Fedora, etc.)
- **Python:** 3.10 or higher
- **Permissions:** User must be in `dialout` group for serial port access

>Note:Before getting started, please make sure you can run the Qwen model on the RK1820. Please refer to the [link](https://github.com/airockchip/rknn3-model-zoo)

---

## Install nanobot

### Step 1: Install uv

```bash
# Install uv
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Step 2: Install nanobot

```bash
# Install nanobot
uv tool install nanobot-ai
```

### Step 3: Configure nanobot

Use command below to open nanobot `config.json`
```bash
nano ~/.nanobot/config.json
```
Then change the `agents` and `vllm` config like below:

```json
    "defaults": {
      "workspace": "/home/~/.nanobot/workspace",
      "model": "rkllm/Qwen3",
      "provider": "vllm",
      "maxTokens": 8192,
      "temperature": 0.1,
      "maxToolIterations": 40,
      "memoryWindow": 100,
      "reasoningEffort": null
    }
    "vllm": {
        "apiKey": "nano",
        "apiBase": "http://127.0.0.1:8080/v1",
        "extraHeaders": null
    },
```

>Note: You can add your channel refer this [link](https://github.com/HKUDS/nanobot/blob/main/docs/CHANNEL_PLUGIN_GUIDE.md).

## Use nanobot

### Start nanobot

Use command below to start nanobot:

```bash
nanobot gateway
nanobot agent
```

### Install clawhub

You can use the following content in the chat box to instal clawhub:
```
Please install clawhub use command：npm install -g clawhub
```

### Install skill with clawhub

You can use the following content in the chat box to install skills:
```
Please install control-usb-relay use command: npx clawhub install Control-Usb-Relay
Please install usb-light-sensor-reader use command: npx clawhub install Usb-Light-Sensor-Reader
```

## Use Skills
### Prompting AI Agents

When working with AI agents, use clear prompts that reference the skills:

#### Example Prompts

**For Relay Control:**
```
Use the control-usb-relay skill to turn on the connected device.
```

**For Sensor Reading:**
```
Read the current light level using the usb-light-sensor-reader skill.
```

**For Automation:**
```
Create an automation that turns on the relay when the light sensor detects 
darkness (below 100 lux) and turns it off when it's bright (above 500 lux).
```

---


---

## Additional Resources

- [ClawHub Documentation](https://clawhub.ai/docs)
- [OpenCLAW GitHub](https://github.com/openclaw/openclaw)
- [pyserial Documentation](https://pyserial.readthedocs.io/)

---