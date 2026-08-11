---
title: '양 헌 | 항공 역학 및 안전 부문 기술 전문가'
date: 2026-07-07
type: landing

sections:
  - block: hero
    id: top
    content:
      eyebrow: 항공 역학 및 비행 안전 기술 자문
      title: 정밀한 항공 역학 분석과 [안전 비행]을 위한 고도의 기술 자문
      text: 유체역학, 공기역학적 분석과 철저한 안전 검증을 통해 항공기 운항의 안정성을 높이고 잠재적 위험 요소를 예방합니다.
      primary_action:
        text: 기술 자문 의뢰하기
        url: "#contact"
        icon: envelope
        style: gradient
      secondary_action:
        text: 소개 보기
        url: "#about"
        icon: user
        style: ghost
      trust:
        stars: 5
        text: "**타협 없는 정밀함이 가장 안전한 비행을 만듭니다.**"
    design:
      spacing:
        padding: [0, 0, 0, 0]
        margin: [0, 0, 0, 0]
      css_class: "dark"
      section_break:
        fade_bottom: "#0a0e27"
      background:
        color: "#0a0e27"
        gradient:
          type: radial
          start: "rgba(30,58,138,0.5)" # Navy spotlight
          end: "transparent"
          position: "50% -10%"
          shape: ellipse
          size: "80% 80%"
        gradient_mesh:
          enable: true
          style: orbs
          intensity: medium
          animation: pulse
          colors: ["primary-500/20", "secondary-500/20"]
          orb_count: 2
          positions: ["top-1/3 left-1/4", "bottom-1/3 right-1/4"]
          sizes: ["w-[32rem] h-[32rem]", "w-[26rem] h-[26rem]"]

  - block: features
    id: about
    content:
      subtitle: About Harry Yang
      title: 타협 없는 정밀함으로 완성하는 최고의 비행 안정성
      text: 수년간 항공 역학 분야에서 쌓아온 전문 지식을 바탕으로 안전 비행을 위한 최적의 기술 자문 솔루션을 제공합니다. 항공기의 물리적 특성과 운항 데이터 분석을 통해 잠재적 위험 요소를 예방하고 신뢰할 수 있는 안전 프로토콜을 구축합니다.
      items:
        - name: 정밀한 공기역학 분석 (Aerodynamics Analysis)
          icon: sparkles
          description: 고고도 및 실속(Stall) 특성 분석, CFD 기반 유동 해석 등 최첨단 항공 역학 설계와 유체역학 솔루션을 검증합니다.
        - name: 엄격한 안전 프로토콜 검증 (Safety Protocol Auditing)
          icon: shield-check
          description: 이착륙 단계별 안전 위험 요소 평가와 글로벌 표준(FAA, SMS 등)에 따른 최적화된 안전 관리 시스템(SMS)을 제공합니다.
        - name: 실효성 있는 기술 자문 (Practical Technical Advisory)
          icon: bolt
          description: 실제 운항 비행 기록 데이터(FDR) 분석 및 규정 준수 패키지 검증을 통하여 즉각적으로 실행 가능한 안전 가이드를 제안합니다.
    design:
      layout: grid
      css_class: "bg-white dark:bg-gray-900"
      spacing:
        padding: ["6rem", 0, "6rem", 0]

  - block: features
    id: projects
    content:
      subtitle: Advisory Projects
      title: 신뢰를 바탕으로 한 주요 자문 실적
      text: 대외비 준수를 위해 세부 내용을 가공한 대표적인 자문 프로젝트 성과입니다. 비행 동역학 시뮬레이션부터 글로벌 안전 규정 패키지 패스포트까지 정밀하게 진단했습니다.
      items:
        - name: 고고도 및 실속(Stall) 특성 분석 자문
          icon: chart-bar
          description: |
            **역할: 수석 기술 자문 (Technical Advisor)**  
            대형 기종의 고고도 운항 중 발생 가능한 공기역학적 불안정성을 정밀 분석하고 예측 가능한 이착륙 안전 마진 및 예방 솔루션을 제시하였습니다.
        - name: 항공 안전 관리 시스템(SMS) 프로토콜 검증
          icon: shield-check
          description: |
            **역할: 안전 검증 책임 (Safety Protocol Auditor)**  
            글로벌 운항 표준에 부합하는 이착륙 단계별 위험 요소를 정량적으로 평가하고 항공사 및 정비 단체의 비행 안전 프로토콜 가이드라인을 최적화했습니다.
        - name: 비행 데이터(FDR) 분석 기반 운항 효율성 최적화
          icon: check-badge
          description: |
            **역할: 역학 데이터 분석가 (Aerodynamics Data Analyst)**  
            실제 FDR 비행 기록 데이터를 기반으로 이착륙 및 순항 시의 양항비(Lift-to-Drag Ratio)를 분석하여 안전 한계를 준수하면서도 연료 효율을 극대화할 수 있는 비행 기동 경로를 자문했습니다.
    design:
      layout: bento
      css_class: "bg-gray-50 dark:bg-gray-900/50"
      spacing:
        padding: ["6rem", 0, "6rem", 0]

  - block: steps
    id: career
    content:
      title: 주요 자문 분야 및 보유 기술 이력
      text: 항공 우주 공학, 유체 역학 및 비행 안전 공학 자문 분야의 전문 기술 이력입니다.
      items:
        - title: Computational Fluid Dynamics (CFD) 해석 자문
          text: 고성능 CFD 해석 툴을 활용하여 날개 주변 및 기체 표면의 유체역학적 거동을 정밀 시뮬레이션하고 유동 실현성 및 공력 문제를 해결합니다.
          icon: computer-desktop
        - title: Flight Data Monitoring (FDM) 및 안전 위험도 평가
          text: 비행 기록 데이터 기반 모니터링 체계를 구축하고, 축적된 운항 원시 데이터를 분석해 위험 이벤트의 발생 추이를 정밀 예측합니다.
          icon: chart-bar
        - title: FAA / 글로벌 항공 안전 규정 검증 자문
          text: 미 연방항공청(FAA) 및 국제민간항공기구(ICAO) 안전 지침 표준에 부합하도록 적합성 서류 검토 및 안전성 검증 패키지를 설계합니다.
          icon: shield-check
    design:
      layout: horizontal
      marker_style: icon
      connector: none
      css_class: "bg-white dark:bg-gray-900"
      spacing:
        padding: ["6rem", 0, "6rem", 0]

  - block: collection
    id: blog
    content:
      title: 📝 기술 칼럼 & 인사이트
      subtitle: Technical Articles
      text: 항공 역학, 비행 안전, FDR 데이터 분석 관련 전문 칼럼과 정보입니다. 지속적으로 최신 기술 글이 업데이트됩니다.
      filters:
        folders:
          - blog
      count: 6
    design:
      columns: "2"
      css_class: "bg-white dark:bg-gray-900"
      spacing:
        padding: ["6rem", 0, "6rem", 0]

  - block: markdown
    id: contact
    content:
      title: ✉️ 기술 자문 및 프로젝트 문의
      subtitle: Contact Harry Yang
      text: |
        항공 기술 자문, 프로젝트 협업, 전문가 자문 위원 초빙 등 관련 문의는 아래 폼을 통해 보내주시면 신속하게 답변드리겠습니다.

        <div class="mt-8 max-w-xl mx-auto">
          <form action="#" method="POST" class="space-y-6 text-left bg-white dark:bg-gray-800 p-8 rounded-xl border border-gray-200 dark:border-gray-700 shadow-lg">
            <div>
              <label for="name" class="block text-sm font-medium text-gray-700 dark:text-gray-300">성함 / 기관명 (Name / Organization)</label>
              <input type="text" name="name" id="name" required class="mt-1 block w-full rounded-md border-gray-300 dark:border-gray-600 bg-gray-50 dark:bg-gray-900 text-gray-900 dark:text-white shadow-sm focus:border-blue-500 focus:ring-blue-500 px-4 py-2 border">
            </div>
            <div>
              <label for="email" class="block text-sm font-medium text-gray-700 dark:text-gray-300">이메일 주소 (Email Address)</label>
              <input type="email" name="email" id="email" required class="mt-1 block w-full rounded-md border-gray-300 dark:border-gray-600 bg-gray-50 dark:bg-gray-900 text-gray-900 dark:text-white shadow-sm focus:border-blue-500 focus:ring-blue-500 px-4 py-2 border">
            </div>
            <div>
              <label for="inquiry_type" class="block text-sm font-medium text-gray-700 dark:text-gray-300">문의 유형 (Inquiry Type)</label>
              <select name="inquiry_type" id="inquiry_type" class="mt-1 block w-full rounded-md border-gray-300 dark:border-gray-600 bg-gray-50 dark:bg-gray-900 text-gray-900 dark:text-white shadow-sm focus:border-blue-500 focus:ring-blue-500 px-4 py-2 border">
                <option>기술 자문 (Technical Consultation)</option>
                <option>프로젝트 협업 (Project Collaboration)</option>
                <option>세미나 및 자문 위원 요청 (Advisory Request)</option>
                <option>기타 (Others)</option>
              </select>
            </div>
            <div>
              <label for="message" class="block text-sm font-medium text-gray-700 dark:text-gray-300">문의 내용 (Message)</label>
              <textarea name="message" id="message" rows="4" required class="mt-1 block w-full rounded-md border-gray-300 dark:border-gray-600 bg-gray-50 dark:bg-gray-900 text-gray-900 dark:text-white shadow-sm focus:border-blue-500 focus:ring-blue-500 px-4 py-2 border"></textarea>
            </div>
            <div>
              <button type="submit" class="w-full flex justify-center py-3 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-blue-600 hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500 cursor-pointer transition-colors duration-200">
                문의 보내기 (Submit)
              </button>
            </div>
          </form>
        </div>
    design:
      css_class: "bg-gray-50 dark:bg-gray-900/50"
      spacing:
        padding: ["6rem", 0, "6rem", 0]
---
