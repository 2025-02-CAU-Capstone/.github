# 🌐 P2L – Problem to Lecture

## 🎓 2025 Fall Semester Capstone Design (1) – Team 6

## 📘 Automated Mapping System Between Problems, Textbooks, and Lecture Chapters


*Note: Korean Version of this document is available below.*

## 🔖 1. Project Title

**“P2L – Problem to Lecture”**

A learning support system that analyzes concepts embedded in problems and **automatically links them to the exact timestamps of relevant lecture videos**.

---

## 🧠 2. Abstract

When students get stuck while solving problems, they often spend a significant amount of time trying to identify which concept in the textbook the problem corresponds to and at what point in the lecture the concept is explained.

Existing solutions—such as printed solution manuals, manual lecture searches, or generative AI–based Q&A systems—are helpful for delivering answers but fail to precisely connect **problems, concepts, and lecture timestamps**.

**P2L (Problem to Lecture)** is a learning support system that leverages **STT-based lecture text extraction** and **semantic search techniques**. By simply uploading an image of a problem, the system automatically provides the **most relevant lecture video timestamps** along with corresponding **textbook chapter information**.

This allows learners to jump directly to the exact explanation they need without navigating long lecture videos. Furthermore, the system has strong potential as a **B2B AI-powered learning integration solution** for private education providers and online lecture platforms.

---

## ❗ 3. Problem Statement

### 👤 3.1 Who

* **Primary**: High school students preparing for the CSAT (College Scholastic Ability Test) and school exams
* **Secondary**: General examinees and self-directed learners using online lecture platforms

### ❓ 3.2 What

* Difficulty in finding the **exact lecture location (chapter and timestamp)** where a specific concept related to a problem is explained

### 🔍 3.3 Why

1. **Limitations of printed solution manuals**

   * Inconsistent explanation quality and potential misconceptions
   * Mismatch with the student’s preferred lecture style

2. **Inefficiency of lecture video navigation**

   * Requires scanning through long videos, disrupting learning flow

3. **Limitations of generative AI–based Q&A**

   * Risk of hallucination leading to conceptual misunderstandings
   * Answer-centric responses that fail to promote conceptual understanding and review

### 📊 3.4 Evidence

* Students rarely rely on a single textbook or lecture source

  * They commonly use **EBS** alongside multiple third-party problem sets

* However, identifying

  > “**At which minute and second of which lecture this problem is explained**”
  > is extremely difficult

* Currently, **no commercial service** provides automatic mapping from
  **problem text → lecture timestamps**

* As a result:

  * Students waste time on manual searching
  * Educational providers fail to systematically utilize learning data

---

## 🎯 4. Objectives

### 🏆 Main Objective

To implement a web-based learning support service that **automatically recommends relevant textbook chapters and precise lecture video timestamps** based on problem text.

### 📌 Sub Objectives

1. Collect lecture subtitles using STT and build sentence-level timestamps
2. Perform semantic mapping between textbook chapter structures and lecture subtitles
3. Enable problem image upload → text extraction → automatic lecture timestamp recommendation
4. Provide intuitive UI/UX that allows one-click navigation to the relevant lecture segment

---

## 🛠️ 5. Proposed Solution

### 🔄 System Workflow

1. Upload lecture videos → generate STT-based text with timestamps
2. Segment lecture text by chapter and index embeddings
3. Student uploads a problem image
4. Extract problem text via OCR
5. Perform semantic similarity search between problem text and lecture text
6. Return the most relevant lecture segment (chapter + timestamp)

### ⭐ Core Features

* Lecture segment recommendation based on problem text
* Direct timestamp links to lecture videos
* Visualization of the **problem–concept–lecture** learning context

### 💡 Unique Selling Points (USP)

#### ✅ Expected Benefits

* **Maximized learning efficiency**: Students can access only the necessary explanations without watching entire lectures
* **Preserved learning flow**: No need to switch between multiple resources
* **Self-directed learning support**: Encourages conceptual understanding rather than answer memorization
* **Increased lecture content utilization**: Educational providers can extract greater value from existing content
* **Data-driven service enhancement**: Enables concept-level difficulty analysis, curriculum optimization, and advanced learning recommendations

#### 🚀 Scalability

* Applicable across various subjects: social studies, mathematics, science, language arts, and more
* Evolves into a personalized learning recommendation system by analyzing individual weak concepts
* Enhanced B2B value through large-scale problem–concept–lecture databases
* Easily integrable with existing LMS, question banks, and educational applications

---

