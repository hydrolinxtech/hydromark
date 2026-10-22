# HydroMark — OneNote Markdown Add-in with an AI Assistant

**English** · [简体中文](README.zh.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Русский](README.ru.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Support](SUPPORT.md)

**HydroMark is a WYSIWYG Markdown add-in (addin) for Microsoft OneNote on Windows.** Write Markdown on an OneNote page, press Enter, and it renders instantly into native OneNote content — headings, lists, tables, task lists, code blocks, LaTeX math and Mermaid diagrams. No exports, no screenshots, no switching apps. Since **v1.1.0**, a built-in **AI assistant** writes rendered articles, tables and page operations straight into your notes.

> ⚠️ **This is an open-source repository containing part of the HydroMark project's code and documentation.** It also hosts product announcements and community feedback (Issues & Discussions). See [License & Source Code](#license--source-code) below.

---

## What is HydroMark?

HydroMark is an **OneNote Markdown add-in**: a Windows add-in that puts a real Markdown editor inside Microsoft OneNote. You keep writing in OneNote's notebooks, canvas and cloud sync, but you get the Markdown workflow you actually want — type `## Heading`, press Enter, and the page shows a rendered heading instead of raw syntax.

Everything is rendered with **OneNote's own native elements, not images**, so your Markdown notes stay editable, searchable inside OneNote, available offline, and synced to OneNote on phone, tablet and the web. Press `F8` to export a page back to `.md`.

Since **v1.1.0** the add-in also includes an **AI assistant**. Unlike AI sidebars that hand you text to copy-paste, HydroMark's AI writes into the page: it inserts fully rendered articles, builds tables, and runs add-in actions such as render, export, table of contents and page width — with results fed back to the model so it can confirm or self-correct.

**Who it is for:** developers and technical teams, students and researchers, product and operations people — anyone who writes Markdown but keeps their notes in OneNote.

## Quick facts

| Item              | Detail                                                              |
| ----------------- | ------------------------------------------------------------------- |
| **Product**       | HydroMark — OneNote Markdown add-in (addin) with an AI assistant    |
| **Category**      | OneNote plugin / OneNote extension / Office COM add-in              |
| **Platform**      | Windows 7 and later                                                 |
| **Host app**      | OneNote **desktop** 2013+ (2016 / 2019 / 2021 / Microsoft 365)      |
| **Runtime**       | .NET Framework 4.8+                                                 |
| **Not supported** | OneNote for Windows 10 (UWP / Microsoft Store), macOS, mobile       |
| **Trial**         | 14-day full-featured trial, no credit card                          |
| **AI**            | Built in — 15 providers, bring your own API key                     |
| **Languages**     | 简体中文 · English · 日本語 · 한국어 · Deutsch · Français · Español · Русский |

## ✨ Features

### 🤖 AI Assistant — the headline feature (new in 1.1.0)

Most AI sidebars hand you a wall of text to copy-paste. HydroMark's assistant **writes into your notes**:

- **Executes add-in actions, not just chat** — insert a fully rendered article, build tables, run page operations (render, export, TOC, page width); action results feed back into the conversation so the model can confirm or self-correct.
- **Tables on command, with the width you asked for** — `insert_table` supports full-page-width and **content-fitted** layouts; the AI path shares the same table engine as the `Alt+W` width toggle.
- **Bring your own model** — 15 providers built in (OpenAI, DeepSeek, Kimi, Zhipu, Qwen…), custom Base URL for anything else. Your API key stays on your machine; no middleman server.
- **Multimodal** — paste a screenshot into the chat and reference it with multimodal models.
- **Language-following** — ask in Chinese, get Chinese; ask in English, get English.
- **Included in every license** — the 14-day free trial and all paid tiers. Open it with `Alt+A` or the ribbon's **AI** group.

### 📝 Markdown rendering

