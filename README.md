<img width="100" height="97" alt="543208578-fd211198-6bd7-4d53-9f72-abc2aea19922" src="https://github.com/user-attachments/assets/35fcd5cd-552e-4a73-82f9-4ef56c33e74f" /><h1 style="font-size: 3em;">[StartUp]: 스타트업 최적화 그룹웨어 시스템</h1>

---

## 목차
1. [프로젝트 개요](#1-프로젝트-개요)
2. [개발 환경](#2-개발-환경)
3. [데이터베이스 설계](#3-데이터베이스-설계)
4. [프로젝트 리더십 및 협업 문화](#4-프로젝트-리더십-및-협업-문화)
5. [전체 기능 및 담당 영역](#5-전체-기능-및-담당-영역)
6. [핵심 구현 기능 및 트러블 슈팅](#6-핵심-구현-기능-및-트러블-슈팅)
7. [프로젝트 참여 소감](#7-프로젝트-참여-소감)

---

## 1. 프로젝트 개요
시스템의 결합도를 낮추고 유지보수성을 극대화하는 아키텍처 설계를 지향하며 구축한 소규모 그룹웨어 시스템입니다. 프론트엔드와 백엔드의 리포지토리를 철저히 분리하고 도메인 간 독립성을 부여하여, 향후 서비스 확장 및 유지보수 시 유연하게 대응할 수 있는 아키텍처 기반을 마련했습니다. 실무 프로젝트 경험을 통해 단순한 기능 구현을 넘어, 서비스의 초기 기반을 기획하고 팀의 협업 인프라를 주도적으로 구축했습니다.

* **진행 기간**: 2025.10.22 ~ 2025.11.26 (5주)
* **개발 인원**: 5명
* **담당 역할**: 프로젝트 리더로서 팀 개발 표준 수립 및 릴리즈 관리를 수행했으며, 백엔드 아키텍처 설계와 서버 인프라(On-premises/Cloud) 구축 및 CI/CD 파이프라인 구성을 담당했습니다.
* **주요 대상**: 스타트업 및 중소기업
* **핵심 목적**: 비즈니스 운영에 필요한 인사, 전자결재 등 핵심 그룹웨어 기능을 도메인 기반으로 모듈화하고 서비스화했습니다.
* **리포지토리**: 
  * Backend: [https://github.com/khyeongtaek/startup_BE](https://github.com/khyeongtaek/startup_BE)
  * Frontend: [https://github.com/khyeongtaek/startup_FE](https://github.com/khyeongtaek/startup_FE)

## 2. 개발 환경

### Backend
<img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=OpenJDK&logoColor=white"/> <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=Spring%20Boot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat-square&logo=Spring%20Security&logoColor=white"/> <img src="https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=Hibernate&logoColor=white"/>

### Frontend
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=black"/> <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=Vite&logoColor=white"/> <img src="https://img.shields.io/badge/MUI-007FFF?style=flat-square&logo=MUI&logoColor=white"/>

### Database
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/>

### Infra & DevOps
<img src="https://img.shields.io/badge/AWS%20EC2-232F3E?style=flat-square&logo=Amazon%20EC2&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=Docker&logoColor=white"/> <img src="https://img.shields.io/badge/Synology-B5B5B6?style=flat-square&logo=Synology&logoColor=white"/> <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=Nginx&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=GitHub%20Actions&logoColor=white"/>

## 3. 데이터베이스 설계
* RDBMS 기반의 논리적/물리적 모델링을 수행하고 ERD를 지속적으로 현행화했습니다.
* 시스템 확장성을 고려하여 물리적 외래키(FK) 제약조건을 최소화하되, **논리 삭제(Soft Delete)** 메커니즘과 애플리케이션 레벨의 비즈니스 로직을 통해 데이터 정합성을 보장하도록 설계했습니다.
* 계층형 공통 코드 테이블을 구축하여 시스템 전역에서 사용되는 분류 값 및 상태 상수를 중앙 집중화했습니다.
<img width="1921" height="1952" alt="erd_1조" src="https://github.com/user-attachments/assets/cdd0bd55-59cf-47c7-aa20-234db3ec817a" />


## 4. 프로젝트 리더십 및 협업 문화
기능 구현에 앞서 팀의 개발 환경과 규칙을 체계화하여 프로젝트 리스크를 최소화했습니다. 특히 **한정된 리소스 내에서 개발 효율성을 극대화하기 위해 상용 템플릿 도입과 같은 전략적 의사결정을 수행했으며,** 이를 통해 확보한 리소스를 백엔드 핵심 도메인 로직과 안정적인 인프라 설계에 집중 투자했습니다.

* **Git 워크플로우 및 코드 리뷰 체계 확립**: `main` - `dev` - `feature` 브랜치 전략을 수립하여 관리했습니다. 개인 환경에서 테스트가 완료된 코드만 PR을 생성하도록 하고, 리뷰 및 병합 프로세스를 통제하여 `dev` 브랜치의 무결성을 엄격하게 유지했습니다.
* **표준화 가이드라인(`CONTRIBUTING.md`) 배포**: 프로젝트 초기, 네이밍 컨벤션 및 RESTful API 설계 기준의 혼선이 개발 지연으로 이어질 것을 예측했습니다. 이를 방지하기 위해 개발 표준 가이드를 선제적으로 배포하여 커뮤니케이션 비용을 줄이고 개발 리드 타임을 단축했습니다.
* **비용 효율적인 환경 분리 및 배포 자동화**: 비용과 리소스의 한계를 극복하기 위해 **On-premises**(Synology NAS) 환경에 Docker를 활용하여 Nginx, MySQL 기반의 격리된 테스트 베드 및 DB 서버를 구축했습니다. 애플리케이션 운영 서버는 AWS EC2로 구성하여 트래픽을 분산시켰으며, GitHub Actions를 활용한 CI/CD 파이프라인을 구축하여 배포 안정성을 확보했습니다.

## 5. 전체 기능 및 담당 영역

| 구분 | 기능 목록 |
| :--- | :--- |
| **전체 구현 기능** | 메뉴 관리, 로그인, 인사관리, 전자결재, 코드 관리, 마이페이지, 업무일지, 첨부 기능, 메일, 알림, 채팅, 조직도, 게시판, 근태 관리, 결재 양식, 일정 관리 |
| **핵심 담당 영역** | **공통 코드 API 설계, 보안/인증 인프라 구축, 전자결재, 인사관리 및 권한 제어** |

## 6. 핵심 구현 기능 및 트러블 슈팅

### 6.1. [아키텍처] 공통 코드 계층화 설계 및 프론트엔드 동적 라우팅 지원
* **Situation**: 메뉴 구성, 직급, 권한 등의 데이터가 소스 코드에 하드코딩될 경우, 요구사항 변경 시마다 서버를 재배포해야 하는 유지보수 한계가 존재했습니다.
* **Task**: 프론트엔드와 백엔드의 강결합을 해소하고, 관리자가 직접 시스템 변수와 메뉴 구성을 제어할 수 있는 유연한 서버 아키텍처를 구축하는 것이 과제였습니다.
* **Action**: 대/소분류를 계층형으로 관리할 수 있는 공통 코드 테이블을 설계했습니다. 백엔드에서 트리 구조의 메뉴 리스트를 API로 제공하여 클라이언트가 런타임에 동적으로 화면을 구성하도록 최적화했습니다.
* **Result**: 개발자의 소스 코드 수정 없이 운영 관리자가 어드민 페이지에서 즉시 메뉴와 권한을 제어할 수 있게 되었습니다. 이를 통해 단순 수정을 위해 소요되던 **약 10분의 배포 공수(CI/CD)를 제거하는 성과를 거두었습니다.**
* **Lesson Learned**: **"핵심 모듈의 무게감과 설계의 무결성"**
    시스템 전역에서 참조되는 공통 코드 모듈은 역설적으로 모든 도메인이 의존할 수밖에 없는 '중심점'이 됨을 체감했습니다. 이 모듈의 작은 결함이 전체 시스템의 마비로 이어질 수 있다는 책임감을 바탕으로, 초기 설계 단계에서부터 '무결점 유지보수'가 가능하도록 견고한 데이터 모델링에 집중했습니다. 또한 이를 통해 프론트엔드의 메뉴 항목을 실시간 동적 렌더링으로 구현하며 진정한 의미의 '비즈니스 유연성'을 경험했습니다.

### 6.2. [보안] HttpOnly 쿠키와 Spring Security를 활용한 안전한 인증 프로세스 구축
* **Situation**: 기존의 헤더 기반 JWT 인증은 브라우저 스토리지 보관 시 XSS 공격에 취약했으며, 토큰 만료 시 사용자가 잦은 재로그인을 수행해야 하는 UX 저하 문제가 있었습니다.
* **Task**: 보안 취약점을 근본적으로 차단하는 동시에, 토큰 재발급 로직을 통해 사용자가 중단 없이 서비스를 이용할 수 있는 안전한 인증 인프라를 설계해야 했습니다.
* **Action**: Spring Security를 연동하고, Access/Refresh Token을 클라이언트 스크립트에서 접근할 수 없는 `HttpOnly` 및 `Secure` 속성의 쿠키로 발급하도록 설계했습니다. 서버 측에서 Refresh Token의 유효성을 검증하고, 만료 시점에 맞춰 안전하게 재발급되는 로직을 구현했습니다.
* **Result**: 세션 탈취 위험을 근본적으로 차단하여 보안성을 강화했으며, 클라이언트 인터셉터 로직과 연계하여 사용자는 토큰 만료를 체감하지 않고 끊김 없는 서비스를 이용할 수 있게 되었습니다.

### 6.3. [성능 및 무결성] 전자결재 쿼리 최적화 및 데이터 정합성 보장
* **Situation**: 다수의 결재선이 포함된 목록 조회 시 N+1 문제로 인한 성능 병목이 우려되었으며, 퇴사자와 연관된 데이터 처리 시 외래키 제약조건 오류나 데이터 유실 위험이 존재했습니다.
* **Task**: 조회 성능을 비약적으로 개선함과 동시에, 인사 데이터 변동 시에도 시스템 전반의 데이터 무결성을 유지할 수 있는 정합성 보장 방안을 마련하는 것이 목표였습니다.
* **Action**: 
    * **쿼리 최적화**: JPA Fetch Join을 활용하여 연관된 엔티티를 단일 쿼리로 조회하도록 개선했습니다.
    * **논리 삭제(Soft Delete)** 적용: 인사 데이터 삭제 시 물리적 삭제 대신 상태값을 비활성화하는 방식을 채택했습니다.
* **Result**: 
    * 데이터 조회 시 발생하는 쿼리 실행 횟수를 $N+1$회에서 $1$회로 최적화하여 DB I/O 부하를 크게 감소시켰습니다.
    * 퇴사자 발생 후에도 과거의 결재 이력 및 게시판 데이터를 유지함으로써 시스템 전반의 데이터 무결성을 확보하고 외래키 위반 에러를 방지했습니다.

## 7. 프로젝트 참여 소감
이번 프로젝트는 비즈니스 로직 구현을 넘어, '시스템 아키텍처의 유연성'과 '기반 코드의 무게감'을 깊이 체감한 계기였습니다. 특히 모든 기능의 뿌리가 되는 공통 코드와 인프라를 설계하며, **객체지향의 지향점인 '낮은 결합도'를 유지하면서도 시스템 전역에 영향을 주는 필수적 의존성을 어떻게 안전하게 관리할 것인가**에 대해 치열하게 고민했습니다. 단순히 작동하는 코드를 넘어, "내가 만든 이 기반 코드가 팀원들의 개발 생산성과 전체 시스템의 안정성에 어떤 영향을 미치는가"를 먼저 생각하는 태도를 갖추게 되었습니다. 이러한 경험을 바탕으로, 앞으로도 확장 가능하고 견고한 백엔드 생태계를 만드는 데 기여하고 싶습니다.
