<p align="center">
  <img src="https://img.shields.io/badge/HTML-Page%20Studio-3b82f6?style=for-the-badge&logo=html5&logoColor=white" alt="HTML Page Studio">
  <br/>
  <strong>零依赖 · 纯前端 · 开箱即用的 HTML 可视化编辑器</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
  <img src="https://img.shields.io/badge/Type-Pure%20Frontend-blue.svg" alt="Type">
  <img src="https://img.shields.io/badge/Size-~35KB-orange.svg" alt="Size">
  <img src="https://img.shields.io/badge/Dependencies-0-success.svg" alt="Dependencies">
</p>

---

## 什么是 HTML Page Studio？

一个**零依赖、纯前端**的 HTML 可视化编辑器。导入任意 HTML 文件，直接在画布上点击编辑文字、替换图片，支持多页翻页，一键导出为独立 HTML 文件分享给任何人。

**不需要服务器、不需要安装、不需要注册账号。** 下载 `index.html`，双击打开就能用。

## 特性

- **导入 HTML 文件** — 支持拖放或选择本地 `.html/.htm` 文件
- **智能分页识别** — 自动识别 `.slide` 幻灯片结构、`<hr>` 分页标记、`<section>` 区块
- **所见即所得编辑** — 点击文字直接编辑，选中弹出富文本工具栏
- **图片/视频替换** — 点击媒体元素弹窗输入新 URL 即可替换
- **多页管理** — 底部导航条翻页，支持插入/删除页面
- **一键导出** — 导出为独立 HTML 文件，双击即可打开查看
- **本地保存** — localStorage 自动存储编辑进度，刷新不丢失
- **全页预览** — 新窗口预览包含所有分页的完整效果
- **零依赖** — 纯 HTML/CSS/JS，无需 Node.js、无需构建工具

## 多语言支持

| 文件 | 语言 | 说明 |
|------|------|------|
| `index.html` | 中文 | 默认入口，中文界面 |
| `index-en.html` | English | 英文界面 |

## 在线体验

直接打开项目中的 `index.html`（中文版）或 `index-en.html`（英文版）即可使用，无需任何环境配置。

## 快速开始

### 方式一：直接使用（推荐）

1. 下载 `index.html`
2. 双击用浏览器打开
3. 导入 HTML 文件或粘贴源码，开始编辑

### 方式二：本地预览

```bash
# 用任意静态服务器打开（可选）
npx serve .
# 或
python -m http.server 8080
```

### 方式三：部署到 GitHub Pages

1. Fork 本仓库
2. Settings → Pages → Source 选择 `main` 分支 → Save
3. 访问 `https://yourname.github.io/html-page-editor/`

## 支持的 HTML 分页格式

| 格式 | 示例 | 说明 |
|------|------|------|
| `.slide` 幻灯片 | `<section class="slide">` | 自动识别 beautiful-html-templates 等模板 |
| `page-break` 标记 | `<hr class="page-break">` | 按标记拆分 |
| 连续 `<hr>` 分页 | `<hr><hr>` | 至少 2 个水平线 |
| `<section>` 区块 | `<section>...</section>` | 至少 2 个区块 |
| 单页 | 任意 HTML | 默认整页为一页 |

## 工作流程

```
导入 HTML → 智能分页 → 画布编辑 → 预览确认 → 导出分享
```

1. **导入**：拖入 HTML 文件或粘贴源码
2. **编辑**：点击文字直接修改，选中弹出格式工具栏
3. **翻页**：底部导航条管理多页内容
4. **导出**：点击「导出HTML」下载文件，发给朋友即可

## 技术栈

- **零依赖** — 纯原生 HTML5 + CSS3 + JavaScript
- **contentEditable** — 浏览器原生富文本编辑 API
- **DOMParser** — HTML 解析与分页引擎
- **localStorage** — 本地数据持久化
- **Blob API** — 客户端文件生成与下载

## 项目结构

```
html-page-editor/
├── index.html      # 编辑器 - 中文版（默认）
├── index-en.html   # 编辑器 - English version
├── README.md       # 项目说明
├── LICENSE         # MIT 开源协议
└── .gitignore      # Git 忽略规则
```

## 浏览器兼容

| 浏览器 | 版本要求 |
|--------|---------|
| Chrome | 80+ |
| Edge | 80+ |
| Firefox | 78+ |
| Safari | 14+ |

## 常见问题

<details>
<summary><b>导出的 HTML 文件别人能直接打开吗？</b></summary>
能。导出的是完全独立的 HTML 文件，包含所有样式和内容，双击即可用浏览器打开，无需服务器。
</details>

<details>
<summary><b>支持哪些 HTML 模板？</b></summary>
支持所有标准 HTML。特别优化了对 `.slide` 幻灯片结构模板的识别（如 [beautiful-html-templates](https://github.com/nicehash/beautiful-html-templates)），会自动分页并保留完整样式。
</details>

<details>
<summary><b>编辑内容保存在哪里？</b></summary>
保存在浏览器 localStorage 中。清除浏览器数据会丢失保存记录，建议及时导出下载。
</details>

<details>
<summary><b>能编辑 CSS 样式吗？</b></summary>
当前版本支持文字格式编辑（加粗、斜体、颜色、对齐）。CSS 样式编辑可以通过「源码编辑」标签手动修改。
</details>

## 贡献

欢迎提交 Issue 和 PR！

1. Fork 本仓库
2. 创建特性分支：`git checkout -b feature/amazing-feature`
3. 提交改动：`git commit -m 'Add amazing feature'`
4. 推送分支：`git push origin feature/amazing-feature`
5. 提交 PR

## License

[MIT](LICENSE) © leefrane-creator
