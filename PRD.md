# [PRD] 개인 브랜드 포트폴리오 웹사이트 (Personal Portfolio)

---

## 1. 문서 정보 (Document Control)
- **프로젝트명**: 개인 브랜드 포트폴리오 웹사이트 (Personal Portfolio)
- **작성자**: 태현 (Taehyun)
- **작성일**: 2026년 8월 4일
- **버전**: v1.0.0
- **상태**: Approved / Deployed

---

## 2. 제품 개요 및 목적 (Product Overview & Goals)

### 2.1 제품 개요
본 제품은 인공지능융합학과 재학생인 '태현'의 개인 브랜드 포트폴리오 웹사이트이다. 기존의 과도하고 화려한 마케팅 요소를 배제하고, **개발자 스튜디오 감성의 테크니컬한 미니멀리즘**과 **지적인 에디토리얼 매거진 스타일에 기반한 모노톤 웹사이트**를 제공한다.

### 2.2 핵심 목적 (Goals)
1. **개인 브랜딩 확립**: 인공지능 연구자로서의 전공성과 '혼자 놀기 장인(몰입과 자유)'이라는 개성적 정체성을 명확하게 전달
2. **미니멀 에디토리얼 UX 구현**: 텍스트 가독성 중심의 디자인 시스템 구축으로 조용한 몰입감 제공
3. **무중단 웹 서비스 배포**: GitHub Pages 플랫폼을 이용한 안정적이고 무료 정적 배포 달성

---

## 3. 사용자 페르소나 (User Persona & Identity)

| 항목 | 내용 |
|---|---|
| **이름 / 학과** | 태현 (Taehyun) / 인공지능융합학과 |
| **핵심 페르소나** | • **AI 연구자**: 딥러닝, 머신러닝, 데이터 분석에 집중하는 인공지능 학도<br>• **혼자 놀기 장인**: 집에서의 온전한 몰입, 취향 플레이리스트, 개인 프로젝트 코딩을 즐김<br>• **자유로운 여행가**: 낯선 도시 탐험 및 자유로운 골목 산책 |
| **디자인 선호도** | • 화려한 AI 생성 이미지 배제<br>• 100% 무채색(Warm Cream & Charcoal) 모노톤 선호<br>• 프리텐다드 서체를 통한 단정하고 한글 가독성 높은 인터페이스 |

---

## 4. 디자인 시스템 명세 (Design System Specification)

### 4.1 Design Philosophy
- **Reference**: Cursor Developer Tool 마케팅 디자인 가이드라인 (`DESIGN.md`) 오마주
- **Principle**: Hairline Depth Only (그림자 완전 제거, 1px 보더 라인 중심 구조)

### 4.2 Color Palette (Monochrome Editorial)
- **Canvas Background**: `#f7f7f4` (Warm Cream Floor)
- **Canvas Soft**: `#fafaf7` (IDE Pane & Code Surface)
- **Surface Card**: `#ffffff` (Pure White Card Surface)
- **Ink & Display Text**: `#26251e` (Refined Charcoal Ink)
- **Body & Subtitle**: `#5a5852` (Muted Charcoal)
- **Hairline Divider**: `#e6e5e0` / `#cfcdc4` (1px Divider Line)

### 4.3 Typography System
- **Main Font**: `Pretendard` (v1.3.9) — `word-break: keep-all;` 및 `text-wrap: balance;` 적용으로 한국어 단어 단위 라인 밸런싱
- **Code Font**: `JetBrains Mono` — 에디터, 스니펫, 수치 데이터 표현 전용 Monospace 서체
- **Hero Title**: 72px Display Mega (`Built for solitude, powered by intelligence.`)

---

## 5. 기능 요구사항 (Functional Requirements)

### FR-01: Top Navigation (헤더)
- **내용**: 64px 높이의 고정(Fixed) 상단 네비게이션 바 구현
- **구성 요소**: 텍스트 브랜드 로고 (`Taehyun.dev`), 한글 메뉴 링크 (`소개`, `관심사`, `전공 탐구`), 우측 CTA 버튼 (`연락하기`)

### FR-02: Hero Band (메인 영역)
- **내용**: 중앙 정렬 구조(Centered Layout)의 거대 타이틀 및 수평 밸런스 배치
- **구성 요소**:
  - 서브 라벨: `인공지능융합학과 · 혼자 놀기 장인 · 여행가` (한글)
  - 메인 헤드라인: `Built for solitude, powered by intelligence.` (영문)
  - 서브 설명문: 프로필 및 가치관 소개 한글 문구

### FR-03: Multi-Pane IDE Mockup Card
- **내용**: 개발자 정체성을 직관적으로 보여주는 3-Pane 모의 에디터 인터페이스
- **구성 요소**:
  - `Left Pane`: 프로젝트 파일 트리를 나타내는 Explorer (Python, JSON, Model 파일)
  - `Center Pane`: Python 프로필 클래스 정의 스니펫
  - `Right Pane`: Cursor AI Agent 형태의 대화형 요약창 (`사용자` & `AI 어시스턴트`)

### FR-04: About Section (정체성 및 통계)
- **내용**: 페르소나 속성 카드 및 수치화된 통계 데이터 뷰
- **구성 요소**:
  - 아이덴티티 박스 (`현재 상태`, `관심 몰입`, `탐험 장소`)
  - 카운터 통계 (`탐험한 도시 12+`, `취향의 자유도 100%`, `AI 탐구일수 365d`)

### FR-05: Interests Section (관심사)
- **내용**: 자유 여행 및 혼자 놀기 예술 카테고리 카드 뷰
- **구성 요소**: 한글 태그 배지(`낯선 도시 탐험`, `아늑한 집콕` 등) 및 코드 프리뷰 인라인 블록

### FR-06: Academics Section (전공 스킬)
- **내용**: 인공지능융합학과 주요 역량 시각화
- **구성 요소**: AI/ML, Python, 몰입 스킬 등의 백분율 프로그레스 바 애니메이션

---

## 6. 비기능 요구사항 (Non-Functional Requirements)

- **NFR-01 (성능 & 가볍움)**: 외부 대용량 이미지 파일 제거로 웹 페이지 최초 로딩 속도 1초 미만 달성
- **NFR-02 (반응형 웹)**: Desktop (1200px), Tablet (768px), Mobile (640px 이하) 환경에 맞춘 유연한 1컬럼 디바이스 반응형 스펙 제공
- **NFR-03 (접근성 & 가독성)**: 한국어 가독성에 특화된 Pretendard 폰트 및 모노톤 명암비 확보

---

## 7. 기술 스택 및 배포 아키텍처 (Technical Stack & Deployment)

- **Frontend**: HTML5, CSS3 (Vanilla CSS variables), JavaScript (ES6+)
- **Font Assets**: Pretendard CDN, JetBrains Mono (Google Fonts)
- **VCS & Hosting**: Git, GitHub Repository (`site`), GitHub Pages (`https://chg990.github.io/site/`)

---

## 8. 마일스톤 및 변경 이력 (Milestones & Changelog)

1. **v0.1.0**: 초기 인터랙티브 다크모드 포트폴리오 뼈대 구축
2. **v0.5.0**: `DESIGN.md` (Cursor Spec) 오마주 디자인 가이드라인 도입
3. **v0.8.0**: AI 이미지 전체 삭제, 무채색 모노톤 전환, Pretendard 한글 폰트 튜닝
4. **v1.0.0**: 3-Pane IDE Mockup 카드 통합, 100% 한글 배지 정돈, GitHub Pages 무료 배포 완료
