# kakao_01_advanced_prompt_engineering

**카카오 개발자 대상 고급 프롬프트 엔지니어링 강의 (with LLMOps)**  
: AI Intensive 실무 적용을 위한 프롬프트 엔지니어링 과정

---

## 📁 프로젝트 구조

```

kakao\_01\_advanced\_prompt\_engineering/
├── data/
│   ├── 01\_order\_delivery/
│   │   ├── answer\_results/
│   │   │   ├── **init**.py
│   │   ├── Customer\_Info.csv
│   │   ├── Delivery\_Address.csv
│   │   ├── Order\_Info.csv
│   │   ├── Scenario\_QA.csv
│   │   └── Shipping\_Issue\_Log.csv
│   ├── 02\_refund/
│   │   ├── answer\_results/
│   │   │   ├── **init**.py
│   │   ├── Scenario\_QA.csv
│   │   ├── T\_CUSTOMER.csv
│   │   ├── T\_ORDER.csv
│   │   ├── T\_PAYMENT.csv
│   │   └── T\_REFUND.csv
│   ├── 03\_account\_login/
│   │   ├── answer\_results/
│   │   │   ├── **init**.py
│   │   ├── login\_history.csv
│   │   ├── Scenario\_QA\_Cases\_Cleaned.csv
│   │   ├── security\_info.csv
│   │   ├── support\_tickets.csv
│   │   └── user\_accounts.csv
├── notebooks/
│   ├── session01\_V0.ipynb
│   └── session02\_V1.ipynb
│   └── session03\_V2.ipynb
│   └── session04\_V3.ipynb
│   └── session05\_V4.ipynb
├── prompts/
├── .env              ← 수동 생성 또는 .env.sample 복사하여, 개인별 환경 변수 설정
├── .env.sample       ← 환경 변수 예시 파일
├── .gitignore
├── LICENSE
└── README.md

```

---

## ⚙️ 사용법

1. `.env.sample` 파일을 복사하여 `.env` 파일을 생성합니다.

   ```bash
   cp .env.sample .env
   ```

2. `.env` 파일 내 각 환경 변수 값(OpenAI API Key 등)을 본인의 설정에 맞게 채워 넣습니다.

   예시:

   ```env
   OPENAI_API_KEY=sk-xxxxxxx
   ```

3. Colab에서 `session01_*.ipynb` 노트북을 실행할 때, `파일 업로드` 기능을 활용하여 `.env` 파일을 업로드합니다.

4. 노트북 내에서 다음 코드를 통해 환경 변수를 로드합니다.

   ```python
   from dotenv import load_dotenv
   load_dotenv()  # .env 파일을 현재 환경에 로드
   ```

---

## 📘 노트

* 각 시나리오별 폴더(`01_order_delivery`, `02_refund`, `03_account_login`)에는 실제 QA 시나리오 및 사용자/이슈 데이터가 포함되어 있습니다.
* `answer_results/` 폴더는 모델 응답 결과를 저장하거나 참조할 수 있도록 구성되어 있습니다.
* 실습은 Langfuse, OpenAI API, Prompt Engineering 기반의 LLMOps 프로젝트 구현을 목표로 합니다.
