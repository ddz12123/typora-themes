# Typora Themes · 浅色主题合集

一套手写的 Typora 浅色主题合集，8 个主题，纯 CSS，零网络依赖。

![license](https://img.shields.io/badge/license-MIT-0f766e?style=flat-square)
![typora](https://img.shields.io/badge/Typora-1.x-4B8BBE?style=flat-square)
![pure css](https://img.shields.io/badge/pure-CSS-5b5bd6?style=flat-square)
![offline](https://img.shields.io/badge/offline-no%20web%20fonts-6d7a77?style=flat-square)

> 全部为**浅色主题**。如果你在找深色主题，Typora 内置的 `night` 已经很好，本仓库不做重复劳动。

---

## 特性

- **8 套风格，一个变量切换气质**：从青瓷素笺到 GitHub 工程风，覆盖阅读、笔记、技术文档三类场景。
- **纯 CSS，零安装成本**：不依赖插件、不需要构建步骤，把 `.css` 丢进主题目录就能用。
- **零网络依赖**：字体走本地字体栈，勾选框/图标用内联 SVG 与 `data:` URI，断网、导出 PDF 都不会掉样式。
- **组件覆盖完整**：标题、段落、列表、表格、引用、五种 Callout、代码块高亮、TOC、YAML front matter、公式、Mermaid、脚注、任务列表。
- **为导出准备过**：每个主题都带 `@media print` 规则，PDF 分页、背景色、代码块跨页都已处理。
- **颜色全部收在 `:root`**：想换主色只改一个变量，不用翻两千行选择器。

## 主题一览

| 主题 | 文件 | 风格 | 主色 | 版心 |
| --- | --- | --- | --- | --- |
| Celadon Mist 青雾 | `celadon-mist.css` | 桌面素笺 + 青瓷点睛 | 青瓷青 `#0f766e` | 900px 起，宽屏逐级放宽至 1440px |
| Geek Tech 极客工程 | `geek-tech.css` | GitHub Primer 网格 + VSCode Light+ 代码色 | GitHub 蓝 `#0969da` | 900px |
| Github Modern | `github-modern.css` | GitHub 骨架 + 靛蓝重设计 | 靛蓝 `#5b5bd6` | 1280px |
| Mist Blue | `mist-blue.css` | 「晨光」母题，晨雾画布 | 湛蓝 `#2563eb` | 860px |
| Mist Green | `mist-green.css` | 同上，薄荷绿变体 | 薄荷绿 `#15803d` | 860px |
| Mist Github | `mist-github.css` | 同上，GitHub 蓝 + 中性灰装饰 | `#0366d6` | 860px |
| Notion Clean 极简无界 | `notion-clean.css` | Notion 式卡片、通透留白 | 靛蓝 `#3f51b5` | 880px |
| Universal Clean | `universal-clean.css` | 中性通用底子，适合二次开发 | 蓝 `#2563eb` | 860px |

## 安装

### 方式一：手动复制（推荐）

1. 打开 Typora → `文件` → `偏好设置` → `外观` → 点击 **打开主题文件夹**。
2. 把想要的 `.css` 文件复制进去（**必须放在 themes 根目录**，不能套子文件夹）。
3. 重启 Typora。
4. 在 `主题` 菜单里选择对应主题。

各平台主题目录位置：

| 平台 | 路径 |
| --- | --- |
| Windows | `%APPDATA%\Typora\themes` |
| macOS | `~/Library/Application Support/abnerworks.Typora/themes` |
| Linux | `~/.config/Typora/themes` |

### 方式二：克隆后复制

```bash
git clone https://github.com/ddz12123/typora-themes.git
cp typora-themes/*.css "$APPDATA/Typora/themes/"     # Windows (Git Bash)
# cp typora-themes/*.css ~/Library/Application\ Support/abnerworks.Typora/themes/   # macOS
# cp typora-themes/*.css ~/.config/Typora/themes/                                   # Linux
```

### 方式三：开发模式（改样式实时看效果）

不想每次改完都手动复制，可以建一个目录联接，让 Typora 直接读仓库里的文件：

```bat
mklink /J "%APPDATA%\Typora\themes\typora-themes" "%USERPROFILE%\code\typora-themes"
```

macOS / Linux 用软链接：

```bash
ln -s ~/code/typora-themes/*.css ~/.config/Typora/themes/
```

## 主题详解

### Celadon Mist 青雾

冷雾灰的窗体是「书桌」，带细描边和柔影的白纸是「正文」，视线自然收拢到版心。强调色只用一个克制的青瓷青，其余交给中性灰阶，不与正文争权重。人文无衬线 + 1.75 行高，中英混排、长文阅读、技术笔记都不违和。**不依赖任何网络字体与图片资源**，适合离线与导出。

### Geek Tech 极客工程

GitHub Primer 设计系统打底：严谨网格、硬朗层次、徽章式标签、规范表格；代码块移植 VSCode Light+ 语义高亮，行号与细线都按工程文档的尺度调过。适合写技术手册、API 文档、工程笔记。

### Github Modern

保留 GitHub 默认主题最舒服的清爽骨架，但**不是复刻**：强调色换成靛蓝，提示卡改成「浅色卡片 + 图标 + 大写标签」而非左边框条，列表用带柔光光环的靛蓝圆点，表格加了可见斑马线与 8px 圆角。版心 1280px，是仓库里最适合宽屏写作的一套，侧边栏、搜索、菜单、对话框也都统一了交互色。

### Mist 系列（Blue / Green / Github）

三套共用一套「清晨的雾」设计系统，只换强调色：

- `h1` 下方是日出渐变线，`h2` 左侧是实心侧条，`h3` 左侧是空心菱形；
- 列表用「实心菱形 → 圆点 → 空心圆」三级露珠递进，有序列表是等宽 `01/02` 编号；
- 代码块右上角自动读取语言名生成徽章（`content: attr(lang)`）；
- 表格是编辑部风格：去竖线，只留横向发丝线 + 表头强调色底线；
- 引用块是雾面卡片配大号装饰引号，分割线中央一颗「晨星」。

> 这三套没有单独为 Callout 做语义配色，`[!NOTE]` 等提示块会走统一的引用块样式。如果你重度使用 Callout，优先选另外四套。

### Notion Clean 极简无界

纯白通透底色、开阔版心、圆角 Callout、柔和阴影、胶囊状行内代码，整体气质接近 Notion 的默认页面。适合写笔记、整理知识库、做轻量文档。

### Universal Clean

最中性的一套：蓝色强调、克制的圆角、干净的层级，没有强烈的风格主张。**想改一套自己的主题，建议直接复制它当起点**，变量表组织得最规整。

## 自定义

### 改主色：一个变量

新建一个与主题同名的 `.user.css`（例如 `celadon-mist.user.css`），Typora 会自动加载它并覆盖主题样式：

```css
/* celadon-mist.user.css */
:root {
    --primary-color: #b4534b;          /* 换成朱砂红 */
    --primary-btn-border-color: #b4534b;
    --primary-color-hover: #96443d;
}
```

### 换字体

```css
:root {
    --font-sans: "LXGW WenKai", "PingFang SC", sans-serif;
    --monospace: "JetBrains Mono", "Cascadia Code", Consolas, monospace;
}
```

### 调版心宽度

```css
:root { --write-max-width: 1100px !important; }
```

> `!important` 是因为部分主题用媒体查询逐级放宽版心，需要提权覆盖。改之前先用 DevTools 确认变量名。

### 改颜色的通用原则

所有主题都把颜色集中在文件顶部的 `:root` 里，注释写明了每个变量的用途（纸/桌、文字、主色、线、代码、控件状态、选中/搜索、聚焦淡化）。**改主题只改这一节就够**，不用碰下面的选择器。

## 兼容性

- **Typora 1.x 桌面版**，开发环境为 Windows。macOS / Linux 未逐一回归，理论上通用，遇到问题欢迎提 issue。
- 全部为浅色主题。Windows / Linux 上 Typora 依据 `body` 背景色判断深浅模式，所以这些主题的 `body` 都是浅底——**请不要把它们改成深色**，否则 UI 会错乱。
- 代码块高亮走 CodeMirror 的 `.cm-s-inner`，源码模式走 `.cm-s-typora-default`，两者独立。
- Typora 版本迭代可能微调类名，遇到个别元素没被样式命中，用 DevTools 现查选择器最快。

## 目录结构

```
typora-themes/
├── celadon-mist.css        # 青雾
├── geek-tech.css           # 极客工程
├── github-modern.css       # 现代浅色
├── mist-blue.css           # Mist 湛蓝
├── mist-github.css         # Mist GitHub 蓝
├── mist-green.css          # Mist 薄荷绿
├── notion-clean.css        # 极简无界
├── universal-clean.css     # 通用底子
├── 测试.md                  # 全要素测试文档（标题/列表/表格/公式/图表/代码全覆盖）
├── 主题开发指南.md           # Typora 主题开发笔记：变量、选择器、常见坑
├── LICENSE
└── README.md
```

## 开发与测试

1. 用开发模式（见安装方式三）把仓库链进 Typora 主题目录。
2. 改完在 `主题` 菜单里重新点选一次当前主题即可刷新，改动较大时重启 Typora。
3. 用 `测试.md` 做回归：它覆盖了 h1~h6、多级列表、宽表格、五种 Callout、四种语言的代码块、行内与块级公式、Mermaid 流程图与时序图、`<details>` 折叠块、脚注、任务列表等。
4. 发布前再走一遍 `@media print`：导出 PDF 看分页、背景色、代码块是否正常。

`主题开发指南.md` 里整理了 CSS 变量表、常用选择器速查、代码高亮移植方法，以及 11 条踩坑记录，改样式前值得先翻一遍。

## 常见问题

**主题菜单里找不到新主题？**
文件名只能是小写字母、数字和 `-`，且必须直接放在 themes 根目录下；放完要重启 Typora。

**装上后整个界面变深色 / 颜色错乱？**
`body` 背景被改成了深色。浅色主题的 `body` 必须是浅底，这是 Typora 在 Win/Linux 上判断深浅模式的依据。

**偏好设置里拖字号滑杆没反应？**
基准字号要写在 `html` 上，正文用 `rem`。本仓库的主题都已处理，自己改的时候别退回 `px`。

**代码块没有语法高亮？**
类名是 `.cm-s-inner`，不是 `.cm-s-default` 或 `.cm-s-material`；源码模式则是 `.cm-s-typora-default`。

**想用深色模式怎么办？**
在偏好设置的「深色模式主题」里选内置的 `night` 或其他深色主题，浅色模式再选本仓库的主题，两者互不影响。

## 贡献

欢迎提 issue 和 PR：

- 报告样式问题时，请附上 Typora 版本、操作系统、截图，以及能复现的最小 Markdown 片段。
- 新增主题请遵循命名规范（小写 + `-`），颜色集中在 `:root`，并用 `测试.md` 过一遍全部要素。
- 基于现有主题改的，请在 PR 里注明原主题出处。

## License

[MIT](LICENSE) © 2026 ddz12123

可以自由使用、修改、商用，保留版权声明即可。
