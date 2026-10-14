# 한정현 (Junghyun Han)

조건이 바뀌는 최적화 문제를 정식화하고, 강화학습 · 수리최적화 · LLM 에이전트로 풀어 검증.
고려대학교 컴퓨터학과 석사 (RAIN Lab). 저궤도 위성망의 경로 · 자원배분 문제를 연구.

## 대표 프로젝트

| 저장소 | 내용 | 핵심 결과 |
|---|---|---|
| [**LEO-Routing-Optimization**](https://github.com/junghyun-han/LEO-Routing-Optimization) | 위성이 움직여도 끊기지 않는 통신 경로 최적화. 그래프 강화학습(PPO-GCN), CP-SAT 정수계획, 운영 조건을 읽고 도구를 골라 쓰는 LLM 에이전트 | 통신 완주율 **92.56%** (기존 최고 83.53%), 여러 운영 조건 동시 준수 **20/20** (LLM + CP-SAT) |
| [**AI-Network-Routing**](https://github.com/junghyun-han/AI-Network-Routing) | 강화학습 라우팅을 운용 가능한 시스템으로 구현. 장애 선제 탐지, 최적해 대비 검증, Kubernetes 배포, 관측, 탐지 → 우회 폐루프 | 최적해 대비 gap **1.83%**, 단절 탐지 ROC-AUC **0.840**, 단절 시간 34.2 s → **0 s** |
| [**MolChat**](https://github.com/junghyun-han/MolChat) | 분자 질문에 답하는 LLM 에이전트. RAG, function calling, LoRA 미세조정, 양자화, FastAPI · ONNX 서빙 | LoRA 학습 파라미터 **0.44%**, 양자화로 모델 **2.5배** 축소 |

## 연구

- IEEE WCNC 2027 (공동 제1저자, 심사 중): 그래프 강화학습 기반 세션 경로 설정
- ICT Express 2026 (SCIE, 공저): 저궤도 위성망의 위성 간 링크 기술과 응용
- 한국항공우주학회 2026 (제1저자, 구두발표): GCN-PPO 기반 선제적 라우팅
- 특허 출원 (발명자 1번): 잔여 접촉시간 기반 선제적 라우팅 장치

## 기술

- **최적화**: OR-Tools (CP-SAT), 정수계획(MILP), 조합최적화, 밴딧(UCB, EXP3)
- **강화학습 · AI**: PyTorch, PyTorch Geometric, GCN, PPO, 다중 에이전트 강화학습
- **LLM**: OpenAI API (function calling, tool use), RAG, LoRA, 4비트 양자화, ONNX
- **Infra**: Docker, Kubernetes, FastAPI, Prometheus, Grafana, GitHub Actions
