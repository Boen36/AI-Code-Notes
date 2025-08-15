# Hooks

## Hook Types

1. On File Create

使用场景：

- 为新组建生成样板代码
- 为新文件添加license头
- 创建implementation files时设置测试文件

2. On File Save

- 运行linting和格式化
- 更新文档
- 运行测试

3. On File Delete

- 清理相关文件
- 正确更新import

4. Manual Trigger

## Hook Design

1. 清晰且具体

- 详细明确的命令
- 每个hook专注于一项具体的任务
- 对于复杂的操作，分步骤拆解任务

2. 对新的hook要进行测试

- 在部署新的hook时，使用测试文件进行测试
- 验证hook能否正常处理边界情况
- 从小范围的文件类型开始入手

3. 对hook的性能进行监控

- 确保hook不会拖慢整个工作流
- 需要考虑触发hook的频率，不能过快
- 优化Promp让它更有效率

## Security Consideration

1. Validate Input
2. Limit Scope

- 尽可能地确定hook作用的文件类型或目录
- 使用精确的文件模型来避免不必要的执行
- 考虑hook对整个代码库产生的影响

3. Review Regularly

- 删除无用的hook
- 随着项目发展，hook也要进行对应的调整
- 根据实际使用效果不断地对hook进行优化

## Team Collaboration

1. 对Hooks进行文档管理

- 清晰地说明每个hook的作用
- 可能地举几个实际的例子
- 列出它的使用限制和边界情况

2. 对Hook版本控制

- 对于适用于所有项目的Hook，使用版本控制，多处共享