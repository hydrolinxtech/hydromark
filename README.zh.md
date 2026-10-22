# HydroMark — 带 AI 助手的 OneNote Markdown 插件

[English](README.md) · **简体中文** · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Русский](README.ru.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [支持](SUPPORT.zh.md)

**HydroMark 是一款面向 Windows 上 Microsoft OneNote 的所见即所得 Markdown 插件。** 在 OneNote 页面上书写 Markdown，按下 Enter，内容即刻渲染为 OneNote 原生内容——标题、列表、表格、任务列表、代码块、LaTeX 公式与 Mermaid 图表。无需导出、无需截图、无需切换应用。自 **v1.1.0** 起，内置的 **AI 助手**可将渲染后的文章、表格和页面操作直接写入你的笔记。

> ⚠️ **本仓库为部分开源：此处发布部分代码与文档。** 同时用于产品公告和社区反馈（Issues 与 Discussions）。详见下方[许可与源代码](#许可与源代码)。

---

## HydroMark 是什么？

HydroMark 是一款 **OneNote Markdown 插件**：一个把真正的 Markdown 编辑器放进 Microsoft OneNote 的 Windows 插件。你继续使用 OneNote 的笔记本、画布和云同步，同时获得你真正想要的 Markdown 工作流——输入 `## Heading`，按下 Enter，页面就会显示渲染后的标题，而不是原始语法。

所有内容都以 **OneNote 原生元素渲染，而非图片**，因此你的 Markdown 笔记始终保持可编辑、可在 OneNote 内搜索、可离线使用，并与手机、平板和网页版 OneNote 同步。按 `F8` 可将页面导出回 `.md`。

自 **v1.1.0** 起，该插件还内置了 **AI 助手**。不同于那些只给你一段文本供你复制粘贴的 AI 侧边栏，HydroMark 的 AI 会直接写入页面：它插入完整渲染的文章、构建表格，并执行渲染、导出、目录和页面宽度等插件操作——操作结果会回传给模型，以便其确认或自我修正。

**适用人群：** 开发者与技术团队、学生与研究人员、产品与运营人员——任何用 Markdown 写作、但把笔记保存在 OneNote 中的人。

## 快速了解

| 项目              | 详情                                                                |
| ----------------- | ------------------------------------------------------------------- |
| **产品**          | HydroMark — 带 AI 助手的 OneNote Markdown 插件                       |
| **类别**          | OneNote 插件 / OneNote 扩展 / Office COM 加载项                      |
| **平台**          | Windows 7 及更高版本                                                |
| **宿主应用**      | OneNote **桌面版** 2013+（2016 / 2019 / 2021 / Microsoft 365）      |
| **运行时**        | .NET Framework 4.8+                                                 |
| **不支持**        | OneNote for Windows 10（UWP / Microsoft Store）、macOS、移动端      |
| **试用**          | 14 天全功能试用，无需信用卡                                          |
| **AI**            | 内置 — 15 家服务商，自带 API 密钥                                    |
| **语言**          | 简体中文 · English · 日本語 · 한국어 · Deutsch · Français · Español · Русский |

## ✨ 功能

### 🤖 AI 助手 — 主打功能（1.1.0 新增）

大多数 AI 侧边栏只会甩给你一大段文字让你复制粘贴。HydroMark 的助手则**直接写入你的笔记**：

- **执行插件操作，而不只是聊天** — 插入完整渲染的文章、构建表格、执行页面操作（渲染、导出、目录、页面宽度）；操作结果会反馈到对话中，让模型能够确认或自我修正。
- **按需生成表格，宽度随心** — `insert_table` 支持整页宽度和**内容自适应**布局；AI 路径与 `Alt+W` 宽度切换共用同一套表格引擎。
- **自带模型** — 内置 15 家服务商（OpenAI、DeepSeek、Kimi、Zhipu、Qwen……），其他模型可自定义 Base URL。你的 API 密钥始终保存在本机，不经过任何中间服务器。
- **多模态** — 可将截图粘贴到聊天中，并使用多模态模型引用它。
- **语言跟随** — 用中文提问，得到中文回答；用英文提问，得到英文回答。
- **所有授权均包含** — 14 天免费试用及所有付费档位。用 `Alt+A` 或功能区中的 **AI** 组打开。

### 📝 Markdown 渲染

- **实时 Markdown 渲染** — 输入 Markdown，按下 Enter，即刻看到格式化效果（所见即所得）。
- **源码 / 渲染双视图** — 随时在原始 Markdown 与渲染结果之间切换，可按页面或按段落切换。
- **从任意来源粘贴 Markdown** — `Ctrl+Shift+V` 可将从网页、文档或 AI 回答中复制的 Markdown 片段变成一篇完成的笔记。
- **代码高亮** — 支持 200+ 种语言、100+ 种主题的语法高亮，一键复制。
- **LaTeX 数学公式** — 行内公式与块级公式均渲染为 OneNote 原生公式。
- **Mermaid / ZenUML 图表** — 26+ 种图表类型：流程图、时序图、类图、状态图、甘特图、思维导图、UML 等。
- **表格整页宽度 ↔ 内容自适应切换** — `Alt+W` 可双向切换任意表格；内容自适应状态会被保留。
- **任务列表** — 复选框保持可点击，并可导出为 `- [x]` / `- [ ]`。
- **斜杠命令** — 按 `/` 打开命令面板，快速插入内容块。
- **高亮块** — 以视觉方式突出重要笔记。
- **页面目录与页面宽度** — 自动生成或隐藏目录；手动或自动调整页面宽度。
- **完整的深色模式适配** — 渲染内容、对话框和 AI 侧边栏均跟随 OneNote 主题。
- **无缝导入 / 导出** — Markdown 文件进，Markdown 文件出（图片可选）。

## 常见问题

**OneNote 有 Markdown 插件吗？**
有——HydroMark 是专为 Windows 上的 Microsoft OneNote 桌面版打造的 Markdown 插件。

**我可以在 OneNote 中用 AI 写笔记吗？**
可以。HydroMark 内置 AI 助手，可将渲染后的 Markdown 文章和表格直接插入当前 OneNote 页面，并能触发渲染、导出或目录等插件操作。

**HydroMark 支持 OneNote for Windows 10、Mac 或移动端吗？**
不支持。HydroMark 支持 Windows 7+ 上的 OneNote **桌面版** 2013 及更高版本（2016 / 2019 / 2021 / Microsoft 365）。OneNote 的 UWP / Microsoft Store 版本、macOS 和移动端均**不**受支持。

**HydroMark 是 OneNote 插件还是一个独立应用？**
它是一个 OneNote 插件，而不是独立的笔记应用。它会安装到 OneNote 中，并在功能区添加一个 **HydroMark** 选项卡；你的笔记仍保留在现有笔记本中。

**Markdown 内容在 OneNote 中会保持原生吗？**
会。渲染使用 OneNote 的原生元素而非图片，因此笔记保持可编辑、可搜索，并能在各 OneNote 客户端之间同步。页面仍可导出为 `.md`。

**如何安装？**
从官网下载单一多语言安装程序，运行后打开 OneNote——功能区中会出现一个 **HydroMark** 选项卡。安装程序会自动适配 32 位和 64 位 OneNote。

**是免费的吗？**
提供 14 天全功能试用。之后按设备授权（邮箱 + 密钥）：个人版与家庭版、基础版与专业版，可选永久或按年。

## 🌐 官方链接

- 中文站：https://hydromark.hydrolinx.cn
- 国际站（English）：https://hydromark.hydrolinx.top
- 文档：https://hydromark.hydrolinx.cn/documentation
- 定价：https://hydromark.hydrolinx.cn/pricing
- 更新日志：https://hydromark.hydrolinx.cn/changelog

## 💬 反馈与支持

这里是与我们联系的最佳渠道：

- 🐛 **缺陷报告与功能请求** → 提交 [Issue](../../issues)
- 💡 **想法与一般性讨论** → 使用 [Discussions](../../discussions)
- 📧 **邮箱** → support@hydrolinx.cn
- 📖 **支持指南** → [SUPPORT.zh.md](SUPPORT.zh.md)

提交 issue 之前，请先搜索已有 issue 以避免重复，并附上你的 Windows / OneNote 版本和复现步骤。

## 🗺️ 路线图

我们正在积极改进 HydroMark。近期计划：

- 更智能的 AI 操作——智能摘要、自动打标签，以及更多助手可执行的插件操作
- 更多图表类型与内容块模板
- 更深入的 OneNote 集成

请关注 [Releases](../../releases) 页面获取更新说明。

## 许可与源代码

HydroMark 是**专有软件**。源代码**并非开源**，也不通过本仓库分发。保留所有权利。

欢迎你：

- 阅读此处的文档和公告
- 提交 issue 并参与讨论，帮助我们改进

未经明确的书面许可，你**不得**：

- 复制、修改或再分发 HydroMark 源代码
- 在衍生产品中使用 HydroMark 名称 / 品牌

© HydroLinx. 保留所有权利。

---

*HydroMark — Markdown，OneNote 本该有的样子。现在更配有会替你打字的 AI 助手。*
