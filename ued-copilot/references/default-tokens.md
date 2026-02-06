# 默认设计 Token

本文档提供推荐的设计 token 体系，当项目没有自定义设计规范时使用。

## 使用说明

这些 token 基于业界最佳实践，融合了 Apple HIG、Material Design 和 WCAG 标准。
用户可以基于这些默认值进行定制。

---

## 颜色系统

### 品牌色（可替换）
```
primary-50:  #f0f9ff
primary-100: #e0f2fe
primary-200: #bae6fd
primary-300: #7dd3fc
primary-400: #38bdf8
primary-500: #0ea5e9  // 主色
primary-600: #0284c7
primary-700: #0369a1
primary-800: #075985
primary-900: #0c4a6e
```

### 中性色（灰度）
```
gray-50:  #fafafa
gray-100: #f5f5f5
gray-200: #e5e5e5
gray-300: #d4d4d4
gray-400: #a3a3a3
gray-500: #737373  // 辅助文字
gray-600: #525252
gray-700: #404040
gray-800: #262626
gray-900: #171717  // 主文字
```

### 语义色
```
// 成功
success-light: #d1fae5
success:       #10b981
success-dark:  #059669

// 警告
warning-light: #fef3c7
warning:       #f59e0b
warning-dark:  #d97706

// 错误
error-light:   #fee2e2
error:         #ef4444
error-dark:    #dc2626

// 信息
info-light:    #dbeafe
info:          #3b82f6
info-dark:     #2563eb
```

### 背景色
```
background:         #ffffff
background-subtle:  #f9fafb
background-muted:   #f3f4f6
surface:            #ffffff
surface-raised:     #ffffff (with shadow)
```

### 边框色
```
border:       #e5e7eb
border-light: #f3f4f6
border-dark:  #d1d5db
```

---

## 字体系统

### 字体家族
```
// 西文
font-sans: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif

// 中文优化
font-sans-cjk: -apple-system, BlinkMacSystemFont, "PingFang SC", "Microsoft YaHei", "Segoe UI", sans-serif

// 等宽（代码）
font-mono: "SF Mono", Monaco, "Cascadia Code", "Consolas", monospace
```

### 字体大小
```
// 移动端
text-xs:   12px  // 辅助信息
text-sm:   14px  // 次要文字
text-base: 16px  // 正文（最小）
text-lg:   18px  // 强调文字
text-xl:   20px  // 小标题
text-2xl:  24px  // 标题 H3
text-3xl:  28px  // 标题 H2
text-4xl:  32px  // 标题 H1

// 桌面端（可适当放大 1.1-1.2 倍）
desktop-text-base: 16px
desktop-text-2xl:  28px
desktop-text-4xl:  40px
```

### 字重
```
font-light:    300
font-normal:   400  // 正文
font-medium:   500  // 强调
font-semibold: 600  // 小标题
font-bold:     700  // 标题
```

### 行高
```
leading-none:   1.0
leading-tight:  1.25   // 标题
leading-normal: 1.5    // 正文
leading-relaxed: 1.625 // 宽松正文
leading-loose:  2.0
```

### 字间距
```
tracking-tighter: -0.05em
tracking-tight:   -0.025em
tracking-normal:  0
tracking-wide:    0.025em
tracking-wider:   0.05em
```

---

## 间距系统（8pt Grid）

```
spacing-0:  0px
spacing-1:  4px    // 超紧密
spacing-2:  8px    // 紧密
spacing-3:  12px   // 小间距
spacing-4:  16px   // 标准间距
spacing-5:  20px
spacing-6:  24px   // 中等间距
spacing-8:  32px   // 大间距
spacing-10: 40px
spacing-12: 48px   // 章节间距
spacing-16: 64px
spacing-20: 80px
spacing-24: 96px   // 超大间距
```

### 使用指南
- 组件内边距：spacing-4 (16px)
- 组件间距：spacing-4 ~ spacing-6 (16-24px)
- 章节间距：spacing-12 ~ spacing-16 (48-64px)
- 页面边距：spacing-4 (移动) / spacing-8 (桌面)

---

## 圆角

```
rounded-none: 0px
rounded-sm:   2px   // 微圆角
rounded:      4px   // 小圆角（输入框、卡片）
rounded-md:   6px
rounded-lg:   8px   // 常规圆角（按钮、卡片）
rounded-xl:   12px  // 大圆角
rounded-2xl:  16px
rounded-3xl:  24px
rounded-full: 9999px // 完全圆形（头像、徽章）
```

