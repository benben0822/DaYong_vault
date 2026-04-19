
---

## 概述

调用 ollama 提供的 cloud 大模型能实现 token 自由的同时又无需本地高配显卡。建议多配置一个低参数模型以备断网或者使用太猛燃尽免费token的情况可以调用本地大模型

---

## 操作步骤

### 1. 安装 Claude Code 和 Ollama

```bash
npm install -g @anthropic-ai/claude-code@latest
```

Ollama 可以通过官网 https://ollama.com/ 下载安装包安装。

> **注意：** Ollama 版本 v0.14.0+，Claude Code 版本 v2.1.12+，可以通过下面命令验证：

```bash
claude --version
ollama --version
```

Ollama 安装后会自动作为后台服务运行。应该可以在 http://localhost:11434 上看到它运行。

---

### 2. 下载大模型

可以通过 Ollama 的 WebUI 页面直接下载，也可以通过命令行快速拉取适合编码的模型：

```bash
# 查看本地模型
ollama list

# 下载新模型
ollama pull qwen2.5-coder:7b

# 删除模型
ollama rm qwen2.5-coder:7b

# 查看模型基本参数
ollama show qwen2.5-coder:7b
```

---

### 3. 配置 Claude Code 连接本地 Ollama

```bash
export ANTHROPIC_AUTH_TOKEN=ollama
export ANTHROPIC_BASE_URL=http://localhost:11434

# 启动 Claude Code 并指定本地模型
claude --model qwen2.5-coder:7b

# 如果想使用云端模型，命令类似
claude --model glm-5.1:cloud
```
或者直接修改 setting.json 文件，settinng文件所在路径：C:\Users\你的用户名\.claude\settings.json
![Pasted image 20260411114501](Pasted%20image%2020260411114501.png)

> **注意：** 如果你开启了系统代理，可能会遇到 `API Error: Connection error`。这是因为流量被转发到了代理服务器而找不到 localhost。请先在终端执行：

```bash
unset https_proxy
unset http_proxy
```

---

### 4. 从 Ollama 打开 Claude code

![Pasted image 20260411121431](Pasted%20image%2020260411121431.png)


复制粘贴命令：
```
ollama launch claude
```
到终端并运行
![Pasted image 20260419193128](Pasted%20image%2020260419193128.png)
![Pasted image 20260419193405](Pasted%20image%2020260419193405.png)


### 备注：

## 1、ollama模型库地址：https://ollama.com/library
## 2、