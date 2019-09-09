---
layout: post
title: kettle spoon数据统计及导出
tags:
- kettle spoon
- 数据处理
categories: 笔记
description: 
typora-root-url: ..
---
# 1. 配置

环境变量设置：

* KETTLE_HOME：D:\setup\pdi-ce-8.2.0.0-342\data-integration
* PENTAHO_JAVA_HOME：D:\Program Files\Java\jdk1.8.0_25（如默认jdk为1.8，可以不增加此项）

内存设置：打开D:\setup\pdi-ce-8.2.0.0-342\data-integration\spoon.bat

* if "%PENTAHO_DI_JAVA_OPTIONS%"=="" set PENTAHO_DI_JAVA_OPTIONS="-Xms4096m" "-Xmx8192m" "-XX:MaxPermSize=256m"



# 2. 导出数据到表

1. 新增转换 表输入>插入/更新

   * 表输入

     设置数据库连接

     ![1568000016640](/assets/blogimg/sjklj.png)

   * 连接

   * 插入/更新

   