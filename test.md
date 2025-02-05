# 🤖🧠 플랫폼 DeiNoN 프로젝트 🧬⚕️
<br>

### 📋 항목 바로가기
1. [🗂 레파지토리 구성](#-레파지토리-구성)
2. [📟 개발 컨밴션](#-개발-컨밴션)
<br><br><br>



## 🗂 레파지토리 구성
### 🔸 infra
- 인프라 구성 및 운영과 관련된 소스코드를 담고있다
- 기술스택
    - CI/CD : Github Action 
    - 컨테이너 : Docker
    - 오케스트레이션 : Docker Compose
    - IaC : Terraform

### 🔸 front
- 화면단 서비스의 소스코드를 담고있다
- 기술스택
    - 언어 : JavaScript
    - UI 라이브러리 : React

### 🔸 back 
- 서버단 서비스의 소스코드를 담고있다
- 기술스택
    - 언어 : Python
    - 프레임워크 : FastAPI

### 🔸 db
- 데이터베이스 구성과 관련된 소스코드를 담고 있다
- 기술스택
  - dbms : PostgreSQL

### 🔸 drug-module
- ㅓㅏㅣ
### 🔸 __config
- 허ㅏㅗ

<br><br><br>
## 📟 개발 컨밴션
### 🔹Single Source of Truth
- 가변성이 있는 변수값은 최대한 하드코딩하지 않는다 
    - 부득이하게 진행되는경우 'HardCording' 문구를 주석으로 표기한다(검색목적)
- 환경변수는 '__config' 레파지토리에서 관리한다
    - 각 서비스별로 '.env'파일을 가지지 않고 중앙관리
### 🔹독자 중심 문서화 구성
- ㄴㅇㄹ
