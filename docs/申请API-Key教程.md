# 申请国内 AI 模型 API Key 教程

独行OKR 的 AI 功能需要调用大模型服务，你要先申请一个 API Key（一般免费或按用量付费，很便宜）。

## 推荐：DeepSeek（深度求索）

1. 打开 https://platform.deepseek.com ，注册并登录
2. 进入左侧「API Keys」页面
3. 点「创建 API Key」，复制生成的 key（形如 `sk-...`）
4. 打开独行OKR →「设置」→「AI 教练」，把 key 填进「API Key」栏
5. Base URL 填 `https://api.deepseek.com`，模型填 `deepseek-v4-pro`
6. 点「测试连接」，看到「连接成功」即可使用

> 建议用 `deepseek-v4-pro`（最强）或 `deepseek-flash`（更快更省）。费用很低，个人日常使用通常每月几块钱。

## 其他国内模型（OpenAI 兼容，都能配）

只要服务商提供 OpenAI 兼容接口，就能填入独行OKR 使用。常见选项：

| 服务商 | 申请入口 | Base URL | 模型名示例 |
|---|---|---|---|
| Kimi（月之暗面） | platform.moonshot.cn | `https://api.moonshot.cn/v1` | `moonshot-v1-8k` |
| 智谱 GLM | open.bigmodel.cn | `https://open.bigmodel.cn/api/paas/v4` | `glm-4-plus` |
| 通义千问 | dashscope.aliyun.com | `https://dashscope.aliyuncs.com/compatible-mode/v1` | `qwen-plus` |
| DeepSeek | platform.deepseek.com | `https://api.deepseek.com` | `deepseek-v4-pro` |

填的时候：Base URL 和模型名一定要配对，填错了会连接失败。

## 数据安全说明

- **API Key 只存你本机浏览器**（localStorage），不会上传到任何服务器
- **只有点「AI 分析」时**，当前正在分析的那部分数据（你的 O / KR / 复盘文字）才会发送给你配置的模型服务商
- **不点 AI 功能，你的数据完全不离开本机**

## 常见问题

**Q：点了 AI 按钮报「请先配置 API key」？**
去「设置 → AI 教练」填 key 和 Base URL。

**Q：报「401」？**
key 填错了或已过期，重新复制粘贴。

**Q：报「请求超时」？**
网络问题，稍后重试；或换一个服务商试试。

**Q：不配 key 能不能用？**
能。基础 OKR 功能（定目标、复盘、归档、导入导出）完全离线可用，只有 AI 功能需要 key。
