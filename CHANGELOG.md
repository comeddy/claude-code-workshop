# Changelog

<a href="#english"><img src="https://img.shields.io/badge/lang-English-blue.svg" alt="English"></a>
<a href="#korean"><img src="https://img.shields.io/badge/lang-한국어-red.svg" alt="Korean"></a>

---

<a id="english"></a>

# English

All notable changes to this project will be documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.2.0] - 2026-07-26

### Added

- Add the Capstone E hands-on lab (`ClaudeCode_CapstoneE_HandsOnLab.html`), an agentic game-development mission that builds a Canvas platformer starring Clawd and deploys it via S3/CloudFront without Bedrock, and add its portal card.
- Add the Capstone F hands-on lab (`ClaudeCode_CapstoneF_HandsOnLab.html`), a generative-art exhibition mission that renders two Canvas artworks, extracts a shared contract from the second, and deploys via S3/CloudFront without Bedrock, and add its portal card.
- Add a claude-hud status-line HUD install step (marketplace add, install, reload, setup) to Mission 0 of all six capstone labs, with a checklist item confirming the status line is visible.

## [1.1.0] - 2026-07-25

### Added

- Add the 2026-07-03 edition of all six chapter PDFs under `20260703/`, newly authored against Claude Code 2.1.198.
- Add `tech_doc/ClaudeCode-Architecture.pdf`, a Claude Code architecture deep-dive document.
- Add `tech_doc/Claude_Cost_Efficiency.pdf`, a Claude cost efficiency guide.
- Add a root `CLAUDE.md` documenting repository layout and content conventions for Claude Code.
- Add `ccw-hands-on-lab/`, a hands-on lab archive of self-contained HTML guides: six chapter labs (Ch1–Ch6) and four capstone labs (main, B, C, D), entered through an `index.html` portal page.
- Add three reference pages to the lab archive covering slash commands, plugins, and the Claude Code directory structure.
- Add GitHub link cards for the 20260703 slide sources and `tech_doc/` to the lab portal page.
- Publish the hands-on lab guides to GitHub Pages at [comeddy.github.io/ccw-hands-on-lab](https://comeddy.github.io/ccw-hands-on-lab/).

### Changed

- Move the 2026-05-25 chapter PDFs from the project root into `20260525/` so each curriculum edition lives in its own date-stamped directory.
- Group supplementary technical documents under `tech_doc/`, separate from the chapter curriculum.
- Update `README.md` paths, project structure tree, and usage examples to reflect the edition directories and `tech_doc/`.
- Update `README.md` features, prerequisites, and project structure tree to document `ccw-hands-on-lab/` and link the published lab portal.
- Revise the Chapter 2 hands-on lab content.
- Point the lab portal GitHub link cards at the `comeddy/claude-code-workshop` repository.
- Rename superpowers workflow commands across the capstone labs and plugin reference to their namespaced forms: `/superpowers:brainstorming`, `/superpowers:writing-plans`, `/superpowers:executing-plans`.
- Split the Bedrock smoke test into a dedicated Claude Code on Bedrock-only step in Mission 0 of all four capstone labs, with per-capstone callouts explaining what the smoke validates.
- Update the lab portal hero metadata to present both authentication paths: Anthropic subscription/Enterprise or Claude Code on Bedrock.

## [1.0.1] - 2026-05-27

### Changed

- Move the six chapter PDFs from `PDF/` to the project root so they can be opened directly without descending into a subdirectory.
- Update `README.md` paths, project structure tree, and usage examples to reflect the new PDF location.

### Removed

- Remove the now-empty `PDF/` directory from the repository.

## [1.0.0] - 2026-05-25

### Added

- Publish the initial Claude Code Deep Dive Workshop release as a PDF-centric distribution of the three-day, 850-slide curriculum.
- Distribute Chapter 1 (Overview, 200 slides) as `PDF/ClaudeCode_Ch1_20260525.pdf`.
- Distribute Chapter 2 (Agents & Subagents, 110 slides) as `PDF/ClaudeCode_Ch2_20260525.pdf`.
- Distribute Chapter 3 (Admin Setup, 120 slides) as `PDF/ClaudeCode_Ch3_20260525.pdf`.
- Distribute Chapter 4 (Settings, 140 slides) as `PDF/ClaudeCode_Ch4_20260525.pdf`.
- Distribute Chapter 5 (CLI Reference, 130 slides) as `PDF/ClaudeCode_Ch5_20260525..pdf`.
- Distribute Chapter 6 (Agent SDK, 150 slides) as `PDF/ClaudeCode_Ch6_20260525.pdf`.
- Add the extracted code snippet archive under `Script/workshop-code/`, totaling 502 markdown files across six chapter folders and 53 part folders.
- Include 108 snippets under `ch1-overview` across 10 parts covering installation, IDE integration, and CLAUDE.md authoring.
- Include 53 snippets under `ch2-agents` across 9 parts covering subagent definition, the Task tool, and five production patterns.
- Include 57 snippets under `ch3-admin` across 9 parts covering deployment, credentials, network security, governance, SSO, and audit logging.
- Include 86 snippets under `ch4-settings` across 9 parts covering `settings.json`, permissions, hooks, MCP, and custom slash commands.
- Include 86 snippets under `ch5-cli` across 8 parts covering the `claude` CLI, headless mode, output formats, and CI/CD integration.
- Include 112 snippets under `ch6-sdk` across 8 parts covering SDK basics, the Messages API, tool use, streaming, MCP integration, and production patterns.
- Provide Python and TypeScript samples side by side across the Agent SDK material.
- Cover three authentication paths in all SDK examples: Anthropic Direct, Amazon Bedrock, and Vertex AI.
- Embed a single-sentence Korean speaker note in every extracted snippet markdown file.
- Apply a consistent design system — 16:9 ratio, Black/Navy theme (`#161D26`), accent color (`#FF9900`) — across all six chapter PDFs.
- Add `Script/workshop-code-README.md` and `Script/workshop-code/README.md` as navigation guides for the snippet archive.

[Unreleased]: https://github.com/comeddy/claude-code-workshop/compare/v1.2.0...HEAD
[1.2.0]: https://github.com/comeddy/claude-code-workshop/compare/v1.1.0...v1.2.0
[1.1.0]: https://github.com/comeddy/claude-code-workshop/compare/v1.0.1...v1.1.0
[1.0.1]: https://github.com/comeddy/claude-code-workshop/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/comeddy/claude-code-workshop/releases/tag/v1.0.0

---

<a id="korean"></a>

# 한국어

이 프로젝트의 모든 주요 변경 사항은 이 파일에 기록됩니다.
이 문서는 [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)를 기반으로 하며, [Semantic Versioning](https://semver.org/spec/v2.0.0.html)을 따릅니다.

## [Unreleased]

## [1.2.0] - 2026-07-26

### Added

- Clawd가 주인공인 Canvas 플랫포머를 Bedrock 없이 S3/CloudFront로 배포하는 에이전틱 게임 개발 미션 Capstone E 랩(`ClaudeCode_CapstoneE_HandsOnLab.html`)과 포털 카드 추가.
- Canvas 제너러티브 아트 두 점을 그리고 두 번째 작품에서 공통 계약을 추출해 Bedrock 없이 S3/CloudFront로 전시를 개장하는 Capstone F 랩(`ClaudeCode_CapstoneF_HandsOnLab.html`)과 포털 카드 추가.
- 캡스톤 랩 6종의 Mission 0에 claude-hud 상태줄 HUD 설치 스텝(marketplace add, install, reload, setup)과 상태줄 표시 확인 체크 항목 추가.

## [1.1.0] - 2026-07-25

### Added

- Claude Code 2.1.198 기준으로 새로 제작한 2026-07-03 에디션 챕터 PDF 6종을 `20260703/` 아래에 추가.
- Claude Code 아키텍처 심층 문서 `tech_doc/ClaudeCode-Architecture.pdf` 추가.
- Claude 비용 효율화 가이드 `tech_doc/Claude_Cost_Efficiency.pdf` 추가.
- 저장소 구조와 콘텐츠 규약을 기술한 루트 `CLAUDE.md` 추가.
- 챕터별 랩 6개(Ch1–Ch6)와 캡스톤 랩 4개(main, B, C, D)를 독립 실행형 HTML로 담은 핸즈온랩 아카이브 `ccw-hands-on-lab/`을 `index.html` 포털 페이지와 함께 추가.
- 슬래시 커맨드, 플러그인, Claude Code 디렉토리 구조를 다루는 참조 문서 3종을 랩 아카이브에 추가.
- 랩 포털 페이지에 20260703 강의자료와 `tech_doc/`으로 연결되는 GitHub 링크 카드 추가.
- 핸즈온랩 가이드를 GitHub Pages([comeddy.github.io/ccw-hands-on-lab](https://comeddy.github.io/ccw-hands-on-lab/))에 게시.

### Changed

- 2026-05-25 챕터 PDF를 저장소 루트에서 `20260525/` 디렉토리로 이동하여 커리큘럼 에디션을 날짜 디렉토리 단위로 관리하도록 변경.
- 보조 기술 문서를 챕터 커리큘럼과 분리하여 `tech_doc/` 아래로 정리.
- 에디션 디렉토리와 `tech_doc/` 구조에 맞게 `README.md`의 경로, 프로젝트 구조 트리, 사용 예시 갱신.
- `ccw-hands-on-lab/` 디렉토리와 게시된 랩 포털 링크를 반영하도록 `README.md`의 주요 기능, 사전 요구 사항, 프로젝트 구조 트리 갱신.
- Chapter 2 핸즈온랩 콘텐츠 개정.
- 랩 포털의 GitHub 링크 카드를 `comeddy/claude-code-workshop` 저장소로 변경.
- 캡스톤 랩과 플러그인 참조 문서의 superpowers 워크플로 커맨드를 네임스페이스 표기(`/superpowers:brainstorming`, `/superpowers:writing-plans`, `/superpowers:executing-plans`)로 통일.
- 캡스톤 랩 4종의 Mission 0에서 Bedrock smoke 테스트를 Claude Code on Bedrock 경로 전용 스텝으로 분리하고, 캡스톤별 검증 대상을 설명하는 콜아웃 추가.
- Anthropic 구독/Enterprise와 Claude Code on Bedrock 두 인증 경로를 모두 안내하도록 랩 포털 히어로 메타 문구 갱신.

## [1.0.1] - 2026-05-27

### Changed

- 6개 챕터 PDF를 `PDF/` 하위에서 저장소 루트로 이동하여 하위 디렉토리로 진입하지 않고도 바로 열람 가능하도록 변경.
- `README.md` 의 PDF 경로, 프로젝트 구조 트리, 사용 예시를 변경된 PDF 위치에 맞게 갱신.

### Removed

- 비어 있는 `PDF/` 디렉토리를 저장소에서 제거.

## [1.0.0] - 2026-05-25

### Added

- 3일 850 슬라이드 분량의 Claude Code Deep Dive Workshop 커리큘럼을 PDF 중심 배포 형태로 최초 공개.
- Chapter 1 (Overview, 200 슬라이드) `PDF/ClaudeCode_Ch1_20260525.pdf` 로 배포.
- Chapter 2 (Agents & Subagents, 110 슬라이드) `PDF/ClaudeCode_Ch2_20260525.pdf` 로 배포.
- Chapter 3 (Admin Setup, 120 슬라이드) `PDF/ClaudeCode_Ch3_20260525.pdf` 로 배포.
- Chapter 4 (Settings, 140 슬라이드) `PDF/ClaudeCode_Ch4_20260525.pdf` 로 배포.
- Chapter 5 (CLI Reference, 130 슬라이드) `PDF/ClaudeCode_Ch5_20260525..pdf` 로 배포.
- Chapter 6 (Agent SDK, 150 슬라이드) `PDF/ClaudeCode_Ch6_20260525.pdf` 로 배포.
- 6개 챕터 폴더와 53개 파트 폴더에 걸친 총 502개 마크다운 파일로 구성된 코드 스니펫 아카이브를 `Script/workshop-code/` 아래에 추가.
- `ch1-overview` 10개 파트에 설치, IDE 통합, CLAUDE.md 작성을 다루는 108개 스니펫 포함.
- `ch2-agents` 9개 파트에 서브에이전트 정의, Task 도구, 5가지 실전 패턴을 다루는 53개 스니펫 포함.
- `ch3-admin` 9개 파트에 배포, 자격 증명, 네트워크 보안, 거버넌스, SSO, 감사 로그를 다루는 57개 스니펫 포함.
- `ch4-settings` 9개 파트에 `settings.json`, Permissions, Hooks, MCP, 커스텀 Slash 명령을 다루는 86개 스니펫 포함.
- `ch5-cli` 8개 파트에 `claude` CLI, Headless 모드, 출력 포맷, CI/CD 통합을 다루는 86개 스니펫 포함.
- `ch6-sdk` 8개 파트에 SDK 기초, Messages API, Tool Use, Streaming, MCP 통합, 프로덕션 패턴을 다루는 112개 스니펫 포함.
- Agent SDK 자료 전반에 Python과 TypeScript 예제 동등 제공.
- 모든 SDK 예제에 Anthropic Direct, Amazon Bedrock, Vertex AI 등 3가지 인증 경로 적용.
- 모든 추출 스니펫 마크다운 파일에 단문화된 한국어 발표자 노트 포함.
- 16:9 비율, Black/Navy 테마(`#161D26`), 액센트 컬러(`#FF9900`)로 구성된 일관된 디자인 시스템을 6개 챕터 PDF 전체에 일관 적용.
- 스니펫 아카이브 탐색을 돕는 `Script/workshop-code-README.md` 와 `Script/workshop-code/README.md` 추가.

[Unreleased]: https://github.com/comeddy/claude-code-workshop/compare/v1.2.0...HEAD
[1.2.0]: https://github.com/comeddy/claude-code-workshop/compare/v1.1.0...v1.2.0
[1.1.0]: https://github.com/comeddy/claude-code-workshop/compare/v1.0.1...v1.1.0
[1.0.1]: https://github.com/comeddy/claude-code-workshop/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/comeddy/claude-code-workshop/releases/tag/v1.0.0
