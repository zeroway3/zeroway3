![header](https://capsule-render.vercel.app/api?type=waving&text=Welcome&color=timeGradient&height=200&section=header&fontSize=64&animation=fadeIn)

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com/?font=Fira+Code&size=20&pause=1000&color=FF6A13&center=true&vCenter=true&width=600&lines=Backend%20Engineer%20%EA%B9%80%EC%98%81%EC%8B%9D;Kotlin%20%2B%20Spring%20Boot%EB%A1%9C%20%EC%8A%A4%ED%83%9D%20%ED%99%95%EC%9E%A5%20%EC%A4%91;%EC%8B%A4%EC%8B%9C%EA%B0%84%20%EB%8D%B0%EC%9D%B4%ED%84%B0%20%ED%8C%8C%EC%9D%B4%ED%94%84%EB%9D%BC%EC%9D%B8%EC%9D%84%20%EB%A7%8C%EB%93%AD%EB%8B%88%EB%8B%A4)](https://git.io/typing-svg)

[![Portfolio](https://img.shields.io/badge/Portfolio-FF6A13?style=for-the-badge&logo=googlechrome&logoColor=white)](https://zeroway3.github.io)
[![Gmail](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ys0000250000@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/zeroway3)

</div>

<br>

## `$ whoami`

```js
const youngsik = {
  role: "Backend Engineer",
  location: "Seoul, South Korea",
  education: "Hannam University — Multimedia Engineering",
  philosophy: "한번 잡으면, 끝까지 간다.",

  stack: {
    backend:   ["NestJS", "Spring Boot (Kotlin)", "TypeScript"],
    database:  ["PostgreSQL", "TimescaleDB", "MongoDB", "Redis"],
    messaging: ["Kafka", "Redis Pub/Sub·Stream", "WebSocket", "SSE"],
    infra:     ["Docker", "GitHub Actions", "AWS", "Terraform"],
    protocol:  ["Modbus", "MQTT", "OPC-UA", "BACnet", "SNMP"],
  },

  currentWork: {
    "엑센솔루션":     "SI/FMS 리뉴얼 — NestJS + PostgreSQL/TimescaleDB, 실시간 텔레메트리 파이프라인",
    "AlphaAdopter": "실시간 뉴스 알림 플랫폼 — Kotlin/Spring Boot + Kafka + MongoDB (사이드)",
  },
};
```

<br>

## Architecture I Build

실제 운영 중인 SI/FMS 시스템의 데이터 파이프라인입니다. (역할 단위로 단순화한 개략도)

```
                    ┌───────────────────────────────────────────────────────┐
                    │              On-Prem / 폐쇄망 · Docker Compose          │
                    │                                                       │
┌──────────────┐    │   ┌───────────┐    ┌───────────┐    ┌──────────────┐ │
│  현장 디바이스   │───▶│   │si-connect │───▶│si-backend │───▶│  PostgreSQL  │ │
│Modbus·MQTT    │    │   │ (수집)     │    │ (정규화)   │    │  TimescaleDB │ │
│OPC-UA·BACnet  │    │   └─────┬─────┘    └─────┬─────┘    └──────────────┘ │
│SNMP (3,501대) │    │         │                │                           │
└──────────────┘    │         ▼                ▼                           │
                    │   ┌───────────┐    ┌───────────┐    ┌──────────────┐ │
                    │   │Redis      │    │Redis      │───▶│ fms-api ·    │ │
                    │   │Pub/Sub    │    │Stream     │    │ auth-server  │ │
                    │   │(실시간 화면)│    │(무손실 이력)│    │ 등 10개+ 서비스│ │
                    │   └───────────┘    └───────────┘    └──────┬───────┘ │
                    │                                             │         │
                    │                                             ▼         │
                    │                              ┌─────────────────────┐ │
                    │                              │ Prometheus / Grafana │ │
                    │                              └─────────────────────┘ │
                    └───────────────────────────────────────────────────────┘
     Device Layer          Ingestion             Cache/Queue        Service Layer
```

<br>

## Tech Radar

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
<br>
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![TimescaleDB](https://img.shields.io/badge/TimescaleDB-FDB515?style=flat-square&logo=timescale&logoColor=black)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
<br>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)

</div>

<br>

## Featured Projects

<table>
<tr><td width="600px" valign="top">

### 🏢 SI/FMS 리뉴얼
건물관리 솔루션(SI/FMS) 백엔드 전면 리뉴얼

`Backend` NestJS · TypeORM · PostgreSQL/TimescaleDB
`Realtime` Redis Pub/Sub·Stream
`Infra` Docker Compose(10개+) · GitHub Actions · Prometheus/Grafana

**Key Contributions**
- 다중 산업 프로토콜(Modbus/MQTT/OPC-UA/SNMP/BACnet) 실시간 텔레메트리 파이프라인 설계, 초당 9,000건 처리 용량 산정
- 레거시 분리 후 데이터 동기화(미러링) 아키텍처 설계
- 실시간 알람(SSE) 캐싱 전략으로 커넥션 풀 고갈 문제 해소
- TimescaleDB 압축 정책으로 653GB → 35GB(94.6%) 절감

</td><td width="600px" valign="top">

### 🔔 AlphaAdopter <sub>(진행 중)</sub>
관심 키워드·종목 뉴스를 실시간 감지해 AI로 필터링하는 알림 플랫폼

`Backend` Kotlin · Spring Boot · JPA
`Messaging` Kafka · MongoDB
`Infra` AWS EKS(예정) · Terraform(예정)

**Key Contributions**
- NAVER API HUB 뉴스 검색 연동 및 데이터 소스 검증
- Kafka 기반 수집 → MongoDB 원본 저장 → PostgreSQL 정규화 → 구독 매칭 파이프라인 설계·구현
- User/Subscription/NewsArticle/Notification 도메인 모델링
- [GitHub 레포 ↗](https://github.com/zeroway3/alpha-adopter)

</td></tr>
<tr><td width="600px" valign="top">

### 🏃 런덤메이트
GPS 러닝 크루 매칭 앱 (App Store·웹 동시 배포)

`Frontend` Next.js · React
`Realtime` STOMP (WebSocket)
`Infra` Docker · AWS ECS

**Key Contributions**
- STOMP 기반 실시간 채팅 클라이언트(연결 수립·구독 관리) 개발
- Docker/AWS ECS 배포 파이프라인 구성·운영
- 커밋 127건 · 변경 파일 402개 · 머지 PR 40건+

</td><td width="600px" valign="top">

### 🛡 VibeShield
AI 생성 코드 보안 검사 도구 · 모두의 창업 프로젝트 1차 선정

`Tool` TypeScript · Electron · Tree-sitter (AST)
`Detection` YAML 룰베이스 · PyPI/npm 화이트리스트

**Key Contributions**
- 결정론적 룰베이스 탐지 엔진 설계 주도, 환각 API 탐지율 83%(Semgrep·SonarQube 0%)
- 관제시스템·인증·보안 아키텍처 설계
- 현업 개발자 9인 PoC, 오탐률 3.8%, 5개사 테스트 도입 협의

</td></tr>
</table>

<br>

## GitHub Analytics

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=zeroway3&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" width="49%" alt="김영식's GitHub stats" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=zeroway3&layout=compact&theme=tokyonight&hide_border=true" width="41%" alt="Top Languages" />

<img src="https://github-readme-streak-stats.herokuapp.com/?user=zeroway3&theme=tokyonight&hide_border=true" width="70%" alt="GitHub Streak" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=zeroway3&theme=react-dark&hide_border=true&area=true" width="95%" alt="Activity Graph" />

</div>

<br>

## Experience & Activities

```text
2025.02 - Present   엑센솔루션              Backend Engineer (NestJS, PostgreSQL, TimescaleDB)
2026.06 - 2026.08   VibeShield             보안 아키텍처 담당 · 모두의 창업 프로젝트 1차 선정
2026.01 - 2026.05   런덤메이트               Frontend(Web) 담당 · App Store·웹 동시 배포
2024.03 - 2024.08   한국소프트웨어인재개발원    개발자 과정 수료 (960시간, 팀 프로젝트 기반)
2025.02             Singapore Institute of Technology 국제 협업 해커톤
2024.10             Brunel University 국제 협업 해커톤
2019.09 - 2021.04   대한민국 육군 병장 만기 전역 (감시장비운용병)
2018.03 - 2025.02   한남대학교 멀티미디어공학과 졸업
```

<br>

## What I'm Working On

🔔 **[AlphaAdopter](https://github.com/zeroway3/alpha-adopter)** — Kotlin/Spring Boot로 실시간 뉴스 알림 플랫폼을 만들며 Kafka·MongoDB·AWS 스택을 서비스 규모로 확장하는 중입니다. 뉴스 수집·매칭 파이프라인까지 구현했고, 다음은 SSE 실시간 알림과 AWS(EKS·RDS·ElastiCache) 전환입니다.

<br>

<div align="center">

![Visitor Count](https://komarev.com/ghpvc/?username=zeroway3&color=FF6A13&style=flat-square&label=Profile+Views)

</div>