## 👥 6. Team Members & Roles

| Name        | Student ID | Role          | Responsibilities                                                                                      |
| ----------- | ---------- | ------------- | ----------------------------------------------------------------------------------------------------- |
| Guebeen Lee | 20235908   | AI / FE       | - AI model implementation for text extraction<br>- Frontend UI/UX development                         |
| Mingyu Lee  | 20215143   | BE / FE / PM  | - Frontend, backend, and AI server development & deployment<br>- Project management and documentation |
| Dongyun Ha  | 20212007   | AI / Planning | - Text similarity matching and STT AI model implementation<br>- Project planning and QA               |

---

## ⚙️ 7. Technology Stack

| Domain    | Technology                                                                   |
| --------- | ---------------------------------------------------------------------------- |
| Frontend  | React                                                                        |
| Backend   | Spring Boot                                                                  |
| Database  | PostgreSQL                                                                   |
| AI Models | - Mapping: SBERT (Sentence Transformers)<br>- OCR: EasyOCR<br>- STT: Whisper |
| Hosting   | AWS (EC2, RDS)                                                               |

---

---

# P2L – Problem to Lecture (KR Ver.)

## 🎓 2025 Fall Semester Capstone Design (1) – Team 6

## 📘 교재·문제 기반 인강 챕터 자동 매핑 시스템

---

## 🔖 1. Project Title (프로젝트 제목)

**“P2L - Problem to Lecture”**

문제 속 개념을 분석해 **관련 강의의 정확한 시점을 자동으로 연결하는 학습 지원 시스템**

---

## 🧠 2. Abstract (요약)

학생들은 문제를 풀다가 막히는 순간, 해당 문제가 교재의 어느 개념이며 강의의 어느 시점에서 설명되는지를 찾기 위해 많은 시간을 소모한다.

기존의 해설집, 강의 검색, 생성형 AI 기반 질문 방식은 정답 전달에는 유용하지만, 문제–개념–강의 시점을 정확히 연결해 주지는 못한다.

본 프로젝트 “P2L(Problem to Lecture)”은 STT 기반 강의 텍스트 추출과 의미 기반 검색(Semantic Search) 기술을 활용하여, 문제 이미지를 촬영해 업로드하면 해당 문제와 가장 관련성이 높은 강의 영상의 정확한 타임스탬프와 교재 챕터 정보를 자동으로 제공하는 학습 지원 시스템이다.

이를 통해 학습자는 긴 강의를 탐색하지 않고도 즉시 필요한 설명으로 이동할 수 있으며, 사교육 업체 및 온라인 강의 플랫폼을 위한 B2B AI 학습 연동 솔루션으로 확장 가능성을 갖는다.

---

## ❗ 3. Problem Statement (문제 정의)

### 👤 3.1 Who (대상)

* **Primary**: 수능 및 내신을 대비하는 고등학생
* **Secondary**: 수험생, 온라인 강의 기반 자기주도 학습자

### ❓ 3.2 What (문제)

* 문제를 풀 때, 해당 개념을 설명하는 강의의 정확한 위치(챕터·시간대)를 찾기 어려움

### 🔍 3.3 Why (원인)

1. **시판 문제집 해설의 신뢰도 한계**

   * 해설의 질 편차 및 오개념 포함 가능성
   * 학생이 선호하는 강의 스타일과 불일치

2. **강의 영상 탐색의 비효율**

   * 긴 영상 전체를 탐색해야 하며 학습 흐름이 끊김

3. **생성형 AI 기반 질문의 한계**

   * Hallucination으로 인한 오개념 학습 위험
   * 정답 중심 응답으로 개념 이해 및 복습 유도에 한계=

### 📊 3.4 Evidence (근거)

* 학생들은 하나의 강의 교재만으로 학습하지 않고,
  EBS 및 다양한 서드파티 문제집을 병행 사용

* 그러나 특정 문제를 보고
  **“이 문제가 어느 강의의 몇 분 몇 초에서 설명되는가”**를 찾는 것은 매우 어려움

* 현재 시중 서비스 중,
  **문제 텍스트 → 강의 시간대 자동 연결**을 제공하는 사례는 없음

* 결과적으로 학생은 탐색에 시간을 소모하고,
  교육 업체는 학습 데이터를 체계적으로 활용하지 못함

---

## 🎯 4. Objectives (목표)

### 🏆 Main Objective

* 문제 텍스트를 기반으로 관련 교재 챕터 및 인강 영상의 정확한 시점을 자동 추천하는 학습 지원 웹 서비스 구현

