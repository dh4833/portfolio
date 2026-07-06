# 👋 안녕하세요, 개발자가 되고싶은 김도현이라고 합니다.

> **"기술적 완성도를 넘어 비즈니스 가치를 증명하는 개발자"**

e비즈니스학과 출신으로, 경영과 IT를 함께 이해하는 시각으로 개발에 임합니다.  
단순히 기능을 구현하는 것을 넘어, **이 시스템이 실제 비즈니스에 어떤 가치를 줄 수 있는지**를 함께 고민합니다.

대학 재학 시절 고령화 사회를 대비한 메디컬 보조 서비스 플랫폼 **OnCare**를 구상하여  
대학생 논문 경진대회에서 **장려상**을 수상하였습니다.

이후 e비즈니스 전공 강점을 살려 블록체인 기반 특허를 출원하였으며,  
현재 **"다중 서명 기반 공급망 추적 및 정품 인증을 위한 사용자 보상 연동 블록체인 플랫폼 및 그 방법"**  
(출원번호: 10-2025-0187770) 심사가 진행 중입니다.

---

## 🛠 기술 스택

### Backend
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/SpringBoot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=flat-square)
![JPA](https://img.shields.io/badge/JPA-59666C?style=flat-square)

### Frontend
![JSP](https://img.shields.io/badge/JSP-007396?style=flat-square)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=flat-square&logo=jquery&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

### Database
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

### Infra / Tools
![AWS](https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![Eclipse](https://img.shields.io/badge/Eclipse-2C2255?style=flat-square&logo=eclipseide&logoColor=white)

### AI / API
![Gemini](https://img.shields.io/badge/Gemini_API-4285F4?style=flat-square&logo=google&logoColor=white)
![Python](https://img.shields.io/badge/Python_Crawling-3776AB?style=flat-square&logo=python&logoColor=white)

---

## 📂 Projects

---

## 1. VERNALIS ATS
> **채용 지원자 관리 시스템 (Applicant Tracking System)**  
> 팀 프로젝트 (3인) · 팀장 · 2025.05 ~ 2025.06

### 개발 목표
채용 담당자가 지원자를 효율적으로 관리할 수 있는 채용 파이프라인 기반의 웹 시스템 구현.  
서류 접수부터 최종 합격/불합격까지 단계별 상태 전이를 칸반 보드 방식으로 시각화하고,  
Google Gemini AI를 연동한 이력서 자동 분석 기능 및 채용 통계 대시보드를 제공함으로써  
**채용 담당자의 업무 시간을 전략 수립 시간으로 전환**하는 것을 목표로 하였습니다.

### 기술 스택
| 구분 | 내용 |
|---|---|
| Backend | Spring Boot 3.2.5, MyBatis, Java 17 |
| Frontend | JSP, JavaScript, jQuery, Ajax, Chart.js, FullCalendar.js |
| Database | MySQL 8.0 |
| AI / API | Google Gemini API (gemini-2.5-flash-lite), Apache POI |
| 보안 | spring-security-crypto (BCrypt) |
| 배포 | AWS EC2 (Ubuntu, t3.micro), Apache Tomcat |
| 협업 | GitHub (develop 브랜치 기반) |

### 주요 구현 기능
- BCrypt 단방향 암호화 기반 로그인 / 회원가입 / 세션 관리
- Spring Interceptor 기반 RBAC 권한 접근 제어 (ADMIN / INTERVIEWER)
- 채용 공고 CRUD (마감일 경과 시 CLOSED 자동 전환)
- 이력서 파일 업로드 (UUID 보안 저장, Apache POI DOCX 텍스트 추출)
- 칸반 보드 드래그 앤 드롭 파이프라인 상태 전이 + stage_history 이력 영구 보관
- 서버사이드 페이지네이션 전환 (LIMIT / OFFSET — 멘토 피드백 반영)
- Google Gemini API 연동 이력서 자동 분석 및 파이프라인 자동 반영
- 대시보드 KPI 실시간 집계 (Chart.js 시각화)
- 면접 일정 관리 (FullCalendar.js, 동일 면접관 충돌 방지)
- Excel 지원자 목록 다운로드 (Apache POI)
- AWS EC2 배포 (민감 정보 런타임 인자 분리)

### ER 다이어그램
![VERNALIS ER Diagram](/VERNALIS_ER_Diagram.png)

### 핵심 코드
**BCrypt 단방향 암호화**
![BCrypt Core Code](/BCrypt_Code.png)

**서버사이드 페이지네이션**
![Pagination Core Code](/Pagination_Code.png)

**대시보드 KPI + Gemini AI 분석**
![Dashboard AI Core Code](/Dashboard_AI_Code.png)

---

## 2. ERP Bridge
> **중소기업 경량형 통합 ERP 시스템**  
> 개인 프로젝트 · 2025.03 ~ 2025.05

### 개발 목표
중소·중견기업의 인사, 근태, 급여, 연차·휴가 업무를 하나의 웹 플랫폼에서 처리할 수 있는  
경량형 통합 ERP 시스템을 구현하였습니다.  
대기업 중심의 SAP·Oracle ERP와 달리 **중소기업이 쉽게 도입할 수 있는 웹 기반 시스템**을  
직접 설계·구현함으로써 IT 기술과 경영 지식을 융합한 실무 역량을 증명하고자 하였습니다.  
이 프로젝트의 경험이 이후 VERNALIS ATS 기획의 직접적인 영감이 되었습니다.

### 기술 스택
| 구분 | 내용 |
|---|---|
| Backend | Spring Boot 3.4, JPA, Java 17 |
| Frontend | Thymeleaf, JavaScript |
| Database | MySQL 8.0 |
| 보안 | spring-security-crypto (BCrypt) |
| 협업 | GitHub |

### 주요 구현 기능
- BCrypt 암호화 기반 로그인 / 회원가입 / 세션 관리
- 아이디 중복 검사, 마지막 로그인 날짜 자동 갱신
- 직원 등록 / 수정 / 퇴직 처리 (소프트 삭제) / 사번 자동 생성 (중복 방지 do-while)
- 출근 / 퇴근 등록, 중복 방지, 지각 자동 판정 (9시 기준)
- 휴가 신청 / 취소 / 관리자 승인·반려 / 권한별 조회 분리
- 4대보험 자동 계산 (국민연금 4.5% / 건강보험 3.545% / 장기요양 / 고용보험 0.9%)
- 소득세 · 지방소득세 자동 계산, 실수령액 자동 산출, 동일 월 중복 계산 방지
- 대시보드 KPI (재직 직원 수 / 금일 출근 인원 / 대기 휴가 수 / 이번 달 급여 총액)
- MySQL 예약어 year_month 충돌 해결 (백틱 처리)
- Spring Security 의존성 충돌 해결 (spring-security-crypto 단독 적용)

### ER 다이어그램
![ERP Bridge ER Diagram](/ERP_Bridge_ER_Diagram.png)

### 핵심 코드
**4대보험 급여 자동 계산**
![Salary Calculation Core Code](/Salary_Calculation_Code.png)

---

## 📜 기타 활동

| 활동 | 내용 | 시기 |
|---|---|---|
| 논문 경진대회 장려상 | 고령화 사회 대비 메디컬 보조 서비스 플랫폼 OnCare 구상 | 대학 재학 중 |
| 특허 출원 (심사 진행 중) | 다중 서명 기반 공급망 추적 및 정품 인증을 위한 사용자 보상 연동 블록체인 플랫폼 및 그 방법 (출원번호: 10-2025-0187770) | 2025.12 |
| 학생연구원 | Python 크롤링 기반 KCI 학술 논문 및 뉴스 데이터 자동 수집 · 전처리 (수작업 대비 80% 시간 단축) | 대학 재학 중 |

---

<div align="center">

**"지금까지 채용을 기술로, 데이터를 전략으로. 감사합니다."**

</div>
