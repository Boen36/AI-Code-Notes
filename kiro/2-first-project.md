# First Project

通过first-project，体验kiro的核心功能

## set up steering files

首先需要创建steering files，让agent理解整个项目，并且添加特定规则，例如编码规则，团队历史的最佳实践，定好整个项目的大方向

## build features with specs

specs 通过以下几个步骤将高级功能构想转化为详细的实施方案：

- 需求阶段

> user stories with acceptance criteria in EARS notation

根据用户故事，使用EARS模板定义准确的验收标准

Requirements 需求指的是最高层级的"要做什么"

user stories 把需求从用户视角讲成一个故事，便于沟通，格式为 as a 用户角色，I want 功能，so that 价值/原因

acceptance criteria 验收标准，一个需求要被统一的理解，就需要有统一的清晰的验收标准。只有这样，设计，开发，测试人员的目标才能保持一致

EARS notation 一种验收标准的语句模板（Easy Approach to Requirements Syntax）用5种固定句式，把验收标准写出无歧义，可测试的短句

EARS格式可以把任何需求写成结构一致，无歧义，可测试的 EARS 格式

EARS的5中固定句式：

1. Ubiquitous 普适场景通用语句，与任何状态事件无关，只关注系统始终要实现的功能

    ` The<系统>shall<相应>`

2. State-Driven 状态驱动，关键词 While，只要系统处于某种状态，就必须保持的行为

    `While<状态>, the <系统> shall <响应>`

3. Event-Driven 事件驱动，关键词 When，在某一瞬间事件发生时触发一次的行为

    `When <事件>，the <系统> shall <响应>`

4. Optional Feature 可选功能，关键词 Where，仅当产品包含某个可选功能时才生效的需求

    `Where <功能已包含>，the <系统> shall <响应> `

5. Unwanted Behaviour 异常/禁止行为，关键词 if .. then，描述系统必须处理的异常，错误，危险输入，

    `if <异常条件> then the <系统> shall <响应>`

- Design 设计

    设计技术架构和实现方式

- Tasks 任务

    > Discrete，trackable implementation steps

    Discrete 离散的，指的是将一个任务拆分为互不重叠的小任务，每个小任务只解决一个具体单一的问题。
    合起来就是，将一个大的任务拆分为一个个互不重叠，具体单一的，且可追踪的小任务

## execute spec tasks

完成 spec 创建后，会生成 tasks.md 文件，可以手动选择要执行的任务，IDE 会自动标记该任务的状态

## Automate workflows with hooks

根据预定义的行为自动触发hooks，自定义的行为有文件的创建删除修改，手动触发，特定的文件类型被修改
