---
version: alpha
name: Career Editorial Warmth
description: A warm, editorial design system for a career timeline and deep-dive profile page. It should feel trustworthy, calm, and precise rather than flashy, salesy, or dashboard-like.
colors:
  primary: "#1F1E1C"
  secondary: "#6B6963"
  tertiary: "#C96442"
  neutral: "#FAF9F5"
  surface: "#F2EFE7"
  border: "#E4DFD4"
  accent-soft: "#F4E3D7"
  on-tertiary: "#FAF9F5"
  focus-ring: "#C96442"
  muted: "#9A968E"
typography:
  display-lg:
    fontFamily: "Source Han Serif SC, Noto Serif SC, Source Serif 4, Georgia, serif"
    fontSize: 2.25rem
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0em
  title-md:
    fontFamily: "Source Han Serif SC, Noto Serif SC, Source Serif 4, Georgia, serif"
    fontSize: 1.375rem
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: 0em
  body-md:
    fontFamily: "Source Han Sans SC, Noto Sans SC, Inter, system-ui, sans-serif"
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.75
    letterSpacing: 0em
  summary-md:
    fontFamily: "Source Han Sans SC, Noto Sans SC, Inter, system-ui, sans-serif"
    fontSize: 1.0625rem
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0em
  label-sm:
    fontFamily: "Source Han Sans SC, Noto Sans SC, Inter, system-ui, sans-serif"
    fontSize: 0.8125rem
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0em
  mono-sm:
    fontFamily: "JetBrains Mono, ui-monospace, Menlo, monospace"
    fontSize: 0.9375rem
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0em
rounded:
  xs: 4px
  sm: 8px
  md: 12px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  xxxl: 64px
  page-desktop: 96px
components:
  page-shell:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
    typography: "{typography.body-md}"
    padding: 24px
  timeline-card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: 24px
  timeline-card-expanded:
    backgroundColor: "{colors.accent-soft}"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: 24px
  field-label:
    textColor: "{colors.tertiary}"
    typography: "{typography.label-sm}"
  button-ghost:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
    rounded: "{rounded.sm}"
    padding: 12px
  button-primary:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    rounded: "{rounded.sm}"
    padding: 12px
  link-inline:
    textColor: "{colors.primary}"
    typography: "{typography.body-md}"
---

# DESIGN.md

## Overview

这个项目的视觉气质必须像排版精良的长文，不像营销站，也不像后台系统。

页面服务的是招聘方、合作方和同行。用户通常先从简历或链接跳进来，目标不是“被惊艳”，而是沿时间线判断这个人每个阶段在做什么、产出了什么、能力如何变化。所以整体设计应该呈现三种感受：

- 可信：像认真整理过的个人档案，而不是包装感很重的作品集。
- 温和：暖色纸白、克制的层级、舒服的留白，避免冷硬和攻击性。
- 准确：页面是在帮助用户建立判断，不是在炫耀技巧。

设计决策应始终服从以下原则：

- 为目标设计，不为功能设计。
- 不要让用户思考。
- 渐进式展示细节，而不是一开始塞满所有信息。
- 简历是“精简履历”，页面只展开职业时间线，不放额外介绍区。

## Colors

色彩必须基于高对比中性色，只允许一个真正的强调色。页面不靠色彩制造情绪，而是靠版式、层级和措辞建立信任。

- **Primary (`#1F1E1C`)**：主文字和最重要的标题色，偏暖的近黑，不用纯黑。
- **Secondary (`#6B6963`)**：时间、注释、说明、分级信息。
- **Tertiary (`#C96442`)**：唯一主要强调色，用于聚焦、链接悬停、字段标签、主按钮或展开态提示。
- **Neutral (`#FAF9F5`)**：页面底色，暖奶油白，禁止纯白大面积铺底。
- **Surface (`#F2EFE7`)**：卡片底色，用色差而不是阴影制造层级。
- **Border (`#E4DFD4`)**：边框和分割线。
- **Accent Soft (`#F4E3D7`)**：展开态或弱提示底色，不能滥用。

颜色使用规则：

- 整页强调色出现位置尽量控制在 3 类以内。
- 不使用渐变、霓虹、高饱和按钮墙、多语义彩虹标签。
- 不依赖颜色单独传达信息，字段差异必须靠文案标签和位置结构体现。
- 正文对比度至少达到 WCAG AA，优先追求 AAA 级别。

