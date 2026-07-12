# 🛠️ Crawl4AI 智能爬虫工作台——Windows 平台安装指南

本指南专为 Windows 10 / 11 用户设计，包含完整细致的保姆级安装步骤。

---

## 📌 第一步：安装基础环境 (Python)
1. 访问 Python 官方网站：[https://www.python.org/downloads/](https://www.python.org/downloads/)
2. 下载 **Python 3.11** 版本（推荐 3.11.x 系列，稳定性最佳，请尽量避免选择 3.12 或 3.13）。
3. **⚠️ 极其重要：** 双击打开安装包时，**务必勾选最下方的 `Add Python.exe to PATH`**（将 Python 添加到系统环境变量），然后再点击 `Install Now`。

---

## 📌 第二步：建立项目文件夹并配置环境
1. 在电脑的任意盘符下（例如 D 盘或 E 盘），新建一个文件夹，命名为 `Crawl4AI-Tool`。
2. 进入该文件夹，在空白处按住键盘上的 **`Shift` 键不放**，同时**点击鼠标右键**，选择 **“在此处打开 PowerShell 窗口”**（或“在此处打开终端”）。
3. 在弹出的黑色窗口中，依次复制并运行以下四行命令（每输入一行就敲一次回车，等待它运行完再输下一行）：
   ```powershell
   # 1. 创建名为 crawl4ai_env 的本地虚拟环境
   python -m venv crawl4ai_env

   # 2. 激活虚拟环境
   .\crawl4ai_env\Scripts\activate

   # 3. 升级基础工具并安装核心爬虫与 UI 界面库
   pip install --upgrade pip
   pip install crawl4ai streamlit nest_asyncio

   # 4. 下载并初始化爬虫专属的无头浏览器内核（这一步下载文件较大，请耐心等待完成）
   crawl4ai-setup
   ```
4. 当看到窗口里不再滚动条，且最左边亮起 `(crawl4ai_env)` 时，代表环境全部配置成功。此时可以关闭该黑窗口。

---

## 📌 第三步：放入核心代码与创建“一键启动开关”
请在新建的 `Crawl4AI-Tool` 文件夹根目录下（**注意：是和 `crawl4ai_env` 文件夹平级，绝对不能放进它内部**），创建以下两个文件：

### 1. 放入核心界面文件：`app_ui.py`
在空白处右键新建一个文本文档，重命名为 `app_ui.py`（注意把最后的 `.txt` 后缀删掉）。将团队统一提供的长篇 Python UI 源代码完整粘贴进去并保存。

### 2. 创建一键启动开关：`启动可视化界面.bat`
在空白处右键新建一个文本文档，重命名为 `启动可视化界面.bat`。右键点击它选择“编辑”或“用记事本打开”，将以下命令完整复制进去并保存：
```bat
@echo off
chcp 65001 >nul
title Crawl4AI 可视化控制台面板
cd /d "%~dp0"
if not exist "crawl4ai_env\Scripts\activate.bat" (
    echo [错误] 未在当前目录下找到 crawl4ai_env 虚拟环境！
    pause
    exit /b
)
call crawl4ai_env\Scripts\activate.bat
streamlit run app_ui.py
pause
```

---

## 🚀 以后如何使用？
以后每次需要使用爬虫时，你**不需要编写或输入任何代码**。
直接**双击运行 `启动可视化界面.bat`**，它会自动唤醒引擎，并在 3 秒内自动在你的浏览器里弹出一个漂亮的智能爬虫控制台大屏！

---

## 💡 小白实用避坑指南
1. **黑窗口不能关**：双击 `.bat` 后会弹出一个黑色的文字窗口，接着才会弹出网页。在整个使用爬虫的过程中，**绝对不能关闭那个黑色窗口**。它是网页界面的后台发动机，关掉它网页就会瘫痪。
2. **首次运行卡顿**：第一次在网页里点击“开始极速抓取”时，系统需要首次唤醒 Chromium 浏览器内核，会有几秒钟的延迟，属于正常现象，第二次点击就会变成毫秒级响应。
