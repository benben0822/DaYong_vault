# 🛠️ Crawl4AI 智能爬虫工作台——Mac (Intel 芯片) 安装指南

本指南专为搭载传统 Intel 处理器（2020年及以前版本）的旧款 Mac 用户设计。请严格对照以下步骤进行无缝配置。

---

## 📌 第一步：准备基础环境
1. 打开 Mac 自带的 **“终端” (Terminal)** 软件。
2. 确保你的电脑中安装了 Homebrew 环境。如未安装，请在终端中运行以下命令：
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
3. 安装适用于 Intel x86_64 架构的 Python 3.11 独立版本：
   ```bash
   brew install python@3.11
   ```

---

## 📌 第二步：创建文件夹与环境编译
由于 Intel 芯片对部分新一代异步并发库（如 Playwright 依赖）的编译方式不同，请务必严格按以下顺序执行：
1. 在 Mac 桌面上右键新建文件夹，命名为 `Crawl4AI-Tool`。
2. 在终端中，切入该文件夹：
   ```bash
   cd ~/Desktop/Crawl4AI-Tool
   ```
3. 依次复制并运行以下四行命令：
   ```bash
   # 1. 独立隔离出本地虚拟环境
   python3.11 -m venv crawl4ai_env

   # 2. 激活虚拟环境
   source crawl4ai_env/bin/activate

   # 3. 升级基础包管理器并安装核心组件
   pip install --upgrade pip
   pip install crawl4ai streamlit nest_asyncio

   # 4. 下载并初始化适配 Intel 架构的 Chromium 浏览器内核
   crawl4ai-setup
   ```
4. 待浏览器内核全部下载解压完成后，终端左侧会常驻显示 `(crawl4ai_env)`。

---

## 📌 第三步：放入核心代码文件
请将团队统一分发的图形化代码文件命名为 **`app_ui.py`**，然后把它粘贴进桌面的 `Crawl4AI-Tool` 文件夹根目录下。

---

## 🚀 以后如何使用？
由于 Mac 无法识别 `.bat` 启动块，Intel 芯片用户日常开启工作台请按以下操作：
1. 启动 Mac 的 **“终端” (Terminal)**。
2. 复制并粘贴运行这行一键合并启动命令：
   ```bash
   cd ~/Desktop/Crawl4AI-Tool && source crawl4ai_env/bin/activate && streamlit run app_ui.py
   ```
3. 几秒钟后，系统会自动在你的浏览器中弹出一个大模型最爱的智能爬虫图形化操作台。

---

## 💡 避坑注意要点
1. **终端不可关闭**：抓取数据期间，背景中的白色或黑色“终端”窗口属于正在运行的服务器进程，切勿点击 `X` 关闭它，不用时将其最小化即可。
2. **硬件发热属于正常现象**：在抓取具有复杂动态 JS 渲染的大型网页时，旧款 Intel 处理器因为要同步唤醒无头浏览器进行页面解析，风扇偶尔会加速转动，这属于正常的高负载处理现象。