## Typography

排版承担这个页面的大部分气质，因此字体选择必须服务于“编辑感”和“可信感”。

- 衬线体用于姓名、公司名、重要标题，承担识别与权威感。
- 无衬线用于正文和界面控件，承担信息流和易读性。
- 等宽字体只用于时间、数字、量化信息，不用于大段正文。

字体使用规则：

- 中文衬线：`Source Han Serif SC` / `Noto Serif SC`
- 中文无衬线：`Source Han Sans SC` / `Noto Sans SC`
- 西文衬线：`Source Serif 4` / `Georgia`
- 西文无衬线：`Inter`
- 等宽：`JetBrains Mono`

版式要求：

- 姓名和公司名必须明显强于正文，但不能做成海报字。
- 正文行高偏松，便于 HR 快速扫读。
- 不能使用负字距制造“设计感”。
- 每行文本宽度应受控，正文不应出现横向阅读疲劳。

字体加载要求：

- 字体必须本地化自托管，或确保 `font-display: swap`。
- 禁止依赖外部字体 CDN 阻塞首屏渲染。

## Layout

布局只以时间线为核心，不做花哨分屏，不做作品集式拼贴。

基础布局原则：

- 移动优先，先保证 360px 宽时完整可读。
- 桌面端最多扩展为双栏：年份列 + 事件内容列，不能出现独立身份区、指标区、页脚联系区。
- 页面主体推荐最大内容宽度控制在 `960px` 到 `1120px` 之间。
- 桌面端两侧安全边距不小于 `96px`，移动端不小于 `20px`。
- 段落间距、字段间距、卡片间距应明显分层，不靠颜色堆出层级。

信息流要求：

- 最近经历在最上面。
- 每家公司内部按年份倒序展示事件。
- 每个年份事件都必须清楚区分“做了什么”和“产出 / 价值”。
- 页面不展示简历预览、联系方式、下载入口等非时间线内容。

Measure 要求：

- 正文单行理想宽度不超过约 36 个中文字符。
- 说明、标签、时间、辅助信息不应超过正文宽度。

## Elevation & Depth

这个页面不需要“深度感”，需要的是“秩序感”。

- 默认不使用投影。
- 卡片层级通过边框和间距来建立。
- 暂不展示重点事件强调线，避免时间线出现额外视觉优先级。
- 禁止玻璃拟态、毛玻璃、悬浮阴影堆叠、厚重发光描边。

## Shapes

造型语言应该规整、节制、低干扰。

- 卡片圆角：`12px`
- 按钮圆角：`8px`
- 轻标签圆角：`4px`
- 分割线为 `1px` 细线

形状规则：

- 不做 pill 风格的大圆角胶囊按钮，除非是非常短的小标签。
- 不做装饰性异形、斜切角、折页角、气泡形状。
- 不把时间线节点做成夸张的视觉锚点，它只需要清楚，不需要抢戏。

## Components

组件必须为阅读服务，而不是为展示组件系统而存在。

### 时间线事件

- 公司阶段：公司名、阶段时间、阶段定位。
- 年份事件：年份、主题、做了什么、产出 / 价值。
- 事件边框清晰，正文层级明确，默认不投影。

### 字段标签

- “做了什么 / 产出与价值” 这类标签用强调色文字，不加厚重色块。
- 标签与内容之间保留明确间距，不要挤成一行密集信息。

### 链接

- 默认主文字色，悬停或聚焦时切换为强调色并加下划线。
- 公司和年份锚点应作为真实可复制链接处理，不做伪按钮。

## Do's and Don'ts

### Do

- 像编辑一篇高质量长文一样设计页面。
- 优先强化“近十年持续有效的能力”而不是“会过哪些旧技术”。
- 用层级和留白帮助 HR 在 30 秒内做出第一判断。
- 让简历链接到这个页面时，读者能直接进入指定公司或年份事件。
- 保持整页节奏稳定，每个年份事件都遵循同一阅读框架。

### Don'ts

- 不要把页面做成作品集式 landing page。
- 不要使用渐变背景、插画、emoji、贴纸、粒子、视差、打字机效果。
- 不要把过时技术堆成大段标签墙。
- 不要为了“看起来高级”降低可读性。
- 不要做像后台系统那样的重表格、重面板、重功能区布局。
- 不要把重要信息埋进折叠层级过深的位置。
