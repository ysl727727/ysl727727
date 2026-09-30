<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,50:161B22,100:1F2A44&height=150&text=%EC%9D%B4%EC%9A%A9%EC%84%9D&fontSize=46&fontColor=E6EDF3&fontAlignY=42&desc=LLM%20Engineer%20in%20Progress&descSize=16&descAlignY=68" alt="이용석 · LLM Engineer in Progress" width="100%" />

실제로 쓰이는 LLM 서비스를 만들고, 오래 안정적으로 운영하는 엔지니어를 목표로 공부하고 있습니다.

[![TIL](https://img.shields.io/badge/TIL-%ED%95%99%EC%8A%B5%20%EA%B8%B0%EB%A1%9D-4B32C3?style=flat-square&logo=github&logoColor=white)](https://github.com/ysl727727/TIL)
[![Document Search](https://img.shields.io/badge/Project-Document%20Search-0EA5E9?style=flat-square&logo=github&logoColor=white)](https://github.com/ysl727727/doc-search-project)

</div>

## 👋 About

KANT Private LLM 엔지니어 교육과정에서 머신러닝 기초부터 RAG, AI Agent, LLMOps, 모델 서빙까지 차근차근 배우고 있습니다.
부동산학을 전공했고, 그 경험을 살려 부동산 실무에 실제로 도움이 되는 LLM 서비스를 만드는 것이 목표입니다.

## 🔭 Current Focus

- **LLM 애플리케이션 구조** — LangChain의 Prompt → Model → Parser, 구조화된 출력과 결과 검증
- **LLM을 붙이는 백엔드** — FastAPI + Pydantic으로 문서 등록·조회·질문 API 설계
- **안정적인 외부 호출** — timeout, 제한된 재시도, Backoff + Jitter, fallback 설계
- **재현 가능한 실험** — baseline 비교, train / validation / test 분리, 누수 방지, 실험 기록
- **배포** — AWS DevOps 특강(배포까지 해내는 개발자) 병행

## 🛠️ Tech Stack

| 분야 | 기술 |
| --- | --- |
| Language | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| Data · ML | ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white) ![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white) |
| Deep Learning | ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black) |
| LLM · Backend | ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white) ![OpenAI API](https://img.shields.io/badge/OpenAI%20API-412991?style=flat-square) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white) |
| Tools | ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white) ![Colab](https://img.shields.io/badge/Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white) ![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat-square&logo=uv&logoColor=white) |

## 📌 Featured Work

### [🔍 Document Search Project](https://github.com/ysl727727/doc-search-project)

Keyword baseline과 TF-IDF 검색을 구현하고 Precision@3, MRR로 성능을 비교한 문서 검색 프로젝트입니다.

- 텍스트 전처리 및 TF-IDF 벡터화
- NumPy 기반 cosine similarity 구현
- 검색 평가 세트와 Precision@3, MRR 적용
- 실패 사례 분석 및 title weighting 실험

### [🏠 부동산 허위매물 탐지 어시스턴트 — 로컬 LLM 선정](https://github.com/ysl727727/real-estate-fake-listing-detector)

매물 광고가 국토교통부 표시·광고 기준에 어긋나는지 판정하는 어시스턴트를 가정하고, 이 업무에 맞는 로컬 모델을 직접 실험해 골랐습니다.

- `gemma3:4b`와 `qwen3:4b-instruct` 비교 — 파라미터 규모(4B)와 양자화(Q4_K_M)를 맞춰 공정하게 비교
- 정상·경계·범위밖 10문항, 총 40회 실행으로 품질과 속도 측정 (RTX 5060 Laptop, VRAM 8GB)
- 답변 정확성 gemma3 57.0% vs **qwen3 80.8%** — `qwen3:4b-instruct` 최종 선정
- 같은 문항을 Cloud API와도 비교해 로컬 운영이 가능한지 확인

### [📚 Today I Learned](https://github.com/ysl727727/TIL)

Private LLM 엔지니어 교육과정에서 배우고 직접 검증한 내용을 기록합니다. 실습은 직접 실행하고 설명할 수 있을 때만 완료로 표시합니다.

| 트랙 | 기록 범위 |
| --- | --- |
| 머신러닝 | 모델 평가, 앙상블, 편향·분산, 불균형·교차검증, CV 튜닝 |
| 딥러닝 기초·심화 | PyTorch, MLP·CNN·RNN, Attention, Tokenization, Fine-tuning, PEFT |
| LLM 실전 | Logit·Loss·Optimizer, 안정적인 LLM API 호출 |
| 데이터 엔지니어링 | API 수집, 정제와 RAG 문서셋, FastAPI·Pydantic, 비동기 호출 |
| LangChain | 앱 구조, Prompt Template, Output Parser |

## 🗺️ Learning Roadmap

```mermaid
flowchart LR
    A[Machine Learning] --> B[Deep Learning] --> C[Transformer & LLM] --> D[LLM Application]
    D --> E[RAG] --> F[AI Agent] --> G[LLMOps] --> H[Private LLM Serving]

    classDef done fill:#dcfce7,stroke:#16a34a,color:#14532d
    classDef now fill:#fef3c7,stroke:#d97706,color:#78350f
    classDef next fill:#f3f4f6,stroke:#9ca3af,color:#374151
    class A,B,C done
    class D now
    class E,F,G,H next
```

## 🌱 Background

- 건국대학교 부동산학과
- 감정평가 프로젝트에서 3가지 평가방식의 계산·검토 및 DCF 수익방식 발표
- 전문자격시험 준비 경험 이후 AI 엔지니어로 직무 전환
- KANT Private LLM 엔지니어 교육과정 참여

## 💡 What I Value

- 모르는 부분은 추측하지 않고 직접 확인합니다.
- 높은 숫자 하나보다 문제 비용에 맞는 평가 기준을 먼저 정의합니다.
- 결과뿐 아니라 가정, 실험 과정과 실패 사례를 함께 기록합니다.
- 오류를 재현하고 사용자 피드백을 개선으로 연결하는 운영을 지향합니다.

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com?user=ysl727727&theme=dark&hide_border=true&background=0D1117&locale=ko" />
  <img src="https://streak-stats.demolab.com?user=ysl727727&theme=default&hide_border=true&locale=ko" alt="GitHub streak" />
</picture>

</div>
