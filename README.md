<div align="center">

# 안녕하세요, 김하민입니다 👋

**모델을 학습하는 데서 끝내지 않고, 사람이 쓰는 서비스까지 연결하는 AI 개발자를 꿈꿉니다.**

컴퓨터 비전 모델 학습 · 평가부터 API 서빙, 웹 프론트엔드까지 직접 만들어 보고 있어요.

</div>

<br>

## 🛠️ Tech Stack

**AI · Vision**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![YOLO](https://img.shields.io/badge/YOLO11-00FFFF?style=flat-square&logo=yolo&logoColor=black)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)

**Backend · Infra**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**Frontend**

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white)

<br>

## 📌 대표 프로젝트

### 🌱 [Plant Disease Vision API](https://github.com/hxxdxm/plant-disease-vision-api)
> 콩잎 사진 한 장으로 잎의 질병을 분류하는 AI 웹 서비스

- `microsoft/resnet-18`을 **각진잎반점병 · 녹병 · 정상** 3클래스로 Fine-tuning
- 제공 코드의 약점 4가지를 실험으로 하나씩 확인해 개선 → **Test 정확도 0.7188 → 0.9844**
- 동기 API · Redis 캐시 · Celery 비동기 작업 · PostgreSQL 기록을 **Docker Compose 4개 서비스**로 구성
- `PyTorch` `Transformers` `FastAPI` `Celery` `Redis` `PostgreSQL` `Docker`

### 🥬 [조각김치 이물 검출](https://github.com/hxxdxm/kimchi-foreign-object-detection) · 5인 팀
> 라벨 검수 도구 제작부터 YOLO 검출 모델 학습 · 검증까지 한 사이클 완성

- 식품 공장 이물 사진 900장을 직접 만든 검수 도구로 **이중 교차검수 (900/900 PASS)**
- YOLO11n 학습 → 실패 분석 → 개선 실험으로 **Val mAP50 0.622 → 0.756**
- 담당: **Docs / Guide** (라벨 검수), **Inference / Document** (검출 모델)
- `Python` `tkinter` `YOLO11n` `Ultralytics`

### 📚 [이음 - 독서 커뮤니티](https://github.com/hxxdxm/Capstone2) · 졸업작품 · 팀장
> 독서 MBTI로 취향을 찾고, 같은 책을 읽는 사람과 실시간으로 이어지는 서비스

- **프론트엔드 전담 + UI/UX**: Next.js App Router 기반 16개 페이지 구현
- Socket.io로 모임방 그룹 채팅 · 1:1 DM 실시간 UI, JWT 인증 흐름 구현
- 졸업 후 버그 수정 · 공통 로직 리팩터링 · 문서화까지 이어서 진행
- `Next.js` `React` `TypeScript` `Socket.io`


<br>

## 📫 Contact

<!-- 공개해도 괜찮은 연락처만 적어 주세요 (예: 이메일, 블로그, LinkedIn) -->
- Email: 1004hamine@naver.com

<br>

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=hxxdxm&show_icons=true&hide_border=true&theme=default)

</div>
