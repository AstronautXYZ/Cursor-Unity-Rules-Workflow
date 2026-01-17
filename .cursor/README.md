# 🤖 AI 助手规则配置

## 🎯 系统概述

**AI 助手规则系统** 是 Cursor-Unity-Rules-Workflow 的核心组件，定义了 AI 助手在不同场景下的行为规范。

## 🗂️ 规则文件结构

### historian.mdc - 史官
- **职责**: 新需求分析、项目复盘、演化节点创建
- **范围**: `_Evolution/**/*` 目录
- **工作流**: 扫描 → 创建节点 → 记录意图 → 初始化账本

### architect.mdc - 架构师  
- **职责**: 技术方案设计、架构合规检查、账本更新
- **范围**: `*.cs`, `_Evolution/**/*.json`, `_Evolution/**/*.md`
- **工作流**: 读取 manifest → 制定蓝图 → 更新 ledger

### coder.mdc - 工程师
- **职责**: 代码编写、逻辑修改、错误修复
- **范围**: `*.cs`, `_Evolution/**/*.json`
- **工作流**: 执行 ledger → 遵循红线 → 更新状态

### qa.mdc - 质检员
- **职责**: 代码审查、测试验证、性能分析
- **范围**: `*.cs`, `*.test.cs`
- **工作流**: 审查标准 → 测试执行 → 质量报告

## 🔄 动态路由机制

根据用户意图自动激活对应规则：
- **新需求/想法/复盘** → `@historian.mdc`
- **设计/方案/可行性分析** → `@architect.mdc`  
- **写代码/修改逻辑/报错修复** → `@coder.mdc`
- **测试/审查/性能分析** → `@qa.mdc`

## 🚨 架构红线 (P0 Constraints)

1. **严禁单例** → 必须使用 `ServiceLocator`
2. **严禁 Instantiate** → 必须使用 `SpawnManager`  
3. **严禁 int/enum 索引** → 必须使用 String ID
4. **严禁 Input.GetKey** → 必须使用 InputSystem

## 📝 规则维护

- 规则文件使用 Markdown 格式
- 保持规则与实际架构同步
- 重要变更需记录到演化时间线
- 定期审查和优化规则内容
