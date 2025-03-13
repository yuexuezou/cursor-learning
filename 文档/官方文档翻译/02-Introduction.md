# 简介

了解如何使用Cursor的核心功能：Tab代码补全、用于代码查询的Chat以及提供辅助的Agent

## 概览

Cursor是一款强大的AI优先代码编辑器，可增强您的开发工作流程。安装后，您将可以使用这些核心功能，它们无缝协作，提高您的工作效率：

* **AI驱动的代码补全**，能够理解您的代码库并提供上下文感知的建议
* **对话界面**，用于通过Ask、Edit和Agent模式探索、理解和修改代码
* **智能工具**，用于处理复杂的开发任务

## 入门指南

开始探索Cursor的AI驱动功能：

* **Tab**：按下`Tab`键获取智能代码补全
* **CMD-K**：使用`Cmd/Ctrl + K`进行内联代码编辑
* **Composer**：使用`⌘I`打开带有Ask、Edit和Agent模式的统一AI界面

## 设置

Cursor设计为灵活且可定制的。您可以通过两种方式进行配置：

### Cursor设置

* 通过齿轮图标、`Cmd/Ctrl + Shift + J`或命令面板 > `Cursor Settings`访问
* 配置AI功能和Cursor特定的偏好设置

### 编辑器设置

* 通过命令面板（`Cmd/Ctrl + Shift + P`）> `"Preferences: Open Settings (UI)"`访问
* 调整编辑器行为和外观

让我们详细探索每个功能：

### Tab

Cursor中的Tab补全由理解您代码上下文的先进AI模型提供支持。在您输入时，您将收到智能建议，这些建议可以：

* 完成您当前的代码行
* 建议完整的函数实现
* 帮助处理常见模式和样板代码
* 随着时间的推移适应您的编码风格

[了解更多Tab功能](https://docs.cursor.com/editor/tab)或[查看它与GitHub Copilot的比较](https://docs.cursor.com/editor/tab/migrating-from-copilot)。

### Composer

Cursor提供了一个统一的AI界面，包含三种无缝协作的模式：

**Ask模式**

* 询问特定代码部分的问题
* 获取复杂函数的解释
* 查找代码模式和示例
* 探索和理解您的代码库

**Edit模式**

* 对代码进行单轮编辑
* 精确应用有针对性的更改
* 自信地审查和应用更改
* 单独处理文件

**Agent模式（默认）**

* 进行代码库范围的更改和重构
* 根据需求实现新功能
* 调试跨多个文件的复杂问题
* 生成测试和文档
* 保持整个项目的一致性

在对话过程中切换模式，以最适合您当前任务的方式工作。[了解更多关于统一AI界面的信息](https://docs.cursor.com/editor/composer)或[探索Agent模式的特定功能](https://docs.cursor.com/editor/agent)。

### Context

Context是支持Cursor所有AI功能的基础。以下是它的工作原理：

* 当您打开代码库时，我们会自动索引您的代码，使其可作为上下文使用
* 使用@符号精确控制您提供的上下文：
  * @files和@folders用于特定路径
  * @web用于外部文档
  * @git用于版本控制上下文
* 配置AI规则以自定义行为
* 设置MCP用于外部上下文提供者

## 模型

您可以在[模型页面](https://docs.cursor.com/settings/models)上查看我们支持的所有模型及其定价。在设置中配置您的API密钥和偏好。

## 使用

强烈建议阅读关于[使用和计划](https://docs.cursor.com/account/usage)以了解Cursor定价如何工作。查看我们的[定价页面](https://docs.cursor.com/account/pricing)获取有关计划和功能的更多详情。

需要帮助？访问我们的[故障排除指南](https://docs.cursor.com/troubleshooting/troubleshooting-guide)或加入我们的[社区论坛](https://forum.cursor.com/)。 