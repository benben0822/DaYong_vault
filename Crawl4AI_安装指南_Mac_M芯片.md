# 🛠️ Crawl4AI 智能爬虫工作台——Mac (M系芯片: M1/M2/M3) 安装指南

本指南专为搭载 Apple Silicon（M1、M2、M3 芯片）的 Mac 用户设计。由于 M 系芯片采用内核级 ARM 架构，安装时需要确保依赖库无缝原生运行。

---

## 📌 第一步：安装 Mac 核心开发包 (Homebrew)
1. 打开 Mac 自带的 **“终端” (Terminal)** 软件（可以通过 Command + 空格键 搜索“终端”找到）。
2. 检查并安装 Homebrew 环境（Mac 必备的包管理工具）。如果电脑里没有，请粘贴以下命令回车安装：
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
3. 利用 Homebrew 一键安装原生兼容 M 芯片的 Python 3.11：
   ```bash
   brew install python@3.11
   ```

---

## 📌 第二步：建立项目文件夹并配置环境
1. 在你的 Mac 桌面上，新建一个文件夹，命名为 `Crawl4AI-Tool`。
2. 在终端 (Terminal) 中，通过 `cd` 命令进入到这个刚刚新建的文件夹：
   ```bash
   cd ~/Desktop/Crawl4AI-Tool
   ```
3. 依次复制并运行以下四行环境配置命令（由于 M 芯片性能优异，编译速度非常快）：
   ```bash
   # 1. 使用原生 3.11 创建本地虚拟环境
   python3.11 -m venv crawl4ai_env

   # 2. 激活虚拟环境
   source crawl4ai_env/bin/activate

   # 3. 升级 pip 并一键安装专属核心库
   pip install --upgrade pip
   pip install crawl4ai streamlit nest_asyncio

   # 4. 下载并初始化原生 ARM 架构的无头浏览器内核
   crawl4ai-setup
   ```
4. 运行完成后，终端左侧会亮起 `(crawl4ai_env)` 标志，代表环境完全就绪。

---

## 📌 第三步：放入核心代码文件
请在桌面的 `Crawl4AI-Tool` 文件夹中，放入团队统一提供的 **`app_ui.py`** 核心界面代码文件（确保名字一字不差）。

由于 Mac 系统不支持双击 `.bat` 批处理文件，为了省去每次敲击一长串路径的麻烦，你可以使用以下的一键日常启动命令。

---

## 🚀 以后如何使用？
以后每次需要开启智能爬虫工作台时，方法非常简单：
1. 打开 Mac 的 **“终端” (Terminal)**。
2. 直接复制并粘贴运行以下这一整行**组合命令**并回车：
   ```bash
   cd ~/Desktop/Crawl4AI-Tool && source crawl4ai_env/bin/activate && streamlit run app_ui.py
   ```
3. 终端会自动完成目录切换与激活，并直接在你的 Safari 或 Chrome 浏览器中拉起绚丽的图形化操作大屏！

---

## 💡 Mac 团队成员共性贴士
1. **保持终端开启**：在浏览器里愉快地点鼠标爬取数据时，请不要随手把后台的“终端”窗口关闭。终端一旦关闭，网页端服务会立即中断。
2. **科学上网环境提示**：M 芯片在抓取部分国外技术文档或学术网站时，如果遇到报错，请检查 Mac 上的系统代理或节点是否切换为了全局模式（Global）。
