# Claude Code Skills 技能列表

> **更新时间：** 2026-04-11
> **来源：** Claude Code 内置技能系统

---

## 开发工作流

| 技能 | 简介 |
|------|------|
| `plan` | 需求分析、风险评估、制定实现计划 |
| `build-fix` | 构建失败时自动诊断并修复错误 |
| `refactor-clean` | 清理死代码、重复代码，优化代码结构 |
| `code-review` | 审查本地未提交的代码变更 |
| `verify` / `verification-loop` | 综合验证系统，确保代码质量 |
| `tdd-workflow` | 强制测试驱动开发流程 |
| `feature-dev` | 引导式功能开发流程 |

---

## 编程语言

### Python

| 技能 | 简介 |
|------|------|
| `python-patterns` | Python 设计模式和最佳实践 |
| `python-testing` | pytest 测试策略和模式 |
| `python-review` | Python 代码审查 |

### Go

| 技能 | 简介 |
|------|------|
| `golang-patterns` | Go 语言设计模式和最佳实践 |
| `golang-testing` | Go 测试模式和表驱动测试 |
| `go-review` | Go 代码审查 |
| `go-test` | Go 测试执行 |
| `go-build` | Go 构建错误修复 |

### Rust

| 技能 | 简介 |
|------|------|
| `rust-patterns` | Rust 所有权、生命周期、错误处理模式 |
| `rust-testing` | Rust 单元测试和集成测试 |
| `rust-review` | Rust 代码审查 |
| `rust-test` | Rust 测试执行 |
| `rust-build` | Rust 构建错误修复 |

### Kotlin

| 技能 | 简介 |
|------|------|
| `kotlin-patterns` | Kotlin 设计模式和最佳实践 |
| `kotlin-testing` | Kotlin 测试模式 |
| `kotlin-review` | Kotlin 代码审查 |
| `kotlin-test` | Kotlin 测试执行 |
| `kotlin-build` | Kotlin/Gradle 构建错误修复 |

### Java / Spring Boot

| 技能 | 简介 |
|------|------|
| `java-coding-standards` | Java/Spring Boot 编码标准 |
| `springboot-patterns` | Spring Boot 架构模式 |
| `springboot-tdd` | Spring Boot TDD 工作流 |
| `springboot-verification` | Spring Boot 验证循环 |

### Flutter / Dart

| 技能 | 简介 |
|------|------|
| `dart-flutter-patterns` | Dart/Flutter 生产级模式 |
| `flutter-review` | Flutter 代码审查 |
| `flutter-test` | Flutter 测试执行 |
| `flutter-build` | Flutter 构建错误修复 |

### PHP / Laravel

| 技能 | 简介 |
|------|------|
| `laravel-patterns` | Laravel 架构模式和最佳实践 |
| `laravel-tdd` | Laravel TDD 工作流 |
| `laravel-verification` | Laravel 验证循环 |
| `laravel-plugin-discovery` | 发现和评估 Laravel 包 |

### Python / Django

| 技能 | 简介 |
|------|------|
| `django-patterns` | Django 架构模式和 REST API |
| `django-tdd` | Django TDD 工作流 |
| `django-verification` | Django 验证循环 |

### C# / .NET

| 技能 | 简介 |
|------|------|
| `csharp-testing` | C#/.NET 测试模式 |
| `dotnet-patterns` | C#/.NET 设计模式 |

### C++

| 技能 | 简介 |
|------|------|
| `cpp-review` | C++ 代码审查 |
| `cpp-test` | C++ 测试执行 |
| `cpp-build` | C++ 构建错误修复 |
| `cpp-coding-standards` | C++ 编码标准 |

### Perl

| 技能 | 简介 |
|------|------|
| `perl-patterns` | Perl 5.36+ 设计模式 |
| `perl-testing` | Perl Test2 测试模式 |

### Android / Compose

| 技能 | 简介 |
|------|------|
| `android-clean-architecture` | Android Clean Architecture 模式 |
| `compose-multiplatform-patterns` | Compose Multiplatform 和 Jetpack Compose 模式 |

---

## 前端开发

| 技能 | 简介 |
|------|------|
| `frontend-patterns` | 前端开发模式和最佳实践 |
| `frontend-design` | 创建独特的生产级前端设计 |
| `frontend-slides` | 创建动画丰富的 HTML 演示文稿 |
| `e2e-testing` | Playwright E2E 测试模式和最佳实践 |
| `mcp-server-patterns` | MCP 服务器设计模式 (Node/TypeScript) |

---

## 后端开发

| 技能 | 简介 |
|------|------|
| `backend-patterns` | 后端架构模式、API 设计 |
| `api-design` | REST API 设计模式 |
| `nestjs-patterns` | NestJS 架构模式 |

---

## 持续学习

