## Hi there 👋

<!--
**LGJ0405/LGJ0405** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

| **Server / WSGI / ASGI** |  |
-->

## 🛠️ 기술 스택 (Tech Stack)

| 분야 | 기술 |
|:--|:--|
| **Languages** | ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=black)|
| **Backend / Frameworks** | ![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white) |
| **Databases** | ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white) ![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white) ![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white) |
| **Deployment** | ![AWS EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazon-ec2&logoColor=white) ![AWS S3](https://img.shields.io/badge/AWS_S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white) ![AWS RDS](https://img.shields.io/badge/AWS_RDS-527FFF?style=for-the-badge&logo=amazon-rds&logoColor=white) |
| **Tools** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![VS_Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white) |

---
# 🎙️ 프로젝트: 말하는대로
> https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN17-FINAL-2Team

## 💡 Key Learnings & Troubleshooting

### Synchronous Bottleneck & Architecture Design
- **Problem**: 모델 추론 지연(2분 이상)으로 인한 프론트엔드 연결 끊김 현상 발생.
- **Analysis**: Nginx, ALB 등 인프라 설정 변경만으로는 클라이언트 브라우저의 물리적 타임아웃 해결에 한계가 있음을 파악.
- **Solution**: 
  - 응답 대기 시간을 최소화하기 위해 **비동기 메시지 큐(Message Queue)** 기반 아키텍처 설계 제안.
  - 연산 로직을 백그라운드로 분리하고, **Polling/WebSocket**을 통해 클라이언트에 상태를 전달하는 구조적 개선안 도출.
- **Result**: 단순 기능 구현을 넘어, 시스템 가용성과 통신 영속성을 고려한 설계의 중요성 체감.
---