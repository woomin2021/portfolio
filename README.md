# 송우민 | 

> NCP 실무 배포부터 AWS 기반 고가용성 아키텍처까지,  
> 경험으로 쌓은 클라우드 인프라 시스템 엔지니어입니다.

📧 이메일 기재 | 📍 서울 | 🔗 [GitHub](https://github.com/woomin2021)

---

## 🏅 Certifications

| 자격증 | 취득연도 |
|--------|----------|
| RHCSA (Red Hat Certified System Administrator) | 2026 |
| AWS Solutions Architect Associate (SAA) | 2026 |
| SQLD | 2024 |
| 정보처리산업기사 | 2025 |
| 리눅스마스터 2급 | 2025 |

---

## 🛠 Skills

| 분류 | 기술 |
|------|------|
| **Cloud** | AWS (VPC, EC2, ALB, ASG, EKS, Lambda, S3, SQS, SNS, ECR, CloudFront, WAF, Route53, CloudWatch, X-Ray), NCP |
| **IaC** | Terraform, Ansible |
| **Container / Orchestration** | Docker, Kubernetes (EKS), Karpenter |
| **CI/CD** | GitHub Actions, ArgoCD (GitOps) |
| **OS** | Linux (RHCSA) |
| **Backend** | Java, Spring Boot, Python (FastAPI) |
| **Database** | MySQL, PostgreSQL (RDS), Redis (ElastiCache), DynamoDB |
| **Monitoring / Test** | CloudWatch, X-Ray, k6, SonarQube, Trivy, Slack 알람 |
| **Tools** | Git, GitHub |

---

## 💼 Projects

### 1. 살리장 — 지역 소상공인 마감 할인 상품 연결 플랫폼

> EKS 기반 클라우드 네이티브 플랫폼 | 2026.04 ~ 2026.05 | 4인 팀

**담당 역할:** Terraform 기반 전체 인프라 설계·구축, CI/CD 파이프라인, 프론트엔드 개발

**주요 구현 내용:**

- Terraform으로 전체 인프라 모듈화 코드화 (network / compute / data / security / messaging 등)
- Private EKS 클러스터 구축 + Karpenter 동적 노드 프로비저닝
- Route53 + CloudFront + WAF + ACM Edge 보안 레이어 구축
- ALB + Ingress Controller 연동, VPC 서브넷 CIDR 설계 (Multi-AZ)
- RDS PostgreSQL + RDS Proxy + ElastiCache Redis 데이터 계층 분리
- VPC Endpoints(PrivateLink)로 AWS 내부망 통신 구성
- IRSA(IAM Roles for Service Accounts)로 Pod별 최소 권한 보안 설계
- SQS & SNS 비동기 처리 레이어 설계
- GitHub Actions CI (SonarQube 코드 품질 + Trivy 이미지 취약점 스캔) + ArgoCD GitOps CD
- React 기반 프론트엔드 개발

🔗 Team Repository: [github.com/Salijang](https://github.com/Salijang)

---

### 2. 고가용성 서버리스 이미지 프로세싱 파이프라인

> AWS 기반 이벤트 드리븐 아키텍처 | 2026.03 ~ 2026.04 | 4인 팀

**담당 역할:** CI/CD 파이프라인 구축·자동화, CloudWatch 모니터링 및 성능 분석

**주요 구현 내용:**

- Terraform으로 전체 인프라 코드화 (모듈 분리: network / compute / storage / messaging / lambda)
- NAT Gateway 없이 VPC Endpoint 8개로 폐쇄망 구성 (보안 강화)
- S3 → SQS → Lambda 이벤트 기반 비동기 이미지 리사이징 파이프라인 구축
- DLQ(Dead Letter Queue)로 3회 실패 메시지 격리 — 데이터 무결성 확보
- GitHub Actions CI/CD — terraform fmt/validate/plan 자동 검증 → apply 자동 배포
- Multi-AZ ALB + Auto Scaling 이중 정책 (ALB 요청 수 기반 + CPU 기반)
- CloudWatch 대시보드 + X-Ray 서비스 맵 + Slack 알람 연동 모니터링 체계 구축
- k6 부하 테스트로 성능 한계 측정 및 인프라 보강 검증

🔗 Repository: [aws-cloud-pipeline-project](https://github.com/woomin2021/aws-cloud-pipeline-project)

---

### 3. JJB — 집 잠시 빌려드립니다 

> 대학생·직장인 대상 중단기 임시 주거 플랫폼 | 2023.09 ~ 2024.02 | 4인 팀 (기여도 65%)

**담당 역할:** NCP 인프라 설계·배포, Spring Boot 백엔드 개발, 예약·결제 API 구현, DB 설계

**주요 구현 내용:**

- NCP 서버-DB 서브넷 분리 배치, ACG 최소 권한 원칙 적용
- Firebase Auth + Spring Boot JWT 검증 연동
- 중복 예약 방지 로직 + 트랜잭션 처리로 데이터 정합성 확보
- 위치·날짜 컬럼 인덱스 적용으로 매물 탐색 성능 개선
- 8개 이상 테이블 정규화 설계
- 발표 전날 이중 장애(ACG 누락 + WAS 타이밍 오류)를 계층별 원인 추적으로 해결

🔗 Repository: [capstone-project](https://github.com/woomin2021/capstone-project) / [jjb-spring-backend](https://github.com/woomin2021/jjb-spring-backend)

---

### 4. Vibe Pro — 실시간 미국 증시 AI 요약 웹 애플리케이션

> AI 바이브코딩 활용 풀스택 프로젝트

- 실시간 미국 증시 지수와 주요 뉴스를 수집
- Google Gemini AI를 활용해 밤사이 핵심 이슈를 한눈에 요약

🔗 Repository: [vibe_pro](https://github.com/woomin2021/vibe_pro)

---

### 5. 수강신청·티켓팅 시뮬레이션 앱

> Android 앱 프로그래밍 프로젝트

- 대규모 트랜잭션 처리와 서버 로직 구현 경험
- Android + Spring Boot 백엔드 연동

🔗 Repository: [course-registration-android](https://github.com/woomin2021/course-registration-android) / [course-registration-backend-jsp](https://github.com/woomin2021/course-registration-backend-jsp)

---

### 6. Java Swing 가계부

> Java 기초·객체지향 개념 적용 프로젝트

- 클래스 구조와 기본 로직 구현
- Java Swing 기반 데스크탑 애플리케이션

🔗 Repository: [java-swing-accountbook](https://github.com/woomin2021/java-swing-accountbook)

---

