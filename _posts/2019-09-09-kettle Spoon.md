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

     设置数据库连接和导出的sql。

     ![1568000016640](/assets/blogimg/sjklj.png)

   * 连接

     按shift连接输入输出

     ![lianjie](/assets/blogimg/kettlelj.png)

   * 插入/更新

     设置数据库连接及目标表、设置查询字段及更新字段。

     ![iu](/assets/blogimg/kettleiu.png)

     如果只是导出，选择“不执行任何更新”，这样异常重新开始会快一些。

   * 最后点击开始即可。

   # 3. 表数据导出excel

   ![lj1](/assets/blogimg/kettlelj1.png)

   * 表输入中设置数据库连接和导出的sql。

   * shift连接

   * excel设置

     ![excel](/assets/blogimg/kettleexcel.png)

     需要注意的就是excel版本的选择，如果数据量太大，可以使用分隔功能，生成多个文件。

     下一步设置导出字段后开始导出即可。

   # 4. 通过文件更新表

   ![lj2](/assets/blogimg/kettlelj2.png)

   * 文本文件输入

     ![wb1](/assets/blogimg/kettleljwbsr.png)

     浏览文件增加到选中文件中。

     ![wb2](/assets/blogimg/kettleljwbsr1.png)

     设置文本字段分隔符及编码方式。

     ![wb3](/assets/blogimg/kettleljwbsr2.png)

     获取文本字段。

   * shift连接

   * 更新

     设置数据库连接、更新表名、查询关键字及需要更新的字段。

   # 5. 问题的处理

* 导出文件时内存溢出：调整spoon.bat中的内存大小。
* 导出excel内存溢出：由于数据太多，内存已调整到上限，最后通过excel的分隔数据行功能，导出了多个文件。