---

## 阴影

```
// 轻微提升
shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05)

// 常规卡片
shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1),
        0 1px 2px -1px rgba(0, 0, 0, 0.1)

// 提升卡片
shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
           0 2px 4px -2px rgba(0, 0, 0, 0.1)

// 悬浮按钮
shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1),
           0 4px 6px -4px rgba(0, 0, 0, 0.1)

// 模态弹窗
shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
           0 8px 10px -6px rgba(0, 0, 0, 0.1)

// 超大阴影
shadow-2xl: 0 25px 50px -12px rgba(0, 0, 0, 0.25)
```

---

## 断点（响应式）

```
// 移动端优先
sm:  640px   // 小屏幕（手机横屏）
md:  768px   // 平板竖屏
lg:  1024px  // 平板横屏 / 小笔记本
xl:  1280px  // 桌面
2xl: 1536px  // 大屏桌面
```

---

## 触控目标

```
// 最小尺寸
touch-target-min: 44px  // iOS (44x44 pt)
touch-target-min-android: 48px  // Android (48x48 dp)

// 推荐尺寸
button-height-sm: 32px  // 小按钮（桌面）
button-height:    44px  // 标准按钮
button-height-lg: 52px  // 大按钮

// 最小间距
touch-spacing: 8px  // 相邻触控元素间距
```

---

## 动画与过渡

### 时长
```
duration-75:  75ms   // 超快（颜色变化）
duration-100: 100ms  // 快速（hover 反馈）
duration-150: 150ms  // 微交互
duration-200: 200ms  // 标准过渡
duration-300: 300ms  // 常规动画
duration-500: 500ms  // 强调动画
duration-700: 700ms  // 慢动画
duration-1000: 1000ms // 超慢（谨慎使用）
```

### 缓动函数
```
ease-linear:   cubic-bezier(0, 0, 1, 1)
ease-in:       cubic-bezier(0.4, 0, 1, 1)      // 加速
ease-out:      cubic-bezier(0, 0, 0.2, 1)      // 减速（推荐）
ease-in-out:   cubic-bezier(0.4, 0, 0.2, 1)    // 先加速后减速
ease-bounce:   cubic-bezier(0.68, -0.55, 0.265, 1.55) // 弹跳效果
```

### 使用指南
- 颜色、透明度变化：duration-100, ease-out
- 位置、大小变化：duration-200, ease-out
- 模态弹窗：duration-300, ease-out
- 页面切换：duration-300, ease-in-out

---

## Z-index 层级

```
z-base:     0    // 基础层
z-dropdown: 1000 // 下拉菜单
z-sticky:   1020 // 固定头部
z-fixed:    1030 // 固定元素
z-modal:    1040 // 模态弹窗背景
z-modal-content: 1050 // 模态内容
z-popover:  1060 // 气泡提示
z-tooltip:  1070 // 工具提示
z-toast:    1080 // Toast 通知
```

---

## 图标尺寸

```
icon-xs:  12px
icon-sm:  16px
icon:     20px  // 标准
icon-lg:  24px
icon-xl:  32px
icon-2xl: 48px
```

---

## 对比度标准（WCAG）

### 文字对比度（最低要求）
- 正常文字（< 18px）：4.5:1
- 大文字（≥ 18px 或 ≥ 14px 粗体）：3:1

### 推荐配色对比
```
// 深色文字 + 浅色背景
gray-900 (#171717) on white: 16.1:1 ✅
gray-700 (#404040) on white: 10.4:1 ✅
gray-500 (#737373) on white: 4.7:1  ✅
gray-400 (#a3a3a3) on white: 2.8:1  ❌ (辅助元素可用)

// 浅色文字 + 深色背景
white on gray-900: 16.1:1 ✅
white on gray-700: 10.4:1 ✅
white on primary-500: 需测试（取决于品牌色）
```

---

## 使用建议

### 颜色使用
1. 主色用于：主按钮、链接、重要操作
2. 中性色用于：文字、边框、背景
3. 语义色用于：状态反馈、提示信息

### 间距使用
1. 遵循 8pt 网格系统
2. 组件内部：4-16px
3. 组件之间：16-24px
4. 大区块：48px+

### 字体使用
1. 标题：font-semibold / font-bold
2. 正文：font-normal, 16px, 行高 1.5
3. 辅助：font-normal, 14px, gray-500

### 响应式
1. 移动端优先
2. 桌面端适当放大字号和间距
3. 触控目标移动端至少 44px
