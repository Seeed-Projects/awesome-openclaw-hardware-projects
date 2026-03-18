# reCamera Web API Skill

[English](control-recamera-v2.md) | [中文](control-recamera-v2-zh.md)

本项目是一个面向 reCamera V2（RV1126B）设备的 Skill，用于帮助 Agent 在开发、联调和排障时，正确调用设备的 HTTP/WebSocket API，以及相关的 [SenseCraft AI](https://sensecraft.seeed.cc/) 云端接口。

它的重点不是简单罗列接口，而是把实际可执行的工作流一起封装进去，比如登录拿 token、配置类接口的读后写、局域网设备发现、录像存储 relay 访问，以及模型推理和云端转换流程。

- GitHub：<https://github.com/mjq2020/reCamera_skill>
- YouTube：<https://www.youtube.com/watch?v=eh7HKjYU2SI>
- ClawHub：<https://clawhub.ai/mjq2020/recamera>

## 核心能力

- 认证登录流程：先调用 `/system/key`，再登录并捕获 `Set-Cookie` 中的 `token`
- 鉴权请求约束：后续请求必须复用 `Cookie: token=<jwt>`
- 配置更新模式：对支持 GET/POST 或 GET/PUT 的接口，遵循“先读后写”
- 设备发现流程：通过 `/cgi-bin/entry.cgi/system/key` 判断局域网内设备是否为 reCamera
- 图像调优流程：进入 scene 编辑态后修改参数，并发送保存命令
- 存储 relay 工作流：创建 relay、列目录、下载文件、处理超时
- AI 能力：模型上传、推理配置、通知输出、SenseCraft 云端模型转换

## 文件说明

- `SKILL.md`：Skill 主入口，定义触发条件、工作流和关键约束
- `API_REFERENCE.md`：更完整的接口参考文档，按模块拆分阅读
- `scripts/discover_recamera.py`：局域网扫描脚本，用于发现子网内的 reCamera 设备

## 快速开始

- 可通过如下方法安装已上传到 `clawhub` 的 `skill`

```bash
# 安装 clawhub CLI，如果安装过可跳过
npm i -g clawhub
# 或
pnpm add -g clawhub

# 通过 CLI 安装 skill
clawhub install recamera

# 更新 skill
clawhub install recamera
```

## 参考资料

- [Agent Skills 协议](https://agentskills.io/home)
- [OpenClaw 使用文档](https://docs.openclaw.ai/)
