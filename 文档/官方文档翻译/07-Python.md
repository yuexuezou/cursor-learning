# Python

本指南将帮助您在Cursor中设置完美的Python开发环境

本指南的灵感来源于Jack Fields关于在VS Code中设置Python开发环境的文章。更多详情请查看他的文章。

## 前提条件

在开始之前，请确保您已安装：

* Python（推荐3.8或更高版本）
* Git用于版本控制
* Cursor已安装并更新至最新版本

## 必备扩展

### 核心Python支持

以下扩展可以使Cursor完全支持Python开发。这些扩展提供语法高亮、代码检查、调试和单元测试功能。

* **Python**：来自Microsoft的核心语言支持
* **Pylance**：快速Python语言服务器
* **Python Debugger**：增强的调试功能
* **Python Test Explorer**：可视化测试界面

### 代码质量工具

* **Python Docstring Generator**：自动文档生成
* **Python Path**：管理Python路径
* **Python Environment Manager**：虚拟环境管理
* **Python Snippets**：Python代码片段

### 高级Python工具

除了上述扩展外，我们还添加了一些额外的扩展，可以帮助您充分利用Python开发。

#### `uv` - Python环境管理器

uv是一个现代Python包管理器，可用于创建和管理虚拟环境，并可替代pip作为默认包管理器。

要安装uv，请在终端中运行以下命令：

```bash
pip install uv
```

#### `ruff` - Python代码检查和格式化工具

Ruff是一个现代Python代码检查和格式化工具，可用于检查编程错误、帮助执行编码标准，并可以建议重构。它可以与Black一起用于代码格式化。

要安装Ruff，请在终端中运行以下命令：

```bash
pip install ruff
```

## Cursor配置

### 1. Python解释器

在Cursor中配置您的Python解释器：

1. 打开命令面板（Cmd/Ctrl + Shift + P）
2. 搜索"Python: Select Interpreter"
3. 选择您的Python解释器（如果您使用虚拟环境，则选择相应的虚拟环境）

### 2. 代码格式化

使用Black设置自动代码格式化：

Black是一个代码格式化工具，可以自动将您的代码格式化为一致的风格。它不需要任何配置，在Python社区中被广泛采用。

要安装Black，请在终端中运行以下命令：

```bash
pip install black
```

然后，通过在`settings.json`文件中添加以下内容，配置Cursor使用Black进行代码格式化：

```json
{
    "python.formatting.provider": "black",
    "editor.formatOnSave": true,
    "python.formatting.blackArgs": [
        "--line-length",
        "88"
    ]
}
```

### 3. 代码检查

我们可以使用PyLint来检查编程错误、帮助执行编码标准，并可以建议重构。

要安装PyLint，请在终端中运行以下命令：

```bash
pip install pylint
```

在`settings.json`中添加以下配置：

```json
{
    "python.linting.enabled": true,
    "python.linting.pylintEnabled": true,
    "python.linting.lintOnSave": true
}
```

### 4. 类型检查

除了代码检查外，我们还可以使用MyPy来检查类型错误。

要安装MyPy，请在终端中运行以下命令：

```bash
pip install mypy
```

在`settings.json`中添加以下配置：

```json
{
    "python.linting.mypyEnabled": true
}
```

## 调试

Cursor为Python提供强大的调试功能：

1. 通过点击装订线设置断点
2. 使用调试面板（Cmd/Ctrl + Shift + D）
3. 配置`launch.json`以自定义调试配置

## 推荐功能

* **Tab自动补全**：理解您操作的智能代码建议
* **聊天**：通过自然对话探索和理解代码
* **Agent**：使用AI助手处理复杂的开发任务
* **Context**：从第三方系统拉取上下文
* **自动导入**：在编写代码时自动导入模块
* **AI代码审查**：Cursor使用AI持续审查您的代码

## 框架支持

Cursor与流行的Python框架无缝协作：

* **Web框架**：Django, Flask, FastAPI
* **数据科学**：Jupyter, NumPy, Pandas
* **机器学习**：TensorFlow, PyTorch, scikit-learn
* **测试**：pytest, unittest
* **API**：requests, aiohttp
* **数据库**：SQLAlchemy, psycopg2 