# OpenClaw with e-ink Displays

> Give e-ink displays the most powerful content generation engine - OpenClaw.


## 1. Overview
While SenseCraft HMI provides numerous templates, they often lack the flexibility required for dynamic content—such as live data charts, daily story updates, or frequently changing image galleries.

The HMI HTML control allows for custom Javascript to fetch data, but the underlying layout remains static. By using OpenClaw, you can generate full web pages (static or dynamic) on demand. By mapping OpenClaw’s local server to a public URL using a reverse proxy (FRP), your e-paper screen effectively becomes a "monitor" for OpenClaw's AI-generated content.

## 2. The Skill: SenseCraft HMI Web Content Generator
This skill is available via ClawHub.

[The link of the Skill](https://clawhub.ai/KillingJacky/sensecraft-hmi-gen)

Security Note: Due to safety constraints, the skill does not include the reverse proxy tool. Users must install and configure it manually. A detailed Wiki guide will be released soon.

Future Consideration: Native support for reverse proxying within the HMI platform would significantly streamline this workflow.

The source of the skill is available [in this github repo](https://github.com/Seeed-Projects/SenseCraft-HMI-Gen) , feel free to make it better.

## 3. Usage Instructions

### Step 1: Install the Skill & Generate a Page
Enter the following prompt into the OpenClaw chat interface:

Prompt:
```
"Use the SenseCraft HMI Gen skill to help me generate a webpage featuring 'Classic Stories of Open Source Software.'
Requirements:

1.Story text should not exceed 200 words; use a large font size.

2.Change the story every time the page is refreshed.

3.Generate 24 different stories daily to ensure variety upon refresh."
```

Configure the settings in the pop-up window. 
<img width="2502" height="1451" alt="image" src="https://github.com/user-attachments/assets/9edf3084-ec91-4cdc-8352-6b8c1bdcc9b7" />
<img width="2488" height="1637" alt="image" src="https://github.com/user-attachments/assets/e5d9d777-0f61-4d7f-ae62-d1396ee0bbc8" />


Direct OpenClaw to finalize the page, then preview and iterate on the design until it meets your requirements.

**Example 1 - Tech Daily**

<img width="800" alt="image" src="https://github.com/user-attachments/assets/93b75357-54b0-4871-8abf-8c41c0da6d80" />

**Example 2 - OSS Stories**

<img width="800" alt="image" src="https://github.com/user-attachments/assets/711101b9-2594-4e69-9483-c325ad739d00" />
<img width="800" alt="image" src="https://github.com/user-attachments/assets/1fa054a0-b3fe-4ab3-aef1-9355e80faf75" />


**Real Device Demo**

<img width="800" alt="image" src="https://github.com/user-attachments/assets/6168669f-5cd2-4b30-9c9a-23904e48ddc1" />


### Step 2: Set Up the Reverse Proxy
If you are unfamiliar with reverse proxying, follow these steps for a basic deployment (Note: The token is your primary security measure).

In the OpenClaw chat, enter:
```
"Please help me install the frp client. Use brew if available; otherwise, download the executable for my system from frp releases. Configure it as follows (choosing a random remote port between 10001–50000):"

Configuration:

Ini, TOML
[common]
server_addr = frp.freefrp.net
server_port = 7000
auth.method = "token"
token = "freefrp.net"

[[proxies]]
name = "sensecraft-hmi-gen"
type = "tcp"
localIP = "localhost"
localPort = 19527
remotePort = <random_remote_port>
Start frpc to test the connection. If the remote port is occupied, try another random port until the connection is successful. Verify by accessing: http://frp.freefrp.net:<remote_port>/?token=<your_token>.
```
Note: You can also ask OpenClaw to set up the client as a background process using PM2.

### Step 3: Deploy to SenseCraft HMI

Open the SenseCraft HMI platform.

Add an HTML Control and resize it to fill the entire screen.

In the URL input field, enter your FRP public URL:
http://frp.freefrp.net:xxxxx/?token=yyyyyyyy

Deploy the configuration to your device.

### 4. Security Considerations
For users with IT experience, using the HTTP mode for FRP is recommended. This adds a layer of security beyond the token but requires a personal domain and DNS configuration. Refer to the FRP Documentation for more details.

### 5. Next Steps
Now that the basic pipeline is functional, you can train your OpenClaw for more complex tasks:

Visual Content: Integrate Text-to-Image skills (e.g., Nano Banana Pro) to generate pages with custom AI-generated artwork.

Live Data: Configure APIs to fetch real-time data and render dynamic charts and graphs.
