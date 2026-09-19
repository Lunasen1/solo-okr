# 申请 AI 教练的 API key

AI 教练直连 OpenAI 兼容的模型服务，默认使用 DeepSeek。你只需要申请一个 API key，配置到「设置 → AI 教练」即可使用。数据不会经过本工具以外的服务器，但请确认你信任所配置的模型服务商。

## 方式一：DeepSeek（推荐）

1. 打开 [DeepSeek 开放平台](https://platform.deepseek.com/) 并登录/注册。
2. 进入「API Keys」页面，点击「创建 API key」。
3. 复制生成的 key（通常以 `sk-` 开头），粘贴到「设置 → AI 教练 → API Key」。
4. Base URL 保持默认：`https://api.deepseek.com`。
5. 模型名默认 `deepseek-v4-pro`；如果你的账号可用模型不同，请填写平台提供的准确模型名。

## 方式二：其他 OpenAI 兼容服务

只要服务提供 `/chat/completions` 且允许浏览器跨域（CORS）访问，就可以使用：

- Base URL 填服务的根地址，例如 `https://api.example.com`（不要带 `/chat/completions`）。
- API Key 填该服务签发的 key。
- 模型名填服务支持的模型 ID。

## 常见问题

- **提示「API key 无效或已过期（401）」**：检查 key 是否复制完整、是否仍有效、是否对应正确的服务商。
- **提示网络失败**：该服务可能不支持浏览器直连，或 Base URL 填错；请改用支持 CORS 的服务。
- **AI 只给建议吗？** 是。所有 AI 输出都不会自动写入，必须由你手动「采纳」或复制后自己修改。
- **Key 会被上传到别处吗？** 不会。Key 只保存在当前浏览器 localStorage 中，仅在你点击 AI 分析时发送给你配置的模型服务商。
