<div align="center">

# 안녕하세요, 정래원입니다 👋

**AI를 실제 문제에 붙여서 동작하는 서비스로 만드는 것**을 좋아합니다.<br/>
LLM · RAG · 텍스트 모델링으로 데이터를 다루고, 결과를 검증할 수 있는 시스템을 만듭니다.

[![Gmail](https://img.shields.io/badge/Gmail-fodnjs68@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:fodnjs68@gmail.com)

</div>

---

### 🧭 관심 분야

- **LLM 활용**: RAG, 에이전트·도구 연동(MCP), 문서 이해(Vision·OCR)
- **데이터 · 모델링**: 텍스트 분류, 표현 방식 비교 실험, 평가 지표 설계
- **검증 가능한 AI**: 판정마다 근거를 붙이고, 테스트로 동작을 확인하는 시스템

---

### 🛠 Tech Stack

**AI · ML**<br/>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

**LLM · RAG**<br/>
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square&logo=modelcontextprotocol&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6446?style=flat-square)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Serving · Tools**<br/>
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

### 🚀 대표 프로젝트

#### 🏗 [ARAE — 건축 도면 분석 보조 시스템](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN20-FINAL-3TEAM) &nbsp;`SKN 최종 프로젝트`
> 건축 도면을 입력하면 **도면 자산화 · 사내 기준 평가 · 유사 도면 검색 · 필지 기반 법규 조회**를 한 흐름에서 제공

- Vision AI(YOLOv5 객체 검출, YOLOv5 + CRNN OCR)로 도면을 **구조화된 데이터**로 변환
- **Qwen3-8B 파인튜닝 모델 2개**를 vLLM으로 서빙, Qwen3-Embedding + pgvector로 유사 도면 검색
- `YOLOv5` `CRNN` `Qwen3` `vLLM` `pgvector` `FastAPI` `React` `AWS` `RunPod`

#### 🎓 [외국인 입학 1차 서류 자동 검증 시스템](https://github.com/Raewon12/mcp)
> 지원자 서류 PDF를 폴더째 올리면 **AI가 읽고 · 검증하고 · 4개 언어 안내 메일까지** 자동 생성

- Claude Vision으로 지원 서류를 읽고 1차 요건을 자동 검증, 지원자별 안내 메일을 4개 언어로 생성
- **MCP 서버**(FastMCP)와 **Streamlit 데모** 두 가지 방식으로 제공, 테스트 63개
- `FastMCP` `Claude Vision` `Streamlit` `pdfplumber`

#### 🔎 [SpecPilot — 기획서 ↔ 코드 구현 여부 자동 판정](https://github.com/SpecPilot-8/backend)
> 화면 기획서와 소스코드를 대조해 **요구사항이 코드에 구현됐는지 판정**하고, 판정마다 **근거 코드 위치**를 첨부

- 기획서 PDF 파싱(OCR) → 요구사항 조건 분해 / 소스코드 청킹(tree-sitter) → LLM 판정
- `Claude` `tree-sitter` `PyMuPDF` `Tesseract` `PostgreSQL`

#### ⚖️ [판례 텍스트 기반 사건 유형 자동 분류 연구](https://github.com/Raewon12/big_data_programming-LEON)
> 판례 **42,601건**을 10개 사건 유형으로 분류할 때, **텍스트 표현 방식**(희소 빈도 · 학습 임베딩 · 사전학습 문맥)에 따른 성능 비교

- TF-IDF + LR/SVM · TextCNN · KLUE-BERT + MLP · Late Fusion 5개 모델 비교, 클래스 불균형(최대 56배)으로 **Macro F1** 평가
- **Late Fusion이 Macro F1 0.656으로 최고 성능**, frozen BERT는 단독보다 앙상블 보조 신호로 효과적임을 확인
- `PyTorch` `Transformers` `scikit-learn`

---

### 📂 그 외 프로젝트

| 프로젝트 | 설명 | 기술 |
|---|---|---|
| 📰 [RAG 속보기사 생성 보조](https://github.com/00three/capstone-project-bigdata) | 보도자료 → 과거 문서 **Hybrid 검색(벡터 + BM25) + 재정렬** → 배경 설명이 담긴 속보 초안 생성 (빅데이터 캡스톤) | `pgvector` `FastAPI` `Next.js` |
| 🛡️ [중고거래 사기 상담 RAG 챗봇](https://github.com/Raewon12/fraud-consultation-chatbot) | 의도 분류 → 목적별 벡터 검색 → **민사/형사 루트별 멀티턴 상담** | `LangChain` `ChromaDB` `OpenAI` |
| 🚀 [Boss Baby AI](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN20-4th-4TEAM) `팀장` | 창업 문서 15,510개 RAG + 사업계획서 AI 분석, **검색 정확도 92.8%**, Multi-Query로 재현율 30%↑ (SKN 4차) | `RAG` `Django` `FastAPI` `MySQL` |
| 💬 [창업자 AI 정책 안내 챗봇](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN20-3rd-4TEAM) | Query Transformation · Multi-Query, 문서 유형별 청킹으로 **정확도 32%↑** (SKN 3차) | `LangChain` `GPT-4o-mini` `Streamlit` |
| 🏦 [은행 고객 이탈 예측](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN20-2nd-1TEAM) | 고객 특성 기반 이탈 예측 모델 비교, 클래스 불균형 처리 (SKN 2차) | `scikit-learn` `pandas` |
| 🚗 [친환경차 등록 추이 분석](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN20-1ST-5TEAM-) | 10년간 차량 등록 데이터 크롤링 → MySQL 설계 → 대시보드 (SKN 1차) | `MySQL` `Streamlit` |

---

### 🎓 Education

- **SK네트웍스 Family AI 캠프 20기** — 데이터 분석부터 ML · RAG · sLLM 파인튜닝까지 프로젝트 5회 수행
