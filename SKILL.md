---
name: ui-sites
description: "UI/UX 离线设计知识库。基于 55 个顶级设计资源网站预提取的设计知识，涵盖配色方案、字体排版、布局模式、组件设计、动效动画、设计系统、Landing Page、移动端 UI 共 8 大主题。无需联网即可直接输出专业的 UI/UX 设计方案和代码。当用户说 '/ui-sites'、'设计方案'、'配色方案'、'字体搭配'、'布局建议'、'组件规范'、'动画效果'、'Landing Page'、'移动端设计'、'设计系统' 时使用。"
argument-hint: "[主题] 如: 配色、字体、布局、组件、动效、设计系统、landing-page、移动端"
user-invocable: true
---

# UI/UX 离线设计知识库

你现在拥有一个基于 **55 个顶级设计资源网站** 预提取的 **离线设计知识库**，无需联网搜索即可直接输出专业的 UI/UX 设计方案和代码。

## 知识库结构

| 文件 | 主题 | 核心内容 |
|------|------|---------|
| `knowledge/color-palettes.md` | 配色方案 | 25+ 套配色（含 hex 值）、CSS 变量、Tailwind 配置、无障碍对比度指南 |
| `knowledge/typography.md` | 字体排版 | 27 组字体搭配、7 种 Type Scale、行高间距规范、中文字体推荐 |
| `knowledge/layout-patterns.md` | 布局模式 | 18 种 Web 布局（含 ASCII 示意图）、网格系统、响应式断点、间距系统 |
| `knowledge/component-design.md` | 组件设计 | 15 种核心组件规范（Button/Input/Card/Modal 等）、状态变体、Tailwind 代码 |
| `knowledge/animation.md` | 动效动画 | 缓动函数速查、入场退场动画、滚动动画、微交互、Framer Motion/GSAP 代码 |
| `knowledge/design-systems.md` | 设计系统 | Token 架构、五大 DS 对比、主题化方案、无障碍标准、搭建清单 |
| `knowledge/landing-pages.md` | Landing Page | 8 大区块模式、6 种行业模板、CRO 转化优化、响应式适配 |
| `knowledge/mobile-ui.md` | 移动端 UI | 导航模式、10 种页面模式、触控规范、iOS/Android 差异、App Store 截图 |

## 使用方式

### 核心原则

1. **直接读取知识文件**，根据用户需求加载对应主题的知识文件
2. **组合引用**，设计方案通常需要同时引用多个知识文件（如配色 + 字体 + 组件）
3. **输出可用代码**，所有知识文件都包含完整的 CSS/Tailwind 代码，直接引用即可

### 按需加载策略

根据用户需求，读取对应的知识文件：

| 用户需求 | 加载文件 |
|---------|---------|
| "帮我选配色" / "配色方案" | `knowledge/color-palettes.md` |
| "字体搭配" / "排版方案" | `knowledge/typography.md` |
| "页面布局" / "怎么排版" | `knowledge/layout-patterns.md` |
| "按钮/输入框/卡片设计" | `knowledge/component-design.md` |
| "加动画" / "动效建议" | `knowledge/animation.md` |
| "设计系统" / "Token 规范" | `knowledge/design-systems.md` |
| "做个 Landing Page" | `knowledge/landing-pages.md` + `knowledge/color-palettes.md` + `knowledge/typography.md` |
| "移动端设计" / "App UI" | `knowledge/mobile-ui.md` |
| "完整网站设计方案" | 全部文件按需组合 |

### 典型工作流

**场景 1：用户要做一个 SaaS Landing Page**

1. 读取 `knowledge/landing-pages.md` → 获取 SaaS 模板的区块组合和代码骨架
2. 读取 `knowledge/color-palettes.md` → 选择科技现代类配色方案
3. 读取 `knowledge/typography.md` → 选择现代简约类字体搭配
4. 组合输出完整设计方案 + 代码

**场景 2：用户要设计一个 Dashboard**

1. 读取 `knowledge/layout-patterns.md` → 获取 Dashboard 布局模式
2. 读取 `knowledge/component-design.md` → 获取表格/卡片/导航组件规范
3. 读取 `knowledge/color-palettes.md` → 选择适合后台的配色
4. 组合输出

**场景 3：用户问"按钮应该怎么设计"**

1. 读取 `knowledge/component-design.md` → 直接引用 Button 组件规范
2. 输出设计规范 + Tailwind 代码

## 网站索引（溯源参考）

知识库的原始来源网站索引保存在 `data/sites.csv`，可通过 Python 脚本查询：

```bash
python scripts/search.py --list          # 列出所有分类
python scripts/search.py "关键词"         # 搜索网站
python scripts/search.py --category color # 按类别过滤
```

## 行为规范

1. **优先使用知识库**：收到设计相关请求时，先读取对应的知识文件，不要凭记忆回答
2. **组合输出方案**：设计方案应同时包含配色、字体、布局、组件等多个维度
3. **输出可用代码**：方案中的代码必须是可以直接使用的 Tailwind/CSS
4. **标注来源**：输出方案时标注参考了哪些知识文件
5. **不联网搜索**：所有知识已预置在本地，无需联网获取
