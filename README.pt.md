<div align="center">

<img src="assets/hydromark-logo.png" alt="HydroMark" width="520" />

**Complemento de Markdown para o OneNote, assistente de IA e ferramenta de produtividade**

[![Release](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.hydromark.hydrolinx.top%2Fapi%2Fversion&query=%24.version&label=Release&color=2ea44f)](https://hydromark.hydrolinx.top/download)

[![X](https://img.shields.io/badge/X-@hydrolinxtech-000000?logo=x&logoColor=white)](https://x.com/hydrolinxtech) [![Product Hunt](https://img.shields.io/badge/Product%20Hunt-@hydrolinx-da7651?logo=producthunt&logoColor=white)](https://www.producthunt.com/@hydrolinx) [![YouTube](https://img.shields.io/badge/YouTube-@hydrolinxtechglobal-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/@hydrolinxtechglobal) [![Instagram](https://img.shields.io/badge/Instagram-hydrolinx.top-E4405F?logo=instagram&logoColor=white)](https://www.instagram.com/hydrolinx.top/)

![HydroMark no OneNote: o separador HydroMark, o Markdown renderizado na página, o painel de índice e o painel do Assistente de IA](assets/hydromark-onenote.png)

Para mais informações, consulte a [Documentação](https://hydromark.hydrolinx.top/documentation)

[English](README.md) · [简体中文](README.zh.md) · [繁體中文](README.zh-TW.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · **Português** · [Русский](README.ru.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [Suporte](SUPPORT.pt.md)

</div>

# HydroMark — Complemento de Markdown para o OneNote com assistente de IA

**O HydroMark é um complemento (add-in) de Markdown com edição imediata (WYSIWYG) para o Microsoft OneNote no Windows.** Escreva Markdown numa página do OneNote, e o conteúdo é de imediato renderizado como conteúdo nativo do OneNote — títulos, listas, tabelas, listas de tarefas, blocos de código, fórmulas LaTeX e diagramas Mermaid. Sem exportações, sem capturas de ecrã, sem mudar de aplicação. Desde a **v1.1.0**, um **assistente de IA** integrado escreve artigos renderizados, tabelas e operações de página diretamente nas suas notas.

> ⚠️ **Este é um repositório de código aberto que contém parte do código e da documentação do projeto HydroMark.** Serve também para anúncios de produto e feedback da comunidade (Issues e Discussions). Consulte [Licença e código-fonte](#licença-e-código-fonte) mais abaixo.

---

## O que é o HydroMark?

O HydroMark é um **complemento de Markdown para o OneNote**: um complemento para Windows que coloca um verdadeiro editor de Markdown dentro do Microsoft OneNote. Continua a escrever nos cadernos, na área de trabalho e na sincronização na nuvem do OneNote, mas com o fluxo de Markdown que sempre quis — escreva `## Heading` seguido de um espaço e a página mostra um título renderizado em vez da sintaxe em bruto.

Tudo é renderizado com **elementos nativos do OneNote, não com imagens**, pelo que as suas notas em Markdown continuam editáveis, pesquisáveis dentro do OneNote, disponíveis offline e sincronizadas com o OneNote no telemóvel, no tablet e na web. Prima `F8` para exportar uma página de volta para `.md`.

Desde a **v1.1.0** o complemento inclui também um **assistente de IA**. Ao contrário das barras laterais de IA que entregam texto para copiar e colar, a IA do HydroMark escreve na própria página: insere artigos totalmente renderizados, constrói tabelas e executa operações do complemento como renderizar, exportar, índice e largura da página — com os resultados a regressarem à conversa para que o modelo possa confirmar ou corrigir-se a si próprio.

**Para quem:** programadores e equipas técnicas, estudantes e investigadores, produtos e operações — qualquer pessoa que escreva Markdown mas guarde as suas notas no OneNote.

## Factos rápidos

| Item                | Detalhe                                                               |
| ------------------- | --------------------------------------------------------------------- |
| **Produto**         | HydroMark — complemento de Markdown para OneNote com assistente de IA  |
| **Categoria**       | Plugin do OneNote / extensão do OneNote / add-in COM do Office         |
| **Plataforma**      | Windows 7 e posteriores                                                |
| **Aplicação anfitriã** | OneNote de **ambiente de trabalho** 2013+ (2016 / 2019 / 2021 / Microsoft 365) |
| **Execução**        | .NET Framework 4.8+                                                    |
| **Não suportado**  | OneNote para Windows 10 (UWP / Microsoft Store), macOS, mobile         |
| **Experimentação**  | 14 dias com todas as funcionalidades, sem cartão de crédito            |
| **IA**              | Integrada — 14 fornecedores, utilize a sua própria chave de API        |
| **Idiomas**         | English · 简体中文 · 繁體中文 · 日本語 · 한국어 · Español · Português · Русский · Deutsch · Français · हिन्दी · العربية |

## ✨ Funcionalidades

| Funcionalidade | O que faz | Atalho |
| --- | --- | --- |
| 🤖 **Assistente de IA** | Escreve artigos e tabelas renderizados e executa operações do complemento na página | `Alt+A` |
| ✍️ **Renderização instantânea** | Títulos, listas e mais são formatados ao escrever | `#` / `-` + Espaço |
| 🔁 **Fonte ↔ renderizado** | Alterna entre Markdown em bruto e resultado renderizado, por página ou parágrafo | — |
| 📥 **Colar Markdown** | Transforma o Markdown copiado numa nota concluída | `Ctrl+Shift+V` |
| 💻 **Destaque de código** | Mais de 200 linguagens, mais de 100 temas, cópia com um clique | — |
| ∑ **Fórmulas LaTeX** | Fórmulas em linha e em bloco como equações nativas do OneNote | `$…$` |
| 📊 **Diagramas** | 26+ tipos Mermaid / ZenUML: fluxo, sequência, Gantt, mapa mental… | — |
| ▱ **Tabelas** | Comutador largura total ↔ ajustada ao conteúdo que persiste | `Alt+W` |
| ☑️ **Listas de tarefas** | Caixas de verificação clicáveis, exportadas como `- [x]` / `- [ ]` | — |
| ⌨️ **Comandos com barra** | Paleta de comandos com `/` para inserir blocos rapidamente | `/` |
| 🖍️ **Blocos de destaque** | Realça visualmente as notas importantes | — |
| 📑 **Índice e largura da página** | Índice automático; largura da página manual ou automática | — |
| 🌙 **Modo escuro** | Conteúdo renderizado, diálogos e barra lateral de IA seguem o tema do OneNote | — |
| 🔄 **Importar / Exportar** | Ficheiros Markdown entram e saem (imagens opcionais) | `F8` |

### 🤖 Assistente de IA — a funcionalidade em destaque (novo na 1.1.0)

A maioria das barras laterais de IA entrega um bloco de texto para copiar e colar. O assistente do HydroMark **escreve nas suas notas**:

- **Executa operações do complemento, não apenas conversa** — insere um artigo totalmente renderizado, constrói tabelas, executa operações de página (renderizar, exportar, índice, largura da página); os resultados voltam à conversa para o modelo confirmar ou autocorrigir.
- **Tabelas a pedido, com a largura que pediu** — `insert_table` suporta largura total da página e layout **ajustado ao conteúdo**; o caminho da IA usa o mesmo motor de tabelas da alternância de largura `Alt+W`.
- **Utilize o seu próprio modelo** — 14 fornecedores integrados (OpenAI, DeepSeek, Kimi, Zhipu, Qwen…), Base URL personalizada para qualquer outro. A sua chave de API fica na sua máquina; nenhum servidor intermediário.
- **Multimodal** — cole uma captura de ecrã no chat e refira-a com modelos multimodais.
- **Segue o idioma** — pergunte em português, receba em português; pergunte em inglês, receba em inglês.
- **Incluído em todas as licenças** — nos 14 dias de experimentação gratuita e em todos os planos pagos. Abra com `Alt+A` ou no grupo **IA** do separador.

### 📝 Renderização de Markdown

- **Renderização de Markdown ao escrever** — escreva `#` ou `-` e depois um espaço: a linha já fica formatada; os restantes blocos continuam com Enter ou F5 (WYSIWYG).
- **Vista dupla código-fonte / renderizado** — alterne entre Markdown em bruto e resultado renderizado a qualquer momento, por página ou por parágrafo.
- **Cole Markdown de qualquer origem** — `Ctrl+Shift+V` transforma um bloco de Markdown copiado de uma página web, documento ou resposta de IA numa nota concluída.
- **Destaque de código** — realce de sintaxe para mais de 200 linguagens, mais de 100 temas, cópia com um clique.
- **Fórmulas LaTeX** — fórmulas em linha e em bloco renderizadas como equações nativas do OneNote.
- **Diagramas Mermaid / ZenUML** — mais de 26 tipos de diagrama: fluxogramas, sequência, classes, estados, Gantt, mapas mentais, UML e mais.
- **Tabelas com alternância largura total ↔ ajustada ao conteúdo** — `Alt+W` alterna qualquer tabela nos dois sentidos; o estado ajustado ao conteúdo é guardado.
- **Listas de tarefas** — as caixas de verificação continuam clicáveis e são exportadas como `- [x]` / `- [ ]`.
- **Comandos com barra** — prima `/` para abrir uma paleta de comandos e inserir blocos rapidamente.
- **Blocos de destaque** — realce visualmente as notas importantes.
- **Índice e largura da página** — gere ou oculte automaticamente um índice; largura da página manual ou automática.
- **Adaptação completa ao modo escuro** — conteúdo renderizado, diálogos e barra lateral de IA seguem o tema do OneNote.
- **Importação / exportação sem atritos** — ficheiros Markdown entram, ficheiros Markdown saem (imagens opcionais).

## 🚀 Primeiros passos

1. **Transferir** o instalador multilíngue único a partir da[página de transferência](https://hydromark.hydrolinx.top/download) (requer Windows 7+ e OneNote **de ambiente de trabalho** 2013+).
2. **Executar** o instalador — adapta-se automaticamente ao OneNote de 32 e 64 bits, pelo que não precisa de escolher a versão x86 / x64.
3. **Abrir o OneNote** e localizar o separador **HydroMark** na fita.
4. **Escrever Markdown** — `## ` e Espaço para um título, `- ` e Espaço para uma lista; os restantes blocos renderizam com Enter ou `F5`.
5. **Configure primeiro a IA** — abra **Definições → Modelo de IA**, escolha um fornecedor e introduza a sua chave de API (utilize a sua própria chave; 14 fornecedores integrados). Depois abra o **assistente de IA** com `Alt+A` (ou o grupo **IA** da fita) e deixe-o escrever artigos e tabelas diretamente na página.
6. **Exportar** a página atual para `.md` com `F8`.

O teste completo de 14 dias inicia automaticamente, sem cartão de crédito. Para o guia completo, consulte a[documentação](https://hydromark.hydrolinx.top/documentation).

## Perguntas frequentes

**Existe um complemento de Markdown para o OneNote?**
Sim — o HydroMark é um complemento de Markdown (add-in) criado especificamente para o Microsoft OneNote de ambiente de trabalho no Windows.

**Posso usar IA para escrever notas no OneNote?**
Sim. O HydroMark inclui um assistente de IA que insere artigos e tabelas de Markdown renderizados diretamente na página atual do OneNote e pode acionar operações do complemento como renderizar, exportar ou gerar índice.

**O HydroMark funciona com o OneNote para Windows 10, Mac ou mobile?**
Não. O HydroMark suporta o OneNote de **ambiente de trabalho** 2013 e posteriores (2016 / 2019 / 2021 / Microsoft 365) no Windows 7+. A versão UWP / Microsoft Store do OneNote, macOS e mobile **não** são suportados.

**O HydroMark é um plugin do OneNote ou uma aplicação separada?**
É um complemento do OneNote, não uma aplicação de notas independente. Instala-se no OneNote e adiciona um separador **HydroMark** à faixa de opções; as suas notas continuam nos seus cadernos.

**O conteúdo em Markdown mantém-se nativo no OneNote?**
Sim. A renderização usa elementos nativos do OneNote em vez de imagens, pelo que as notas permanecem editáveis, pesquisáveis e sincronizáveis entre clientes do OneNote. As páginas podem ser exportadas para `.md`.

**Como instalo?**
Transfira o instalador multilíngue único a partir do site, execute-o e abra o OneNote — aparece um separador **HydroMark** na faixa de opções. O instalador adapta-se automaticamente ao OneNote de 32 e de 64 bits.

**É gratuito?**
Há 14 dias de experimentação com todas as funcionalidades. Depois, as licenças são por dispositivo (email + chave): planos Individual e Família, Básico e Pro, vitalício ou anual.

## 🌐 Links oficiais

- Site (English): https://hydromark.hydrolinx.top
- Site (中文): https://hydromark.hydrolinx.cn
- Download: https://hydromark.hydrolinx.top/download
- Documentação: https://hydromark.hydrolinx.top/documentation
- Preços: https://hydromark.hydrolinx.top/pricing
- Registo de alterações: https://hydromark.hydrolinx.top/changelog

## 💬 Feedback e suporte

Este é o melhor sítio para nos contactar:

- 🐛 **Relatórios de erros e pedidos de funcionalidades** → abra um [Issue](../../issues)
- 💡 **Ideias e discussão geral** → use as [Discussions](../../discussions)
- 📧 **Email** → support@hydrolinx.top (fora da China) · support@hydrolinx.cn (China)
- 📖 **Guia de suporte** → [SUPPORT.pt.md](SUPPORT.pt.md)

Antes de abrir um issue, procure issues existentes para evitar duplicados e indique a sua versão do Windows / OneNote e os passos para reproduzir.

## 🗺️ Roda-mestra

Estamos a melhorar ativamente o HydroMark. A curto prazo:

- Ações de IA mais inteligentes — resumos automáticos, etiquetagem automática e mais operações do complemento executáveis pelo assistente
- Mais tipos de diagrama e modelos de blocos
- Integração mais ampla com o OneNote

Siga a página [Releases](../../releases) para notas de atualização.

## Licença e código-fonte

Este é um **repositório de código aberto**. Contém parte do código-fonte e da documentação do projeto HydroMark; o restante do projeto não está aqui publicado.

Pode, sem problema:

- Ler, estudar e reutilizar o código e a documentação deste repositório
- Abrir issues e participar em discussões para nos ajudar a melhorar
- Usar o nome HydroMark ao apresentar ou analisar o projeto

Não use o nome ou a marca HydroMark em produtos ou serviços derivados, para não induzir os utilizadores em erro quanto à origem.

© HydroLinx. HydroMark e o respetivo logótipo são marcas da HydroLinx.

---

*HydroMark — Markdown como o OneNote sempre devia ter tido. Agora com um assistente de IA que escreve por si.*
