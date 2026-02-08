# ChiXiao (赤霄) - 安全工具管理平台

<div align="center">
  <img src="./build/appicon.png" width="128" height="128" alt="ChiXiao Logo">
  <h3>赤霄 (ChiXiao)</h3>
  <p>一款专为安全工程师打造的现代化、跨平台本地工具管理与协作平台。</p>
</div>

---

## 📖 项目简介

**ChiXiao (赤霄)** (原 SecuHub-Wails) 是一款基于 **Wails** (Go + Vue 3) 开发的桌面端安全工具箱。它旨在解决安全工程师在日常工作中工具分散、环境配置繁琐、常用命令遗忘等痛点，提供了一个统一、高效、美观的作业环境。

## ✨ 核心功能

### 1. 🛠️ 工具箱 (Toolbox)
核心的工具管理模块，支持任意本地工具的快速接入与启动。
*   **多环境支持**：自动识别并配置 Java (8/11/17+)、Python (2/3) 等运行环境。
*   **快速启动**：一键启动 GUI 工具或自动打开终端运行 CLI 工具。
*   **分类管理**：自定义工具分类，支持拖拽排序与图标自定义。
*   **智能搜索**：支持拼音/首字母快速检索工具。

### 2. 🌐 信息收集 (Info Gathering)
集成主流的空间测绘与信息收集能力。
*   **空间测绘**：集成 **Fofa**、**Hunter** 等 API，支持直接在客户端进行资产检索与导出。
*   **网址导航**：内置精选的安全圈常用网站、在线工具书签，支持自定义添加。
*   **Map API**：提供地图 API 相关的测试与利用辅助功能。

### 3. ⚔️ 攻防赋能 (Attack & Defense)
提供红队作业中常用的辅助生成与检测工具。
*   **反弹 Shell 生成器**：可视化的反弹 Shell 命令生成，支持多种语言 (Bash, Python, PHP, PowerShell 等) 及编码方式 (Base64, URL 等)。
*   **社工字典生成**：基于个人信息（姓名、生日、手机号等）生成定制化的社工密码字典。
*   **弱口令查询**：内置常见弱口令库，支持快速查询与匹配。
*   **Java 编码辅助**：提供 Java 相关的常见编码转换与利用辅助。

### 4. 🧰 辅助工具 (Auxiliary)
提升日常效率的实用小工具集合。
*   **CyberChef 集成**：内置本地化 CyberChef，无需联网即可使用强大的编解码功能。
*   **数据对比**：支持两个文本列表的交集、并集、差集运算，快速处理资产/域名列表。
*   **IP 提取**：从凌乱的文本中快速提取 IPv4/IPv6 地址。
*   **仓库更新**：一键更新本地工具仓库，保持工具库的最新状态。

### 5. 📚 知识库 (Knowledge Base)
*   **漏洞文库**：本地化的漏洞详情查阅与 POC 管理。
*   **备忘录**：随手记录渗透测试过程中的关键信息、Payload 或待办事项，支持 Markdown。

## ⚙️ 技术栈

*   **Frontend**: Vue 3, TypeScript, Tailwind CSS, Vite
*   **Backend**: Go 1.23+
*   **Framework**: Wails v2.5.0
*   **OS Support**: Windows (主要), macOS/Linux (理论支持)

## 🚀 快速开始

### 环境要求
*   **Go**: 1.23+
*   **Node.js**: 16+
*   **NPM/Yarn/Pnpm**

### 开发运行
```powershell
# 克隆项目
git clone https://github.com/your-repo/chixiao.git
cd chixiao

# 安装前端依赖
cd frontend
npm install
cd ..

# 运行开发模式 (支持热重载)
wails dev
```

### 编译构建
```powershell
# 构建 Windows 版本
wails build -platform windows/amd64
```

## 📝 目录结构

```
ChiXiao/
├── backend/            # Go 后端源码 (服务、模型、配置)
├── frontend/           # Vue 3 前端源码
│   ├── src/
│   │   ├── pages/      # 页面组件
│   │   ├── components/ # 通用组件
│   │   └── ...
├── build/              # 构建产物与资源
├── wails.json          # Wails 项目配置
└── go.mod              # Go 依赖管理
```

## 📄 许可证

本项目采用 MIT 许可证。详见 [LICENSE](LICENSE) 文件。

---
<p align="center">Made with ❤️ by ChiXiao Team</p>
