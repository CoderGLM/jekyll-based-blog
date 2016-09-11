---
layout: post
title: 总结vim的使用方法
date: 2016.09.08 10:17.000000000 +09:00
category: 工具
description: 是时候总结vim的用法了
tags: exvim;vim;使用;方法;终极;总结;入门;
---

> 是时候总结一下vim的使用方法了，一方面防止自己忘记不常用的指令，另一方面给大家提供一个参考。
> 等有时间再把文中的链接内容展开介绍。

![vim键盘图]({{site.imageurl}}/assets/images/2016/how-to-use-vim1.png)

## vim的安装

[exvim中文](http://exvim.github.io/docs-zh/)这里面包含了exvim的安装与配置，以及插件的安装。

## vim指令入门

[Vim入门教程](http://blog.jobbole.com/86132/)这篇文件是我**强烈推荐**的，入门必备，告诉你如何使用指令，
如何**人类的语言**来使用指令。

## 高频组合指令

单指令是必须记住的，这里提几个组合指令。<br/>

- **:9y**: 拷贝第9行，不必首先移动光标;
- **ggvG**: 全选文件内容，不过我比较喜欢<ctrl + a>
- **gg=G**: 格式化文件
- **ciw**: 修改光标所在单词
- **vip**: 选取当前光标所在段落
- **<<**: 左缩进
- **>>**: 右缩进
- **:bn**: 切换缓冲区（即编辑窗口） 
- **:bp**: 切换缓冲区
- **mx**: 添加（移除）x标签
- **`x**: 跳转到标签x
- **:marks**: 查看所有标签
- **delm x**: 删除标签x
- **:ls**: 查看缓冲区
- **:bN**: 打开缓冲区No
- **:shell/:sh**: 执行shell命令

## 常用功能

### 如何查找js函数定义

1. 安装etags插件，如果不知道如何安装，请谷度或者百歌；
2. 在项目根目录执行etags -R；
3. 将光标置于某函数上，按ctrl+]就可跳转到函数定义，ctrl+t可以跳回去；

### 如何全局查找

使用命令：GS: <your-word>，如果提示lid: can't locate 'ID': No such file or directory，
说明ID索引文件没有生成，在你的macvim执行:Update(注意大小写)，会更新你的工程，
看看里面是不是却少安装gawk，如果是，请参考[这里](http://macappstore.org/gawk/)

### 如何快速注释js

1. 选中待注释的代码块（用鼠标或v）；
2. 按下ctrl＋v，进入块选择模式；
3. 输入大写i，进入插入模式；
4. 输入//，然后esc，搞定。

### 提高html编码效率的zen-coding

什么是Zen-Coding?自行百度吧。[插件在这里](https://github.com/mattn/emmet-vim)
有一点要说明，就是插件装完了输入html:5然后按快捷键 <Ctrl+y+,>居然不展开，最后发现需要把当前文件先保存成html格式才行，
估计是这个插件对当前文件类型有检查。

## 参考
[exvim中文](http://exvim.github.io/docs-zh/)
[Vim入门教程](http://blog.jobbole.com/86132/)