# Java

几分钟内从JetBrains IDEs迁移到Cursor

本指南将帮助您为Java开发配置Cursor，包括设置JDK、安装必要的扩展、调试、运行Java应用程序以及集成Maven和Gradle等构建工具。它还涵盖了类似于IntelliJ或VS Code的工作流程功能。

在开始之前，请确保您已安装Cursor并更新到最新版本。

## 为Cursor设置Java

### Java安装

在设置Cursor本身之前，您需要在机器上安装Java。

Cursor不附带Java编译器，因此如果您尚未安装JDK，则需要安装一个。

## Windows安装

下载并安装JDK（例如OpenJDK、Oracle JDK、Microsoft Build of OpenJDK）。  
设置JAVA_HOME并将JAVA_HOME\bin添加到PATH中。

## macOS安装

通过Homebrew（`brew install openjdk`）安装或下载安装程序。  
确保JAVA_HOME指向已安装的JDK。

## Linux安装

使用您的包管理器（`sudo apt install openjdk-17-jdk`或等效命令）或通过SDKMAN安装。

要检查安装，请运行：

```bash
java -version
javac -version
```

如果Cursor未检测到您的JDK，请在settings.json中手动配置：

```json
{
  "java.jdt.ls.java.home": "/path/to/jdk",
  "java.configuration.runtimes": [
    {
      "name": "JavaSE-17",
      "path": "/path/to/jdk-17",
      "default": true
    }
  ]
}
```

重启Cursor以应用更改。

### Cursor设置

Cursor支持VS Code扩展。手动安装以下扩展：

Extension Pack for Java：包括Java语言支持、调试器、测试运行器、Maven支持和项目管理器  
Gradle for Java：使用Gradle构建系统的必备工具  
Spring Boot Extension Pack：Spring Boot开发所需  
JavaFX Support：JavaFX应用程序开发必需

### 配置构建工具

#### Maven

确保已安装Maven（`mvn -version`）。如果需要，从maven.apache.org安装：

1. 下载二进制存档
2. 解压到所需位置
3. 将MAVEN_HOME环境变量设置为解压文件夹
4. 将%MAVEN_HOME%\bin（Windows）或$MAVEN_HOME/bin（Unix）添加到PATH

#### Gradle

确保已安装Gradle（`gradle -version`）。如果需要，从gradle.org安装：

1. 下载二进制分发版
2. 解压到所需位置
3. 将GRADLE_HOME环境变量设置为解压文件夹
4. 将%GRADLE_HOME%\bin（Windows）或$GRADLE_HOME/bin（Unix）添加到PATH

或者，使用Gradle Wrapper，它将自动下载并使用正确的Gradle版本。

## 运行和调试

现在您已完成所有设置，是时候运行和调试您的Java代码了。根据您的需求，您可以使用以下方法：

## 运行

点击任何main方法上方出现的"Run"链接，快速执行您的程序

## 调试

打开"运行和调试"侧边栏面板，使用"运行"按钮启动您的应用程序

## 终端

使用Maven或Gradle命令从命令行执行

## Spring Boot

直接从Spring Boot Dashboard扩展启动Spring Boot应用程序

## Java x Cursor工作流程

Cursor的AI驱动功能可以显著增强您的Java开发工作流程。以下是一些专门针对Java利用Cursor功能的方法：

## Tab补全

为方法、签名和Java样板代码（如getter/setter）提供智能补全。

## Agent模式

实现设计模式、重构代码或生成具有适当继承关系的类。

## Cmd-K

快速内联编辑方法、修复错误或生成单元测试，而不中断工作流程。

## 聊天

获取Java概念帮助、调试异常或了解框架功能。

### 示例工作流程

1. **生成Java样板代码**  
   使用Tab补全快速生成构造函数、getter/setter、equals/hashCode方法和其他重复的Java模式。
2. **调试复杂的Java异常**  
   当面对晦涩的Java堆栈跟踪时，突出显示它并使用Ask来解释根本原因并建议潜在的修复方法。
3. **重构遗留Java代码**  
   使用Agent模式现代化旧的Java代码 - 将匿名类转换为lambda表达式，升级到更新的Java语言功能，或实现设计模式。
4. **框架开发**  
   使用@docs将您的文档添加到Cursor的上下文中，并在整个Cursor中生成特定于框架的代码。 