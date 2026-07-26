# Claude Code Deep Dive Workshop

[![License: Proprietary](https://img.shields.io/badge/license-Proprietary-blue.svg)](#license)
[![Version](https://img.shields.io/badge/version-1.2.0-green.svg)](./CHANGELOG.md)
<a href="#english"><img src="https://img.shields.io/badge/lang-English-blue.svg" alt="English"></a>
<a href="#korean"><img src="https://img.shields.io/badge/lang-한국어-red.svg" alt="Korean"></a>

A 3-day Claude Code curriculum delivered as dated PDF chapter editions and 502 extracted code snippets. | 날짜별 챕터 PDF 에디션과 502개 추출 코드 스니펫으로 제공되는 3일간의 Claude Code 커리큘럼입니다.

---

<a id="english"></a>

# English

## Overview

Claude Code Deep Dive Workshop is a Korean-language technical curriculum delivered as ready-to-present PDF slide decks and a searchable archive of every code example used in the workshop. Chapter PDFs ship in date-stamped edition directories — `20260525/` for the original edition and `20260703/` for the latest, newly authored against Claude Code 2.1.198 — each containing six chapters, while `tech_doc/` holds supplementary deep-dive documents on Claude Code architecture and cost efficiency. The decks are paired with 502 markdown files under `Script/workshop-code/` that extract each code-bearing slide into a standalone, grep-friendly snippet with Korean speaker notes. All slide artifacts follow a consistent design system for visual identity.

## Features

- **Six chapter PDFs per edition** — Overview, Agents & Subagents, Admin Setup, Settings, CLI Reference, and the Agent SDK; each curriculum edition ships in a date-stamped directory (`20260525/`, `20260703/`). The latest `20260703/` edition is newly authored against Claude Code 2.1.198.
- **Supplementary technical documents** — `tech_doc/` carries deep-dive references beyond the curriculum: `ClaudeCode-Architecture.pdf` and `Claude_Cost_Efficiency.pdf`.
- **Hands-on lab guides** — `ccw-hands-on-lab/` provides self-contained HTML lab guides: one per chapter (Ch1–Ch6), six capstone labs (main, B, C, D, E, F), and three reference pages (slash commands, plugins, directory structure), with an `index.html` portal page as the entry point. The labs cover both authentication paths: Anthropic subscription/Enterprise or Claude Code on Bedrock. Published at [comeddy.github.io/ccw-hands-on-lab](https://comeddy.github.io/ccw-hands-on-lab/).
- **502 extracted code snippets** — Each code-bearing slide is exported as a numbered markdown file under `Script/workshop-code/`, organized by chapter and part for fast lookup.
- **Bilingual coverage in code** — Python and TypeScript samples appear side by side across SDK material, with three authentication paths (Anthropic Direct, Amazon Bedrock, Vertex AI).
- **Korean speaker notes per snippet** — Every extracted markdown file embeds the original Korean speaker script alongside the code.
- **Self-contained — no build step required** — PDFs and markdown ship pre-rendered; consumers only need a PDF viewer and a text editor.

## Prerequisites

- A PDF viewer to read the chapter decks under the dated edition directories (`20260525/`, `20260703/`) and `tech_doc/`.
- A web browser to open the hands-on lab guides under `ccw-hands-on-lab/`.
- A text editor or GitHub viewer to read markdown snippets under `Script/workshop-code/`.
- `grep` and `find` (or any equivalent search tool) to locate snippets by keyword or file name.
- `git` to clone the repository.

## Installation

```bash
# 1. Clone the repository
git clone https://github.com/comeddy/claude-code-workshop.git
cd claude-code-workshop

# 2. Open the PDF for a given chapter from the latest edition (example: Chapter 1)
xdg-open 20260703/ClaudeCode_Ch1_20260703.pdf    # Linux
# open  20260703/ClaudeCode_Ch1_20260703.pdf       # macOS

# 3. Browse extracted code snippets
ls Script/workshop-code/ch6-sdk/part-06-production/
```

## Usage

```bash
# Find Python retry patterns
grep -rn "tenacity" Script/workshop-code/

# Find hook examples across all chapters
grep -rn "PreToolUse" Script/workshop-code/

# Find authentication-related snippets by file name
find Script/workshop-code/ -name "*auth*"

# List all snippets in a specific part
ls Script/workshop-code/ch6-sdk/part-01-sdk-basics/
# → 007-python-install-first-call.md
# → 008-typescript-install-first-call.md
# → ...

# Open a single snippet
cat Script/workshop-code/ch6-sdk/part-06-production/104-retry-python.md

# Open a supplementary technical document
xdg-open tech_doc/ClaudeCode-Architecture.pdf    # Linux
```

## Project Structure

```text
claude-code-workshop/
├── README.md                                  # This file
├── CHANGELOG.md                               # Per-version change history
├── CLAUDE.md                                  # Claude Code project guidance
├── 20260525/                                  # 2026-05-25 edition chapter PDFs (Ch1–Ch6)
├── 20260703/                                  # 2026-07-03 edition (latest, Claude Code 2.1.198 based)
├── ccw-hands-on-lab/                          # Hands-on lab guides (HTML)
│   ├── index.html                             # Lab portal entry page
│   ├── ClaudeCode_Ch{1..6}_HandsOnLab.html    # Chapter labs (Ch1–Ch6)
│   ├── ClaudeCode_Capstone*_HandsOnLab.html   # Capstone labs (main, B, C, D, E, F)
│   └── ClaudeCode_Reference{1..3}_*.html      # Reference pages (commands, plugins, directory)
├── tech_doc/                                  # Supplementary technical documents
│   ├── ClaudeCode-Architecture.pdf            # Claude Code architecture deep dive
│   └── Claude_Cost_Efficiency.pdf             # Claude cost efficiency guide
└── Script/
    ├── workshop-code-README.md                # Top-level guide for the snippet archive
    └── workshop-code/                         # 502 extracted code snippets
        ├── README.md
        ├── ch1-overview/                      # 10 parts, 108 snippets
        ├── ch2-agents/                        #  9 parts,  53 snippets
        ├── ch3-admin/                         #  9 parts,  57 snippets
        ├── ch4-settings/                      #  9 parts,  86 snippets
        ├── ch5-cli/                           #  8 parts,  86 snippets
        └── ch6-sdk/                           #  8 parts, 112 snippets
```

Each snippet file is named `NNN-meaningful-slug.md`, where `NNN` is the slide number. The markdown body contains the slide title, the full code block, and the Korean speaker note.

## Contributing

Contributions are welcome. Follow this flow:

1. **Fork** the repository on GitHub.
2. **Branch** from `main`: `git checkout -b fix/your-change`.
3. **Commit** using [Conventional Commits](https://www.conventionalcommits.org):
   - `feat: add ch6-sdk multi-agent orchestration snippet`
   - `fix: correct retry backoff in 104-retry-python.md`
   - `docs: clarify directory layout in README`
4. **Push** to your fork: `git push origin fix/your-change`.
5. **Open a Pull Request** referencing the relevant issue and describing the change.

For changes that affect snippet content, please cite the source slide number in the commit body so reviewers can cross-reference the PDF.

## License

This project is distributed under **Proprietary** terms. Internal use, private delivery to customers, and modification for internal training are permitted; external redistribution and commercial resale are prohibited.

## Contact

- Maintainer: **Youngjin Kim**
- Email: comeddy@gmail.com
- GitHub: [github.com/comeddy](https://github.com/comeddy)
- Issues: open an issue on the repository hosting this project.

---

<a id="korean"></a>

# 한국어

## 개요

Claude Code Deep Dive Workshop은 발표 가능한 PDF 슬라이드 자료와 워크샵에서 사용된 모든 코드 예제를 검색 가능한 형태로 함께 제공하는 한국어 기술 커리큘럼입니다. 챕터 PDF는 날짜 기반 에디션 디렉토리로 제공됩니다 — 최초 에디션은 `20260525/`, 최신 에디션은 Claude Code 2.1.198 기준으로 새로 제작한 `20260703/`이며 각 에디션은 6개 챕터로 구성됩니다. `tech_doc/`에는 Claude Code 아키텍처와 비용 효율화를 다루는 보조 심층 문서가 들어 있습니다. 슬라이드 자료와 함께 `Script/workshop-code/` 아래에는 코드를 포함한 슬라이드를 각각 독립된 마크다운 파일로 추출한 502개의 스니펫이 제공되며, 각 파일에는 한국어 발표자 노트가 포함되어 있습니다. 모든 슬라이드 자료는 일관된 디자인 시스템을 따라 시각 정체성을 유지합니다.

## 주요 기능

- **에디션별 6개 챕터 PDF** — Overview, Agents & Subagents, Admin Setup, Settings, CLI Reference, Agent SDK. 각 커리큘럼 에디션은 날짜 디렉토리(`20260525/`, `20260703/`)로 제공됩니다. 최신 `20260703/` 에디션은 Claude Code 2.1.198 기준으로 새로 제작되었습니다.
- **보조 기술 문서** — `tech_doc/`에 커리큘럼 외 심층 참고 자료인 `ClaudeCode-Architecture.pdf`와 `Claude_Cost_Efficiency.pdf`가 포함됩니다.
- **핸즈온랩 가이드** — `ccw-hands-on-lab/`에 챕터별 랩 6개(Ch1–Ch6), 캡스톤 랩 6개(main, B, C, D, E, F), 참조 문서 3개(슬래시 커맨드, 플러그인, 디렉토리 구조)가 독립 실행형 HTML로 제공되며, 진입점 역할을 하는 `index.html` 포털 페이지가 포함됩니다. 랩은 Anthropic 구독/Enterprise와 Claude Code on Bedrock 두 인증 경로를 모두 다룹니다. [comeddy.github.io/ccw-hands-on-lab](https://comeddy.github.io/ccw-hands-on-lab/)에 게시되어 있습니다.
- **502개 추출 코드 스니펫** — 코드를 포함하는 모든 슬라이드가 `Script/workshop-code/` 아래에 챕터·파트 단위로 번호가 매겨진 마크다운으로 정리되어 빠른 검색이 가능합니다.
- **코드 수준의 이중 언어 지원** — SDK 자료 전반에 Python과 TypeScript 예제가 나란히 제공되며, 3가지 인증 경로(Anthropic Direct, Amazon Bedrock, Vertex AI)를 모두 다룹니다.
- **스니펫별 한국어 발표자 노트** — 추출된 모든 마크다운 파일에 코드와 함께 원본 한국어 발표 스크립트가 포함됩니다.
- **빌드 단계 없는 즉시 활용** — PDF와 마크다운이 사전 렌더링되어 제공되므로 PDF 뷰어와 텍스트 에디터만 있으면 바로 사용할 수 있습니다.

## 사전 요구 사항

- 날짜 에디션 디렉토리(`20260525/`, `20260703/`)와 `tech_doc/`의 PDF를 열어볼 수 있는 PDF 뷰어.
- `ccw-hands-on-lab/`의 핸즈온랩 가이드를 열어볼 수 있는 웹 브라우저.
- `Script/workshop-code/` 아래 마크다운을 확인할 수 있는 텍스트 에디터 또는 GitHub 웹 뷰어.
- 키워드나 파일명으로 스니펫을 찾기 위한 `grep`, `find` (또는 동등한 검색 도구).
- 저장소 클론에 사용할 `git`.

## 설치 방법

```bash
# 1. 저장소 클론
git clone https://github.com/comeddy/claude-code-workshop.git
cd claude-code-workshop

# 2. 최신 에디션에서 원하는 챕터 PDF 열기 (예: Chapter 1)
xdg-open 20260703/ClaudeCode_Ch1_20260703.pdf    # Linux
# open  20260703/ClaudeCode_Ch1_20260703.pdf       # macOS

# 3. 추출된 코드 스니펫 탐색
ls Script/workshop-code/ch6-sdk/part-06-production/
```

## 사용법

```bash
# Python retry 패턴 찾기
grep -rn "tenacity" Script/workshop-code/

# 전체 챕터에서 Hook 예제 찾기
grep -rn "PreToolUse" Script/workshop-code/

# 인증 관련 스니펫을 파일명으로 찾기
find Script/workshop-code/ -name "*auth*"

# 특정 파트의 스니펫 목록 확인
ls Script/workshop-code/ch6-sdk/part-01-sdk-basics/
# → 007-python-install-first-call.md
# → 008-typescript-install-first-call.md
# → ...

# 단일 스니펫 열기
cat Script/workshop-code/ch6-sdk/part-06-production/104-retry-python.md

# 보조 기술 문서 열기
xdg-open tech_doc/ClaudeCode-Architecture.pdf    # Linux
```

## 프로젝트 구조

```text
claude-code-workshop/
├── README.md                                  # 이 파일
├── CHANGELOG.md                               # 버전별 변경 사항
├── CLAUDE.md                                  # Claude Code 프로젝트 가이드
├── 20260525/                                  # 2026-05-25 에디션 챕터 PDF (Ch1–Ch6)
├── 20260703/                                  # 2026-07-03 에디션 (최신, Claude Code 2.1.198 기준)
├── ccw-hands-on-lab/                          # 핸즈온랩 가이드 (HTML)
│   ├── index.html                             # 랩 포털 진입 페이지
│   ├── ClaudeCode_Ch{1..6}_HandsOnLab.html    # 챕터별 랩 (Ch1–Ch6)
│   ├── ClaudeCode_Capstone*_HandsOnLab.html   # 캡스톤 랩 (main, B, C, D, E, F)
│   └── ClaudeCode_Reference{1..3}_*.html      # 참조 문서 (커맨드, 플러그인, 디렉토리)
├── tech_doc/                                  # 보조 기술 문서
│   ├── ClaudeCode-Architecture.pdf            # Claude Code 아키텍처 심층 문서
│   └── Claude_Cost_Efficiency.pdf             # Claude 비용 효율화 가이드
└── Script/
    ├── workshop-code-README.md                # 스니펫 아카이브 최상위 가이드
    └── workshop-code/                         # 추출된 502개 코드 스니펫
        ├── README.md
        ├── ch1-overview/                      # 10개 파트, 108개 스니펫
        ├── ch2-agents/                        #  9개 파트,  53개 스니펫
        ├── ch3-admin/                         #  9개 파트,  57개 스니펫
        ├── ch4-settings/                      #  9개 파트,  86개 스니펫
        ├── ch5-cli/                           #  8개 파트,  86개 스니펫
        └── ch6-sdk/                           #  8개 파트, 112개 스니펫
```

각 스니펫 파일은 `NNN-의미있는-슬러그.md` 형식이며, `NNN`은 슬라이드 번호입니다. 마크다운 본문에는 슬라이드 제목, 전체 코드 블록, 한국어 발표자 노트가 포함됩니다.

## 기여 방법

기여를 환영합니다. 아래 순서를 따라 주세요.

1. GitHub에서 저장소를 **포크(Fork)** 합니다.
2. `main`에서 새 **브랜치(Branch)** 를 생성합니다: `git checkout -b fix/your-change`.
3. [Conventional Commits](https://www.conventionalcommits.org) 형식으로 **커밋(Commit)** 합니다.
   - `feat: ch6-sdk 멀티 에이전트 오케스트레이션 스니펫 추가`
   - `fix: 104-retry-python.md의 retry backoff 수정`
   - `docs: README의 디렉토리 구조 설명 명확화`
4. 포크된 저장소에 **푸시(Push)** 합니다: `git push origin fix/your-change`.
5. 관련 이슈를 참조하고 변경 사항을 설명하며 **Pull Request** 를 엽니다.

스니펫 내용이 변경되는 경우, 리뷰어가 PDF와 대조할 수 있도록 커밋 본문에 원본 슬라이드 번호를 명시해 주세요.

## 라이선스

이 프로젝트는 **Proprietary** 조건으로 배포됩니다. 내부 활용, 고객사 대상 비공개 발표, 사내 교육 목적의 수정은 허용되며, 외부 공개 재배포와 상업적 재판매는 금지됩니다.

## 연락처

- 메인테이너: **김영진(Youngjin Kim)**
- 이메일: comeddy@gmail.com
- GitHub: [github.com/comeddy](https://github.com/comeddy)
- 이슈: 이 프로젝트가 호스팅된 저장소에 이슈를 등록해 주세요.
