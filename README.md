## About
백엔드/서버 개발자로서 기능 구현보다 기준과 검증을 먼저 정리하는 개발을 지향합니다.
팀 프로젝트에서는 서버 구조와 데이터 흐름을 책임지고, 예외·보안·운영 관점에서 안정적인 동작을 만드는 역할을 맡아왔습니다.

## Projects

### DON DO THAT
KB IT’s Your Life 교육 과정 최종 프로젝트로, 실제 은행 계좌를 연동해 지출 내역을 자동 수집·분류하고
과소비 분석과 절약 챌린지를 통해 소비 습관 형성을 돕는 핀테크 서비스입니다.

Links
- Server: https://github.com/bbaegi-six/dondothat-server
- Client: https://github.com/bbaegi-six/dondothat-client

My Role
- 백엔드 리드로 서버 아키텍처와 데이터 처리 흐름 설계
- CODEF API 연동을 통한 계좌·거래내역 수집 및 중복·누락 방지 로직 구현
- 키워드 기반 1차 분류와 LLM 기반 2차 분류를 결합한 지출 분류 구조 설계
- Redis Pub/Sub 기반 실시간 챌린지 채팅 구조 구현
- JWT(HttpOnly) 인증과 AES-256 암호화를 적용해 금융 데이터 보안 기준 정립
- API 명세, 예외 처리 기준, 운영 시나리오를 문서화해 팀 협업 기준으로 활용

Key Contributions
- LLM 호출 비용과 지연을 줄이기 위해 키워드 사전 + 배치 처리 구조를 설계
- 비동기 처리와 동시 요청 제한을 적용해 분류 안정성과 응답 속도 개선
- 챌린지 실패 시 채팅 자동 종료 구조로 서비스 집중도와 지속성 확보
- GitHub Actions 캐시 적용으로 Docker 빌드 시간 10분 → 2~3분 단축

Tech Stack
- Backend: Java 17, Spring Framework, MyBatis
- LLM: FastAPI, GPT-4o, asyncio
- DB / Cache: MySQL, Redis
- Real-time: Spring WebSocket, STOMP
- Auth / Security: Spring Security, OAuth2, JWT(HttpOnly), AES-256
- Infra / CI: Docker, Docker Compose, Nginx, AWS EC2, GitHub Actions
