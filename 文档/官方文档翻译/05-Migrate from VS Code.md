# 从VS Code迁移

基于VS Code的编辑器，具有AI功能，支持扩展导入和自定义配置

Cursor是VS Code的一个分支。这使我们能够专注于打造最佳的AI驱动编码体验，同时提供熟悉的文本编辑体验。

## 导入扩展、主题、设置和键绑定

您可以一键将VS Code配置导入到Cursor中。导航至`Cursor设置` > `通用` > `账户`。

## 保持更新

我们定期将Cursor重新基于最新版本的VS Code。

## 为什么不做成扩展？

作为独立应用程序，Cursor对编辑器的UI有更多控制权，实现更深入的AI集成。我们的一些功能，如Cursor Tab和CMD-K，无法作为现有编码环境的插件实现。

## 设置

您可以通过点击右上角的齿轮按钮、按下`Ctrl/⌘ + Shift + J`或使用`Ctrl/⌘ + Shift + P`并输入`Cursor Settings`来打开Cursor特定的设置面板。

您可以通过`Ctrl/⌘ + Shift + P`，然后输入`VS Code Settings`来打开VS Code特定的设置。

## 为什么Cursor的活动栏是水平的？

活动栏默认为水平方向，以便为聊天节省空间。如果您更喜欢普通的垂直活动栏，可以进入VS Code设置并将`workbench.activityBar.orientation`设置为`vertical`，然后重启Cursor。 