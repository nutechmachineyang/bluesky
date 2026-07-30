# 📝 문제 보고서 & 변경 이력 (Issue Report & Changelog)

이 문서는 **양 헌 (Harry Yang) 공식 웹사이트** 개발 및 유지보수 과정에서 발견된 주요 문제점, 해결책 및 업데이트 변경 이력을 기록하는 문서입니다.

---

## 1. 현재 감지된 주요 이슈 및 해결 가이드

### ⚠️ [이슈 01] 문의 폼(Contact Form) 백엔드 연동 필요
* **현상**: 현재 [`content/_index.md`](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/content/_index.md)의 `#contact` 섹션 내 커스텀 HTML 폼의 `action`이 `"#"`로 지정되어 있어 실제 문의 제출 시 데이터가 유실되거나 전송되지 않습니다.
* **해결책**: 향후 Formspree, Netlify Forms, Web3Forms 등 정적 웹사이트용 폼 백엔드 서비스를 연동하고 `action="[API_URL]"`을 업데이트해야 합니다.

### ⚠️ [이슈 02] Hugo Extended 버전 의존성
* **현상**: Hugo Blox Builder는 Sass/SCSS 컴파일이 필요하므로, 기본 Hugo가 아닌 **Hugo Extended** 버전이 설치되어 있어야 로컬 빌드가 정상 작동합니다.
* **해결책**: 로컬 개발 시 반드시 `hugo version` 명령어로 `extended` 버전이 맞는지 확인하십시오. (예: `Hugo Static Site Generator v0.162.0/extended`)

### ⚠️ [이슈 03] 테마 커스텀 클래스 충돌 방지
* **현상**: 커스텀 CSS 작성 시 기존 TailwindCSS 스타일이나 Hugo Blox 테마 내장 스타일과 명칭이 겹쳐 레이아웃이 깨질 우려가 있습니다.
* **해결책**: 커스텀 CSS 클래스는 고유의 접두사(예: `hy-`)를 붙여 작성하는 것을 권장합니다.

### ⚠️ [이슈 04] 로컬 빌드 시 pnpm 명령어 실행 불가로 인한 빌드 실패
* **현상**: `npm run build` 실행 시 내부적으로 `pnpm run pagefind`가 호출되나, 시스템에 `pnpm`이 글로벌하게 설치되어 있지 않은 경우 `'pnpm' is not recognized` 에러가 발생하여 빌드가 최종 실패합니다.
* **해결책**: `package.json`의 빌드 스크립트 중 `pnpm run pagefind`를 `npx pagefind --site public` 또는 `npm run pagefind`로 변경하거나, 로컬 개발 환경에 `pnpm`을 글로벌로 설치(`npm install -g pnpm`)하여 해결해야 합니다.

### ⚠️ [이슈 05] Cloudflare Pages 빌드 명령어 오타 (`--go` 플래그 오류)
* **현상**: Cloudflare Pages 빌드 시 `Executing user command: hugo --go --minify`가 실행되며 `ERROR command error: unknown flag: --go` 에러로 빌드가 실패합니다.
* **해결책**: Cloudflare Pages 대시보드의 Build command(빌드 명령어) 설정에서 오타 플래그인 `--go`를 제거/수정하거나, `npm run build` (또는 `pnpm run build`)로 변경해야 합니다. (Hugo 가비지 컬렉션 플래그는 `--gc`입니다.)

---

## 2. 프로젝트 변경 이력 (Changelog)

### [2026-07-28] Cloudflare Pages 메인 도메인 설정에 따른 baseURL 업데이트 (작업자: Antigravity AI)
* **내용**:
  * [`config/_default/hugo.yaml`](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/config/_default/hugo.yaml)의 `baseURL`을 `https://bluesky-pages.dev/`로 변경하여 Cloudflare Pages 배포 시 자원 로드 및 경로 이탈 현상 방지.

### [2026-07-28] 로컬 개발 서버 스크립트 오버라이드 수정 (작업자: Antigravity AI)
* **내용**:
  * [package.json](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/package.json)의 `dev` 스크립트에 `-b http://localhost:1313/` 옵션을 추가하여, 로컬 실행 시 GitHub Pages `baseURL` 경로(`/bluesky/`)로 인해 발생하던 404/자원 로드 문제 해결.

### [2026-07-28] Cloudflare Pages 빌드 오류 원인 분석 및 이슈 기록 (작업자: Antigravity AI)
* **내용**:
  * Cloudflare Pages 빌드 로그 분석 결과, 빌드 명령어 내 존재하지 않는 `--go` 플래그 오타로 인한 실패 원인 규명.
  * 해결 가이드 및 [issues.md](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/doc/issues.md) 내 이슈 05 기록 추가.

### [2026-07-28] 현재 상황 점검 및 빌드 스크립트 이슈 추가 (작업자: Antigravity AI)
* **내용**:
  * 현재 프로젝트 설정(hugo.yaml, params.yaml, menus.yaml, content/_index.md)의 적합성을 전반적으로 점검.
  * 로컬 빌드 테스트 과정에서 발견된 `pnpm` 의존성 문제(이슈 04)를 `doc/issues.md`에 추가 기록.

### [2026-07-16] 초기 프로젝트 구성 및 매뉴얼 작성 (작업자: Antigravity AI)
* **내용**:
  * 현 사이트의 구성 파악 및 기획안([plan.md](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/plan.md))과 콘텐츠 싱크 정합성 검토.
  * 프로젝트 공식 제작 매뉴얼([doc/manual.md](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/doc/manual.md)) 신규 생성.
  * 문제 보고서 및 변경 이력([doc/issues.md](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/doc/issues.md)) 신규 생성.
  * 루트 디렉토리의 [README.md](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/README.md)에 문서 링크 추가 및 연동.
  * 프로젝트 전용 AI 규칙 파일([.agents/AGENTS.md](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/.agents/AGENTS.md)) 생성 및 문서 자동 갱신 룰 추가.

### [2026-07-16] GitHub 원격 저장소 연동 및 배포 환경 구성 (작업자: Antigravity AI)
* **내용**:
  * 원격 저장소 `https://github.com/nutechmachineyang/bluesky.git` 추가.
  * [`config/_default/hugo.yaml`](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/config/_default/hugo.yaml)의 `baseURL`을 `https://nutechmachineyang.github.io/bluesky/`로 수정하여 GitHub Pages 경로 오류 방지.

---

## 3. 작성 가이드
* 새로운 기능 개발, 설정 변경, 버그 수정이 발생할 때마다 **2. 프로젝트 변경 이력** 섹션에 날짜와 상세 내용을 추가하십시오.
* 신규 버그 또는 개선이 필요한 이슈 발견 시 **1. 현재 감지된 주요 이슈 및 해결 가이드**에 기록하고 추적하십시오.
