# HydroMark

**A WYSIWYG Markdown editor add-in for Microsoft OneNote — now with an AI assistant that writes into your notes.**

Type Markdown directly inside OneNote and watch it render instantly — no exports, no switching apps. Built for developers, students, and technical writers who love OneNote but can't live without Markdown. And as of **v1.1.0**, just tell the built-in AI assistant what you need — an article, a table, a page operation — and it lands in your notes, rendered.

---

> ⚠️ **This repository is NOT open source.** It exists only for product documentation, announcements, and community feedback (Issues & Discussions). The HydroMark source code is proprietary and is **not** published here. See [License & Source Code](#license--source-code) below.

---

## ✨ Features

### 🤖 AI Assistant — the headline feature (new in 1.1.0)

Most AI sidebars hand you a wall of text to copy-paste. HydroMark's assistant **writes into your notes**:

- **Executes add-in actions, not just chat** — it can insert a fully rendered article, build tables, run page operations (render, export, TOC, page width), and the action results feed back into the conversation so the model can confirm or self-correct.
- **Tables on command, with the width you asked for** — `insert_table` supports full-page-width and **content-fitted** layouts; the AI path shares the same table engine as the new `Alt+W` width toggle.
- **Bring your own model** — 15 providers built in (OpenAI, DeepSeek, Kimi, Zhipu, Qwen…), custom Base URL for anything else. Your API key stays on your machine; no middleman server.
- **Multimodal** — paste a screenshot into the chat and reference it with multimodal models.
- **Language-following** — ask in Chinese, get Chinese; ask in English, get English.
- **Included in every license** — the 14-day free trial and all paid tiers. Open it with `Alt+A` or the ribbon's **AI** group.

### 📝 Markdown rendering

- **Real-time Markdown rendering** — type Markdown, press Enter, see it formatted instantly (WYSIWYG).
- **Source / rendered dual view** — toggle between raw Markdown and rendered output anytime.
- **Code highlighting** — clean syntax highlighting for dozens of languages.
- **LaTeX math** — inline and block formulas rendered as native OneNote equations.
- **Mermaid / ZenUML diagrams** — draw flowcharts, sequence diagrams, and more.
- **Tables with full-width ↔ content-fitted toggle** — tables render full-page-width by default; `Alt+W` switches any table bidirectionally, and the content-fitted state persists.
- **Slash commands** — insert blocks the fast way.
- **Highlight blocks** — call out important notes visually.
- **Full dark-mode adaptation** — rendered content, dialogs and the AI sidebar all follow OneNote's theme.
- **Seamless import / export** — Markdown files in and out.

## 🌐 Official Links

- Website (English): https://hydromark.hydrolinx.top
- Website (中文): https://hydromark.hydrolinx.cn
- Documentation: https://hydromark.hydrolinx.top/documentation
- Pricing: https://hydromark.hydrolinx.top/pricing

## 💬 Feedback & Support

This is the best place to reach us:

- 🐛 **Bug reports & feature requests** → open an [Issue](../../issues)
- 💡 **Ideas & general discussion** → use [Discussions](../../discussions)
- 📧 **Email** → support@hydrolinx.top

Before opening an issue, please search existing ones to avoid duplicates, and include your Windows / OneNote version and steps to reproduce.

## 🗺️ Roadmap

We're actively improving HydroMark. Near-term:

- Smarter AI actions — smart summaries, auto-tagging, and more add-in operations the assistant can execute
- More diagram types and block templates
- Broader OneNote integration

Follow the [Releases](../../releases) page for update notes.

## 📄 License & Source Code

HydroMark is **proprietary software**. The source code is **not open source** and is not distributed through this repository. All rights reserved.

You are welcome to:

- Read the documentation and announcements here
- File issues and join discussions to help us improve

You may **not**, without explicit written permission:

- Copy, modify, or redistribute the HydroMark source code
- Use the HydroMark name / brand in derivative products

© HydroLinx. All rights reserved.

---

*HydroMark — Markdown, the way OneNote should have had it. Now with an AI assistant that does the typing.*
