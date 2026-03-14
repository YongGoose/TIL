# CHAPTER 02. LLM, 완전히 새로운 시대의 개막

## LLM의 빅뱅

- **LLM (Large Language Model)**: 대규모 텍스트 데이터로 학습된 거대 언어 모델
- GPT, Claude, Gemini 등 다양한 LLM이 등장하며 AI의 새로운 시대를 열었음
- 기존 AI와 달리 범용적인 언어 이해와 생성 능력을 보유
- ChatGPT의 등장이 대중적 관심을 폭발적으로 증가시킨 계기

## LLM의 작동 원리

- 핵심은 **다음 토큰 예측(Next Token Prediction)**
  - 주어진 텍스트 다음에 올 확률이 가장 높은 토큰을 예측
- **토큰화(Tokenization)**: 텍스트를 모델이 처리할 수 있는 단위(토큰)로 분할
- 확률 분포를 기반으로 텍스트를 생성하므로, 같은 입력에도 다른 출력이 나올 수 있음
- Temperature 등의 파라미터로 출력의 창의성/일관성을 조절

## LLM 성능을 향상시킨 주요 기술

- **Transformer 아키텍처**: Self-Attention 메커니즘으로 문맥을 효과적으로 파악
- **스케일링 법칙(Scaling Law)**: 모델 크기, 데이터 양, 컴퓨팅을 늘릴수록 성능 향상
- **RLHF (Reinforcement Learning from Human Feedback)**: 인간 피드백을 통한 강화학습으로 답변 품질 개선
- **In-Context Learning**: 별도 학습 없이 프롬프트 내 예시만으로 새로운 태스크 수행

## LLM 응용 기술

- **RAG (Retrieval-Augmented Generation)**: 외부 지식을 검색하여 답변에 활용, 환각(hallucination) 감소
- **Fine-tuning**: 특정 도메인/태스크에 맞게 모델을 추가 학습
- **Agent**: LLM이 도구를 사용하고 자율적으로 작업을 수행하는 시스템
- **Function Calling**: LLM이 외부 API나 함수를 호출하여 실시간 정보 활용
