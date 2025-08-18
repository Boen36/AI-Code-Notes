## Plan Mode

`claude -p "review this code" --permission-mode plan`

只查看不修改的模式

## 自定义系统提示词

system prompt 系统提示词，用来定义agent的角色，专业知识和行为，相当于定义一个人的职业角色

`claude -p "API is down" --append-system-prompt "you are an SRE expert"`

## MCP

`mcp__<serverName>__<toolName>` 表明可以使用mcp服务器上的哪些工具
`mcp__<serverName>`可以使用所有工具