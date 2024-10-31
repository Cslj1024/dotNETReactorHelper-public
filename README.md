# dotNETReactorHelp扩展工具使用文档

------

## 1. 工具简介

### 1.1 工具简介

dotNETReactorHelper是一款基于C#开发的VS扩展，主要用于简化对C#项目中.exe文件和.dll文件的混淆操作。

### 1.2 编写目的与项目背景

在日常工作中，为了应对潜在的安全威胁并保护公司的商业机密，开发人员需要采取多种安全措施，确保应用程序的安全性。并且.NET程序容易被反编译，我们为了防止被反编译，所以需要代码混淆。代码混淆是一种常见且有效的安全技术，它能够在不改变原始功能的前提下，使代码变得难以理解和分析，从而提升应用程序的防护能力。

dotNET_Reactor 作为一款广泛使用的 .NET 代码混淆和加密工具，能够有效防止程序被反编译和破解。然而，其在操作过程中需要频繁点击多个按钮和在不同文件夹中选择文件，增加了使用的复杂性，并容易导致错误。

为了解决这些问题，开发了 dotNETReactorHelper 扩展工具，以简化和自动化代码混淆流程，提高工作效率，并减少人为操作失误。 

## 2. 工具环境要求

### 2.1 工具要求

#### 扩展需求

适用于 VS 的 社区版，专业版 ，企业版

#### 软件需求

dotNET_Reactor.exe



## 3. 工具安装与卸载

### 3.1安装dotNETReactorHelper.vsix（如果VS2022无法安装，建议使用或者直接更新到最新版的VS2022）

（1） 退出所有VS（如果不退出VS可能出现以下内容如图）

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\下载扩展工具2.png)



（2）双击dotNETReactorHelper.vsix安装，如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\卸载扩展工具2.png)

（3）把dotNET_Reactor.exe 拷贝到devenv.exe所在目录。如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelp扩展使用说明\dotNET_Reactor目录.png)



（4）安装完成后，VS 工具 菜单中会加入dotNETReactorHelper菜单项。如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\用户文档\Snipaste_2024-10-12_09-18-47.png)

### 3.2 卸载步骤（不用本工具时候步骤）：

（1）  VS -- 扩展 -- 管理扩展。如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelp扩展使用说明\Snipaste_2024-08-28_09-27-53.png)

（2） 在已安装中找到dotNETReactorHelper，选择卸载（点击完卸载后，关闭VS，然后会自动开始卸载）。如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\用户文档\Snipaste_2024-10-12_09-20-57.png)

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\卸载扩展工具2.png)

## 4. 工具使用步骤

### 4.1 待混淆项目设置

解决方案中所有项目生成目录设置到同一目录（因为设置成不同生成目录时，混淆代码在对应目录混淆，拷贝到exe生成目录可能和exe引用过来的没有混淆的dll混乱）如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\用户文档\Snipaste_2024-10-11_17-50-14.png)

### 4.2 工具启动

在 VS 工具 菜单中会有会加入dotNETReactorHelper菜单项，点击即可运行，如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\用户文档\Snipaste_2024-10-12_09-18-47.png)

### 4.3 工具主操作界面介绍

主要由 选择引用的dll路径的窗体 和 VS输出框 组成

#### 选择引用的dll路径的窗体

在此窗体中选择需要混淆的 DLL 文件，如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\扩展工具运行图.png)

#### VS输出框

在VS的输出框中将会展示混淆文件的信息和进程,该扩展会自动识别当前活动的配置是Debug还是Release，如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\用户文档\Snipaste_2024-10-11_14-36-56.png)

### 4.4 工具结束

当在 VS 输出框中出现 **混淆完成！** 时，扩展自动关闭，如下图：

![](C:\Users\jun.luo\Desktop\dotNETReactorHelper\Document\用户文档\Snipaste_2024-10-11_14-37-43.png)
