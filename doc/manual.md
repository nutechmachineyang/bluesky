# 🛠️ 제작 매뉴얼 (Production Manual)

이 문서는 **양 헌 (Harry Yang) - 항공 역학 및 안전 부문 기술 전문가 공식 웹사이트** 프로젝트의 구성, 제작 가이드 및 유지보수를 위한 지침서입니다.

---

## 1. 프로젝트 개요
* **대상**: 양 헌 (Harry Yang) | 항공 역학 및 안전 분야 기술 전문가
* **목적**: 전문성(공기역학 분석, SMS 검증, FDR 최적화 등)을 강조하고 자문 및 프로젝트 의뢰를 유도하는 공식 포트폴리오/랜딩 웹사이트
* **기술 스택**: 
  * 정적 사이트 생성기: **Hugo (v0.162.0)**
  * 프레임워크: **Hugo Blox Builder** (SaaS Landing Page 템플릿)
  * **호스팅/배포**: Cloudflare Pages / GitHub Pages (도메인: https://bluesky-pages.dev/, 저장소: https://github.com/nutechmachineyang/bluesky.git)

---

## 2. 프로젝트 디렉토리 구조
프로젝트의 핵심 디렉토리 및 파일 정보는 다음과 같습니다:

```text
harryyang/
├── .agents/
│   └── AGENTS.md            # AI 에이전트를 위한 작업 규칙 및 가이드
├── config/
│   └── _default/
│       ├── menus.yaml       # 상/하단 메뉴 네비게이션 설정
│       └── params.yaml      # 사이트 전역 정보, SEO, 테마 설정
├── content/
│   └── _index.md            # 메인 랜딩 페이지 콘텐츠 및 레이아웃 정의 (YAML Frontmatter)
├── doc/
│   ├── manual.md            # [본 파일] 제작 매뉴얼
│   └── issues.md            # 문제 해결 및 변경 이력 보고서
├── hugoblox.yaml            # Hugo Blox 빌더 핵심 템플릿 설정
└── README.md                # 프로젝트 메인 리드미
```

---

## 3. 주요 구성 및 설정 방법

### A. 기본 정보 및 SEO 설정
* **위치**: [`config/_default/params.yaml`](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/config/_default/params.yaml)
* **내용**: 
  * `identity.name`: 사이트 표시 이름 (`양 헌`)
  * `identity.tagline`: 메인 타이틀 아래 슬로건
  * `identity.description`: 검색 노출용 SEO 설명문
  * `theme`: 테마 모드(`dark` 기본), Slate 배경색, Blue/Sky 계열 포인트 색상 설정

### B. 네비게이션 메뉴
* **위치**: [`config/_default/menus.yaml`](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/config/_default/menus.yaml)
* **내용**: 
  * 상단 네비게이션 바 링크 구성. `#top`, `#about`, `#projects`, `#career`, `#contact` 해시 링크를 통해 한 페이지 내에서 스크롤 이동하도록 설정되어 있습니다.

### C. 페이지 레이아웃 및 콘텐츠 편집
* **위치**: [`content/_index.md`](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/content/_index.md)
* **구성 섹션**:
  1. **Hero (`#top`)**: 메인 헤드라인 및 배경 radial mesh orb 애니메이션 설정
  2. **Features (`#about`)**: 주요 강점 3대 요소 소개 (공기역학, 안전 프로토콜, 기술 자문)
  3. **Features (`#projects`)**: Bento 그리드 형태의 포트폴리오 및 프로젝트 수행 실적
  4. **Steps (`#career`)**: 수평 타임라인 레이아웃 기반의 상세 핵심 스킬
  5. **Markdown (`#contact`)**: 문의 접수를 위한 커스텀 HTML/CSS 폼 탑재

---

## 4. 로컬 개발 및 실행 방법

### 요구사항
* Hugo Extended 버전 설치 권장
* Node.js 설치

### 실행 명령어
로컬에서 실시간 반영 서버를 띄워 확인하려면 아래 명령어를 사용합니다. (기본 주소: `http://localhost:1313`)

```bash
# npm 스크립트 실행 (Base URL 오버라이드가 적용되어 서브경로 없이 http://localhost:1313/으로 바로 접속 가능)
npm run dev
```

또는 CLI 명령어로 직접 실행할 경우:
```bash
hugo server --disableFastRender -b http://localhost:1313/
```

> 💡 **Windows PowerShell 권한 관련 팁**:
> PowerShell에서 `npm run dev` 실행 시 스크립트 보안 정책 오류(`UnauthorizedAccess / PSSecurityException`)가 발생하는 경우, 터미널을 **CMD**로 전환하여 `cmd /c npm run dev`를 실행하거나 직접 `hugo server` 명령어를 입력하십시오.

---

## 5. 유지보수 및 추가 개발 가이드
* **새로운 섹션 추가**: [`content/_index.md`](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/content/_index.md)의 `sections` 리스트 하단에 적절한 `block` 타입(features, steps, contact 등)을 추가하여 작성합니다.
* **디자인 커스텀**: [`content/_index.md`](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/content/_index.md) 내 각 섹션의 `design` 필드를 통해 패딩, 마진, 배경 그라디언트, 커스텀 CSS 클래스 등을 쉽게 수정할 수 있습니다.
* **문서 업데이트 규칙**: 프로젝트 파일이 변경되거나 구조가 바뀔 시, 본 매뉴얼과 [`doc/issues.md`](file:///c:/Users/nutec/OneDrive/Desktop/harryyang/doc/issues.md)를 함께 갱신해야 합니다.
