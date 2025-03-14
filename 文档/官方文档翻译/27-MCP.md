# 模型上下文协议

了解如何在Cursor功能中添加和使用自定义MCP工具

## 什么是MCP？

模型上下文协议（Model Context Protocol，MCP）是一个开放协议，用于标准化应用程序如何向LLM提供上下文和工具。可以将MCP视为Cursor的插件系统 - 它允许您通过标准化接口将Agent连接到各种数据源和工具来扩展其功能。

## 用途

MCP允许您将Cursor连接到外部系统和数据源。这意味着您可以将Cursor与现有工具和基础设施集成，而不必在代码之外告诉Cursor项目的结构。

MCP服务器可以用任何能够输出到`stdout`或提供HTTP端点的语言编写。这种灵活性使您能够快速使用首选的编程语言和技术栈实现MCP服务器。

### 示例

#### 数据库
允许Cursor直接查询您的数据库，而不是手动输入架构或自己操作数据。

#### Notion
从Notion读取数据以指导Cursor实现功能。

#### GitHub
让Cursor创建PR、创建分支、查找代码等。

#### 内存
允许Cursor在您工作时记住和回忆信息。

#### Stripe
允许Cursor创建客户、管理订阅等。

## 架构

MCP服务器是通过标准化协议公开特定功能的轻量级程序。它们充当Cursor与外部工具或数据源之间的中介。

Cursor支持两种传输类型的MCP服务器：

### 💻 stdio传输

- 在您的**本地机器**上运行
- 由Cursor自动管理
- 通过`stdout`直接通信
- 仅您本地可访问

**输入：** Cursor自动运行的有效shell命令

### 🌐 SSE传输

- 可以**本地或远程**运行
- 由您管理和运行
- **通过网络**通信
- 可以跨机器**共享**

**输入：** MCP服务器的`/sse`端点URL

对于stdio服务器，命令应该是Cursor可以运行的有效shell命令。

对于SSE服务器，URL应该是SSE端点的URL，例如 http://example.com:8000/sse。

每种传输类型都有不同的用例，stdio更适合本地开发，而SSE则为分布式团队提供更大的灵活性。

## 配置MCP服务器

MCP服务器可以通过三种方式配置，按推荐顺序列出。所有配置方法都使用相同的JSON格式：

### 配置格式

MCP配置文件使用以下结构的JSON格式：

```json
{
  "mcpServers": {
    "server-name": {
      "command": "npx",
      "args": ["-y", "mcp-server"],
      "env": {
        "API_KEY": "your-api-key"
      }
    },
    "another-server": {
      "url": "http://localhost:8000/sse"
    }
  }
}
```

* `command`：（stdio）要运行的命令
* `args`：（stdio）命令的参数列表
* `env`：（stdio）环境变量
* `url`：（SSE）服务器的 SSE 端点 URL

### 配置位置

您可以根据使用场景将配置放在两个位置：

#### 项目配置
对于特定项目的工具，在项目目录中创建`.cursor/mcp.json`文件。这允许您定义仅在该特定项目中可用的MCP服务器。

#### 全局配置
对于想要在所有项目中使用的工具，在您的主目录中创建`~/.cursor/mcp.json`文件。这使MCP服务器在所有Cursor工作区中都可用。

### UI配置（不推荐）

虽然您可以通过UI添加MCP服务器，但不推荐这种方法，因为它不支持环境变量，并且需要为每个工作区手动配置。

要通过UI添加MCP服务器：

1. 转到`Cursor设置` > `功能` > `MCP`
2. 点击`+ 添加新MCP服务器`
3. 填写表单：
   * 选择传输类型（stdio或SSE）
   * 输入服务器名称
   * 对于stdio：输入要运行的命令（例如`node ~/mcp-quickstart/weather-server-typescript/build/index.js`）
   * 对于SSE：输入SSE端点URL（例如`http://localhost:8765/sse`）

## 在Agent中使用MCP工具

如果Composer Agent认为MCP设置页面上列出的"可用工具"相关，它会**自动**使用这些工具。要有意提示工具使用，只需通过名称或描述告诉agent使用该工具。

### 工具审批

默认情况下，当Agent想要使用MCP工具时，它会显示一条消息请求您的批准。您可以使用工具名称旁边的箭头展开消息，查看Agent使用该工具的参数。

#### Yolo模式

您可以启用Yolo模式，允许Agent自动运行MCP工具而无需批准，类似于执行终端命令的方式。

### 工具响应

当使用工具时，Cursor会在聊天中显示响应。

## 限制

MCP是一个非常新的协议，仍在积极开发中。需要注意一些已知的注意事项：

### 工具数量
某些MCP服务器或拥有多个活动MCP服务器的用户可能有许多可用工具。目前，Cursor只会向Agent发送前40个工具。

### 远程开发
Cursor直接从您的本地机器与MCP服务器通信，可以通过`stdio`直接通信或通过网络使用`sse`。因此，当通过SSH或其他开发环境访问Cursor时，MCP服务器可能无法正常工作。我们希望在未来的版本中改进这一点。

### MCP资源
MCP服务器提供两个主要功能：工具和资源。工具目前在Cursor中可用，允许Cursor执行MCP服务器提供的工具，并在后续步骤中使用输出。但是，资源目前尚不支持。我们希望在未来的版本中添加资源支持。 