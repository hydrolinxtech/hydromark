<div align="center">

<img src="assets/hydromark-logo.png" alt="HydroMark" width="520" />

**OneNote Markdown 外掛、AI 助理與效率工具**

[![Release](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.hydromark.hydrolinx.top%2Fapi%2Fversion&query=%24.version&label=Release&color=2ea44f)](https://hydromark.hydrolinx.top/download)

[![X](https://img.shields.io/badge/X-@hydrolinxtech-000000?logo=x&logoColor=white)](https://x.com/hydrolinxtech) [![Product Hunt](https://img.shields.io/badge/Product%20Hunt-@hydrolinx-da7651?logo=producthunt&logoColor=white)](https://www.producthunt.com/@hydrolinx) [![YouTube](https://img.shields.io/badge/YouTube-@hydrolinxtechglobal-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/@hydrolinxtechglobal) [![Instagram](https://img.shields.io/badge/Instagram-hydrolinx.top-E4405F?logo=instagram&logoColor=white)](https://www.instagram.com/hydrolinx.top/)

![HydroMark 在 OneNote 中執行的介面：HydroMark 索引標籤、頁面上渲染完成的 Markdown、目錄面板與 AI 助理面板](assets/hydromark-onenote.png)

更多資訊請查閱我們的[文件](https://hydromark.hydrolinx.cn/documentation)

[English](README.md) · [简体中文](README.zh.md) · **繁體中文** · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Português](README.pt.md) · [Русский](README.ru.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [支援](SUPPORT.zh-TW.md)

</div>

# HydroMark — 內建 AI 助理的 OneNote Markdown 外掛

**HydroMark 是一款面向 Windows 上 Microsoft OneNote 的所見即所得 Markdown 外掛（add-in）。** 在 OneNote 頁面上書寫 Markdown，輸入即渲染為 OneNote 原生內容（`#` 加空格成標題、`-` 加空格成清單）——標題、清單、表格、工作清單、程式碼區塊、LaTeX 公式與 Mermaid 圖表。無需匯出、無需螢幕擷取、無需切換應用程式。自 **v1.1.0** 起，內建的 **AI 助理**可將渲染後的文章、表格與頁面操作直接寫入你的筆記。

> ⚠️ **本儲存庫為開放原始碼儲存庫，存放 HydroMark 專案的部分程式碼與文件。** 同時用於產品公告與社群回饋（Issues 與 Discussions）。詳情見下方[授權與原始碼](#授權與原始碼)。

---

## HydroMark 是什麼？

HydroMark 是一款 **OneNote Markdown 外掛**：一個把真正的 Markdown 編輯器放進 Microsoft OneNote 的 Windows 外掛。你繼續使用 OneNote 的筆記本、畫布與雲端同步，同時獲得你真正想要的 Markdown 工作流——輸入 `## Heading` 再敲空格，頁面就會顯示渲染後的標題，而不是原始語法。

所有內容都以 **OneNote 原生元素渲染，而非圖片**，因此你的 Markdown 筆記始終保持可編輯、可在 OneNote 內搜尋、可離線使用，並與手機、平板和網頁版 OneNote 同步。按 `F8` 可將頁面匯出回 `.md`。

自 **v1.1.0** 起，該外掛也內建了 **AI 助理**。不同於只給你一段文字供你複製貼上的 AI 側邊欄，HydroMark 的 AI 會直接寫入頁面：插入完整渲染的文章、建立表格，並執行渲染、匯出、目錄與頁面寬度等外掛操作——操作結果會回傳給模型，以便其確認或自我修正。

**適用對象：** 開發者與技術團隊、學生與研究人員、產品與營運人員——任何用 Markdown 寫作、卻把筆記保存在 OneNote 中的人。

## 快速了解

| 項目              | 內容                                                                |
| ----------------- | ------------------------------------------------------------------- |
| **產品**          | HydroMark — 內建 AI 助理的 OneNote Markdown 外掛                     |
| **類別**          | OneNote 外掛 / OneNote 擴充功能 / Office COM 增益集                  |
| **平台**          | Windows 7 及更高版本                                                 |
| **宿主應用程式**  | OneNote **桌面版** 2013+（2016 / 2019 / 2021 / Microsoft 365）       |
| **執行環境**      | .NET Framework 4.8+                                                 |
| **不支援**        | OneNote for Windows 10（UWP / Microsoft Store）、macOS、行動版       |
| **試用**          | 14 天全功能試用，無需信用卡                                          |
| **AI**            | 內建 — 14 家供應商，自備 API 金鑰                                    |
| **語言**          | English · 简体中文 · 繁體中文 · 日本語 · 한국어 · Español · Português · Русский · Deutsch · Français · हिन्दी · العربية |

## ✨ 功能

| 功能 | 說明 | 快捷鍵 |
| --- | --- | --- |
| 🤖 **AI 助理** | 在頁面中直接寫入渲染後的文章、表格並執行外掛操作 | `Alt+A` |
| ✍️ **即時渲染** | 標題、清單等輸入即成型 | `#` / `-` + 空格 |
| 🔁 **原始碼 ↔ 渲染** | 隨時在原始 Markdown 與渲染結果間切換，可依頁面或段落 | — |
| 📥 **貼上 Markdown** | 將複製的 Markdown 片段變成一篇完成的筆記 | `Ctrl+Shift+V` |
| 💻 **程式碼突顯** | 200+ 種語言、100+ 種主題，一鍵複製 | — |
| ∑ **LaTeX 公式** | 行內與區塊公式渲染為 OneNote 原生公式 | `$…$` |
| 📊 **圖表** | 26+ 種 Mermaid / ZenUML：流程圖、時序圖、甘特圖、心智圖…… | — |
| ▱ **表格** | 整頁寬度 ↔ 內容自適應切換，狀態保留 | `Alt+W` |
| ☑️ **工作清單** | 核取方塊可點選，匯出為 `- [x]` / `- [ ]` | — |
| ⌨️ **斜線命令** | 按 `/` 開啟命令面板快速插入區塊 | `/` |
| 🖍️ **突顯區塊** | 以視覺方式突出重要筆記 | — |
| 📑 **頁面目錄與寬度** | 自動產生目錄；手動或自動調整頁面寬度 | — |
| 🌙 **深色模式** | 渲染內容、對話方塊與 AI 側邊欄均跟隨 OneNote | — |
| 🔄 **匯入 / 匯出** | Markdown 檔案進、Markdown 檔案出（圖片可選） | `F8` |

### 🤖 AI 助理 — 主打功能（1.1.0 新增）

大多數 AI 側邊欄只會丟給你一大段文字讓你複製貼上。HydroMark 的助理則**直接寫入你的筆記**：

- **執行外掛操作，而不只是聊天** — 插入完整渲染的文章、建立表格、執行頁面操作（渲染、匯出、目錄、頁面寬度）；操作結果會回饋到對話中，讓模型能夠確認或自我修正。
- **依需求產生表格，寬度隨心** — `insert_table` 支援整頁寬度與**內容自適應**版面；AI 路徑與 `Alt+W` 寬度切換共用同一套表格引擎。
- **自備模型** — 內建 14 家供應商（OpenAI、DeepSeek、Kimi、Zhipu、Qwen……），其他模型可自訂 Base URL。你的 API 金鑰始終保存在本機，不經過任何中介伺服器。
- **多模態** — 可將螢幕擷取貼到對話中，並使用多模態模型引用它。
- **語言跟隨** — 用繁體中文提問，就得到繁體中文回答；用英文提問，就得到英文回答。
- **所有授權皆包含** — 14 天免費試用與所有付費方案均可使用。以 `Alt+A` 或功能區中的 **AI** 群組開啟。

### 📝 Markdown 渲染

- **即時 Markdown 渲染** — 輸入 `#` 或 `-` 後敲空格即刻成型，其他區塊語法按 Enter 或 F5 渲染（所見即所得）。
- **原始碼 / 渲染雙檢視** — 隨時在原始 Markdown 與渲染結果之間切換，可依頁面或依段落切換。
- **從任何來源貼上 Markdown** — `Ctrl+Shift+V` 可將在網頁、文件或 AI 回答中複製的 Markdown 片段變成一篇完成的筆記。
- **程式碼突顯** — 支援 200+ 種語言、100+ 種主題的語法突顯，一鍵複製。
- **LaTeX 數學公式** — 行內公式與區塊公式均渲染為 OneNote 原生公式。
- **Mermaid / ZenUML 圖表** — 26+ 種圖表類型：流程圖、序列圖、類別圖、狀態圖、甘特圖、心智圖、UML 等。
- **表格整頁寬度 ↔ 內容自適應切換** — `Alt+W` 可雙向切換任意表格；內容自適應狀態會被保留。
- **工作清單** — 核取方塊保持可點選，並可匯出為 `- [x]` / `- [ ]`。
- **斜線命令** — 按 `/` 開啟命令面板，快速插入內容區塊。
- **突顯區塊** — 以視覺方式突顯重要筆記。
- **頁面目錄與頁面寬度** — 自動產生或隱藏目錄；手動或自動調整頁面寬度。
- **完整的深色模式支援** — 渲染內容、對話方塊與 AI 側邊欄均跟隨 OneNote 主題。
- **無縫匯入 / 匯出** — Markdown 檔案進，Markdown 檔案出（圖片可選）。

## 🚀 快速開始

1. **下載** 單一多語系安裝程式（[下載頁](https://hydromark.hydrolinx.cn/download)，需 Windows 7+ 與 OneNote **桌面版** 2013+）。
2. **執行** 安裝程式——它會自動適應 32 位元與 64 位元 OneNote，無需選擇 x86 / x64 版本。
3. **開啟 OneNote**，在功能區中找到 **HydroMark** 索引標籤。
4. **書寫 Markdown** —— 輸入 `## ` 再敲空格得到標題，`- ` 再敲空格得到清單；其他區塊按 Enter 或 `F5` 渲染。
5. **先配置 AI**：開啟「設定 → AI 大模型」，選擇服務商並填入你的 API 金鑰（自備金鑰，內建 14 家服務商）。配置好後按 `Alt+A`（或功能區中的 **AI** 群組）開啟 **AI 助理**，讓它把文章和表格直接寫進頁面。
6. **匯出** 當前頁面為 `.md`：按 `F8`。

14 天全功能試用自動開始，無需信用卡。完整指南請見[文件](https://hydromark.hydrolinx.cn/documentation)。

## 常見問題

**OneNote 有 Markdown 外掛嗎？**
有——HydroMark 是專為 Windows 上的 Microsoft OneNote 桌面版打造的 Markdown 外掛。

**我可以在 OneNote 中用 AI 寫筆記嗎？**
可以。HydroMark 內建 AI 助理，可將渲染後的 Markdown 文章與表格直接插入目前的 OneNote 頁面，並能觸發渲染、匯出或目錄等外掛操作。

**HydroMark 支援 OneNote for Windows 10、Mac 或行動版嗎？**
不支援。HydroMark 支援 Windows 7+ 上的 OneNote **桌面版** 2013 及更高版本（2016 / 2019 / 2021 / Microsoft 365）。OneNote 的 UWP / Microsoft Store 版本、macOS 與行動版均**不**受支援。

**HydroMark 是 OneNote 外掛還是獨立應用程式？**
它是 OneNote 外掛，而不是獨立的筆記應用程式。它會安裝到 OneNote 中，並在功能區新增一個 **HydroMark** 索引標籤；你的筆記仍保留在既有筆記本中。

**Markdown 內容在 OneNote 中會保持原生嗎？**
會。渲染使用 OneNote 的原生元素而非圖片，因此筆記保持可編輯、可搜尋，並能在各 OneNote 用戶端之間同步。頁面仍可匯出為 `.md`。

**如何安裝？**
從官網下載單一多語系安裝程式，執行後開啟 OneNote——功能區中會出現一個 **HydroMark** 索引標籤。安裝程式會自動適應 32 位元與 64 位元 OneNote。

**是免費的嗎？**
提供 14 天全功能試用。之後依裝置授權（電子郵件 + 金鑰）：個人版與家庭版、基礎版與專業版，可選永久或按年。

## 🌐 官方連結

- 國際站（English）：https://hydromark.hydrolinx.top
- 中國站（简体中文）：https://hydromark.hydrolinx.cn
- 下載：https://hydromark.hydrolinx.top/download
- 文件：https://hydromark.hydrolinx.top/documentation
- 定價：https://hydromark.hydrolinx.top/pricing
- 更新日誌：https://hydromark.hydrolinx.top/changelog

## 💬 回饋與支援

這裡是與我們聯絡的最佳管道：

- 🐛 **錯誤回報與功能請求** → 提交 [Issue](../../issues)
- 💡 **想法與一般性討論** → 使用 [Discussions](../../discussions)
- 📧 **電子郵件** → support@hydrolinx.top（海外）· support@hydrolinx.cn（中國大陸）
- 📖 **支援指南** → [SUPPORT.zh-TW.md](SUPPORT.zh-TW.md)

提交 issue 之前，請先搜尋既有 issue 以避免重複，並附上你的 Windows / OneNote 版本與重現步驟。

## 🗺️ 路線圖

我們正在持續改進 HydroMark。近期計畫：

- 更聰明的 AI 操作——智慧摘要、自動標記，以及更多助理可執行外掛操作
- 更多圖表類型與內容區塊範本
- 更深入的 OneNote 整合

請關注 [Releases](../../releases) 頁面取得更新說明。

## 授權與原始碼

本儲存庫為**開放原始碼儲存庫**，存放 HydroMark 專案的部分原始碼與文件；專案其餘部分不在本儲存庫中。

歡迎你：

- 閱讀、研究並重複使用本儲存庫中的程式碼與文件
- 提交 issue、參與討論，協助我們改進
- 在介紹或評測本專案时使用 HydroMark 名稱

請勿在衍生產品或服務中使用 HydroMark 名稱與品牌，以免使用者對來源產生誤解。

© HydroLinx。HydroMark 及其圖標為 HydroLinx 的商標。

---

*HydroMark — Markdown，OneNote 本該有的樣子。現在更配有會替你打字的 AI 助理。*
