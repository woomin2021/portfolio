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

### 1. 살리장 — 지역 소상공인 마감 할인 플랫폼

> AWS EKS 기반 커머스 플랫폼 | 2026.04 ~ 2026.05 | 6인 팀

담당 역할: 인프라 2인 중 Terraform 기반 AWS 인프라 구축, EKS 운영, ArgoCD 배포 환경 구성 담당

주요 구현 및 결과

- Terraform으로 VPC, EKS, RDS, ElastiCache, CloudFront, WAF 등 인프라 모듈화
- GitHub Actions에서 코드·이미지 검증 후 ArgoCD가 Kubernetes 배포를 수행하도록 CI/CD 역할 분리
- Karpenter 기반 워커 노드 동적 프로비저닝 구성
- ALB Ingress Controller와 EKS 서비스 연동
- IAM Role, IRSA, Security Group, WAF 기반 접근 권한과 외부 요청 보호 구성
- kubelet 10250 포트와 Security Group 규칙을 분석해 kubectl logs/exec 타임아웃 복구
- Terraform for_each의 Plan 단계 미확정 값 오류를 고정 key 구조로 변경해 서브넷 태깅 자동화
- 해결한 장애 원인과 점검 항목을 문서화해 동일 유형 문제의 확인 기준 마련

🔗 Team Repository: [github.com/Salijang](https://github.com/Salijang)

---

### 2. 고가용성 서버리스 이미지 프로세싱 파이프라인

> AWS 이벤트 기반 이미지 처리 시스템 | 2026.03 ~ 2026.04 | 4인 팀

담당 역할: 인프라·CI/CD 담당, Terraform 구성, 폐쇄망 네트워크, 모니터링과 부하 테스트 설계

주요 구현 및 결과

- Terraform으로 VPC, EC2, ALB, ASG, S3, SQS, Lambda 인프라 모듈화
- Interface/Gateway VPC Endpoint를 이용한 Private Subnet 폐쇄망 구성
- S3 → SQS → Lambda 비동기 이미지 리사이징 파이프라인 구축
- ALB 요청 수와 CPU 사용률 기반의 이중 Auto Scaling 정책 구성
- CloudWatch, X-Ray, Slack 알림을 활용한 상태 확인과 장애 탐지 환경 구성
- SSM과 cloud-init 로그로 컨테이너 기동 실패 원인을 분석하고 서비스 복구
- 실제 S3 이벤트와 테스트 이벤트를 분리해 Lambda KeyError와 DLQ 오탐 제거
- k6 에러 주입 수와 DLQ 메시지 수가 156/156, 148/148, 456/456으로 일치하는지 검증

🔗 Repository: [aws-cloud-pipeline-project](https://github.com/woomin2021/aws-cloud-pipeline-project)

---

### 3. JJB — 집 잠시 빌려드립니다

> 중단기 임시 주거 매칭 플랫폼 | 2025.09 ~ 2025.12 | 4인 팀  

담당 역할: NCP 인프라 설계·배포, Spring Boot 백엔드, 예약·결제 API와 DB 설계

주요 구현 및 결과

- NCP Server, Subnet, ACG 기반 서버·DB 네트워크 분리
- DB ACG의 3306 포트 누락으로 발생한 통신 장애를 telnet으로 확인해 복구
- Shell 배포 스크립트에서 파일 복사 전 WAS가 재시작되는 순서 오류를 찾아 배포 순서 재설계
- curl로 실제 서버 응답을 확인해 구버전 응답 문제 해결
- Firebase Auth와 Spring Boot JWT 인증 연동
- 예약 중복 방지와 트랜잭션 처리로 데이터 정합성 관리
- 해결 과정과 재발 방지 절차를 팀 문서로 작성

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

