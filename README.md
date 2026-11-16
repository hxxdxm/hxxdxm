<!-- GitHub Profile README | hxxdxm/hxxdxm -->
<a id="top"></a>

<div align="center">

<img src="assets/header-v2.svg" width="100%" alt="김하민 Hamin Kim · Vision AI · Data Quality · Web Service"/>

<br/>

[![About](https://img.shields.io/badge/About_Me-2F6B5E?style=for-the-badge)](#-about-me)
[![Impact](https://img.shields.io/badge/Impact-5B8A72?style=for-the-badge)](#-impact-at-a-glance)
[![Projects](https://img.shields.io/badge/Projects-7FA88F?style=for-the-badge)](#-projects)
[![Stack](https://img.shields.io/badge/Tech_Stack-3D5266?style=for-the-badge)](#-tech-stack)
[![Contact](https://img.shields.io/badge/Contact-C9A86A?style=for-the-badge)](#-contact)

</div>

<br/>

## 🌱 About Me

> **모델의 점수에서 멈추지 않고, 그 점수를 믿을 수 있는 데이터 기준부터 사람이 쓰는 서비스 화면까지 연결합니다.**

<table>
<tr>
<td width="33%" valign="top">

**🔍 Vision AI & Data Quality**

라벨 기준서 작성 → 교차검수 → 데이터 분할 → 모델 학습 · 오류 분석까지, ‘**정답지가 맞는가**’부터 확인합니다.

</td>
<td width="33%" valign="top">

**⚙️ Model to Service**

Fine-tuning한 모델을 **FastAPI · Celery · Docker**로 서비스하고, **Next.js** 웹 화면으로 사용자에게 연결합니다.

</td>
<td width="33%" valign="top">

**📝 Evidence & Sharing**

실험 기록, 오류 분석표, README, 발표자료로 **다른 사람이 이해하고 검증할 수 있는 결과**를 남깁니다.

</td>
</tr>
</table>

<br/>

## 📊 Impact at a Glance

<img src="assets/impact-v2.svg" width="100%" alt="이물 검출 mAP50 0.62 → 0.76 · 이미지 분류 Test 정확도 98.4% · 프론트엔드 16개 화면 · NET 챌린지 본선 진출"/>

<sub>※ 각 수치는 아래 프로젝트 README에 기록된 결과입니다. 조각김치 이물 검출의 수치는 5인 팀 공동 성과입니다.</sub>

<div align="right"><a href="#top"><sub><b>↑ 맨 위로</b></sub></a></div>

<br/>

## 🚀 Projects

<sub>카드를 누르면 저장소로 이동합니다.</sub>

<a href="https://github.com/hxxdxm/kimchi-foreign-object-detection"><img src="assets/project-01-v2.svg" width="100%" alt="01 조각김치 이물 검출: 흔들리던 라벨 기준을 바로잡아야 모델도 믿을 수 있기에, 기준서와 교차검수로 900장 정답지를 다시 세워 검출 성능(mAP50)을 0.62에서 0.76으로 높였습니다."/></a>

<table>
<tr><td width="96" nowrap><b>핵심 성과 (팀)</b></td><td>검출 성능 <b>Val mAP50 0.62 → 0.76</b> · 900 / 900 교차검수 PASS · AI 후보 라벨 72% 그대로 승인</td></tr>
<tr><td width="96" nowrap><b>문제</b></td><td>식품 공장 이물 사진 900장 중 <b>52%의 라벨이 수정이 필요할 만큼 기준이 흔들려</b> 있었고, 같은 촬영 세션의 사진이 학습 · 검증 데이터에 섞여 있었습니다.</td></tr>
<tr><td width="96" nowrap><b>내 역할</b></td><td>LLM을 활용해 <b>라벨링 프로그램 1.0 초안</b> 작성 → 팀과 v4.1까지 발전<br/><b>Class · BBox 라벨 기준서</b> 작성, 250장 1차 검수 (애매한 경우 REVIEW로 보내 교차검수)<br/>세션 단위 <b>데이터 재분할</b> · 산출물 11개 최종 점검</td></tr>
<tr><td width="96" nowrap><b>오류 분석</b></td><td>'나뭇가지' 예측 38건 중 20건을 직접 확인 → <b>16건이 김치 줄기 · 배추 그림자 착각</b>임을 오류 분석표로 정리</td></tr>
<tr><td width="96" nowrap><b>기술</b></td><td><code>Python</code> <code>tkinter</code> <code>YOLO11n</code> <code>Ultralytics</code> <code>Figma</code></td></tr>
</table>

<a href="https://github.com/hxxdxm/kimchi-foreign-object-detection"><img src="https://img.shields.io/badge/Repository-1F2D3A?style=flat-square&logo=github" alt="repository"/></a>


<div align="right"><a href="#top"><sub><b>↑ 맨 위로</b></sub></a></div>

<br/>

<a href="https://github.com/hxxdxm/plant-disease-vision-api"><img src="assets/project-02.svg" width="100%" alt="02 Plant Disease Vision API: 기준 모델이 병든 잎을 정상으로 놓치는 문제를 해결하려고, 약점을 실험으로 하나씩 고쳐 정확도를 높이고 서비스로 배포했습니다. Test 정확도 98.4%"/></a>

<table>
<tr><td width="96" nowrap><b>문제</b></td><td>제공된 기준 코드로 학습하면 Test 정확도가 71.9%에 그치고, <b>병든 잎 13장을 정상으로 놓쳤습니다.</b> 모델을 실제 요청으로 받을 서비스 구조도 필요했습니다.</td></tr>
<tr><td width="96" nowrap><b>수행</b></td><td><code>ResNet-18</code>을 <b>각진잎반점병 · 녹병 · 정상</b> 3클래스로 Fine-tuning · 제공 코드의 약점 4가지를 <b>변수 하나씩 바꾸는 실험</b>으로 확인 · Validation으로 모델을 고른 뒤 Test는 단 1회 평가</td></tr>
<tr><td width="96" nowrap><b>결과</b></td><td>Test 정확도 <b>71.9% → 98.4%</b> · 병든 잎 놓침 <b>13장 → 0장</b> · 이미지 변형 8종 평균 정확도 95.7%</td></tr>
<tr><td width="96" nowrap><b>서비스</b></td><td>FastAPI 동기 API · Redis 캐시 · Celery 비동기 작업 · PostgreSQL 기록을 <b>Docker Compose 4개 서비스</b>로 구성</td></tr>
<tr><td width="96" nowrap><b>기술</b></td><td><code>PyTorch</code> <code>Transformers</code> <code>FastAPI</code> <code>Celery</code> <code>Redis</code> <code>PostgreSQL</code> <code>Docker</code></td></tr>
</table>

<a href="https://github.com/hxxdxm/plant-disease-vision-api"><img src="https://img.shields.io/badge/Repository-1F2D3A?style=flat-square&logo=github" alt="repository"/></a>


<div align="right"><a href="#top"><sub><b>↑ 맨 위로</b></sub></a></div>

<br/>

<a href="https://github.com/hxxdxm/Capstone2"><img src="assets/project-03.svg" width="100%" alt="03 이음 독서 커뮤니티: 혼자 하는 독서를 취향이 맞는 사람과 잇고 싶어 서비스를 기획하고, 프론트엔드 16개 화면을 만들어 졸업작품발표회에서 발표했습니다."/></a>

<table>
<tr><td width="96" nowrap><b>문제</b></td><td>혼자 하는 독서를 <b>취향이 맞는 사람과 연결</b>하고, 감상과 문장을 나눌 공간이 필요했습니다.</td></tr>
<tr><td width="96" nowrap><b>내 역할</b></td><td>2인 팀 <b>팀장</b> · 서비스 기획 · UI/UX 설계 · <b>프론트엔드 16개 화면</b> 구현 (모임방 채팅, DM, 필사 전시회, 마이페이지 등)</td></tr>
<tr><td width="96" nowrap><b>개선</b></td><td>졸업 후 저장소를 다시 실행해 <b>빌드 오류(누락된 의존성)와 화면 버그</b>를 찾아 수정, 4개 화면에 흩어진 로직을 공통 함수로 정리</td></tr>
<tr><td width="96" nowrap><b>기술</b></td><td><code>Next.js</code> <code>React</code> <code>TypeScript</code> <code>Socket.io</code></td></tr>
</table>

<a href="https://github.com/hxxdxm/Capstone2"><img src="https://img.shields.io/badge/Repository-1F2D3A?style=flat-square&logo=github" alt="repository"/></a>


<div align="right"><a href="#top"><sub><b>↑ 맨 위로</b></sub></a></div>

<br/>

<!-- TODO: TrueHue 저장소를 fork하면 아래 img를 <a href="https://github.com/hxxdxm/저장소이름">...</a>로 감싸기 -->
<img src="assets/project-04.svg" width="100%" alt="04 TrueHue: 색 구분이 어려운 사람도 지금 보는 색을 알 수 있도록, 색각이상자를 위한 색 탐지 프로그램을 기획하고 Figma로 화면을 설계하고 있습니다."/>

<table>
<tr><td width="96" nowrap><b>소개</b></td><td>색각이상자를 위한 색 탐지 프로그램</td></tr>
<tr><td width="96" nowrap><b>내 역할</b></td><td>2인 팀 · <b>Figma 화면 설계</b></td></tr>
<tr><td width="96" nowrap><b>상태</b></td><td>진행 중 · 저장소 연결 예정</td></tr>
<tr><td width="96" nowrap><b>기술</b></td><td><code>Figma</code></td></tr>
</table>

<br/>

#### 🗂️ 그 밖의 활동

| 프로젝트 | 내용 | 역할 · 상태 |
| :--- | :--- | :--- |
| **netimize** (넷티마이즈) | **AI 기반 네트워크 최적화 솔루션** — 가상기업(5G 통신장비 회사)의 신규사업 추진계획 · 시장 · 경쟁사 · 재무 분석 → 구독형 수익 모델 · 투자 · 마케팅 계획 · 2024-2학기 취업역량경진대회 | 5인 팀 · 🏆 **대상** · 상금 100만 원 |
| **CrossSafe** | **안전한 횡단보도 통행을 위한 자동차 탐지 시스템** — 교차로에서 우회전 차량의 일시정지 여부를 인식 · K-디지털 챌린지 : NET 챌린지 캠프 시즌10 | 자료조사 · 발표자료 제작 · 🏆 **기획안 심사 통과 (15팀 선정) · 본선 진출** |

<div align="right"><a href="#top"><sub><b>↑ 맨 위로</b></sub></a></div>

<br/>

## 🎯 What I Do

| 영역 | 해 본 것 |
| :--- | :--- |
| **🔍 Vision AI** | 이미지 분류 Fine-tuning (ResNet-18), 객체 검출 (YOLO11n), 실패 사례 · 오검출 원인 분석 |
| **🧹 Data Quality** | Class · BBox 라벨 기준서, 1차 검수 · 교차검수 규칙, 촬영 세션 단위 데이터 분할 |
| **⚙️ Model Serving** | FastAPI · Redis 캐시 · Celery 비동기 작업 · PostgreSQL 기록 · Docker Compose |
| **🖥️ Web Frontend** | Next.js · React 화면 구현, 실시간 채팅 UI, Figma 화면 설계 |
| **📈 Data Analysis** | R · SPSS · Excel 통계 분석 (신뢰구간 · 가설검정 · 다변량분석) |
| **📝 Documentation** | README · 트러블슈팅 · 오류 분석표 · 발표자료 · 팀 산출물 점검 |

<div align="right"><a href="#top"><sub><b>↑ 맨 위로</b></sub></a></div>

<br/>

## 🔄 How I Work

<p align="center"><img src="assets/how-i-work.svg" width="100%" alt="End-to-End Project Flow: Plan → Design → Build → Ship → Review"/></p>

<sub>기획부터 배포까지 <b>한 프로젝트의 전체 흐름</b>을 설계하고, 각 계층이 주고받는 <b>데이터 약속</b>을 먼저 맞춘 뒤 구현합니다.<br/>배포 후에는 <b>리뷰와 회고</b>로 찾은 개선점을 다음 설계에 다시 반영합니다.</sub>

<div align="right"><a href="#top"><sub><b>↑ 맨 위로</b></sub></a></div>

<br/>

## 🛠 Tech Stack

<div align="center">

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![YOLO11](https://img.shields.io/badge/YOLO11-111F68?style=flat-square&logo=yolo&logoColor=white) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
<br/>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white) ![EC2](https://img.shields.io/badge/EC2-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white) ![S3](https://img.shields.io/badge/S3-569A31?style=flat-square&logo=amazonwebservices&logoColor=white) ![G5](https://img.shields.io/badge/G5-76B900?style=flat-square&logo=nvidia&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=white)

<sub>Frontend · Backend · AI &nbsp;&nbsp;|&nbsp;&nbsp; Language · Deploy · Collaboration</sub>

</div>

<br/>

<br/>

| 분야 | 기술 |
| :--- | :--- |
| 🖥️ **Frontend** | `HTML5` `CSS3` `JavaScript` `TypeScript` `React` `Next.js` `Socket.io` |
| ⚙️ **Backend** | `FastAPI` `Celery` `Redis` `PostgreSQL` |
| 🤖 **AI · Vision** | `PyTorch` `Hugging Face Transformers` `YOLO11 (Ultralytics)` `OpenCV` |
| 📈 **Data** | `R` `SPSS` `Excel` |
| 💻 **Language · CS** | `Python` `C` `C++` |
| ☁️ **Deploy · Infra** | `Docker` `Docker Compose` `Kubernetes` `Nginx` `Linux` `AWS EC2` `AWS S3` `AWS EC2 G5` |
| 🤝 **Collaboration** | `Git` `GitHub` `Figma` |


<div align="right"><a href="#top"><sub><b>↑ 맨 위로</b></sub></a></div>

<br/>

## 🎓 Education & Activities

| 기간 | 내용 | |
| :--- | :--- | :---: |
| 2023 – | **컴퓨터공학** 전공 | 🎓 |
| 2023.06 – 2023.11 | **K-디지털 챌린지 : NET 챌린지 캠프 시즌10** (과학기술정보통신부 주최) · CrossSafe | 🏆 본선 진출 |
| 2024 – | **빅데이터분석 융합전공** (부전공 18학점) | 📈 |
| 2024.11 | **2024-2학기 취업역량경진대회** · 팀 netimize · AI 기반 네트워크 최적화 신규사업 기획 | 🏆 대상 |
| 2026.06 | 춘계 졸업작품발표회 · 이음 (팀장 · 프론트엔드) | 🎤 발표 |
| 2026.07 – 2027.02 | 현장 데이터 기반 Vision AI & 산업분야 Vertical AI 융합 전문가 양성 과정 | 🌱 수강 중 |

**📈 빅데이터분석 융합전공 수강 과목**

<br/>

| 과목 | 도구 · 내용 |
| :--- | :--- |
| 빅데이터마이닝 | `Excel` 신뢰구간 · 필요한 표본 크기 · 가설검정 |
| 빅데이터프로그래밍 | `R` |
| 다변량분석 | `SPSS` |
| 빅데이터마케팅 · 빅데이터시각화디자인 · 빅데이터개론 | 데이터 해석 · 시각화 |


<br/>

## 📬 Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-hxxdxm-1F2D3A?style=for-the-badge&logo=github)](https://github.com/hxxdxm)
[![Email](https://img.shields.io/badge/Email-1004hamine@naver.com-2F6B5E?style=for-the-badge&logo=naver&logoColor=white)](mailto:1004hamine@naver.com)

<br/>

<sub>Set the standard · Check the data · Build the model · Serve the result · Share the evidence</sub>

</div>

<div align="right"><a href="#top"><sub><b>↑ 맨 위로</b></sub></a></div>
