# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2026-02-06

### 🎉 改进 | Improved

**大幅优化互动体验**：
- ✅ 强化互动对话模式，严格禁止一次性输出所有问题
- ✅ 添加"核心原则"章节，明确互动规则
- ✅ 每次只展示一个问题，展示后立即停止并等待用户反馈
- ✅ 优化问题展示格式，减少单次输出长度（控制在约 30 行内）
- ✅ 增强选项式交互，让用户更清晰地控制审查节奏
- ✅ 更新示例对话，展示正确的逐步互动流程
- ✅ 改进总览展示：只显示问题标题列表，不展开详细内容

**解决的问题**：
- 修复用户反馈的"罗列一大串文字"的阅读体验问题
- 让 AI 真正像"设计顾问"而非"报告生成器"
- 显著提升用户控制感和交互流畅度

## [1.0.0] - 2026-02-06

### Added
- 初始发布
- 单次审查模式：系统化设计审查工作流
- Copilot 模式：持续监控设计决策
- 智能设计规范管理
- 互动对话式问题展示
- 可执行的修复方案生成
- 默认设计 token 体系
- 设计原则快速参考（HIG/Material/Nielsen/WCAG）
- 设计规范审查清单
- 完整的页面审查清单
- 跨平台支持（iOS/Android/Web）
- 无障碍性审查（WCAG 2.1/2.2）

### Features
- 支持截图、URL、自然语言描述等多种输入方式
- 自动询问和验证用户设计规范
- 优先级分级（严重/建议/次要）
- 代码修改建议和 CSS 示例
- 可选的代码自动修复
- 阶段性审查总结
- 设计决策辅助建议

[1.0.0]: https://github.com/Rocccccc-hub/ued-copilot/releases/tag/v1.0.0
