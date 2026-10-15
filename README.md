# 송우민 | Cloud & DevOps Engineer

> 클라우드 인프라 구축 · 배포 자동화 · 로그 기반 장애 분석

AWS·NCP 기반 팀 프로젝트에서 인프라 구성부터 서비스 배포와 동작 확인까지 담당.
Terraform 기반 인프라 코드화, Kubernetes 배포 환경 구성, 로그와 통신 경로를 근거로 한 장애 분석 경험.

[GitHub](https://github.com/woomin2021) · [프로젝트 포트폴리오](https://github.com/woomin2021/portfolio)

## 대표 프로젝트

### 1. 살리장 | 지역 소상공인 마감 할인 플랫폼

SeSAC 교육 팀 프로젝트 · 2026.04.01 ~ 2026.05.12 · 6인 팀

**담당:** 인프라 담당 2명 중 Terraform 기반 AWS 인프라 구축·모듈화, EKS·Karpenter 구성, ArgoCD 배포 환경 구성

- Terraform으로 VPC, EKS, RDS, ElastiCache, CloudFront, WAF 등 인프라 모듈화
- GitHub Actions의 이미지 빌드·검증과 ArgoCD의 Kubernetes 배포 역할 분리
- Karpenter 기반 워커 노드 동적 프로비저닝 구성
- CloudFront·WAF 구성 및 EKS 개발 환경 접근 제한
- kubelet 10250 포트의 통신 경로와 Security Group 규칙을 점검해 `kubectl logs`·`kubectl exec` 타임아웃 복구
- Terraform `for_each`의 Plan 단계 미확정 값 오류를 고정 key 구조로 변경해 서브넷 태깅 문제 해결
- Amazon Bedrock Claude 이미지 분석 연동과 비식품 입력·응답 형식 검증 구현

[팀 인프라 저장소](https://github.com/Salijang/sallijang-infra) · [본인 기여 PR: CloudFront·WAF 및 EKS 접근 제한](https://github.com/Salijang/sallijang-infra/pull/21) · [팀 GitHub](https://github.com/Salijang)

### 2. AWS 기반 고가용성 이미지 처리 파이프라인

SeSAC 교육 팀 프로젝트 · 2026.03 ~ 2026.04 · 4인 팀

**담당:** Terraform 인프라 설계·구축, VPC Endpoint 기반 네트워크 구성, GitHub Actions CI/CD 자동화, k6 부하 테스트 설계·검증

- Terraform으로 VPC, EC2, ALB, ASG와 이미지 처리 관련 AWS 리소스 구성
- VPC Endpoint를 활용해 Private Subnet에서 필요한 AWS 서비스에 접근하는 네트워크 구성
- S3 → SQS → Lambda 비동기 이미지 처리 구조를 지원하는 인프라 구축
- EC2 Running 상태와 ALB Unhealthy 상태를 구분하고, SSM으로 접속해 `cloud-init-output.log` 점검
- ECR 로그인 실패를 단서로 STS VPC Endpoint와 EC2 IAM 권한을 점검·보완한 뒤, 컨테이너 기동 및 ALB Healthy 전환 확인
- k6를 활용한 부하 테스트 설계와 응답·오류 결과 검증

[저장소](https://github.com/woomin2021/aws-cloud-pipeline-project)

### 3. JJB | 집 잠시 빌려드립니다

캡스톤디자인 팀 프로젝트 · 2025.09 ~ 2025.12 · 4인 팀

**담당:** NCP 인프라 설계·배포, Java·Spring Boot 백엔드, 예약·결제 API와 DB 설계

- NCP Server, Subnet, ACG 기반 서버·DB 네트워크 구성
- 예약·결제 REST API 구현과 MySQL 테이블 설계·트랜잭션 처리
- Firebase Auth와 JWT 기반 인증 연동
- `telnet`으로 DB 연결 상태를 확인하고 ACG의 3306 포트 누락을 수정해 통신 복구
- 배포 스크립트의 파일 복사·WAS 재시작 순서를 수정하고 `curl`로 실제 서버 응답 확인
- 캡스톤디자인 경진대회 장려상 수상

[백엔드 저장소](https://github.com/woomin2021/jjb-spring-backend) · [Android 앱 저장소](https://github.com/woomin2021/capstone-project)

## 기술

프로젝트와 학습에서 사용한 기술. 구체적인 담당 범위는 각 프로젝트에 구분해 기재.

| 분야 | 사용 기술 |
| --- | --- |
| Cloud | AWS: VPC, EC2, ALB, ASG, EKS, S3, SQS, Lambda, ECR, CloudFront, WAF / NCP |
| OS / Language | Linux, Java, Python, Shell Script, SQL |
| Infrastructure as Code | Terraform, Ansible |
| Container | Docker, Kubernetes, Karpenter |
| CI/CD | GitHub Actions, ArgoCD |
| Monitoring / Test | CloudWatch, X-Ray, Prometheus, Grafana, k6 |
| Security / Quality | IAM, Security Group, ACG, WAF, Trivy, SonarQube |
| Backend / Database | Spring Boot, MySQL, PostgreSQL, Redis, DynamoDB |
| Development Tools / AI | Git, GitHub, Codex, Claude Code, Terraform MCP, Amazon Bedrock |

## 자격증

| 자격증 | 취득연도 |
| --- | --- |
| RHCSA — Red Hat Certified System Administrator | 2026 |
| AWS Certified Solutions Architect – Associate | 2026 |
| 정보처리산업기사 | 2025 |
| 리눅스마스터 2급 | 2025 |
| SQLD | 2024 |

## 기타 프로젝트

- [Vibe Pro](https://github.com/woomin2021/vibe_pro): Google Gemini를 활용한 미국 증시·뉴스 요약 웹 애플리케이션
- 수강신청·티켓팅 연습 앱: [Android](https://github.com/woomin2021/course-registration-android) / [JSP 백엔드](https://github.com/woomin2021/course-registration-backend-jsp)
