# 실행의 경계 — Coding Agent Sandbox

Slidev 발표자료. 본문 23장, 부록 3장, 출처 2장입니다. 발표 원고와 자체 JavaScript 컴포넌트는 없습니다.

[웹에서 발표자료 보기](https://tolskais.github.io/coding-agent-sandbox-seminar/)

`main` 브랜치에 push하면 GitHub Actions가 빌드하여 GitHub Pages에 자동 배포합니다.

## 열기

```sh
npm install
npm run dev
```

터미널에 표시되는 로컬 주소를 브라우저에서 엽니다. 화살표로 이동하며 Slidev 기본 목차·전체 화면 기능을 사용할 수 있습니다.

## 수정·출력

- `slides.md`: 슬라이드 내용, Mermaid 도식, 출처
- `style.css`: 기본 테마의 색·글꼴·간격 조정
- `npm run build`: 정적 웹 발표자료를 `dist/`로 출력

Slidev 52.19.1과 기본 테마를 사용하며, 툴팁 의존성 호환성을 위해 `floating-vue`를 5.2.2로 고정했습니다. `package-lock.json`도 함께 보관합니다.

## 발표 목표

Coding agent에서 Sandbox를 어떻게 구축하고 실행 경로에 연결하는지 설명한다. OS 기능의 상세 분류보다 Tool call 승인 → Sandbox 설정 → 격리된 명령 실행 → 결과 반환를 중심으로 구성한다.

## 범위

OS의 Process 제한 기능(Windows 중심, Linux 비교) → 실행 도구 → Agent별 구현과 MXC → Container 환경 구성 → Docker Sandboxes의 microVM 사례 순서입니다. 각 방식은 준비·실행 위치·제한을 강제하는 경계로 설명합니다. Codex, Claude Code, OpenCode V2, Docker Sandboxes를 앞의 구조에 연결합니다. 제품 문서와 공개 런타임 main의 지원 범위를 구분했습니다. 문서 확인일은 2026-09-13이며 특정 제품 버전의 실행 결과를 재현한 자료는 아닙니다.
