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

---

## 2. 프로젝트 변경 이력 (Changelog)

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
