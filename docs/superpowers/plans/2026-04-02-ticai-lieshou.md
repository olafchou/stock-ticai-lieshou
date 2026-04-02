# 题材猎手 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 创建一个名为“题材猎手”的 skill，能对文字或图片里的财经事件做实时核验、逻辑推演和 A 股题材映射输出。

**Architecture:** skill 只固化方法，不固化个股数据库。核心文件为 `SKILL.md` 和 `agents/openai.yaml`，前者定义工作流和输出规范，后者提供 UI 元数据与默认调用提示。

**Tech Stack:** Markdown, YAML

---

### Task 1: 建立 skill 目录与元数据

**Files:**
- Create: `/Users/haibaotujidui/Vibe Coding/skill/ticai-lieshou/SKILL.md`
- Create: `/Users/haibaotujidui/Vibe Coding/skill/ticai-lieshou/agents/openai.yaml`

- [ ] **Step 1: 创建 skill 目录结构**

创建 `ticai-lieshou/` 与 `ticai-lieshou/agents/`，保持结构最小化，不创建不需要的资源目录。

- [ ] **Step 2: 编写 `SKILL.md` frontmatter**

写入 skill 的内部名、触发说明和核心用途，确保描述清楚何时使用该 skill。

- [ ] **Step 3: 编写 `SKILL.md` 主体**

定义输入类型、核验流程、搜索顺序、推理框架、股票筛选规则和输出格式，强调“搜索优先，推理校验”。

- [ ] **Step 4: 编写 `agents/openai.yaml`**

写入 `display_name`、`short_description` 与默认 prompt，保证中文显示名为“题材猎手”。

### Task 2: 校对和验证 skill 可读性

**Files:**
- Modify: `/Users/haibaotujidui/Vibe Coding/skill/ticai-lieshou/SKILL.md`
- Modify: `/Users/haibaotujidui/Vibe Coding/skill/ticai-lieshou/agents/openai.yaml`

- [ ] **Step 1: 通读 `SKILL.md`**

确认没有把固定题材结论写死，且能覆盖文字和图片输入两类场景。

- [ ] **Step 2: 通读 `agents/openai.yaml`**

确认默认 prompt 显式提到 `$ticai-lieshou`，并与 `SKILL.md` 的用途一致。

- [ ] **Step 3: 做一次静态自检**

检查描述是否清楚、结构是否简洁、是否遗漏输出格式和风险提示。
