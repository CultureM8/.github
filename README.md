# 🎭 Culture-Mate (컬쳐메이트)

> **문화 생활을 함께 즐기는 커뮤니티 플랫폼**
> 문화 이벤트 정보를 공유하고, 함께 갈 동반자를 찾으며, 경험을 나누는 종합 문화 커뮤니티 서비스

[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5.5-6DB33F?style=flat&logo=spring-boot)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-21-007396?style=flat&logo=java)](https://www.oracle.com/java/)
[![Next.js](https://img.shields.io/badge/Next.js-15.4.4-000000?style=flat&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.1.0-61DAFB?style=flat&logo=react)](https://react.dev/)

## 📋 목차

- [프로젝트 소개](#-프로젝트-소개)
- [주요 기능](#-주요-기능)
- [기술 스택](#-기술-스택)
- [시작하기](#-시작하기)
- [프로젝트 구조](#-프로젝트-구조)
- [API 문서](#-api-문서)
- [개발 가이드](#-개발-가이드)
- [팀 정보](#-팀-정보)

## 🎯 프로젝트 소개

**Culture-Mate**는 문화 활동을 혼자가 아닌 함께 즐기고 싶은 사람들을 위한 플랫폼입니다. 공연, 전시, 영화 등 다양한 문화 이벤트 정보를 제공하고, 함께 참여할 동반자를 찾을 수 있으며, 경험을 공유할 수 있는 커뮤니티 공간을 제공합니다.

### 핵심 가치

- 🤝 **연결**: 같은 관심사를 가진 사람들을 연결
- 🎪 **발견**: 새로운 문화 이벤트와 경험 발견
- 💬 **공유**: 문화 경험과 정보를 나누는 커뮤니티
- 🚀 **접근성**: 누구나 쉽게 문화 생활을 즐길 수 있도록

## ✨ 주요 기능

### 1. 🎪 이벤트 관리
- **이벤트 탐색**: 공연, 전시, 영화 등 다양한 문화 이벤트 정보
- **상세 정보**: 일정, 장소, 가격, 출연진 등 상세 정보 제공
- **검색 & 필터링**: 카테고리, 지역, 날짜별 맞춤 검색
- **관심 이벤트**: 좋아하는 이벤트 저장 및 관리

### 2. 👥 Together (동행 모집)
- **모집글 작성**: 함께 갈 문화 이벤트 동반자 모집
- **참여 신청**: 관심 있는 모집글에 참여 신청
- **승인 시스템**: 호스트의 참여자 승인/거절 관리
- **실시간 채팅**: 참여자 간 실시간 소통 (WebSocket)

### 3. 💬 커뮤니티
- **게시판**: 자유, 후기, 질문, 정보 게시판
- **계층형 댓글**: 대댓글을 지원하는 댓글 시스템
- **추천 기능**: 유용한 게시글 추천
- **이미지 첨부**: 게시글에 이미지 첨부 가능

### 4. ⭐ 리뷰 시스템
- **이벤트 리뷰**: 참여한 이벤트에 대한 리뷰 작성
- **평점 시스템**: 5점 만점 별점 평가
- **리뷰 통계**: 평균 평점 및 리뷰 수 표시

### 5. 👤 회원 관리
- **JWT 인증**: 안전한 토큰 기반 인증
- **프로필 관리**: 개인 정보 및 관심 분야 설정
- **활동 내역**: 참여 이벤트, 작성글 관리
- **권한 관리**: 일반 회원, 관리자 권한 구분

### 6. 🖼️ 이미지 관리
- **통합 관리**: 프로필, 이벤트, 게시글 이미지 통합 관리
- **자동 썸네일**: 업로드 이미지 자동 썸네일 생성
- **보안 처리**: 안전한 파일명 생성 및 저장

## 🛠 기술 스택

### Backend
- **Framework**: Spring Boot 3.5.5
- **Language**: Java 21
- **Database**: H2 (개발), Oracle (운영)
- **ORM**: Spring Data JPA / Hibernate
- **Security**: Spring Security + JWT
- **Real-time**: WebSocket + STOMP
- **API Doc**: SpringDoc OpenAPI 3
- **Build**: Gradle

### Frontend
- **Framework**: Next.js 15.4.4 (App Router)
- **Runtime**: React 19.1.0
- **Styling**: Tailwind CSS 4
- **HTTP Client**: Axios
- **Real-time**: STOMP.js + SockJS
- **Build**: Turbopack (개발)
- **State**: Context API + localStorage

### DevOps & Tools
- **VCS**: Git & GitHub
- **IDE**: IntelliJ IDEA, VS Code
- **API Test**: Postman, Swagger UI
- **Database Tool**: H2 Console

## 🚀 시작하기

### 사전 요구사항

- Java 21 이상
- Node.js 18 이상
- Git

### 설치 및 실행

#### 1. 저장소 클론
```bash
git clone https://github.com/your-username/culture-mate.git
cd culture-mate
```

#### 2. Backend 실행
```bash
cd culture-mate-BACK

# 환경 변수 설정 (.env 파일 생성)
cp .env.example .env

# 빌드 및 실행
./gradlew clean build
./gradlew bootRun
```

Backend 서버는 http://localhost:8080 에서 실행됩니다.

#### 3. Frontend 실행
```bash
cd culture-mate-FRONT

# 패키지 설치
npm install

# 개발 서버 실행 (Turbopack)
npm run dev
```

Frontend 애플리케이션은 http://localhost:3000 에서 실행됩니다.

### 개발 도구 접근

- **H2 Console**: http://localhost:8080/h2-console
- **Swagger UI**: http://localhost:8080/swagger-ui.html

## 📁 프로젝트 구조

```
CULTURE-MATE/
├── culture-mate-BACK/              # Spring Boot Backend
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/culturemate/culturemate_api/
│   │   │   │   ├── controller/    # REST API Controllers
│   │   │   │   ├── service/       # Business Logic
│   │   │   │   ├── repository/    # Data Access Layer
│   │   │   │   ├── domain/        # JPA Entities
│   │   │   │   │   ├── member/    # 회원 관련
│   │   │   │   │   ├── event/     # 이벤트 관련
│   │   │   │   │   ├── together/  # 동행 모집
│   │   │   │   │   ├── community/ # 게시판, 댓글
│   │   │   │   │   └── chatting/  # 채팅
│   │   │   │   ├── dto/           # Data Transfer Objects
│   │   │   │   ├── config/        # Configuration
│   │   │   │   └── exceptions/    # Custom Exceptions
│   │   │   └── resources/
│   │   └── test/
│   └── build.gradle
│
├── culture-mate-FRONT/             # Next.js Frontend
│   ├── app/                       # App Router Pages
│   │   ├── events/               # 이벤트 페이지
│   │   ├── together/             # 동행 모집 페이지
│   │   ├── community/            # 커뮤니티 페이지
│   │   ├── mypage/               # 마이페이지
│   │   ├── admin/                # 관리자 페이지
│   │   └── (auth)/               # 인증 페이지
│   ├── components/                # React Components
│   │   ├── global/               # 공통 컴포넌트
│   │   ├── auth/                 # 인증 컴포넌트
│   │   └── [feature]/            # 기능별 컴포넌트
│   ├── lib/                      # Utilities & API
│   │   └── api/                  # API 통신 모듈
│   ├── constants/                # 상수 정의
│   ├── public/                   # Static Assets
│   └── package.json
│
├── docs/                         # 프로젝트 문서
└── README.md
```

## 📡 API 문서

### 주요 API Endpoints

#### 인증 (Authentication)
- `POST /api/v1/auth/register` - 회원가입
- `POST /api/v1/auth/login` - 로그인
- `POST /api/v1/auth/logout` - 로그아웃
- `POST /api/v1/auth/refresh` - 토큰 갱신

#### 회원 (Members)
- `GET /api/v1/members/{id}` - 회원 정보 조회
- `PUT /api/v1/members/{id}` - 회원 정보 수정
- `DELETE /api/v1/members/{id}` - 회원 탈퇴
- `GET /api/v1/members/{id}/profile` - 프로필 조회

#### 이벤트 (Events)
- `GET /api/v1/events` - 이벤트 목록
- `GET /api/v1/events/{id}` - 이벤트 상세
- `POST /api/v1/events` - 이벤트 등록
- `PUT /api/v1/events/{id}` - 이벤트 수정
- `DELETE /api/v1/events/{id}` - 이벤트 삭제

#### 동행 모집 (Together)
- `GET /api/v1/together` - 모집 목록
- `GET /api/v1/together/{id}` - 모집 상세
- `POST /api/v1/together` - 모집글 작성
- `PUT /api/v1/together/{id}` - 모집글 수정
- `POST /api/v1/together/{id}/apply` - 참여 신청
- `POST /api/v1/together/{id}/participants/{participantId}/approve` - 참여 승인

#### 게시판 (Boards)
- `GET /api/v1/boards` - 게시글 목록
- `GET /api/v1/boards/{id}` - 게시글 상세
- `POST /api/v1/boards` - 게시글 작성
- `PUT /api/v1/boards/{id}` - 게시글 수정
- `DELETE /api/v1/boards/{id}` - 게시글 삭제

#### 실시간 채팅 (WebSocket)
- `WS /ws` - WebSocket 연결
- `SUBSCRIBE /topic/chatroom/{id}` - 채팅방 구독
- `SEND /app/chatroom/{id}/send` - 메시지 전송

### API 인증

모든 인증이 필요한 API는 JWT Bearer 토큰을 사용합니다:

```http
Authorization: Bearer <access_token>
```

## 🔧 개발 가이드

### 코드 스타일

#### Java (Backend)
- **들여쓰기**: 2 spaces
- **네이밍**: PascalCase (클래스), camelCase (변수/메서드)
- **어노테이션**: Lombok 적극 활용
- **예외 처리**: 한국어 메시지 사용

#### JavaScript/React (Frontend)
- **들여쓰기**: 2 spaces
- **세미콜론**: 필수
- **네이밍**: PascalCase (컴포넌트), camelCase (변수/함수)
- **컴포넌트**: 함수형 컴포넌트 + Hooks

### 커밋 컨벤션

```
<type>: <subject>

- 주요 변경사항 1
- 주요 변경사항 2
```

**Types:**
- `feat`: 새로운 기능
- `fix`: 버그 수정
- `docs`: 문서 수정
- `style`: 코드 포맷팅
- `refactor`: 코드 리팩토링
- `test`: 테스트 추가/수정
- `chore`: 기타 변경사항

### 브랜치 전략

```
main
├── develop
│   ├── feature/기능명
│   ├── fix/버그명
│   └── refactor/리팩토링명
├── release/v1.0.0
└── hotfix/긴급수정
```

## 📊 프로젝트 현황

### 개발 진행도

- **Backend**: ~95% 완료
  - ✅ 모든 도메인 엔티티 구현
  - ✅ RESTful API 구현
  - ✅ JWT 인증 시스템
  - ✅ WebSocket 실시간 통신
  - ✅ 이미지 관리 시스템

- **Frontend**: ~85% 완료
  - ✅ 주요 페이지 UI 구현
  - ✅ API 연동
  - ✅ 실시간 채팅 UI
  - ✅ 반응형 디자인
  - 🔄 세부 기능 개선 진행 중

### 다음 단계

- [ ] 테스트 코드 작성
- [ ] 성능 최적화
- [ ] 모바일 앱 개발
- [ ] CI/CD 파이프라인 구축
- [ ] 클라우드 배포

## 👥 팀 정보

### 기여자

- **Backend Development**: Spring Boot, JPA, WebSocket 구현
- **Frontend Development**: Next.js, React, UI/UX 디자인
- **Database Design**: ERD 설계, 쿼리 최적화
- **DevOps**: 환경 구성, 배포 자동화

### 연락처

- **Email**: contact@culturemate.com
- **GitHub**: https://github.com/culturemate

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

---

<div align="center">

**Culture-Mate** - 문화를 함께 즐기는 가장 쉬운 방법 🎭

[프로젝트 시작하기](#-시작하기) | [API 문서](#-api-문서) | [기여하기](CONTRIBUTING.md)

</div>
