# 2025 금융 AI 챌린지: AI 금융 자문 챗봇

본 프로젝트는 2025 금융 AI 챌린지를 위해 개발된 AI 금융 자문 챗봇입니다. 사용자의 목표와 성향에 맞춰 개인화된 금융 포트폴리오를 추천하고, 시장 상황에 따라 동적으로 포트폴리오를 관리해주는 지능형 금융 비서입니다.

## 프로젝트 목표

본 프로젝트는 다음 목표를 달성하기 위해 설계되었습니다.

*   **금융 접근성 향상**: 누구나 전문가 수준의 금융 자문 서비스를 쉽고 편리하게 이용할 수 있도록 합니다.
*   **개인화된 금융 솔루션**: 사용자의 투자 성향, 목표, 기간 등을 종합적으로 분석하여 최적의 맞춤형 포트폴리오를 제공합니다.
*   **데이터 기반 의사결정**: 실시간 금융 데이터, 시장 뉴스, 공시 정보 등을 분석하여 객관적이고 합리적인 투자 결정을 지원합니다.
*   **지능형 에이전트 구현**: LangGraph를 활용하여 복잡한 금융 분석 및 추천 과정을 자동화하고, 사용자에게 진행 상황을 투명하게 시각화하여 신뢰를 제공합니다.

## 팀

*   **KFC** (Kookmin Financial seCurity)

## 시스템 아키텍처

이 시스템은 세 개의 주요 구성요소로 이루어져 있습니다.

*   **Frontend**: 사용자가 챗봇과 대화하는 웹 애플리케이션입니다. (React, Vite, Tailwind CSS)
*   **Backend**: FastAPI 기반의 API 서버로, LangGraph를 사용하여 대화 흐름과 비즈니스 로직을 관리하는 지능형 에이전트를 실행합니다.
*   **Agent**: 백엔드 에이전트가 사용하는 데이터 모델과 상태를 정의하는 공유 라이브러리입니다.

각 구성요소는 독립적인 저장소로 관리됩니다.

## 🔗 Link

본 프로젝트의 상세 코드는 아래 링크에서 확인하실 수 있습니다.

*   **Agent**: [https://github.com/FSI-AI-Challenge/agent](https://github.com/FSI-AI-Challenge/agent)
*   **Backend**: [https://github.com/FSI-AI-Challenge/backend](https://github.com/FSI-AI-Challenge/backend)
*   **Frontend**: [https://github.com/FSI-AI-Challenge/frontend](https://github.com/FSI-AI-Challenge/frontend)

## Run

### 1. Backend 서버 실행

백엔드 서버는 포트폴리오 추천, 데이터 분석 등 핵심 로직을 수행합니다.

```bash
# 1. backend 디렉터리로 이동
cd backend

# 2. 필요한 Python 패키지 설치
pip install -r requirements.txt

# 3. FastAPI 서버 실행
uvicorn main:app --reload --host 127.0.0.1 --port 3000
```

서버가 `http://127.0.0.1:3000`에서 실행됩니다.

### 2. Frontend 웹 애플리케이션 실행

프론트엔드는 사용자가 상호작용하는 UI를 제공합니다.

```bash
# 1. frontend 디렉터리로 이동
cd frontend

# 2. 필요한 Node.js 패키지 설치
npm install

# 3. Vite 개발 서버 실행
npm run dev
```

웹 애플리케이션이 `http://localhost:5173`에서 실행됩니다. 브라우저에서 이 주소로 접속하여 챗봇을 사용할 수 있습니다.

## 💡 주요 기능

*   **대화형 인터페이스**: 챗봇과 자연스럽게 대화하며 금융 목표를 설정합니다.
*   **개인화된 목표 설정**: 목표 금액, 투자 기간 등 사용자 맞춤형 목표를 입력받습니다.
*   **동적 포트폴리오 생성**: 사용자의 투자 성향과 목표에 따라 금융 상품과 주식을 조합한 포트폴리오를 추천합니다.
*   **실시간 뉴스 분석**: 최신 뉴스를 수집하고 감성 분석을 통해 포트폴리오 리밸런싱 여부를 판단합니다.
*   **진행 상태 시각화**: 백엔드에서 작업이 처리되는 과정을 프론트엔드에서 실시간으로 확인할 수 있습니다.
