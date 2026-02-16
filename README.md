# ChiXiao (赤霄)




<p align="center">
  <a href="https://wails.io/"><img src="https://img.shields.io/badge/Wails-v2-red.svg" alt="Wails"></a>
  <a href="https://go.dev/"><img src="https://img.shields.io/badge/Go-1.21+-blue.svg" alt="Go"></a>
  <a href="https://vuejs.org/"><img src="https://img.shields.io/badge/Vue-3-green.svg" alt="Vue"></a>
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License"></a>
</p>


<p align="center">
  <strong>现代化红队攻防综合平台 | Modern Integrated Security Platform</strong>
</p>


---

## 🚀 项目简介

**ChiXiao (赤霄)** 是一款专为红队工程师和渗透测试人员打造的现代化、跨平台安全工具箱。它集成了工具管理、智能研判、资产测绘与攻防辅助等核心功能，旨在解决传统渗透测试中工具分散、环境配置繁琐、协作效率低下等痛点，构建个人专属的“数字化武器库”。

## ✨ 核心功能

### 1. 🛠️ 智能工具箱 (Smart Toolbox)

- **统一管理**：支持 Nmap, Burp Suite, Metasploit 等任意 GUI/CLI 工具的接入与一键启动。
- **环境隔离**：自动识别并独立配置 Java (8/11/17)、Python (2/3) 运行环境，彻底告别环境冲突。
- **极速检索**：内置高性能模糊搜索（FZF算法），毫秒级定位目标工具。

### 2. 🧠 AI 智能研判 (AI Analysis)

- **日志分析**：基于大模型的 Web 日志深度研判，自动识别 SQL 注入、XSS、Webshell 等攻击特征。
- **Payload 解码**：智能识别并递归解码 Base64, Hex, URL 等多层混淆 Payload。
- **威胁溯源**：结合 IP 归属地与行为特征，自动生成攻击者画像与处置建议。
- **多模型支持**：支持 OpenAI、DeepSeek、Local (Ollama) 等多种模型后端。

### 3. 🌐 资产测绘 (Asset Mapping)

- **多源集成**：聚合 Fofa, Hunter, Quake 等主流测绘引擎 API。
- **数据导出**：支持测绘结果的一键检索与导出（CSV/Excel），助力资产梳理。

### 4. ⚔️ 攻防辅助 (Red Team Utils)

- **反弹 Shell**：可视化生成 Bash, Python, PHP, Java 等多语言反弹 Shell 命令。
- **编解码工具**：集成 CyberChef 核心功能，支持 URL, Base64, Hash, Encryption 等常见操作。
- **应急响应**：内置系统进程分析、网络连接监控与文件扫描功能。

---

## 🏗️ 技术架构

- **前端**：Vue 3 + Tailwind CSS (现代化响应式 UI)
- **后端**：Go (高性能逻辑处理) + Wails v2 (原生跨平台 WebView)
- **数据存储**：SQLite (本地加密存储，确保数据安全)
- **性能优化**：
  - **File-Offset Indexing**：GB 级日志文件秒级加载与检索。
  - **Native API**：直接调用系统底层 API (Windows syscall) 实现文件交互，移除 PowerShell 依赖，提升稳定性。

---

## � 快速开始

### 运行环境

- Windows 10/11 (x64)
- macOS / Linux (计划中)

### 部署说明

下载最新 Release 版本，解压即可运行。

```text
ChiXiao/
├── ChiXiao.exe             # 主程序
└── data/                   # 数据目录 (首次运行自动生成)
    ├── data.db             # 核心数据库
    └── GeoLite2-City.mmdb  # GeoIP 数据库 (可选)
```

> **注意**：部分功能（如 IP 归属地查询）需要 `GeoLite2-City.mmdb` 数据库文件。





