# Specs

## What are Specs

Specs 是 Specifications 的简称，一般被翻译为规格。规格我们比较熟悉的是商城中商品的规格，有颜色，大小，你会发现这些都是用来描述商品的具体信息的。在软件开发领域，我有一个需求，这个需求具体是什么样的，这个就是需求的规格，它更具体，更可执行。最终目的是通过结构化的文档，将大任务拆分为具体的小规格，帮助我们标准化开发一个复杂的需求。借助它我们可以将一个高度抽象的想法，转化为可追踪可追责可执行的具体的计划

因此以Kiro的Specs为核心，我们可以：

1. 拆分需求，将它转化为有明确验收标准的用户故事
2. 构建设计文档，包括核心流程和架构设计
3. 离散且清晰的任务划分，并且可以对任务的执行进行跟踪
4. 团队之间可以通过Specs进行有效地沟通交流

整体的流程为 Requirements -> Design -> Implementation

## Concepts

需求概念和具体实现在以往的AI编程中存在巨大的鸿沟，Specs填补了这个鸿沟，保证了它们之间的一致性并且减少了实现所需要的迭代次数

Kiro 为 Specs 生成了三个关键的文件，来构成 Specs 的基础：

- requirements.md

  使用结构化的 EARS (Easy Approach to Requirements Syntax) 记录用户故事和具体的验收标准

- design.md

  用文档记录了技术架构，序列图，和实现时的注意事项

- tasks.md

  提供了详细的实现计划，由单一的可追踪的任务组成

总的来说，构成 Specs 的三个文件，越来越细化，越来越可执行

### Workflow

具体的工作流遵循逻辑顺序，按序经历这些阶段 Requirements，Design，Implementation Planning，Execution。在进入下一个阶段前都要确保当前阶段已经被很好的完成了

- Requirements Phase 需求阶段 使用结构化的 EARS 记录用户故事和具体的验收标准
- Design Phase 设计阶段 使用文档记录技术架构，序列图以及实现的注意细节
- Implementation Planning 实施计划阶段，将工作拆分为可追踪的原子任务，并且提供清晰的描述和结果
- Execution Phase 执行阶段，跟踪任务完成的进度，并根据需要更新和完善Specs


> 每个阶段完成的质量越高，下个阶段的质量相对来说也会更好。实际的开发中，我们经常遇到需求的调整，这时就需要重复这几个阶段。工程的规范化程序与实际的产品质量高度相关，因此有一个规范的工作流程是非常有必要的

### Requirements

`requirements.md`文件中使用 ESRS（Easy Approach to Requirements Syntax）格式记录的带有明确验收标准的用户故事

在 Kiro 中，每个需求描述都遵循以下的格式：

```
WHEN [condition/event]
THE SYSTEM SHALL [expected behaviour]
```

这样的格式明确清晰且易于理解，易于测试追踪，并且鼓励你思考所有的条件和行为

### Design

`design.md`中记录了技术实现，序列图，以及实现所需要注意的地方。描述了系统运作的全景，以及组件之间的交互方式

### Implementation Plan

将需求拆分为可追踪的原子任务，并且进行详细的计划，每个任务清晰无疑义，且有清晰的验收标准。任务完成后，会自动同步该任务的状态

### Best Practices

1. 如何迭代 Specs

Kiro 的 Specs 支持不断完善和迭代，更新每个阶段的文档，都会自动同步关联的信息，并且每个具体的文档都有单独的更新功能

2. 如果使用Kiro继续原有的项目

让 Kiro 自动识别代码库，并标记已完成的任务

3. 不同的功能对应不同的 Specs，功能之间要清晰且解藕