

● 由于技能数量非常庞大，我将所有 Skill 按照功能领域进行分类整理，以便你快速检索。

  🛠️ 系统配置与环境 (System & Config)

  - update-config: 配置 Claude Code 运行环境 (settings.json)。
  - harness-audit: 审计当前 Claude Code 的运行配置。
  - sessions / save-session / resume-session: 管理、保存和恢复会话状态。
  - pm2: 初始化 PM2 进程管理。
  - hookify / hookify-rules / hookify-list / hookify-help: 创建和管理自动化钩子 (Hooks)。

  📋 项目规划与管理 (Planning & Management)

  - prp-prd: 交互式生成 PRD (产品需求文档)。
  - prp-plan / plan: 构建详细的实现计划并评估风险。
  - prp-implement: 根据既定计划执行具体实现。
  - prp-commit / prp-pr: 快速提交代码及创建 GitHub PR。
  - projects: 查看已知项目及其关联的 Instincts。
  - jira: 检索和分析 Jira 任务单。

  🔍 代码质量与安全 (Quality & Security)

  - code-review / simplify: 审查代码质量、可读性并进行简化重构。
  - quality-gate: 执行质量门禁检查。
  - tdd / test-coverage: 实施 TDD 工作流并检查测试覆盖率。
  - ai-regression-testing: 针对 AI 生成代码的回归测试策略。
  - refactor-clean: 识别并清理冗余/死代码。
  - agent-introspection-debugging: 结构化自调试工作流。

  📚 语言与框架专家 (Language Specializations)

  通用标准：coding-standards (跨项目通用标准)。

  - Python: python-review (代码审查), python-patterns (惯用法)。
  - Rust: rust-reviewer (所有权/生命周期), rust-build (构建修复)。
  - Go: go-reviewer (并发/错误处理), go-build (构建修复), golang-patterns (惯用法)。
  - Java/Kotlin: java-coding-standards, kotlin-patterns, kotlin-review, kotlin-build (构建修复)。
  - C++/C#: cpp-coding-standards, cpp-review, cpp-build, dotnet-patterns。
  - Web/Frontend: frontend-design (UI/UX), frontend-patterns (架构), mcp-server-patterns (MCP 服务)。
  - Frameworks: django-patterns, nestjs-patterns, laravel-patterns 等。

  🧠 增强学习与 AI 进化 (Learning & AI Evolution)

  - Instincts (本能系统):
    - learn / continuous-learning: 从代码/对话中提取可复用模式。
    - instinct-status / instinct-import / instinct-export: 管理学习到的本能知识。
    - promote: 将项目级本能提升为全局本能。
    - evolve: 分析并优化现有本能。
  - Advanced AI:
    - gan-design / gan-build: GAN 闭环开发流 (规划 $\rightarrow$ 生成 $\rightarrow$ 评估)。
    - multi-workflow / multi-plan / multi-execute: 多模型协同工作流。
    - council: 召集多角色委员会进行多维度审查。

  📖 文档与知识库 (Docs & Knowledge)

  - update-docs: 更新项目文档。
  - update-codemaps: 更新代码地图 (Codemaps)。
  - code-tour: 创建交互式代码导览 (.tour 文件)。
  - skill-create: 从 Git 历史中自动提取并创建新 Skill。
  - skill-health: 查看 Skill 库的健康度和覆盖情况。

  ⚡ 实用工具 (Utilities)

  - loop / loop-start / loop-status: 设定定时/循环执行任务。
  - aside: 在主任务之外快速回答侧边问题。
  - checkpoint: 为当前工作状态创建检查点。

  💡 使用提示：
  如果你不确定使用哪个，可以直接告诉我你的最终目标（例如：“我想优化这段代码的性能”），我会自动选择最合适的 Skill
  或工作流来帮你完成。