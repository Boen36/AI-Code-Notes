# Kiro简介

Kiro是一款由AI智能体驱动的IDE（agentic IDE），帮你实现从原型到产品的完整服务。相比于cursor，它具有更标准的工程化流程。以各类标准的产品文档组成工程流程的核心，包括产品需求文档，设计文档，开发文档，官方称其为`sepc-driven`规格驱动开发。它还有agent-hooks功能，可以在智能体执行完文件操作之后，执行一系列hooks，例如完善文档，添加单元测试，让整个流程更加规范完整

## 核心能力

- Specs

使用结构化的规范文档定义与规划功能，将需求分解为详细的实施计划

- Hooks

在文件变动或者发生特定的开发事件（development event，例如 git 提交）时，agent会智能地触发对应的hooks，hooks中包括可重复执行的任务或逻辑

- Agentic Chat

kiro 了解项目的上下文，并让你通过自然语言实现需求，它会将自然语言的需求转化为详细的实施计划

- Steering 掌舵

可以通过自定义规则和项目特定的上下文来指导kiro的行为

- MCP Servers

通过 MCP 连接外部工具和数据源

- Privacy First

通过企业级安全和隐私保护你的代码资产
