# Bright Data ChatGPT 搜索抓取器（Python）

[![Bright Data 推广](https://github.com/luminati-io/LinkedIn-Scraper/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://www.bright.cn/)

<a href="https://githubbox.com/brightdata/bright-data-scrape-chatgpt-search-python-project?file=index.py" target="_blank">在 CodeSandbox 中打开</a>，使用 GitHub 登录，然后 fork 该仓库开始进行更改。

本项目提供一个使用 Bright Data Web Scraper API 抓取 [ChatGPT AI 搜索](https://www.bright.cn/products/web-scraper/chatgpt) 结果的简易 Python 样板代码。

---

## 目录
- [概览](#概览)
- [功能](#功能)
- [演示](#演示)
- [先决条件](#先决条件)
- [安装](#安装)
- [使用方法](#使用方法)
- [配置](#配置)
- [输出](#输出)

---

## 概览

该仓库演示如何使用 Bright Data Scraper API 触发并下载 ChatGPT AI 搜索结果。包含用于批量与自定义搜索的示例提示词与实用函数。

---

## 功能

- 通过 Bright Data Scraper 的 `/trigger` API 端点触发 ChatGPT AI 搜索
- 使用 `/progress` 端点监控进度
- 将结果下载并保存为 JSON
- 彩色控制台输出，提升用户体验
- 支持单次、批量与自定义搜索

---

## 演示

https://github.com/user-attachments/assets/5fe827aa-b672-4b57-b284-cc285ae40c2e

---

## 先决条件

- Python 3.7 或更高版本
- 拥有带 API Key 的 Bright Data 账户

---

## 安装

```bash
git clone https://github.com/your-org/bright-data-scrape-chatgpt-search-python-project.git
cd bright-data-scrape-chatgpt-search-python-project
pip install -r requirements.txt
```

### 依赖项

本项目需要以下 Python 包：
- `requests` - 用于发起 HTTP API 调用
- `colorama` - 用于彩色控制台输出

安装方式：
```bash
pip install requests colorama
```

---

## 使用方法

1. 设置 Bright Data API 令牌
   
   编辑 [`index.py`](index.py) 并设置你的 API 令牌：
   ```python
   API_TOKEN = 'YOUR_API_TOKEN_HERE'
   ```

2. 运行抓取器
   ```bash
   python index.py
   ```
   
   结果将以带时间戳的 `.json` 文件保存在项目目录中。

---

## 配置

- API 令牌：  
  在 Bright Data 控制台的 Account Settings → API Key 中获取你的 API 令牌。

- 数据集 ID：  
  ChatGPT AI Search 的默认数据集 ID 已在 [`index.py`](index.py) 中设置：
  ```python
  DATASET_ID = 'gd_m7aof0k82r803d5bjm'
  ```

---

## 输出

- 结果会保存为 JSON 文件（例如：`chatgpt_results_2024-01-15T10-30-45.json`）。
- 每个文件包含来自 Bright Data 的原始 API 响应。
- 控制台输出以彩色格式提供实时进度更新。

### 控制台输出示例

```
🌟 ChatGPT AI 搜索抓取器
=============================

📋 正在运行示例搜索...
🤖 开始 ChatGPT AI 搜索...
📝 搜索 3 个提示词
📤 发送 JSON 请求体:
[
  {
    "url": "https://chatgpt.com/",
    "prompt": "纽约顶级酒店",
    "country": ""
  }
]
✅ 搜索已启动！快照 ID: abc123
⏳ 正在处理搜索...
📊 状态：运行中 (1/60)
📊 状态：就绪 (2/60)
⬇️ 正在下载 AI 响应...
🎉 成功！已下载结果
💾 结果已保存到 chatgpt_results_2024-01-15T10-30-45.json

✨ 全部完成！请查看保存的 JSON 文件以获取结果。
```

---
