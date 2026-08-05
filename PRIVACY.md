# 隐私政策 / Privacy Policy — 秒变爆款 (Miǎo Biàn Bào Kuǎn)

最后更新 / Last updated: 2026

## 简体中文

**秒变爆款** 是一款开源 Chrome 扩展。我们的核心原则是：**你的数据留在你的设备上。**

### 我们收集什么
本扩展**不设任何服务器**，不收集、不上传、不留存你的个人数据。具体而言：

- **API Key**：你填写的大模型 API Key 仅保存在浏览器本地的 `chrome.storage.local` 中，用于对**你所选择的**大模型厂商发起 API 调用。它不会被发送到开发者或任何第三方。
- **素材内容**：你粘贴的文本或视频链接，仅用于构建发送给**你所选择的**大模型 API 的生成请求。本扩展不会另行保存或转发这些内容。
- **设置项**：所选提供商、模型、水印开关等偏好仅存于本地。

### 数据发往何处
当你点击「生成爆文」时，你的素材会由浏览器**直接**发送给你所选的大模型厂商（如 Moonshot、DeepSeek、阿里云、智谱、MiniMax）。这些请求受各厂商自身隐私政策约束。除此之外，本扩展不与任何其他服务器通信。

抓取 YouTube / B站 字幕时，请求直接发往对应平台。

### 我们不做的事
- 不出售或转让任何数据。
- 不用于广告、画像或与本扩展用途无关的目的。
- 不设分析/埋点上报。

### 权限
本扩展申请的权限（storage、activeTab、scripting、clipboardWrite、downloads 及有限的主机权限）仅用于实现文案生成、转录、复制与导出功能。详见项目 README 与商店权限说明。

### 开源
本扩展完全开源（Apache 2.0），你可以审计全部源代码：
https://github.com/wushu75/-Mi-o-Bi-n-B-o-Ku-n-

### 联系
如有疑问，请在 GitHub 提交 Issue：
https://github.com/wushu75/-Mi-o-Bi-n-B-o-Ku-n-/issues

---

## English

**秒变爆款 (Miǎo Biàn Bào Kuǎn)** is an open-source Chrome extension. Our core principle: **your data stays on your device.**

### What we collect
The extension has **no server** and does not collect, upload, or retain your personal data:

- **API keys** you enter are stored only in your browser's local `chrome.storage.local`, and are used solely to call the LLM provider **you選択**. They are never sent to the developer or any third party.
- **Your input** (pasted text or a video link) is used only to build the generation request sent to the LLM API **you chose**. The extension does not otherwise store or forward it.
- **Settings** (chosen provider, model, watermark toggle) are stored locally.

### Where data goes
When you click "生成爆文" (Generate), your material is sent **directly** from your browser to the LLM provider you selected (e.g., Moonshot, DeepSeek, Alibaba Cloud, Zhipu, MiniMax), governed by that provider's own privacy policy. Fetching YouTube/Bilibili captions sends requests directly to those platforms. The extension communicates with no other server.

### What we don't do
- No selling or transferring of data.
- No advertising, profiling, or unrelated use.
- No analytics or telemetry.

### Open source
Fully open-source under Apache 2.0 — audit the code:
https://github.com/wushu75/-Mi-o-Bi-n-B-o-Ku-n-

### Contact
Open an issue on GitHub:
https://github.com/wushu75/-Mi-o-Bi-n-B-o-Ku-n-/issues
