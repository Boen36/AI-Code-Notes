# Steering

定义通用的规则和标准，并带来了以下好处：

- 使用既定的模式和约定生成一致风格的代码
- 不用在每次对话中，重复解释项目的标准和规则
- 团队开发采用一致的标准
- 从实际项目开发经验中，不断总结有用的标准和规则，并以Steering的形式沉淀下来

Steering 由以下关键文档组成：

- `product.md` Product Overview

产品最基础的背景信息，该产品主要解决什么问题，目标用户是谁，关键功能有哪些，商业目标是怎样的

- `tech.md` Technology Stack

选择什么技术栈，开发工具

- `structure.md` Project Structure

项目结构，命名约定，结构决策

这些文件包含在每次交互中，是该项目的基石，为Kiro整体定调

## Inclusion Modes

可以对Kiro如何使用Steering files进行设置，默认一直包含，也可以选择根据条件使用，或者手动调用

## Best Practice

- One domain per file

  API design，testing，deployment procedures

- use clear names

  `api-rest-conventions.md`
  `testing-unit-patterns.md`

- include context

  包含为什么要这么做，不仅仅提供要遵守的规则，可以让Kiro更懂你的意图

- 对于一些比较难描述的，可以提供代码片段

## Common Steering File Strategies

1. API Standards

REST (Representational State Transfer) 表述状态如何进行转移，它的核心思想是互联网上的所有资源都通过URL表示，通过HTTP动词（GET/POST/PUT/DELETE）去操作这些资源

REST 倡导无状态，每个请求自带全部信息，通过HTTP状态码表示结果

用一个例子来解释无状态和有状态，无状态就像自助售货机，售货机在不认识你的情况下完成交易。有状态就像你去银行取钱，需要你提供身份证明

传统的有状态的请求有什么坏处？

REST请求又有什么好处?