# 김하민 | Hamin Kim

### AI Vision · Model Serving · Web Frontend

Python · PyTorch · YOLO · OpenCV · FastAPI · Celery · Docker · Next.js

---

## About

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

## Highlights

| Project | Result |
| --- | --- |
| 🌱 콩잎 질병 분류 AI 서비스 | Test 정확도 **0.7188 → 0.9844** · 병든 잎을 정상으로 놓친 사례 **13 → 0장** |
| 🥬 조각김치 이물 검출 (5인 팀) | 이물 사진 900장 이중 교차검수 **900 / 900 PASS** · Val mAP50 **0.622 → 0.756** |
| 📚 이음 독서 커뮤니티 (졸업작품 · 팀장) | 프론트엔드 **16개 페이지** · 실시간 채팅/DM · 졸업 후 버그 수정과 리팩터링까지 |

---

## Tech Stack

### AI / Vision

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
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
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

### Frontend

![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white)

### Collaboration

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

---

## Projects

### 🌱 [Plant Disease Vision API](https://github.com/hxxdxm/plant-disease-vision-api)

> 콩잎 사진 한 장으로 잎의 질병을 분류하는 AI 웹 서비스

- `microsoft/resnet-18`을 **각진잎반점병 · 녹병 · 정상** 3클래스로 Fine-tuning
- 제공 코드의 약점 4가지를 실험으로 하나씩 확인해 개선 → **Test 정확도 0.7188 → 0.9844**
- 동기 API · Redis 캐시 · Celery 비동기 작업 · PostgreSQL 기록을 **Docker Compose 4개 서비스**로 구성

`PyTorch` `Transformers` `FastAPI` `Celery` `Redis` `PostgreSQL` `Docker`

### 🥬 [조각김치 이물 검출](https://github.com/hxxdxm/kimchi-foreign-object-detection) · 5인 팀

> 라벨 검수 도구 제작부터 YOLO 검출 모델 학습 · 검증까지 한 사이클 완성

- 식품 공장 이물 사진 900장을 직접 만든 검수 도구로 **이중 교차검수 (900 / 900 PASS)**
- YOLO11n 학습 → 실패 분석 → 개선 실험으로 **Val mAP50 0.622 → 0.756**
- 담당: **Docs / Guide** (라벨 검수), **Inference / Document** (검출 모델)

`Python` `tkinter` `YOLO11n` `Ultralytics`

### 📚 [이음 - 독서 커뮤니티](https://github.com/hxxdxm/Capstone2) · 졸업작품 · 팀장

> 독서 MBTI로 취향을 찾고, 같은 책을 읽는 사람과 실시간으로 이어지는 서비스

- **프론트엔드 전담 + UI/UX**: Next.js App Router 기반 16개 페이지 구현
- Socket.io로 모임방 그룹 채팅 · 1:1 DM 실시간 UI, JWT 인증 흐름 구현
- 졸업 후 버그 수정 · 공통 로직 리팩터링 · 문서화까지 이어서 진행

`Next.js` `React` `TypeScript` `Socket.io`

---

## Contact

- GitHub: [@hxxdxm](https://github.com/hxxdxm)
- Email: 1004hamine@naver.com
