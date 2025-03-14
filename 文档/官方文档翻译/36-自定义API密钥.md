# 自定义 API 密钥

## Azure LLM 提供商

Cursor 允许您输入各种 LLM 提供商的自己的 API 密钥，以便按照您自己的成本发送任意数量的 AI 消息。当使用客户 API 密钥时，我们会在调用 LLM 提供商时使用该密钥。

要使用您自己的 API 密钥，请转到 `Cursor Settings > Models` 并输入您的 API 密钥。然后，点击"验证"按钮。一旦您的密钥通过验证，您的 API 密钥就会被启用。

> ⚠️ 某些 Cursor 功能（如代码补全）需要专门的模型，无法与自定义 API 密钥一起使用。自定义 API 密钥只能用于使用来自 OpenAI、Anthropic 等标准模型的功能。

## OpenAI API 密钥

您可以从 [OpenAI 平台](OpenAI platform) 获取您自己的 API 密钥。

> ⚠️ OpenAI 的推理模型（o1、o1-mini、o3-mini）需要特殊配置，目前不支持自定义 API 密钥。

### OpenAI API 密钥
您可以输入您的 OpenAI 密钥以使用 Cursor 的公共 API 成本。注意：这可能比 pro 订阅更贵，而且不适用于自定义模型功能。

[输入您的 OpenAI API 密钥] [验证]

## Anthropic API 密钥

与 OpenAI 类似，您也可以设置自己的 Anthropic API 密钥，这样您将使用基于 claude 的模型，费用由您自己承担。

### Anthropic API 密钥
您可以输入您的 Anthropic 密钥以按成本使用 Claude。启用后，此密钥将用于所有以"claude-"开头的模型。

[输入您的 Anthropic API 密钥] [验证]

## Google API 密钥

对于 Google API 密钥，您可以设置自己的 API 密钥，这样您将使用如 `gemini-1.5-flash-500k` 等 Google 模型，费用由您自己承担。

### Google API 密钥
您可以输入您的 Google AI Studio 密钥以使用 Google 模型。Google 模型仅通过您自己的 API 访问提供。

[输入您的 Google AI Studio API 密钥] [验证]

## Azure 集成

最后，您也可以设置自己的 Azure API 密钥，这样您将使用 Azure OpenAI 模型，费用由您自己承担。

### Azure API 密钥
您可以使用 OpenAI 的 API 或 pro 版本，通过 Azure API 按成本使用 Cursor。

[开关按钮]

基础 URL：[例如：https://your-api.openai.azure.com/]
部署名称：[您在 Azure 上部署模型时选择的部署名称]
API 密钥：[输入您的 Azure OpenAI API 密钥]
[保存]

## FAQ

### 我的 API 密钥会被存储或离开我的设备吗？

您的 API 密钥不会被存储，但会随每个请求发送到我们的服务器。所有请求都通过我们的后端路由，我们在那里进行最终提示构建。

### 支持哪些自定义 LLM 提供商？

Cursor 仅支持与 OpenAI API 格式兼容的 API 提供商（如 OpenRouter）。我们不提供对自定义本地 LLM 设置或其他 API 格式的支持。如果您遇到自定义 API 设置问题，而该设置不是来自我们支持的提供商，我们很遗憾无法提供技术支持。 