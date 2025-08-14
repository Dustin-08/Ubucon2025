# 🚀 Ubucon2025

Ubucon Korea 2025 행사 기록과 Canonical 워크숍 실습 자료를 정리한 저장소입니다.  
세션별 필기 노트📝와 발표 자료(PDF)📎, 그리고 “12‑factor 애플리케이션 end‑to‑end 배포” 워크숍 자료🧑💻를 포함합니다.

## 🗂️ 레포지토리 구성

- 📁 Ubucon2025_Canonical_Workshop  
  - 📄 README.md / README.ko.md: 워크숍 개요, 진행 방법, 지원 프레임워크 안내 (Django, FastAPI, Go, Flask, ExpressJS, Spring Boot)
  - 📁 docs/  
    - 🖼 juju_status.png: Juju 상태 예시 스크린샷
- 📁 Ubucon_Record_Note  
  - 📝 세션별 필기 Markdown + 📑 발표 자료 PDF 모음  
    - 예: 01) Opening remarks.md, 02) 기조연설(김세영, Canonical).md, 06) Deploy a 12-factor application.md 등

## 🌟 주요 콘텐츠 하이라이트

- 🧑🏫 Canonical Workshop: “Deploy a 12‑factor application of your choice end‑to‑end!”  
  - 🎯 목표: 선택 프레임워크로 12‑factor 앱을 OCI 이미지로 빌드/푸시하고, Juju + MicroK8s 환경에 배포
  - 🧩 요구 도구: Rockcraft, Charmcraft, Juju, LXD
  - 🔀 브랜치 기반 워크플로우: 프레임워크 선택 → 해당 브랜치 전환 → README 지침에 따라 실습 진행
- 🧷 세션 기록 모음
  - 🔓 Opening remarks(오픈소스 철학)
  - 🌱 기조연설: 오픈소스 열정을 틔우는 씨앗(김세영, Canonical) — 토이 프로젝트, MS의 OSS 수용, Canonical Sustaining Engineering 등
  - 🛠 Workshop 필기: Juju/Charmcraft/Rockcraft, COS, 12‑factor 원칙, Django Hands‑on, PostgreSQL 연동
  - 🧠 그 외: Azure/AI/AIoT/WSL GPU/오픈소스 컨트리뷰션/문서 표준 등 다양한 발표 PDF

## 🚀 시작하기

### 1) 워크숍 실습(요약)

- 이 저장소는 Canonical PaaS charm workshop 템플릿 흐름(브랜치 기반)을 따릅니다.
- 🧭 절차 개요  
  1) 레포지토리 클론  
  2) 원하는 프레임워크 선택 후 해당 브랜치로 전환  
  3) README 지침에 따라 Rockcraft/Charmcraft/Juju로 OCI 빌드·배포·관계 설정  
- ⚙️ 의존 도구: Rockcraft, Charmcraft, Juju, LXD 설치
- 📐 주제: 12‑factor 원칙(환경변수 구성, 빌드/릴리즈/실행 분리, 무상태 프로세스, 포트 바인딩, 로그 스트리밍 등)을 Ubuntu/Juju 환경에서 실천

### 2) 세션 기록 탐색

- 📚 Ubucon_Record_Note 디렉토리에서 세션별 Markdown과 PDF를 확인하세요.
  - 예: “06) Deploy a 12‑factor application.md”에는 실습 흐름, Multipass 사용, PostgreSQL 연동, Ingress/라우팅 설정 메모 등이 정리되어 있습니다.

## 🧩 12‑factor 앱 한눈에 보기

- 핵심 원칙(요약):  
  1) 코드베이스 단일화  2) 명시적 종속성  3) 환경변수 구성  4) 백엔드 서비스 외부화  
  5) 빌드/릴리즈/실행 분리  6) 무상태 프로세스  7) 포트 바인딩  8) 수평 확장  
  9) 신속 종료  10) Dev/Prod 동등성  11) 로그 스트림  12) 일회성 관리 작업
- 🧰 Juju/Charmcraft/Rockcraft로 Ubuntu 환경에서 위 원칙을 체계적으로 적용할 수 있습니다.

## 🔎 디렉토리 상세

- 📁 Ubucon2025_Canonical_Workshop  
  - 📄 README.md / README.ko.md: 실습 개요, 프레임워크 브랜치 전환 가이드, 요구 도구
  - 🖼 docs/juju_status.png: Juju 상태 예시
- 📁 Ubucon_Record_Note  
  - 🕙 01) Opening remarks.md: 개회 및 오픈소스 철학(10:00~10:30)
  - 🗣 02) 기조연설 … .md: Canonical, OSS, 커뮤니케이션, SRU/Kernel/Charm 등 키워드 정리
  - 🧪 06) Deploy a 12‑factor application.md: 실습 개요, 도구, 개념, Hands‑on 메모
  - 📑 추가 PDF: LibreOffice/문서 표준, WSL GPU 오케스트레이션, 번역과 컨트리뷰션 등 다양한 발표 자료