| 技能 | 简介 |
|------|------|
| `learn` / `learn-eval` | 从项目/全局提取可复用模式 |
| `continuous-learning` | 自动提取模式并持续学习 |
| `continuous-learning-v2` | 基于本能的学习系统 |
| `evolve` | 分析本能并建议改进 |
| `instinct-status` | 显示已学习的本能（项目+全局）|
| `instinct-export` | 导出本能到文件或 URL |
| `instinct-import` | 从文件或 URL 导入本能 |
| `prune` | 删除过期的待处理本能 |
| `promote` | 将项目级本能提升为全局 |
| `skill-health` | 技能组合健康仪表板 |
| `skill-create` | 从 git 历史提取技能 |
| `skill-stocktake` | 审计技能和资源 |

---

## AI / Agent 相关

| 技能                              | 简介                              |
| ------------------------------- | ------------------------------- |
| `claude-api`                    | Claude API / Anthropic SDK 应用开发 |
| `agent-introspection-debugging` | 结构化自我调试工作流                      |
| `council`                       | 四角色共识评审（多视角分析）                  |
| `agent-sort`                    | 构建 ECC 即时响应代理                   |
| `ai-regression-testing`         | AI 回归测试策略                       |
| `multi-workflow`                | 多模型协作工作流                        |
| `multi-plan`                    | 多模型协作计划                         |
| `multi-execute`                 | 多模型协作执行                         |
| `multi-frontend`                | 前端专注开发                          |
| `multi-backend`                 | 后端专注开发                          |

---

## 循环任务

| 技能 | 简介 |
|------|------|
| `loop` | 循环运行提示或命令（默认 10 分钟）|
| `loop-start` | 启动循环任务 |
| `loop-status` | 查看循环任务状态 |

---

## PR / Git 工作流

| 技能 | 简介 |
|------|------|
| `prp-prd` | 交互式 PRD 生成器 |
| `prp-plan` | 创建功能实现计划 |
| `prp-implement` | 执行实现计划 |
| `prp-pr` | 从当前分支创建 GitHub PR |
| `prp-commit` | 快速提交（自然语言描述）|
| `review-pr` | 使用规格审查 PR |

---

## 会话管理

| 技能 | 简介 |
|------|------|
| `save-session` | 保存当前会话状态 |
| `resume-session` | 加载最近的会话文件 |
| `sessions` | 管理会话历史 |

---

## 文档 / 代码地图

| 技能 | 简介 |
|------|------|
| `update-codemaps` | 更新代码地图 |
| `update-docs` | 更新文档 |
| `code-tour` | 创建 CodeTour `.tour` 文件 |
| `docs-lookup` | 查询库/框架文档 |

---

## Hook 系统

| 技能 | 简介 |
|------|------|
| `hookify` | 创建 Hook 防止不良行为 |
| `hookify-list` | 列出已配置的 hookify 规则 |
| `hookify-help` | Hookify 帮助 |
| `hookify-configure` | 启用/禁用 hookify 规则 |
| `hookify-rules` | Hook 规则（当需要防止行为时使用）|

---

## 测试 / 质量

| 技能 | 简介 |
|------|------|
| `test-coverage` | 测试覆盖率分析 |
| `quality-gate` | 质量门禁命令 |
| `plankton-code-quality` | 写时代码质量强制 |
| `coding-standards` | 基础跨项目编码规范 |

---

## 配置 / 管理

| 技能 | 简介 |
|------|------|
| `update-config` | 配置 Claude Code harness |
| `configure-ecc` | Everything-Claude-Code 交互式安装 |
| `harness-audit` | Harness 审计命令 |
| `projects` | 列出已知项目及其本能 |
| `model-route` | 模型路由命令 |

---

## 其他实用

| 技能 | 简介 |
|------|------|
| `simplify` | 审查代码的可复用性、质量和效率 |
| `aside` | 快速回答侧边问题 |
| `checkpoint` | 检查点命令 |
| `jira` | 获取 Jira 工单并分析需求 |
| `pm2` | PM2 初始化 |
| `logo-designer-skill` | 迭代式 Logo 设计（SVG/PNG）|
| `context-budget` | 上下文预算管理 |
| `strategic-compact` | 建议手动上下文压缩 |
| `iterative-retrieval` | 渐进式检索模式 |

---

## 使用方式

### 基本用法

```bash
/技能名 [参数]
```

### 示例

```bash
# 进入计划模式
/plan

# 代码审查
/code-review

# 提取可复用模式
/learn

# TDD 工作流
/tdd-workflow

# 查看循环任务状态
/loop-status
```

### 常用组合

| 场景 | 推荐技能 |
|------|----------|
| 新功能开发 | `plan` → `tdd-workflow` → `code-review` |
| Bug 修复 | `build-fix` → `verify` |
| 代码清理 | `refactor-clean` → `code-review` |
| 学习模式 | `learn` → `instinct-status` |
| PR 流程 | `prp-prd` → `prp-plan` → `prp-implement` → `prp-pr` |

---

## 相关链接

- [Claude Code 官方文档](https://docs.anthropic.com/claude-code)
- [Anthropic API 文档](https://docs.anthropic.com/)
- [Ollama 官网](https://ollama.com/)