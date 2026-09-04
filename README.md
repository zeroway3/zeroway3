![header](https://capsule-render.vercel.app/api?type=waving&text=Kim%20Youngsik&color=0:0e0c0b,100:FF6A13&height=180&section=header&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=38)

<div align="center">

**다중 프로토콜 데이터를 하나의 파이프라인으로 모으는 백엔드 개발자**
<br>
서로 다른 규격의 외부 데이터를 단일 모델로 수렴시키고, 대량 유입 상황에서 정합성과 성능을 지키는 설계를 좋아합니다.

<a href="https://zeroway3.github.io"><img src="https://img.shields.io/badge/-Portfolio-FF6A13?style=flat-square&logo=googlechrome&logoColor=white" /></a>
<a href="mailto:ys0000250000@gmail.com"><img src="https://img.shields.io/badge/-Email-1c1310?style=flat-square&logo=gmail&logoColor=white" /></a>
<a href="https://github.com/zeroway3/alpha-adopter"><img src="https://img.shields.io/badge/-Building%20AlphaAdopter-1c1310?style=flat-square&logo=apachekafka&logoColor=white" /></a>

</div>

<br>

## 지금 풀고 있는 문제들

회사(SI/FMS)와 사이드 프로젝트(AlphaAdopter)에서 실제로 부딪힌 설계 판단들입니다. 클릭하면 이유가 열립니다.

<details>
<summary><b>왜 Redis Pub/Sub과 Stream을 같이 쓰나요?</b></summary>
<br>

화면은 최신값만 지연 없이 필요해서 Pub/Sub을, 알람 평가·이력 적재는 값이 유실되면 안 되기 때문에 Stream을 씁니다. 구독마다 `deliveryReliability`(realtime / durable / both) 값으로 채널을 선택하게 해서, 소비자 특성에 안 맞는 채널을 강제하지 않도록 했습니다.
</details>

<details>
<summary><b>배치 주기를 왜 하필 1.5초로 정했나요?</b></summary>
<br>

500ms는 트랜잭션 수 대비 화면 체감 개선이 미미했고, 5초는 운영자가 느리다고 느끼는 지연이었습니다. 가장 느린 프로토콜(BACnet)의 폴링 사이클을 온전히 담는 최소 단위가 1.5초였고, 실측 p99 이벤트 루프 지연(38.6ms)에도 여유가 남는 값이었습니다.
</details>

<details>
<summary><b>DB를 왜 스키마가 아니라 서비스 단위로 분리했나요?</b></summary>
<br>

장애 격리(한 서비스의 쓰기 부하가 다른 서비스 커넥션 풀에 영향을 주면 안 됨)와 배포 독립성(서비스마다 마이그레이션 시점이 다름) 때문입니다. 스키마만 나누면 커넥션 풀과 락 경쟁은 여전히 공유되어 리소스 격리가 되지 않습니다.
</details>

<details>
<summary><b>AlphaAdopter는 왜 뉴스 원본을 MongoDB에 먼저 저장하나요?</b></summary>
<br>

뉴스 소스마다 필드 구성이 달라 스키마를 고정하기 어렵습니다. 정규화 전 원본을 스키마 유연한 MongoDB에 landing zone으로 먼저 저장하고, PostgreSQL에는 링크 기준 중복 제거를 거친 정규화된 데이터만 적재합니다.
</details>

<br>

## 손에 익은 도구들

|  |  |
|---|---|
| **Backend** | ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) |
| **Data** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![TimescaleDB](https://img.shields.io/badge/TimescaleDB-FDB515?style=flat-square&logo=timescale&logoColor=black) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white) ![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white) |
| **Infra** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white) ![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) |
| **Observability** | ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white) |
| **Protocol** | ![Modbus](https://img.shields.io/badge/Modbus-4B5563?style=flat-square) ![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white) ![OPC--UA](https://img.shields.io/badge/OPC--UA-4B5563?style=flat-square) ![BACnet](https://img.shields.io/badge/BACnet-4B5563?style=flat-square) |

<br>

## Projects

**🏢 [SI/FMS 리뉴얼](https://zeroway3.github.io)** — 건물관리 솔루션 백엔드, 디바이스 3,501대·태그 3만 개 규모 실시간 파이프라인을 NestJS + PostgreSQL/TimescaleDB로 설계·운영 (`NestJS` `TimescaleDB` `Redis Stream`)

**🔔 [AlphaAdopter](https://github.com/zeroway3/alpha-adopter)** — 관심 키워드·종목 뉴스를 실시간 감지해 AI로 필터링하는 알림 플랫폼, Kotlin/Spring Boot로 새 스택 확장 중 (`Kotlin` `Spring Boot` `Kafka` `MongoDB`) *· 진행 중*

**🏃 [런덤메이트](https://apps.apple.com/kr/app/id6761368135)** — GPS 러닝 크루 매칭 앱, STOMP 실시간 채팅과 AWS ECS 배포 파이프라인 담당 (`Next.js` `STOMP` `AWS ECS`)

**🛡 VibeShield** — AI 생성 코드 보안 검사 도구, 환각 API 탐지율 83% 실측 · 모두의 창업 프로젝트 1차 선정 (`TypeScript` `Electron` `Tree-sitter`)

<br>

## Timeline

| 기간 | 활동 |
|---|---|
| 2025.02 – 현재 | **엑센솔루션** · Backend Engineer (NestJS, PostgreSQL, TimescaleDB) |
| 2026.09 – 현재 | **AlphaAdopter** 사이드 프로젝트 진행 중 (Kotlin/Spring Boot 스택 확장) |
| 2026.06 – 2026.08 | **VibeShield** 보안 아키텍처 담당 · 모두의 창업 프로젝트 1차 선정 |
| 2026.01 – 2026.05 | **런덤메이트** Frontend(Web) 담당 · App Store·웹 동시 배포 |
| 2024.03 – 2024.08 | 한국소프트웨어인재개발원 개발자 과정 수료 (960시간) |
| 2025.02 | Singapore Institute of Technology 국제 협업 해커톤 |
| 2024.10 | Brunel University 국제 협업 해커톤 |
| 2019.09 – 2021.04 | 대한민국 육군 병장 만기 전역 |
| 2018.03 – 2025.02 | 한남대학교 멀티미디어공학과 졸업 |

<br>

<div align="center">

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=zeroway3&background=0e0c0b00&border=33261f&ring=FF6A13&fire=FF6A13&currStreakLabel=FF6A13&hide_border=false)

![Visitor Count](https://komarev.com/ghpvc/?username=zeroway3&color=FF6A13&style=flat-square&label=Profile+Views)

</div>
