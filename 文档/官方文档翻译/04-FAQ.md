# 常见问题（FAQ）

关于Cursor的功能、语言支持、模型和使用的常见问题

## Cursor支持哪些编程语言？

虽然Cursor可以与任何编程语言一起使用，但由于模型训练数据丰富，它在Python和JavaScript/TypeScript方面表现尤为出色。它在Swift、C和Rust方面也表现良好。您可以通过在项目中添加相关文档来增强对任何语言的支持。

## 如何保持AI模型与最新文档同步？

Cursor利用强大的基础模型，如Claude 3.5和GPT-4。对于最新的库信息，您可以使用我们的[@web搜索功能](https://docs.cursor.com/context/@-symbols/@-web)。由于核心语言概念很少发生剧烈变化，这些模型能够长期保持其有效性。

## MCP服务器的目的是什么？

MCP服务器作为将外部上下文引入Cursor的桥梁。它支持连接到Google Drive和Notion等服务，帮助您将这些来源的文档和需求整合到您的工作流程中。更多信息请参阅[Model Context Protocol](https://docs.cursor.com/context/model-context-protocol)。

## 项目索引有大小限制吗？

默认情况下，项目限制为10,000个文件，不过这可以根据需要进行调整。为了优化索引性能，您可以使用[`.cursorignore`](https://docs.cursor.com/context/ignore-files)从索引过程中排除不必要的文件。

## 如何在多个代码库之间共享上下文？

目前，最简单的方法是将相关代码库放在同一目录中，并从那里启动Cursor。我们正在积极开发改进的多项目文件夹管理支持。

## Cursor更新是如何工作的？

Cursor经常更新新功能和改进。您可以在[cursor.com/changelog](https://cursor.com/changelog)的更新日志中找到最新的变更和更新。我们定期发布更新，以增强您的体验并添加新功能。

## 为什么我还没有收到最新版本？

我们会在多天内逐步推出新版本，以确保稳定性。如果您还没有收到更新，可以预期它很快就会出现。您也可以通过打开命令面板（Cmd/Ctrl + Shift + P）并输入"Attempt Update"来手动检查更新。

## 如何删除我的数据？

您可以通过进入您的[仪表板](https://cursor.com/dashboard)并点击"Delete Account"（删除账户）按钮来删除您的账户和所有相关数据。

## 其他资源

* [常见问题](https://docs.cursor.com/troubleshooting/common-issues) - 常见问题的解决方案
* [键盘快捷键](https://docs.cursor.com/editor/keyboard-shortcuts) - 完整的键绑定和快捷键列表 