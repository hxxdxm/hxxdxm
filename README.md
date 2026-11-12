# 김하민 | Hamin Kim

### AI Vision · Model Serving · Web Frontend

Python · PyTorch · YOLO · OpenCV · FastAPI · Celery · Docker · Next.js

---

## About Me

저는 **실험으로 근거를 찾고, 그 결과를 사람이 쓰는 서비스로 만드는 AI Vision 개발자**입니다.

데이터 검수부터 모델 학습 · 평가, API 서빙, 웹 화면까지 직접 만들며  
하나의 AI 기능이 **실제 서비스로 동작하기까지의 전 과정**을 끝까지 완성하는 경험을 쌓고 있습니다.

점수가 올랐다는 사실보다 **왜 올랐는지 설명할 수 있는 것**을 더 중요하게 생각합니다.

---

## How I Work

```text
데이터 점검
→ 기준선(Baseline) 학습
→ 실패 사례 분석
→ 변수 하나씩 바꾸는 개선 실험
→ Validation으로 모델 선택 · Test는 단 1회 평가
→ API · 화면으로 서비스화
→ README · 트러블슈팅으로 기록
```

---

## Projects

### 🌱 [Plant Disease Vision API](https://github.com/hxxdxm/plant-disease-vision-api)

#### 📈 콩잎 질병 분류 정확도 `71.9%` → `98.4%` · 학습한 모델을 Docker 서비스로 배포

- 콩잎 사진을 **각진잎반점병 · 녹병 · 정상** 3클래스로 분류하도록 `ResNet-18` Fine-tuning
- 제공 코드의 약점 4가지를 실험으로 하나씩 개선 · 병든 잎을 정상으로 놓친 사례 13장 → 0장
- FastAPI · Redis 캐시 · Celery 비동기 작업 · PostgreSQL 기록을 Docker Compose 4개 서비스로 구성

`PyTorch` `Transformers` `FastAPI` `Celery` `Redis` `PostgreSQL` `Docker`

<br>

### 🥬 [조각김치 이물 검출](https://github.com/hxxdxm/kimchi-foreign-object-detection) · 5인 팀

#### 🔍 공장 이물 사진 `900장` 전수 교차검수 · 검출 성능(mAP50) `0.62` → `0.76`

- LLM을 활용해 **라벨링 프로그램 1.0 초안** 작성 → 팀과 함께 v4.1까지 발전, 수정한 라벨이 교차검수 없이 최종 데이터로 넘어가지 않도록 하는 규칙 추가
- **Class · BBox 라벨 기준서** 작성, 900장 중 250장 1차 검수 (판단이 애매하면 REVIEW로 보내 교차검수)
- 같은 촬영 세션이 학습 · 검증에 섞이는 문제를 분석해 **데이터 재분할**
- '나뭇가지' 오검출 분석: 예측 38건 중 20건을 직접 확인 → 16건이 김치 줄기 · 배추 그림자 착각임을 오류 분석표로 정리
- 팀 산출물 11개 최종 점검

`Python` `tkinter` `YOLO11n` `Ultralytics`

<br>

### 📚 [이음 - 독서 커뮤니티](https://github.com/hxxdxm/Capstone2) · 졸업작품 · 팀장

#### 🖥️ 프론트엔드 `16개 화면` 단독 구현 · 2인 팀 팀장 · 졸업 후 버그 수정과 리팩터링까지

- 독서 MBTI로 취향을 찾고, 같은 책을 읽는 사람과 모임 · 채팅으로 이어지는 서비스
- 기획 · UI/UX 설계와 프론트엔드 전체 개발 담당 (모임방 채팅, DM, 필사 전시, 마이페이지 등)
- 졸업 후 빌드 오류 · 화면 버그를 찾아 고치고, 흩어진 로직을 공통 함수로 정리

`Next.js` `React`

---

## Awards & Activities

| 기간 | 내용 | 결과 |
| --- | --- | --- |
| 2023.06 – 2023.11 | **K-디지털 챌린지 : NET 챌린지 캠프 시즌10** (과학기술정보통신부 주최)<br>`CrossSafe` 교차로 우회전 차량의 일시정지 여부 인식 · 자료조사 · 발표자료 제작 | **본선 진출** |
| 2026.06 | 춘계 졸업작품발표회 · 이음 (팀장 · 프론트엔드) | 발표 |
| 2026.07 – 2027.02 | 현장 데이터 기반 Vision AI & 산업분야 Vertical AI 융합 전문가 양성 과정 | 수강 중 |
| 2026 – | `TrueHue` 색각이상자를 위한 색 탐지 프로그램 (2인 팀) · Figma 화면 설계 | 진행 중 |

---

## Education

- 컴퓨터공학 전공
- <details>
  <summary><b>빅데이터분석 융합전공</b> (부전공 18학점) · 수강 과목 보기</summary>

  - 빅데이터마이닝 `Excel` 신뢰구간 · 표본 크기 · 가설검정
  - 빅데이터프로그래밍 `R`
  - 다변량분석 `SPSS`
  - 빅데이터마케팅 · 빅데이터시각화디자인 · 빅데이터개론

  </details>

---

## Tech Stack

### Language

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)

### AI / Vision

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![YOLO](https://img.shields.io/badge/YOLO11-111F68?style=for-the-badge&logo=yolo&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)

### Backend / Infra

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

### Web / Frontend

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white)

### Data

![SPSS](https://img.shields.io/badge/SPSS-052FAD?style=for-the-badge&logo=ibm&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)

### Collaboration

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)

---

## Contact

- GitHub: [@hxxdxm](https://github.com/hxxdxm)
<!-- 공개해도 괜찮은 연락처가 있으면 아래 줄의 주석을 풀고 채워 주세요 -->
<!-- - Email: -->
