# UED Copilot

<div align="center">

**资深 UI/UX 设计审查与优化智能体**

基于 Apple HIG、Material Design、Nielsen 可用性原则和 WCAG 无障碍标准

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude-Code-5A67D8)](https://claude.ai/code)

</div>

---

## 🎯 简介

UED Copilot 是一个专业的 UI/UX 设计审查技能，可以自动识别页面中的设计缺陷，并给出可执行的修复方案。特别适合在快速开发（vibe coding）后进行设计优化。

### 核心特性

- ✅ **系统化审查**：覆盖 UI、UX、可用性、无障碍性、平台规范等维度
- ✅ **智能规范管理**：支持自定义设计规范，或使用业界最佳实践
- ✅ **互动对话模式**：逐个展示问题，用户可选择重点关注的类别
- ✅ **可执行修复方案**：提供具体的代码示例和修改步骤
- ✅ **Copilot 模式**：持续监控开发过程，主动提供优化建议
- ✅ **跨平台支持**：Web、iOS、Android 全平台设计审查

### 基于的设计规范

- 🍎 **Apple Human Interface Guidelines (HIG)**
- 🎨 **Google Material Design**
- 📊 **Nielsen 十大可用性原则**
- ♿ **WCAG 2.1/2.2 无障碍标准**
- 🎯 **ISO 9241-210 以人为中心的设计**

---

## 📦 安装

### 前置要求

- [Claude Code CLI](https://github.com/anthropics/claude-code) 已安装

### 安装步骤

1. **下载技能文件**

```bash
# 克隆仓库
git clone https://github.com/your-username/ued-copilot.git
cd ued-copilot
```

2. **安装技能**

```bash
# 安装打包好的技能
claude skills install ued-copilot.skill
```

或者从源码构建：

```bash
# 使用 skill-creator 打包
python3 /path/to/skill-creator/scripts/package_skill.py ./ued-copilot
claude skills install ued-copilot.skill
```

3. **验证安装**

```bash
# 列出已安装的技能
claude skills list
```

---

## 🚀 使用方法

### 模式 1：单次审查模式

当你需要审查某个页面时：

```
用户：帮我审查这个登录页面（上传截图）
```

AI 会引导你：
1. 确认是否有设计规范
2. 收集页面上下文信息
3. 进行系统化审查
4. 生成评估报告
5. 互动展示问题
6. 生成行动计划

### 模式 2：Copilot 模式（持续监控）

在项目开始时启动：

```
用户：启动 UED Copilot，在整个项目过程中协助我
```

Copilot 会：
- 主动监控你的设计决策
- 及时提醒潜在问题
- 在功能模块完成时提供总结
- 帮助你做设计选择

### 触发方式

技能会在以下情况自动触发：
- 用户说"审查设计"、"检查 UI"、"UX 优化"
- 用户上传页面截图
- 用户提到"设计缺陷"、"可用性问题"
- 用户主动调用 `/ued-copilot`

---

## 📖 工作流程示例

### 示例 1：审查移动端登录页面

```
用户：审查这个移动端登录页面（上传截图）

AI：👋 收到！在审查前，先确认一下：
你的项目是否有自己的设计规范（Design System）？
1️⃣ 有 - 请分享你的设计规范
2️⃣ 没有 - 我将使用业界最佳实践
3️⃣ 不确定 - 先用默认标准

用户：没有，用默认的

AI：好的！我会基于以下标准审查：
- Apple HIG（触控目标、反馈等）
- Material Design（间距、层级等）
- WCAG 2.1 AA（无障碍标准）

开始审查移动端登录页面...

## 📊 页面整体评估

### 评分
- **可用性**：70/100
- **可访问性**：55/100 ⚠️
- **视觉一致性**：85/100
- **iOS 规范遵循**：65/100

### 风险等级：🟡 中等

### 发现问题总数：8 个
- 🔴 严重：2 个
- 🟡 建议：5 个
- 🟢 次要：1 个

### Top 3 优先修复
1. "忘记密码"链接触控目标仅 28px（需 ≥ 44px）
2. 错误提示对比度不足（2.9:1，需 ≥ 4.5:1）
3. 输入框焦点状态不明显

接下来你想：
1️⃣ 查看所有问题详情
2️⃣ 只看严重问题
3️⃣ 直接生成修复计划
```

### 示例 2：审查自定义设计规范

```
用户：帮我审查一下我们的设计规范（提供 design-tokens.json）

AI：收到你的设计规范！让我先审查一下规范本身...

## 设计规范审查报告

### 整体评估
- 完整度：⭐⭐⭐⭐☆ (4/5)
- 合理性：⭐⭐⭐⭐⭐ (5/5)
- 可访问性：⭐⭐⭐☆☆ (3/5)
- 可维护性：⭐⭐⭐⭐☆ (4/5)

### 严重问题（必须修复）
1. 主色对比度不足
   - 问题：主色 #3498db 在白底上对比度仅 3.2:1
   - 标准：WCAG AA 要求 ≥ 4.5:1
   - 建议：调整为 #2563eb（对比度 4.6:1）

是否先优化规范，然后再审查页面？
```

---

## 📚 技能结构

```
ued-copilot/
├── SKILL.md                           # 核心工作流程
└── references/                        # 参考文档
    ├── default-tokens.md              # 默认设计规范
    ├── design-principles.md           # 设计原则快速参考
    ├── design-system-audit.md         # 设计规范审查清单
    └── page-audit-checklist.md        # 页面审查清单（核心）
```

### 文档说明

- **SKILL.md**：定义了完整的工作流程，包括两种工作模式和六步审查流程
- **default-tokens.md**：提供业界最佳实践的默认设计规范（颜色、字体、间距等）
- **design-principles.md**：汇总 Apple HIG、Material Design、Nielsen、WCAG 的核心原则
- **design-system-audit.md**：用于审查用户提供的设计规范是否完整、合理
- **page-audit-checklist.md**：系统化的页面审查清单，覆盖 UI、UX、可用性、无障碍性

---

## 🎨 审查维度

### 1. 视觉层面（UI）
- ✅ 排版与可读性（字体大小、行高、字重）
- ✅ 颜色与对比（WCAG 对比度标准）
- ✅ 间距与对齐（8pt 网格系统）
- ✅ 信息层级（视觉权重）
- ✅ 组件一致性（按钮、输入框、卡片）
- ✅ 响应式设计

### 2. 交互层面（UX）
- ✅ 导航与信息架构
- ✅ 任务流程优化
- ✅ 反馈与状态提示
- ✅ 错误处理与预防
- ✅ 操作确认机制
- ✅ 内容与文案

### 3. 可用性原则（Nielsen）
- ✅ 系统状态可见性
- ✅ 系统与真实世界匹配
- ✅ 用户控制与自由
- ✅ 一致性与标准
- ✅ 错误预防
- ✅ 识别胜于记忆
- ✅ 灵活高效使用
- ✅ 美观与极简设计
- ✅ 错误识别与恢复
- ✅ 帮助与文档

### 4. 无障碍性（WCAG）
- ✅ 颜色对比度（AA/AAA 标准）
- ✅ 键盘操作支持
- ✅ 触控目标尺寸（44×44px）
- ✅ 语义化 HTML
- ✅ 屏幕阅读器支持
- ✅ 内容可理解性

### 5. 平台规范
- ✅ iOS (Apple HIG)
- ✅ Android (Material Design)
- ✅ Web (响应式、浏览器兼容性)

---

## 💡 特色功能

### 智能规范管理
- 支持自定义设计规范（Design System / Design Tokens）
- 优先审查规范本身的完整性和合理性
- 无规范时自动使用业界最佳实践

### 互动对话模式
- 不输出冗长的完整报告
- 逐个展示问题，等待用户反馈
- 用户可选择重点（所有问题 / 严重问题 / 某类别）

### 可执行修复方案
每个问题都包含：
- 📐 设计层建议（布局、样式、交互）
- 💬 文案层建议（按钮文本、提示语）
- 🧩 组件层建议（是否替换组件）
- 💻 代码层建议（CSS 示例、实现参考）

### Copilot 持续监控
- 主动识别设计问题
- 及时礼貌介入提醒
- 阶段性总结和建议
- 辅助设计决策

---

## 🛠️ 常见用例

1. **快速开发后的设计优化**
   - Vibe coding 完成后，快速审查设计
   - 识别并修复可用性和可访问性问题

2. **设计规范建立**
   - 审查现有设计规范
   - 建议优化方向
   - 对齐行业标准

3. **跨平台设计审查**
   - 检查 iOS/Android/Web 平台规范遵循
   - 确保触控目标、交互符合平台习惯

4. **无障碍性审查**
   - WCAG 合规性检查
   - 对比度、键盘操作、语义化验证

5. **设计 Copilot**
   - 项目全程设计助手
   - 持续监控设计决策
   - 主动提供优化建议

---

## 🤝 贡献

欢迎贡献！如果你有改进建议或发现问题：

1. Fork 这个仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开一个 Pull Request

### 改进方向

- 添加更多平台规范（如 Windows、macOS）
- 补充更多常见问题模式库
- 添加自动化测试工具集成
- 支持更多设计工具导出格式

---

## 📄 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

---

## 🙏 致谢

本技能基于以下设计规范和标准：

- [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)
- [Google Material Design](https://material.io/design)
- [Nielsen Norman Group - 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/)
- [WCAG 2.1 Web Content Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [ISO 9241-210](https://www.iso.org/standard/77520.html)

---

## 📧 联系方式

如有问题或建议，欢迎：
- 提交 [Issue](https://github.com/your-username/ued-copilot/issues)
- 发起 [Discussion](https://github.com/your-username/ued-copilot/discussions)

---

<div align="center">

Made with ❤️ by [Your Name]

使用 [Claude Code](https://claude.ai/code) 开发

</div>
