<div align="center">

<img src="assets/hydromark-logo.png" alt="HydroMark" width="520" />

**OneNote Markdown アドイン、AI アシスタント、生産性ツール**

[![Release](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.hydromark.hydrolinx.top%2Fapi%2Fversion&query=%24.version&label=Release&color=2ea44f)](https://hydromark.hydrolinx.top/download)

[![X](https://img.shields.io/badge/X-@hydrolinxtech-000000?logo=x&logoColor=white)](https://x.com/hydrolinxtech) [![Product Hunt](https://img.shields.io/badge/Product%20Hunt-@hydrolinx-da7651?logo=producthunt&logoColor=white)](https://www.producthunt.com/@hydrolinx) [![YouTube](https://img.shields.io/badge/YouTube-@hydrolinxtechglobal-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/@hydrolinxtechglobal) [![Instagram](https://img.shields.io/badge/Instagram-hydrolinx.top-E4405F?logo=instagram&logoColor=white)](https://www.instagram.com/hydrolinx.top/)

![OneNote 内で動作する HydroMark：HydroMark リボン、ページ上のレンダリング済み Markdown、目次パネル、AI アシスタントパネル](assets/hydromark-onenote.png)

詳細はこちらの[ドキュメント](https://hydromark.hydrolinx.top/documentation)をご確認ください

[English](README.md) · [简体中文](README.zh.md) · [繁體中文](README.zh-TW.md) · **日本語** · [한국어](README.ko.md) · [Español](README.es.md) · [Português](README.pt.md) · [Русский](README.ru.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [サポート](SUPPORT.ja.md)

</div>

# HydroMark — AI アシスタントを備えた OneNote Markdown アドイン

**HydroMark は、Windows 版 Microsoft OneNote 向けの WYSIWYG Markdown アドインです。** OneNote ページに Markdown を入力すると、その場で見出し、リスト、表、タスクリスト、コードブロック、LaTeX 数式、Mermaid 図が OneNote ネイティブの内容として瞬時にレンダリングされます。エクスポートもスクリーンショットも、アプリの切り替えも不要です。**v1.1.0** 以降、内蔵の **AI アシスタント**がレンダリング済みの記事や表、ページ操作をノートに直接書き込みます。

> ⚠️ **このリポジトリはオープンソースのリポジトリで、HydroMark プロジェクトのコードとドキュメントの一部を収録しています。** 製品のお知らせとコミュニティフィードバック（Issues と Discussions）もここで行います。詳細は下記の[ライセンスとソースコード](#ライセンスとソースコード)をご覧ください。

---

## HydroMark とは？

HydroMark は **OneNote Markdown アドイン**です。Microsoft OneNote の中に本物の Markdown エディターを組み込む Windows アドインです。OneNote のノートブック、キャンバス、クラウド同期はそのままに、本当に欲しかった Markdown ワークフローを手に入れられます。`## Heading` と入力してスペースを打つと、生の構文ではなくレンダリングされた見出しがページに表示されます。

すべての内容は**画像ではなく OneNote ネイティブの要素**でレンダリングされるため、Markdown ノートは編集可能なまま、OneNote 内で検索でき、オフラインでも使え、スマートフォン、タブレット、Web 版の OneNote にも同期されます。`F8` を押すとページを `.md` に書き出せます。

**v1.1.0** 以降、このアドインには **AI アシスタント**も搭載されています。コピー＆ペースト用のテキストを渡すだけの AI サイドバーとは違い、HydroMark の AI はページに直接書き込みます。完全にレンダリングされた記事を挿入し、表を構築し、レンダリング、エクスポート、目次、ページ幅といったアドイン操作を実行します。操作の結果はモデルに返されるので、モデル自身が確認や自己修正を行えます。

**こんな方に：** 開発者や技術チーム、学生や研究者、プロダクトや運用担当者——Markdown で書きながらノートは OneNote に置いておきたい、というすべての方に。

## 概要

| 項目              | 詳細                                                                  |
| ----------------- | --------------------------------------------------------------------- |
| **製品**          | HydroMark — AI アシスタントを備えた OneNote Markdown アドイン         |
| **カテゴリ**      | OneNote プラグイン / OneNote 拡張 / Office COM アドイン               |
| **プラットフォーム** | Windows 7 以降                                                     |
| **ホストアプリ**  | OneNote **デスクトップ版** 2013+（2016 / 2019 / 2021 / Microsoft 365） |
| **ランタイム**    | .NET Framework 4.8+                                                   |
| **非対応**        | OneNote for Windows 10（UWP / Microsoft Store）、macOS、モバイル      |
| **トライアル**    | 14 日間の全機能トライアル、クレジットカード不要                       |
| **AI**            | 内蔵 — 14 のプロバイダー、API キーはご自身で用意                      |
| **言語**          | English · 简体中文 · 繁體中文 · 日本語 · 한국어 · Español · Português · Русский · Deutsch · Français · हिन्दी · العربية |

## ✨ 機能

| 機能 | 説明 | ショートカット |
| --- | --- | --- |
| 🤖 **AI アシスタント** | レンダリング済みの記事や表をページに直接書き込み、アドイン操作も実行 | `Alt+A` |
| ✍️ **即時レンダリング** | 見出しやリストなどを入力するとその場で整形 | `#` / `-` + スペース |
| 🔁 **ソース ↔ レンダリング** | 生 Markdown とレンダリング結果をページ単位または段落単位で切り替え | — |
| 📥 **Markdown を貼り付け** | コピーした Markdown を完成したノートに変換 | `Ctrl+Shift+V` |
| 💻 **コードハイライト** | 200 以上の言語、100 以上のテーマ、ワンクリックコピー | — |
| ∑ **LaTeX 数式** | インライン・ブロック数式を OneNote ネイティブの数式として表示 | `$…$` |
| 📊 **図表** | 26 種類以上の Mermaid / ZenUML：フロー、シーケンス、ガント、マインドマップ… | — |
| ▱ **表** | 全幅 ↔ 内容に合わせるを切り替え、状態を保持 | `Alt+W` |
| ☑️ **タスクリスト** | チェックボックスはクリック可能、`- [x]` / `- [ ]` として書き出し | — |
| ⌨️ **スラッシュコマンド** | `/` でコマンドパレットを開きブロックを素早く挿入 | `/` |
| 🖍️ **ハイライトブロック** | 重要なノートを視覚的に目立たせ | — |
| 📑 **ページ目次と幅** | 目次を自動生成；ページ幅を手動・自動調整 | — |
| 🌙 **ダークモード** | レンダリング内容、ダイアログ、AI サイドバーが OneNote のテーマに追従 | — |
| 🔄 **インポート / エクスポート** | Markdown ファイルを読み込み、Markdown ファイルとして書き出し（画像は任意） | `F8` |

### 🤖 AI アシスタント — 目玉機能（1.1.0 で新登場）

多くの AI サイドバーは、コピー＆ペーストするためのテキストの塊を渡すだけです。HydroMark のアシスタントは**ノートに直接書き込みます**：

- **チャットだけでなく、アドイン操作を実行** — 完全にレンダリングされた記事の挿入、表の構築、ページ操作（レンダリング、エクスポート、目次、ページ幅）の実行。操作結果は会話にフィードバックされるため、モデルは確認や自己修正ができます。
- **指定した幅で表をコマンド一発** — `insert_table` はページ全幅と**内容に合わせる**レイアウトに対応。AI 経由の処理は `Alt+W` の幅切り替えと同じ表エンジンを共有します。
- **お好みのモデルを持ち込み** — 14 のプロバイダーを内蔵（OpenAI、DeepSeek、Kimi、Zhipu、Qwen…）。それ以外は Base URL をカスタム指定できます。API キーはお使いのマシン上に留まり、中継サーバーはありません。
- **マルチモーダル** — チャットにスクリーンショットを貼り付け、マルチモーダルモデルで参照できます。
- **言語に追従** — 中国語で質問すれば中国語で、英語で質問すれば英語で回答します。
- **すべてのライセンスに含まれる** — 14 日間の無料トライアルとすべての有料プラン。`Alt+A` またはリボンの **AI** グループから開けます。

### 📝 Markdown レンダリング

- **即座の Markdown レンダリング** — `#` や `-` の後にスペースを入力するとその場で整形されます。他のブロックは Enter か F5 でレンダリングします（WYSIWYG）。
- **ソース / レンダリングのデュアルビュー** — 生の Markdown とレンダリング結果をいつでも切り替え可能。ページ単位でも段落単位でも切り替えられます。
- **どこからでも Markdown を貼り付け** — `Ctrl+Shift+V` で、Web ページやドキュメント、AI の回答からコピーした Markdown のブロックを完成したノートに変えます。
- **コードハイライト** — 200 以上の言語、100 以上のテーマに対応したシンタックスハイライト、ワンクリックコピー。
- **LaTeX 数式** — インライン数式もブロック数式も OneNote ネイティブの数式としてレンダリングされます。
- **Mermaid / ZenUML ダイアグラム** — 26 以上の図の種類：フローチャート、シーケンス図、クラス図、状態遷移図、ガントチャート、マインドマップ、UML など。
- **表の全幅 ↔ 内容に合わせる切り替え** — `Alt+W` でどの表も双方向に切り替えられます。内容に合わせた状態は保持されます。
- **タスクリスト** — チェックボックスはクリック可能なまま、`- [x]` / `- [ ]` として書き出せます。
- **スラッシュコマンド** — `/` を押すとコマンドパレットが開き、ブロックを素早く挿入できます。
- **ハイライトブロック** — 重要なノートを視覚的に目立たせます。
- **ページ目次とページ幅** — 目次の自動生成や非表示、ページ幅の手動・自動調整ができます。
- **ダークモードに完全対応** — レンダリング内容、ダイアログ、AI サイドバーがすべて OneNote のテーマに追従します。
- **シームレスなインポート / エクスポート** — Markdown ファイルを読み込み、Markdown ファイルとして書き出し（画像は任意）。

## 🚀 クイックスタート

1. **ダウンロード** — 単一の多言語インストーラーを[ダウンロードページ](https://hydromark.hydrolinx.top/download)から入手（Windows 7+ と OneNote **デスクトップ版** 2013+ が必要）。
2. **実行** — インストーラーは 32 ビットと 64 ビットの OneNote に自動対応するため、x86 / x64 版を選ぶ必要はありません。
3. **OneNote を開く** — リボンに **HydroMark** タブが表示されます。
4. **Markdown を書く** — `## ` の後にスペースで見出し、`- ` の後にスペースでリスト；その他のブロックは Enter または `F5` でレンダリング。
5. **まず AI を設定** — 「設定 → AI モデル」を開き、プロバイダーを選んで API キーを入力します（ご自身のキーを使用、14 のプロバイダーを内蔵）。設定後、`Alt+A`（またはリボンの **AI** グループ）で **AI アシスタント**を開き、記事や表をページに直接書き込みます。
6. **書き出し** — 現在のページを `F8` で `.md` に書き出し。

14 日間の全機能トライアルが自動開始、クレジットカード不要。詳しいガイドは[ドキュメント](https://hydromark.hydrolinx.top/documentation)をご覧ください。

## よくある質問

**Q: OneNote 用の Markdown アドインはありますか？**

**A:** はい。HydroMark は、Windows 版 Microsoft OneNote デスクトップ専用に作られた Markdown アドインです。

**Q: OneNote で AI を使ってノートを書けますか？**

**A:** はい。HydroMark には AI アシスタントが搭載されており、レンダリング済みの Markdown 記事や表を現在の OneNote ページに直接挿入し、レンダリング、エクスポート、目次といったアドイン操作を実行できます。

**Q: 画像を貼り付けて AI に質問できますか？**

**A:** はい。画像をコピーするかスクリーンショットを撮り、AI アシスタントの入力欄で Ctrl+V を押すと、その画像について質問できます（1 回に複数枚可）。画像入力に対応したモデルを選ぶ必要があり、非対応のプロバイダーでは HydroMark がその旨を表示します。画像はご自身の API キーで選択中のプロバイダーに送信されます。

**Q: HydroMark は OneNote for Windows 10、Mac、モバイルで使えますか？**

**A:** いいえ。HydroMark は Windows 7+ 上の OneNote **デスクトップ版** 2013 以降（2016 / 2019 / 2021 / Microsoft 365）に対応しています。OneNote の UWP / Microsoft Store 版、macOS、モバイルには**対応していません**。

**Q: HydroMark は OneNote のプラグインですか、それとも別のアプリですか？**

**A:** OneNote のアドインであり、独立したノートアプリではありません。OneNote にインストールされ、リボンに **HydroMark** タブを追加します。ノートは既存のノートブックにそのまま残ります。

**Q: Markdown の内容は OneNote 内でネイティブのままですか？**

**A:** はい。レンダリングには画像ではなく OneNote ネイティブの要素を使うため、ノートは編集可能で検索可能なまま、各 OneNote クライアント間で同期できます。ページは引き続き `.md` に書き出せます。

**Q: インストール方法は？**

**A:** 公式サイトから単一の多言語インストーラーをダウンロードして実行し、OneNote を開くと、リボンに **HydroMark** タブが表示されます。インストーラーは 32 ビット版と 64 ビット版の OneNote に自動で対応します。

**Q: 無料ですか？**

**A:** 14 日間の全機能トライアルがあります。その後はデバイス単位のライセンス（メール + キー）です。個人版とファミリー版、Basic と Pro、買い切りまたは年間から選べます。

## 🌐 公式リンク

- ウェブサイト（English）：https://hydromark.hydrolinx.top
- ウェブサイト（中文）：https://hydromark.hydrolinx.cn
- ダウンロード：https://hydromark.hydrolinx.top/download
- ドキュメント：https://hydromark.hydrolinx.top/documentation
- 価格：https://hydromark.hydrolinx.top/pricing
- 変更履歴：https://hydromark.hydrolinx.top/changelog

## 💬 フィードバックとサポート

私たちへの連絡はここが最適です：

- 🐛 **バグ報告・機能リクエスト** → [Issue](../../issues) を作成
- 💡 **アイデア・一般的な議論** → [Discussions](../../discussions) を利用
- 📧 **メール** → support@hydrolinx.top
- 📖 **サポートガイド** → [SUPPORT.ja.md](SUPPORT.ja.md)

Issue を作成する前に、重複を避けるため既存の Issue を検索し、Windows / OneNote のバージョンと再現手順を記載してください。

## 🗺️ ロードマップ

私たちは HydroMark を積極的に改善しています。当面の予定：

- より賢い AI 操作 — スマート要約、自動タグ付け、アシスタントが実行できるさらなるアドイン操作
- より多くの図の種類とブロックテンプレート
- より広範な OneNote 統合

更新情報は [Releases](../../releases) ページをご確認ください。

## ライセンスとソースコード

このリポジトリは**オープンソース**で、HydroMark プロジェクトのソースコードとドキュメントの一部を収録しています。プロジェクトの残りの部分はこのリポジトリには含まれていません。

歓迎する行為：

- このリポジトリのコードとドキュメントを読み、学び、再利用すること
- Issue を提出し、ディスカッションに参加して改善に協力すること
- プロジェクトを紹介・レビューする際に HydroMark の名称を用いること

派生製品やサービスで HydroMark の名称・ブランドを使用しないでください。ユーザーが出所を誤解する恐れがあります。

© HydroLinx。HydroMark およびそのロゴは HydroLinx の商標です。

---

*HydroMark — Markdown は、OneNote が最初から備えているべきでした。今なら、タイピングを代行する AI アシスタント付き。*
