# 从VS Code迁移

几分钟内从VS Code迁移到Cursor

Cursor基于VS Code代码库构建，这使我们能够专注于打造最佳的AI驱动编码体验，同时保持熟悉的编辑环境。这使得将您现有的VS Code设置迁移到Cursor变得非常容易。

## 配置文件迁移

### 一键导入

以下是如何一键获取您的整个VS Code设置：

1. 打开Cursor设置（⌘/Ctrl + Shift + J）
2. 导航至General > Account（通用 > 账户）
3. 在"VS Code Import"（VS Code导入）下，点击Import（导入）按钮

这将传输您的：

* 扩展
* 主题
* 设置
* 键绑定

### 手动配置文件迁移

如果您在不同机器之间迁移，或者想要更多地控制您的设置，您可以手动迁移您的配置文件。

#### 导出配置文件

1. 在您的VS Code实例中，打开命令面板（⌘/Ctrl + Shift + P）
2. 搜索"Preferences: Open Profiles (UI)"（首选项：打开配置文件（UI））
3. 在左侧边栏找到您想要导出的配置文件
4. 点击3点菜单并选择"Export Profile"（导出配置文件）
5. 选择将其导出到本地机器或GitHub Gist

#### 导入配置文件

1. 在您的Cursor实例中，打开命令面板（⌘/Ctrl + Shift + P）
2. 搜索"Preferences: Open Profiles (UI)"（首选项：打开配置文件（UI））
3. 点击'New Profile'（新建配置文件）旁边的下拉菜单，然后点击'Import Profile'（导入配置文件）
4. 粘贴GitHub Gist的URL或选择'Select File'（选择文件）上传本地文件
5. 点击对话框底部的'Import'（导入）以保存配置文件
6. 最后，在侧边栏中选择新配置文件，并点击勾选图标激活它

## 设置和界面

### 设置菜单

#### Cursor设置

通过命令面板（⌘/Ctrl + Shift + P）访问，然后输入"Cursor Settings"（Cursor设置）

#### VS Code设置

通过命令面板（⌘/Ctrl + Shift + P）访问，然后输入"Preferences: Open Settings (UI)"（首选项：打开设置（UI））

### 版本更新

我们定期将Cursor重新基于最新的VS Code版本，以保持与功能和修复的同步。为了确保稳定性，Cursor通常使用稍旧的VS Code版本。

### 活动栏方向

我们将其设为水平方向以优化AI聊天界面的空间。如果您更喜欢垂直方向：

1. 打开命令面板（⌘/Ctrl + Shift + P）
2. 搜索"Preferences: Open Settings (UI)"（首选项：打开设置（UI））
3. 搜索`workbench.activityBar.orientation`
4. 将值设置为`vertical`（垂直）
5. 重启Cursor

## 保持更新

我们定期将Cursor重新基于最新版本的VS Code。

## 为什么不做成扩展？

作为独立应用程序，Cursor对编辑器的UI有更多控制权，实现更深入的AI集成。我们的一些功能，如Cursor Tab和CMD-K，无法作为现有编码环境的插件实现。

## 为什么Cursor的活动栏是水平的？

活动栏默认为水平方向，以便为聊天节省空间。如果您更喜欢普通的垂直活动栏，可以进入VS Code设置并将`workbench.activityBar.orientation`设置为`vertical`，然后重启Cursor。 