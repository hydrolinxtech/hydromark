# HydroMark — AI 어시스턴트가 포함된 OneNote Markdown 애드인

[English](README.md) · [简体中文](README.zh.md) · [日本語](README.ja.md) · **한국어** · [Español](README.es.md) · [Русский](README.ru.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [지원](SUPPORT.ko.md)

**HydroMark는 Windows용 Microsoft OneNote를 위한 WYSIWYG Markdown 애드인(addin)입니다.** OneNote 페이지에 Markdown을 작성하고 Enter를 누르면 제목, 목록, 표, 작업 목록, 코드 블록, LaTeX 수식, Mermaid 다이어그램이 기본 OneNote 콘텐츠로 즉시 렌더링됩니다. 내보내기나 스크린샷, 앱 전환도 필요 없습니다. **v1.1.0**부터는 내장 **AI 어시스턴트**가 렌더링된 문서, 표, 페이지 작업을 노트에 바로 작성합니다.

> ⚠️ **이 저장소는 오픈 소스 저장소로, HydroMark 프로젝트의 코드와 문서 일부를 담고 있습니다.** 제품 공지와 커뮤니티 피드백(Issues & Discussions)도 이곳에서 진행합니다. 자세한 내용은 아래의 [라이선스 및 소스 코드](#라이선스-및-소스-코드)를 참조하세요.

---

## HydroMark란 무엇인가요?

HydroMark는 **OneNote Markdown 애드인**입니다. Microsoft OneNote 안에 실제 Markdown 편집기를 넣어 주는 Windows 애드인입니다. OneNote의 노트북, 캔버스, 클라우드 동기화를 그대로 사용하면서도 원하는 Markdown 워크플로를 얻을 수 있습니다. `## Heading`을 입력하고 Enter를 누르면 페이지에 원시 문법 대신 렌더링된 제목이 표시됩니다.

모든 내용은 **이미지가 아닌 OneNote 자체의 기본 요소**로 렌더링되므로 Markdown 노트는 계속 편집 가능하고, OneNote 안에서 검색 가능하며, 오프라인에서 사용할 수 있고, 휴대폰·태블릿·웹의 OneNote와 동기화됩니다. `F8`을 눌러 페이지를 다시 `.md`로 내보낼 수 있습니다.

**v1.1.0**부터 애드인에는 **AI 어시스턴트**도 포함됩니다. 텍스트를 복사해 붙여넣는 AI 사이드바와 달리 HydroMark의 AI는 페이지에 직접 작성합니다. 완전히 렌더링된 문서를 삽입하고, 표를 만들고, 렌더링·내보내기·목차·페이지 너비 같은 애드인 작업을 실행하며, 그 결과를 모델에 다시 전달해 확인하거나 스스로 수정할 수 있습니다.

**대상 사용자:** 개발자와 기술 팀, 학생과 연구자, 제품 및 운영 담당자 — Markdown으로 작성하지만 노트는 OneNote에 보관하는 모든 사람.

## 빠른 정보

| 항목              | 세부 정보                                                              |
| ----------------- | ------------------------------------------------------------------- |
| **제품**          | HydroMark — AI 어시스턴트가 포함된 OneNote Markdown 애드인(addin)     |
| **범주**          | OneNote 플러그인 / OneNote 확장 / Office COM 애드인                   |
| **플랫폼**        | Windows 7 이상                                                        |
| **호스트 앱**     | OneNote **데스크톱** 2013+ (2016 / 2019 / 2021 / Microsoft 365)       |
| **런타임**        | .NET Framework 4.8+                                                   |
| **지원하지 않음** | OneNote for Windows 10 (UWP / Microsoft Store), macOS, 모바일         |
| **체험**          | 14일 전체 기능 체험, 신용카드 불필요                                  |
| **AI**            | 내장 — 15개 제공업체, 자체 API 키 사용                                |
| **언어**          | 简体中文 · English · 日本語 · 한국어 · Deutsch · Français · Español · Русский |

## ✨ 기능

### 🤖 AI 어시스턴트 — 핵심 기능 (1.1.0 신규)

대부분의 AI 사이드바는 복사해 붙여넣을 텍스트 덩어리를 제공합니다. HydroMark의 어시스턴트는 **노트에 직접 작성합니다**:

- **단순 채팅이 아닌 애드인 작업 실행** — 완전히 렌더링된 문서 삽입, 표 생성, 페이지 작업(렌더링, 내보내기, 목차, 페이지 너비) 실행. 작업 결과가 대화로 다시 전달되어 모델이 확인하거나 스스로 수정할 수 있습니다.
- **요청한 너비로 표 생성** — `insert_table`은 전체 페이지 너비와 **내용에 맞춘** 레이아웃을 지원하며, AI 경로는 `Alt+W` 너비 전환과 동일한 표 엔진을 사용합니다.
- **자체 모델 사용** — 15개 제공업체 내장(OpenAI, DeepSeek, Kimi, Zhipu, Qwen…), 그 외에는 사용자 지정 Base URL. API 키는 사용자 컴퓨터에 보관되며 중간 서버가 없습니다.
- **멀티모달** — 채팅에 스크린샷을 붙여넣고 멀티모달 모델로 참조할 수 있습니다.
- **언어 자동 맞춤** — 중국어로 질문하면 중국어로, 영어로 질문하면 영어로 답합니다.
- **모든 라이선스에 포함** — 14일 무료 체험과 모든 유료 요금제에 포함됩니다. `Alt+A` 또는 리본의 **AI** 그룹에서 엽니다.

### 📝 Markdown 렌더링

- **실시간 Markdown 렌더링** — Markdown을 입력하고 Enter를 누르면 즉시 서식이 적용됩니다(WYSIWYG).
- **소스 / 렌더링 이중 보기** — 페이지 단위 또는 단락 단위로 원시 Markdown과 렌더링 결과를 언제든 전환합니다.
- **어디서나 Markdown 붙여넣기** — `Ctrl+Shift+V`로 웹페이지, 문서, AI 답변에서 복사한 Markdown 블록을 완성된 노트로 만듭니다.
- **코드 하이라이팅** — 200개 이상 언어, 100개 이상 테마의 구문 강조, 원클릭 복사.
- **LaTeX 수식** — 인라인 및 블록 수식을 OneNote 기본 수식으로 렌더링합니다.
- **Mermaid / ZenUML 다이어그램** — 순서도, 시퀀스, 클래스, 상태, 간트, 마인드맵, UML 등 26가지 이상의 다이어그램 유형.
- **전체 너비 ↔ 내용 맞춤 표 전환** — `Alt+W`로 모든 표를 양방향 전환하며, 내용 맞춤 상태는 유지됩니다.
- **작업 목록** — 체크박스는 클릭 가능하게 유지되고 `- [x]` / `- [ ]`로 내보내집니다.
- **슬래시 명령** — `/`를 눌러 명령 팔레트를 열고 빠르게 블록을 삽입합니다.
- **강조 블록** — 중요한 노트를 시각적으로 강조합니다.
- **페이지 목차 및 페이지 너비** — 목차를 자동 생성하거나 숨기고, 페이지 너비를 수동 또는 자동으로 설정합니다.
- **완전한 다크 모드 대응** — 렌더링된 콘텐츠, 대화 상자, AI 사이드바가 모두 OneNote 테마를 따릅니다.
- **원활한 가져오기 / 내보내기** — Markdown 파일로 들여오고 내보냅니다(이미지 선택 사항).

## 자주 묻는 질문

**OneNote용 Markdown 애드인이 있나요?**
네 — HydroMark는 Windows의 Microsoft OneNote 데스크톱을 위해 특별히 만들어진 Markdown 애드인(addin)입니다.

**OneNote에서 AI로 노트를 작성할 수 있나요?**
네. HydroMark에는 렌더링된 Markdown 문서와 표를 현재 OneNote 페이지에 직접 삽입하고 렌더링, 내보내기, 목차 같은 애드인 작업을 실행할 수 있는 AI 어시스턴트가 포함되어 있습니다.

**HydroMark는 OneNote for Windows 10, Mac, 모바일에서 작동하나요?**
아니요. HydroMark는 Windows 7+의 OneNote **데스크톱** 2013 이상(2016 / 2019 / 2021 / Microsoft 365)을 지원합니다. UWP / Microsoft Store 버전의 OneNote, macOS, 모바일은 **지원하지 않습니다**.

**HydroMark는 OneNote 플러그인인가요, 별도 앱인가요?**
별도의 노트 앱이 아닌 OneNote 애드인입니다. OneNote에 설치되어 리본에 **HydroMark** 탭을 추가하며, 노트는 기존 노트북에 그대로 유지됩니다.

**Markdown 콘텐츠가 OneNote에서 기본 형식으로 유지되나요?**
네. 렌더링은 이미지가 아닌 OneNote 기본 요소를 사용하므로 노트는 계속 편집·검색·동기화할 수 있습니다. 페이지는 여전히 `.md`로 내보낼 수 있습니다.

**설치는 어떻게 하나요?**
웹사이트에서 다국어 단일 설치 프로그램을 다운로드해 실행하고 OneNote를 열면 리본에 **HydroMark** 탭이 나타납니다. 설치 프로그램은 32비트 및 64비트 OneNote에 자동으로 맞춰집니다.

**무료인가요?**
14일 전체 기능 체험이 있습니다. 이후 라이선스는 기기 단위(이메일 + 키)이며, Individual 및 Family, Basic 및 Pro, 영구 또는 연간 요금제가 있습니다.

## 🌐 공식 링크

- 웹사이트(영어): https://hydromark.hydrolinx.top
- 웹사이트(中文): https://hydromark.hydrolinx.cn
- 문서: https://hydromark.hydrolinx.top/documentation
- 가격: https://hydromark.hydrolinx.top/pricing
- 변경 로그: https://hydromark.hydrolinx.top/changelog

## 💬 피드백 및 지원

가장 빠르게 연락할 수 있는 곳입니다:

- 🐛 **버그 신고 및 기능 요청** → [Issue](../../issues) 열기
- 💡 **아이디어 및 일반 토론** → [Discussions](../../discussions) 이용
- 📧 **이메일** → support@hydrolinx.top
- 📖 **지원 가이드** → [SUPPORT.ko.md](SUPPORT.ko.md)

이슈를 열기 전에 중복을 피하기 위해 기존 이슈를 검색하고, Windows / OneNote 버전과 재현 단계를 포함해 주세요.

## 🗺️ 로드맵

HydroMark는 계속 개선되고 있습니다. 가까운 계획:

- 더 똑똑한 AI 작업 — 스마트 요약, 자동 태깅, 어시스턴트가 실행할 수 있는 더 많은 애드인 작업
- 더 많은 다이어그램 유형과 블록 템플릿
- 더 폭넓은 OneNote 통합

업데이트 내용은 [Releases](../../releases) 페이지를 참고하세요.

## 라이선스 및 소스 코드

이 저장소는 **오픈 소스**이며 HydroMark 프로젝트의 소스 코드와 문서 일부를 담고 있습니다. 프로젝트의 나머지 부분은 이 저장소에 포함되어 있지 않습니다.

다음은 환영합니다:

- 이 저장소의 코드와 문서를 읽고 배우고 재사용하기
- 이슈를 등록하고 토론에 참여해 개선에 기여하기
- 프로젝트를 소개하거나 리뷰할 때 HydroMark 이름 사용하기

파생 제품이나 서비스에 HydroMark 이름과 브랜드를 사용하지 마세요. 사용자가 출처를 오해할 수 있습니다.

© HydroLinx. HydroMark 및 로고는 HydroLinx의 상표입니다.

---

*HydroMark — Markdown, OneNote에 원래 있었어야 했던 방식. 이제 타이핑을 대신하는 AI 어시스턴트와 함께.*
