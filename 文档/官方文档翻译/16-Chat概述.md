# Chat概述

统一的AI界面，结合了询问、编辑和Agent模式，帮助您直接在编辑器中编写、编辑和理解代码

Cursor的统一AI界面将不同的功能结合在一个无缝的体验中。使用`⌘I`打开它，使用`⌘N`创建新对话。通过输入框中的模式选择器切换模式。

## 模式

界面提供三种模式，您可以从模式选择器中选择：

### Agent

访问工具和推理能力，用于复杂任务。默认模式。(⌘I)

### 编辑

精确清晰地对代码进行单次编辑。

### 询问

询问有关代码的问题，获取解释，探索代码库。(⌘L)

您可以在对话过程中使用模式选择器或`⌘.`快捷键切换模式。这种灵活性让您可以根据当前需求进行调整 - 从提问到修改再到使用高级工具。

## 上下文

您可以使用@符号在提示中包含相关上下文。界面将根据您的查询自动建议相关上下文。

### 自动上下文（测试版）

Cursor可以使用嵌入和自定义模型在对话中自动包含相关代码。无需使用@符号手动选择上下文，它会分析您的提示并包含代码库中最相关的代码。在设置 > 功能 > 自动上下文中启用此功能。

## 生成和应用更改

Cursor有一个内部训练的自定义模型，能够接受您使用的AI模型建议的一系列编辑，并在几秒钟内将其应用到包含数千行的文件中。

这在Agent和编辑模式下自动发生。

在询问模式下，您可以通过点击差异视图右下角的`应用`按钮来应用更改。

完成更改后，您可以在代码库中查看它们，然后选择接受或拒绝它们，如果您想进一步迭代。

了解更多关于应用：了解更多关于使用Cursor自定义训练模型应用更改的信息。

## 检查点

每次迭代都会创建一个检查点。您可以通过点击该检查点附近的`检出`返回到任何先前版本。如果您不喜欢当前更改并想恢复到早期状态，这很方便。

## 聊天历史

通过历史记录访问以前的对话。从Cursor Tab右侧的历史图标打开它。您将看到可以重新访问、重命名或删除的过去对话列表。

当界面处于焦点状态时，使用`⌘+⌥+L`或`Ctrl+Alt+L`打开。

## 布局

* **面板**：左侧是界面，右侧是代码编辑器的侧边栏。
* **编辑器**：单个编辑器窗口，类似于正常查看代码。您可以移动它，拆分它，甚至将它放在单独的窗口中。
* **浮动**：可以放置在您喜欢位置的可拖动窗口。

您可以从菜单 > 打开为[布局]更改此设置。

## 迭代代码检查

Cursor让AI直接访问代码库中的代码检查工具，这有助于它检查自己的代码以及项目中的现有代码。

当Cursor检测到已安装的代码检查工具标记的问题时，AI可以智能地尝试自行修复它们，并在需要时迭代更改。

这意味着您将始终得到干净、合规的代码，而无需手动检查和修复任何问题。

某些语言（如Rust）要求保存文件后才会出现代码检查错误，这可能会限制此功能在所有语言中的有效性。

## 常见问题

### 各种模式有什么区别？

**询问模式**帮助您理解和探索代码。使用它来提问、获取解释和了解您的代码库。

**编辑模式**专注于对代码进行单次编辑。它提供了一个工作区，您可以在其中对文件进行精确更改。

**Agent模式**（默认）将两种功能与额外的工具和推理能力结合起来，用于处理复杂任务。

### 如何处理长对话？

对于长对话，Cursor使用较小的模型（如`cursor-small`和`gpt-4o-mini`）总结早期消息，以保持响应快速和相关。

这种方法有助于确保即使是扩展的对话也保持响应性和连贯性，而不会丢失早期交流中的关键细节。

### 我可以在另一台计算机上访问我的对话历史吗？

对话历史存储在您的计算机本地，不存储在Cursor的服务器上，也不与您的Cursor账户关联。

这意味着如果您切换到不同的计算机，您将无法访问以前的历史记录。您只能在最初创建历史记录的计算机上访问您的历史记录。 