- **Real-time Markdown rendering** — type Markdown, press Enter, see it formatted instantly (WYSIWYG).
- **Source / rendered dual view** — toggle between raw Markdown and rendered output anytime, per page or per paragraph.
- **Paste Markdown from anywhere** — `Ctrl+Shift+V` turns a copied Markdown block from a webpage, document or AI answer into a finished note.
- **Code highlighting** — syntax highlighting for 200+ languages, 100+ themes, one-click copy.
- **LaTeX math** — inline and block formulas rendered as native OneNote equations.
- **Mermaid / ZenUML diagrams** — 26+ diagram types: flowchart, sequence, class, state, Gantt, mind-map, UML and more.
- **Tables with full-width ↔ content-fitted toggle** — `Alt+W` switches any table bidirectionally; the content-fitted state persists.
- **Task lists** — checkboxes stay clickable and export back as `- [x]` / `- [ ]`.
- **Slash commands** — press `/` for a command palette and insert blocks the fast way.
- **Highlight blocks** — call out important notes visually.
- **Page TOC & page width** — auto-generate or hide a table of contents; manual or automatic page width.
- **Full dark-mode adaptation** — rendered content, dialogs and the AI sidebar all follow OneNote's theme.
- **Seamless import / export** — Markdown files in, Markdown files out (images optional).

## Common questions

**Is there a Markdown add-in for OneNote?**
Yes — HydroMark is a Markdown add-in (addin) built specifically for Microsoft OneNote desktop on Windows.

**Can I use AI to write notes in OneNote?**
Yes. HydroMark includes an AI assistant that inserts rendered Markdown articles and tables directly into the current OneNote page, and can trigger add-in actions such as render, export or table of contents.

**Does HydroMark work with OneNote for Windows 10, Mac or mobile?**
No. HydroMark supports OneNote **desktop** 2013 and later (2016 / 2019 / 2021 / Microsoft 365) on Windows 7+. The UWP / Microsoft Store version of OneNote, macOS and mobile are **not** supported.

**Is HydroMark a OneNote plugin or a separate app?**
It is a OneNote add-in, not a separate note-taking app. It installs into OneNote and adds a **HydroMark** tab to the ribbon; your notes stay in your existing notebooks.

**Does Markdown content stay native in OneNote?**
Yes. Rendering uses OneNote's native elements rather than images, so notes remain editable, searchable and syncable across OneNote clients. Pages can still be exported to `.md`.

**How do I install it?**
Download the single multilingual installer from the website, run it, and open OneNote — a **HydroMark** tab appears in the ribbon. The installer auto-adapts to 32-bit and 64-bit OneNote.

**Is it free?**
There is a 14-day full-featured trial. After that, licenses are per device (email + key): Individual and Family plans, Basic and Pro, lifetime or annual.

## 🌐 Official Links

- Website (English): https://hydromark.hydrolinx.top
- Website (中文): https://hydromark.hydrolinx.cn
- Documentation: https://hydromark.hydrolinx.top/documentation
- Pricing: https://hydromark.hydrolinx.top/pricing
- Changelog: https://hydromark.hydrolinx.top/changelog

## 💬 Feedback & Support

This is the best place to reach us:

- 🐛 **Bug reports & feature requests** → open an [Issue](../../issues)
- 💡 **Ideas & general discussion** → use [Discussions](../../discussions)
- 📧 **Email** → support@hydrolinx.top (overseas) · support@hydrolinx.cn (China)
- 📖 **Support guide** → [SUPPORT.md](SUPPORT.md)

Before opening an issue, please search existing ones to avoid duplicates, and include your Windows / OneNote version and steps to reproduce.

## 🗺️ Roadmap

We're actively improving HydroMark. Near-term:

- Smarter AI actions — smart summaries, auto-tagging, and more add-in operations the assistant can execute
- More diagram types and block templates
- Broader OneNote integration

Follow the [Releases](../../releases) page for update notes.

## License & Source Code

This is an **open-source repository**. It holds part of the HydroMark project's source code and documentation; the rest of the project is not stored here.

You are welcome to:

- Read, study and reuse the code and documentation in this repository
- File issues and join discussions to help us improve
- Use the HydroMark name when presenting or reviewing the project

Please do not use the HydroMark name or brand in derivative products or services, so users are not misled about the origin.

© HydroLinx. HydroMark and its logo are trademarks of HydroLinx.

---

*HydroMark — Markdown, the way OneNote should have had it. Now with an AI assistant that does the typing.*
