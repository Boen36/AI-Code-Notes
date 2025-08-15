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

所谓的状态是指在服务器中存储的上下文，服务器为了完成当前请求，需要依赖先前请求的上下文。这样的架构不够灵活，无法方便地横向拓展。

REST请求又有什么好处?

REST 强调的无状态指的是，多次请求之间没有相关联的状态，服务器的角色就像一个函数，不存储任何状态，只处理输入输出。这样服务器就可以很好的进行横向拓展

如何理解Session?

Session用于标记一次对话，用户首次登陆时，输入用户名和密码，服务端根据用户名和密码生成一个sessionId传回给客户端，客户端往后的请求都必须携带这个sessionId，sessionId背后的用户信息，存储于服务器的内存中，后续请求时，根据sessionId获取用户身份，然后进行与用户身份有关的处理逻辑。在这个过程中，服务器存储的状态是“用户身份”，如果此时需要进行横向拓展，则两台服务中都得保持相同的状态信息，否则，对于同一个客户端的多次请求都只能在同一台服务器中完成。session就像一把钥匙，需要使用这把钥匙，去对应的服务器中获取相关的数据，而现在，REST 的请求是无状态的，所有信息都存在于该请求的参数中，任何一台服务器都可以像处理函数一样，处理这个请求，可以很好地进行横向拓展

需要在 API Standards 中定义REST的规范，错误的返回形式，验权的流程，如何处理API的不同版本

2. Testing Approach testing-standards.md

定义单元测试的模式，集成测试的策略，模拟策略以及预期的测试覆盖率

3. Code Style code-conventions.md

4. Security Guidelines security-policies.md

5. deployment process deployment-workflow.md