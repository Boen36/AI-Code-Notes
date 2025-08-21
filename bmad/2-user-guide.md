# User Guide

## The BMad Plan and Execute Workflow

首先，这是针对 Greenfield 项目的规划和执行工作流。Greenfield 在软件领域特指全新的没有历史包袱的项目，对应的 brownfield 项目指的是老旧的有历史包袱的项目。处理Brownfield 项目原理很相似，但还是建议先理解并实践一遍 Greenfield，再去应对更复杂的 Brownfield。BMad Method 需要安装在项目根目录。在规划阶段，使用思考能力更强的模型和更大的上下文窗口，同时把智能体当作真正的合作伙伴，才能获得更好的结果。

### The Planning Workflow

在正式开发前，BMad 会遵循一套结构化的规划流程，为了节省成本，这一步可以在 Web UI 中完成。

```mermaid
graph TD
  A[Start: Project Idea] --> B{可选:分析师调研}
  B --> |Yes| C["分析师:头脑风暴(可选)"]
  B --> |No| G["是否有项目简报？"]
  C --> C2["分析师:市场调研(可选)"]
  C2 --> C3["分析师:竞争对手分析(可选)"]
  C3 --> D["分析师:生成项目简报"]
  D --> G
  G --> |Yes| E["PM:根据简报生成PRD
                  (Fast Track)
                  不再进行二次调研
                  使用预置的模板直接生成"]
  G --> |No| E2["PM:交互式生成PRD<br/>通过来回问答迭代"]
  E --> F["包含 FRs,NFRs,Epics
            和Stories的PRD
            (functional requirements)
            功能性需求定义做什么
            (non functional requirements)
            非功能性需求定义得做多好
            (Epics)
            大体量的业务模块
            一个Epic类似小说的章节
            一个Epic里有很多的Story
            无数的Story构成了一部史诗
            "]
  E2 --> F
  F --> F2{"是否需要UX"}
  F2 --> |Yes| F3["UX专家:生成前端规格说明书
                    页面/组件结构
                    交互流程
                    响应式断点适配方案
                    Design token"]
  F2 --> |No| H["架构师:根据PRD设计架构"]
  F3 --> F4["UX专家:生成AI提示词
              (可选)"]
  F4 --> H2["架构师:设计系统架构
              (根据PRD和UX Spec)"]
  H --> Q{"早期测试策略(可选)
            (正式编码前对高风险
            区域设计早期测试策略)
            (识别容易出错和影响最大的
            模块)
            (提前设计测试思路，数据，
            自动化策略)"}
  H2 --> Q
  Q --> |Yes| R["QA:早期测试架构
                  针对高风险区域
                  可能炸的坑提前标出来"]
  Q --> |No| I
  R --> I["PO:清单检查"]
  I --> J{"所有文档是否已对齐？"}
  J --> |Yes| K["规划阶段完成"]
  J --> |No| L["PO: 更新Epics和Stories"]
  L --> M["根据需要更新PRD和架构"]
  M --> I
  K --> N["切换到IDE"]
  N --> O["PO:对大文档切片"]
  O --> P["接下来准备对接SM和Dev
            Scrum Master"]

```