### 📌 Sub Objectives

1. STT 기반 인강 자막 수집 및 문장 단위 타임스탬프 구축
2. 교재 챕터 구조와 강의 자막 간 의미 기반 매핑
3. 문제 이미지 업로드 → 텍스트 추출 → 강의 시점 자동 추천
4. 클릭 한 번으로 해당 강의 구간으로 이동 가능한 UI/UX 제공

---

## 🛠️ 5. Proposed Solution (제안하는 해결책)

### 🔄 시스템 흐름

1. 강의 영상 업로드 → STT 기반 텍스트 및 타임스탬프 생성
2. 강의 텍스트를 챕터 단위로 분할 및 임베딩 인덱싱
3. 학생이 문제 이미지를 업로드
4. OCR로 문제 텍스트 추출
5. 문제 텍스트와 강의 텍스트 간 의미 기반 유사도 검색
6. 가장 적합한 강의 구간(챕터 + 시간대) 반환

### ⭐ Core Features

* 문제 텍스트 기반 강의 내 구간 추천
* 강의 영상 타임스탬프 링크 제공
* 문제–개념–강의 흐름을 한 눈에 보여주는 학습 맥락 제시

### 💡 Unique Selling Point (USP)

#### ✅ 기대효과

* **학습 효율 극대화**: 학생은 긴 강의 전체를 탐색할 필요 없이 필요한 개념만 바로 확인하여 학습 시간과 피로도를 크게 줄일 수 있음.
* **학습 흐름 유지**: 문제를 이해하려고 학습 동선을 복잡하게 바꾸지 않아도 되어, 집중도 유지
* **자기 주도 학습**: 단순히 정답을 알려주는 것이 아닌 학생이 직접 찾아보고 응용을 하여 문제를 풀게 하므로 학생 역량 증진에 긍정적인 효과 제공
* **강의 콘텐츠 활용도 증가**: 사교육 업체는 기존 강의 자료를 정교하게 활용할 수 있어, 콘텐츠 가치 상승 및 재활용성이 높아짐.
* **데이터 기반 서비스 고도화**: 어떤 문제, 개념에서 학생들이 어려움을 겪는지 파악할 수 있어, 강의 구성 개선, 개념별 난이도 조정, 학습 추천 등 고도화된 서비스 개발 가능.

#### 🚀 확장성

* 다양한 과목 확대 가능: 사회탐구뿐 아니라 수학, 과학, 언어 등 텍스트 기반 과목 전반에 적용 가능
* 개인화 학습 추천 시스템으로 발전: 매칭 로드를 기반으로 학생의 약점 개념을 자동 분석하여 개인 맞춤형 강의 추천이 가능한 구조로 확장 가능
* 문항 데이터베이스 구축으로 B2B 사업성 증가: 문제-개념-강의가 연결된 대규모 데이터베이스를 통해 사교육 업체에 새로운 가치 제공(커리큘럼 분석, 문제 제작 자동화 등)
* AI 학습 도구와의 연동 용이: 기존 LMS, 문제은행, 학습앱과 쉽게 연결될 수 있어 서비스 확장성 높음

---

## 👥 6. 팀원 목록 및 역할 분담

| 이름                | 학번       | 역할           | 상세 내용                                                                 |
| ----------------- | -------- | ------------ | --------------------------------------------------------------------- |
| 이규빈 (Guebeen Lee) | 20235908 | AI / FE      | - 텍스트 추출 AI 모델 implementation<br>- 프런트엔드측 UI/UX 구축                    |
| 이민규 (Mingyu Lee)  | 20215143 | BE / FE / PM | - 프런트엔드, 백엔드 및 AI 서버 구축 및 배포<br>- Project Management 및 Documentations |
| 하동윤 (Dongyun Ha)  | 20212007 | AI / 기획      | - 텍스트 유사도 매칭 및 STT AI 모델 implementation<br>- 프로젝트 기획 및 QA             |

---

## ⚙️ 7. Technology Stack (기술 스택)

| 영역       | 기술                                                                                       |
| -------- | ---------------------------------------------------------------------------------------- |
| Frontend | React                                                                                    |
| Backend  | Spring Boot                                                                              |
| Database | PostgreSQL                                                                               |
| AI Model | - 매핑: SBERT (Sentence Transformers)<br>- 카메라 인식: EasyOCR<br>- STT 기반 강의 text 추출: Whisper |
| Hosting  | AWS (EC2, RDS)                                                                           |



