# json解析 环境准备

- [json解析 环境准备](#json解析-环境准备)
  - [内容](#内容)
  - [什么是Json](#什么是json)
  - [编译环境搭建](#编译环境搭建)

## 内容

- json是什么

- 搭建编译环境

- 头文件与API设计

- JSON语法子集

- 单元测试

- 宏的编写技巧

- 实现解析器

- 关于断言

- 总结和练习

## 什么是Json

- JSON(javascript Object Notation): 是一个用于数据交换的文本格式, 现在的标准为ECMA-404

- json源于JavaScript, 但只是一种数据格式, 可以用于任何编程语言

- json实例

    ```json
    {
        "name": "lcwspr",
        "old": 18
    }
    ```

- 可知, json是一个树状结构, 并且json只包含6种数据类型

    1. `null`: 表示null

    2. `boolean`: 表示true或false

    3. `number`: 一般的浮点数表示方式

    4. `string`: 表示为"xxx"

    5. `array`: 表示为`[]`

    6. `object`: 表示为`{}`

- 我们如果要实现json解析库, 需要完成3个需求

    1. 把json文本解析为一个树状数据结构(parse)

    2. 提供一个接口访问该数据结构(access)

    3. 把数据结构转换为JSON文本(stringify)

## 编译环境搭建

- json库介绍: 文件介绍

    1. `leptjson.h`: 头文件, 包含对外的类型和API函数声明

    2. `leptjson.c`: 实现文件(implementation file), 包含内部的类型声明和函数实现文件

    3. `test.c`: 使用`test driven development, TDD`: 包含测试程序