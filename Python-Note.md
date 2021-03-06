## 基础

* 以#开头的语句是注释

* 其他每一行都是一个语句，当语句以冒号:结尾时，缩进的语句视为代码块。

* 4个空格的缩进。

* 在Python中，能够直接处理的数据类型有以下几种：整数，浮点数，字符串

* 整数和浮点数在计算机内部存储的方式是不同的，整数运算永远是精确的（除法难道也是精确的？是的！），而浮点数运算则可能会有四舍五入的误差。

* 如果'本身也是一个字符，那就可以用""括起来，如果字符串内部既包含'又包含"可以用转义字符\来标识，比如：'I\'m \"OK\"!'

* Python还允许用r''表示''内部的字符串默认不转义

* 如果字符串内部有很多换行，为了简化，Python允许用'''...'''的格式表示多行内容print('''line1... line2... line3''')

* 布尔值可以用and、or和not运算

* 事实上常量仍然是一个变量，Python根本没有任何机制保证常量不会被改变

* 整数的除法为什么也是精确的，/除法计算结果是浮点数，即使是两个整数恰好整除，结果也是浮点数，//，称为地板除，整数的地板除//永远是整数，即使除不尽，//除法只取结果的整数部分

* Python的整数没有大小限制，Python的浮点数也没有大小限制，但是超出一定范围就直接表示为inf（无限大）。

* 一个字节能表示的最大的整数就是255（二进制11111111=十进制255），两个字节可以表示的最大整数是65535

* 比如大写字母A的编码是65，小写字母a的编码是97

* Unicode用2个字节表示一个字符，为了节约空间，出现了把Unicode编码转化为“可变长编码”的UTF-8编码。UTF-8编码把一个Unicode字符根据不同的数字大小编码成1-6个字节，常用的英文字母被编码成1个字节，汉字通常是3个字节，只有很生僻的字符才会被编码成4-6个字节。如果你要传输的文本包含大量英文字符，用UTF-8编码就能节省空间

* 在计算机内存中，统一使用Unicode编码，当需要保存到硬盘或者需要传输的时候，就转换为UTF-8编码。浏览网页的时候，服务器会把动态生成的Unicode内容转换为UTF-8再传输到浏览器

* 最新的Python 3版本中，字符串是以Unicode编码的，也就是说，Python的字符串支持多语言

* 对于单个字符的编码，Python提供了ord()函数获取字符的整数表示，chr()函数把编码转换为对应的字符

* *#!/usr/bin/env python3*

  *# -\*- coding: utf-8 -*-*

  第一行注释是为了告诉Linux/OS X系统，这是一个Python可执行程序，Windows系统会忽略这个注释；

  第二行注释是为了告诉Python解释器，按照UTF-8编码读取源代码，否则，你在源代码中写的中文输出可能会有乱码。

* 如果要取最后一个元素，除了计算索引位置外，还可以用-1做索引，直接获取最后一个元素，以此类推，可以获取倒数第2个、倒数第3个.......但是耶不能越界。

* list里面的元素的数据类型可以不同

* tuple一种有序列表叫元组。tuple和list非常类似，但是tuple一旦初始化就不能修改，list是可变的

* 如果要定义一个空的tuple，可以写成()，但是，要定义一个只有1个元素的tuple，如果你这么定义：t = (1)

  定义的不是tuple，是1这个数！这是因为括号()既可以表示tuple，又可以表示数学公式中的小括号，因此，Python规定，这种情况下，按小括号进行计算，计算结果自然是1。

  ​

