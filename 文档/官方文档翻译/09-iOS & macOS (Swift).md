# iOS & macOS (Swift)

了解如何为Swift设置Cursor

欢迎使用Cursor进行Swift开发！无论您是构建iOS应用、macOS应用还是服务器端Swift项目，我们都能满足您的需求。本指南将帮助您在Cursor中设置Swift环境，从基础开始，逐步深入到更高级的功能。

## 基本工作流程

使用Cursor进行Swift开发的最简单方法是将其作为主要代码编辑器，同时仍然依靠Xcode来构建和运行您的应用。您将获得以下出色功能：

* 智能代码补全
* AI驱动的编码辅助（在任何行上尝试CMD+K）
* 使用@Docs快速访问文档
* 语法高亮
* 基本代码导航

当您需要构建或运行应用时，只需切换到Xcode。这种工作流程非常适合那些希望利用Cursor的AI功能，同时坚持使用熟悉的Xcode工具进行调试和部署的开发者。

### 热重载

当使用XCode工作区或项目（而不是直接在XCode中打开文件夹）时，XCode通常会忽略在Cursor中或一般在XCode外部对文件所做的更改。

虽然您可以在XCode中打开文件夹来解决这个问题，但您可能需要使用项目进行Swift开发工作流程。

解决这个问题的一个很好的方法是使用Inject，这是一个Swift热重载库，允许您的应用"热重载"并在实时更改后立即更新。这不会受到Xcode工作区/项目问题的副作用影响，并允许您在Cursor中进行更改并立即在应用中反映出来。

Inject - Swift的热重载：了解更多关于Inject以及如何在Swift项目中使用它。

## 高级Swift开发

本指南的这一部分的灵感主要来自Thomas Ricouard及其关于使用Cursor进行iOS开发的文章。请查看他的文章了解更多详情，并关注他获取更多Swift内容。

如果您希望一次只需打开一个编辑器，并且想避免在Xcode和Cursor之间切换的需要，您可以使用像Sweetpad这样的扩展将Cursor直接与Xcode的底层构建系统集成。

Sweetpad是一个强大的扩展，允许您直接在Cursor中构建、运行和调试Swift项目，而不会影响Xcode的功能。

要开始使用Sweetpad，您仍然需要在Mac上安装Xcode - 这是Swift开发的基础。您可以从Mac App Store下载Xcode。一旦您设置好Xcode，让我们用一些基本工具增强您在Cursor中的开发体验。

打开终端并运行：

```bash
# 无需打开XCode即可构建项目
brew install xcode-build-server

# 将`xcodebuild`命令输出美化到Cursor的终端
brew install xcbeautify

# 允许高级格式化和语言功能
brew install swiftformat
```

接下来，在Cursor中安装Swift Language Support扩展。这将为您提供开箱即用的语法高亮和基本语言功能。

然后，我们可以安装Sweetpad扩展将Cursor与Xcode集成。Sweetpad在`xcodebuild` CLI（以及更多）周围包装了一系列快捷方式，允许您扫描目标、选择目标、构建和运行应用，就像Xcode一样。除此之外，它还将为Xcode Build Server设置您的项目，以便您获得上述所有功能。

### Sweetpad使用

安装Sweetpad后，并且在Cursor中打开Swift项目后，您应该首先运行`Sweetpad: Generate Build Server Config`命令。这将在项目根目录中生成一个`buildServer.json`文件，允许Xcode Build Server与您的项目一起工作。

然后，从命令面板或Sweetpad侧边栏，您可以选择要构建和运行的目标。

您需要构建项目一次以启用自动完成、跳转到定义和其他语言功能。

您现在还可以按F5键使用调试器构建和运行项目 - 您可能需要首先创建启动配置，但在提示时只需从列表中选择Sweetpad即可！

与Cursor中的许多扩展一样，您可以将许多Sweetpad命令绑定到键盘快捷键，使您的工作流程更加高效。

要了解更多关于Sweetpad的信息，请查看以下资源：

Sweetpad网站：具有功能和安装说明的官方Sweetpad网站  
Sweetpad指南：涵盖配置、使用和高级功能的综合指南 