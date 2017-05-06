---
layout: post
title: Eclipse笔记(一)
tags:
- Eclipse
- 笔记
- oneNote整理
categories: 笔记
description: onenote整理
---
###常见问题
**1. the method list(String, Object[]) is ambiguous for the type**

**解决方法** 打开eclipse.ini，在-vmargs后面添加 
`-DtolerateIllegalAmbiguousVarargsInvocation=true`
重启eclipse，clean一下项目,重新编译即可,此问题是eclipse的版本不支持可变函数造成。 

**2. Failed to connect to remote VM. Connection timed out.Timeout occurred while waiting for packet 1479.**

进入Window/Preferences，在Java/Debug中设置DebuggerTimeout的值。

**3. 工作空间崩溃，再打开时看不到项目。**

删除工作空间目录下的.metadata，然后打开eclipse点import->General->existing project to workspace。

**4. 快捷键ctrl+T失效**

关闭Eclipse。
删除 workspace/.metadata/.plugins/org.eclipse.jdt.core/*.index和workspace/.metadata/.plugins/org.eclipse.jdt.core/savedIndexNames.txt。
重启 Eclipse。


**5. 清除svn用户名**

删除eclipse安装目录\configuration\org.eclipse.core.runtime下的.keyring文件。 

**6. jsf不提示自定义标签**

重启eclipse project，右键项目，点击Validate， => The (false) warnings are gone.

###主题安装
[http://eclipse-color-theme.github.com/update](http://eclipse-color-theme.github.com/update)
