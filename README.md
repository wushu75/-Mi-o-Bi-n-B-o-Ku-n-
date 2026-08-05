# 秒变爆款 (Miǎo Biàn Bào Kuǎn) 🚀

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](./LICENSE)
[![Manifest](https://img.shields.io/badge/manifest-v3-FF2442.svg)](./manifest.json)
[![China LLM Only](https://img.shields.io/badge/LLM-China%20only-FFD700.svg)](#-api-key-配置)

**一键三平台，AI 帮你秒出爆文** — 免费、开源、无境外 LLM 依赖的内容生成工具。

> One input → Xiaohongshu + Douyin + Bilibili posts, powered only by China-based LLMs.

---

## ✨ 核心功能 / Features

- 🎯 **一键三平台**：输入文字或 YouTube/B 站链接 → 自动生成小红书 + 抖音 + B 站优化文案
- 🇨🇳 **中国 LLM 原生**：支持 Kimi、DeepSeek、Qwen、GLM、MiniMax（**不含** OpenAI / Claude / Gemini）
- 🔓 **完全开源**：Apache 2.0 许可，社区驱动，代码透明可审计
- 💧 **开源水印**：每篇导出自动附带 `Made with 秒变爆款` 署名（可在设置关闭，欢迎保留）
- 🎬 **长视频转录**：自动抓取 YouTube / B 站字幕并总结改写
- 🎨 **品牌配色**：爆款红 `#FF2442` + 金光 `#FFD700`，专为创作者设计

## 🚀 快速开始 / Quick start

### 本地构建 / Build from source

```bash
git clone https://github.com/wushu75/-Mi-o-Bi-n-B-o-Ku-n-.git
cd -Mi-o-Bi-n-B-o-Ku-n-
npm install
npm run build          # 产物在 dist/
```

### 加载到 Chrome / Load unpacked

1. 打开 `chrome://extensions`
2. 右上角开启「开发者模式 / Developer mode」
3. 点击「加载已解压的扩展程序 / Load unpacked」，选择 `dist/` 目录

### 使用 / Usage

1. 点击工具栏的扩展图标 ⚡
2. 在设置 ⚙️ 中选择提供商并填入对应 API Key
3. 粘贴一段文字，或 YouTube/B 站链接（可点「使用当前标签页链接」）
4. 勾选目标平台（小红书 / 抖音 / B 站）
5. 点击「生成爆文」，复制或导出带水印文案

## 🔑 API Key 配置 / Providers

在设置中填入你自己的中国大模型 API Key（密钥仅保存在本机 `chrome.storage.local`，不上传任何服务器）：

| 提供商 | 厂商 | 获取地址 |
| --- | --- | --- |
| Kimi | 月之暗面 Moonshot | https://platform.moonshot.cn |
| DeepSeek | 深度求索 | https://platform.deepseek.com |
| Qwen 通义千问 | 阿里云 | https://dashscope.aliyun.com |
| GLM | 智谱 AI | https://open.bigmodel.cn |
| MiniMax | 稀宇科技 | https://api.minimaxi.com |

所有调用均走各家的 OpenAI 兼容接口。**本项目不集成任何境外大模型。**

## 🛠️ 技术栈 / Stack

- **Manifest V3**（Chrome 2026 标准）
- **TypeScript + React 18**
- **Tailwind CSS 3**
- **Vite 5** + `@crxjs/vite-plugin`
- **GitHub Actions**（打 tag 自动构建 & 发布）

## 📁 项目结构 / Structure

```
src/
├── popup/          # 弹出界面 (React)
│   └── components/ # InputPanel / OutputPanel / PlatformSelector / WatermarkBadge
├── background/     # Service Worker：调用 LLM、执行转录
├── content/        # Content Script：抓取当前页面文本
├── utils/          # llm-providers · platform-templates · watermark · transcriber · storage
└── types/          # 共享 TypeScript 类型
```

## 🔐 隐私 / Privacy

- API Key 与设置仅存于本地 `chrome.storage.local`。
- 生成请求由本机浏览器直接发往你所选的大模型厂商，项目方不设中转服务器。
- 转录仅抓取公开视频的字幕文本。

## 🤝 贡献 / Contributing

欢迎提交 Issue 与 PR！功能建议走 Issues，代码贡献走 Pull Requests。请遵循 `npm run typecheck` 通过后再提交。

## 🌟 路线图 / Roadmap

- [x] Kimi / DeepSeek / Qwen / GLM / MiniMax 集成
- [x] 小红书 / 抖音 / B 站模板
- [x] YouTube / B 站字幕转录
- [ ] 一键发布
- [ ] 团队协作与多账号
- [ ] 数据分析面板

## 📄 许可证 / License

[Apache 2.0](./LICENSE) — Made with ❤️ for Chinese creators · 为中国创作者打造。
