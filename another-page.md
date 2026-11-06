---
layout: default
---

## 박사과정생 연구기록

[back](./)

---

## GitHub — 연구 프로젝트 (tsarkr)

GitHub 계정 [tsarkr](https://github.com/tsarkr)의 공개 저장소입니다. 설치와 사용법은 각 저장소의 README를 참고하세요.

| 저장소 | 언어 | 내용 |
|---|---|---|
| [D-CENT](https://github.com/tsarkr/D-CENT) | Python, PHP | 3·1운동 기록 기반 RAG 역사 서사 재구성 프레임워크 ([사이트](https://gyungmin.tsar.kr/D-CENT/)) |
| [darkstar](https://github.com/tsarkr/darkstar) | Rust | OWL 2 RL 온톨로지 편집기·추론 엔진 ([사이트](https://gyungmin.tsar.kr/darkstar/)) |
| [hexedit](https://github.com/tsarkr/hexedit) | TypeScript | 웹 기반 16진수 편집기 ([사이트](https://gyungmin.tsar.kr/hexedit/)) |
| [K-D-H](https://github.com/tsarkr/K-D-H) | Python | 「케이팝 데몬 헌터스」 유튜브 댓글 분석 |
| [k-heritage](https://github.com/tsarkr/k-heritage) | Python | 국가유산채널 유튜브 댓글 텍스트 마이닝 |
| [kci_scrape](https://github.com/tsarkr/kci_scrape) | Python | KCI 논문 수집, 연구 동향·공저 네트워크 분석 |
| [redditgo](https://github.com/tsarkr/redditgo) | Jupyter Notebook | Reddit 한·중·일 게시물 감정 분석 및 토픽 모델링 |
| [shortener_11e](https://github.com/tsarkr/shortener_11e) | PHP | URL 단축 서비스 ([11e.kr](https://11e.kr)) |

---

# D-CENT
[GitHub](https://github.com/tsarkr/D-CENT) | [Site](https://gyungmin.tsar.kr/D-CENT/)

Digital Contextualized Entity & Narrative Technology. 3·1운동 기록을 PostgreSQL, TEI, CIDOC-CRM, Neo4j로 연결하고, 질문마다 날짜가 있는 사건 서사를 기록 인용과 함께 재구성합니다.

- 데이터 구축: 원천 자료 → PostgreSQL/TEI → Neo4j 그래프. 인명 태깅(한자 독음 ruby), 인물사전(i815) 연계, CIDOC-CRM 매핑, 한국사 시소러스 연결
- 웹 도슨트: 그래프 조회, Text-to-Cypher, 하이브리드 기록 검색(BM25 + dense + cross-encoder), LLM 1회 호출로 서사 생성
- 평가: 벤치마크 구축, 시스템 비교, 역사 전문가 검증 및 블라인드 평가
- MCP 클라이언트용 읽기 전용 데이터베이스 도구 제공

English: A RAG-based research framework that links March First Movement records through PostgreSQL, TEI, CIDOC-CRM, and Neo4j and reconstructs dated narratives with citations to the records.

# Darkstar
[GitHub](https://github.com/tsarkr/darkstar) | [Site](https://gyungmin.tsar.kr/darkstar/)

Rust로 만든 OWL 2 RL 온톨로지 편집기이자 추론 엔진(Protégé 대안)입니다.

- Rayon 기반 병렬 Forward-chaining 추론과 추론 근거(Justification) 추적
- SPARQL 1.1(Oxigraph 구성요소 기반)과 Manchester Syntax DL Query
- 여러 레이아웃의 그래프 시각화, Turtle/RDF 소스 편집기, `owl:imports` 처리
- 네이티브 동적 플러그인(.dylib/.so/.dll) 로딩

English: A Rust-based OWL 2 RL ontology editor and inference engine with SPARQL/DL queries, inference explanations, dynamic plugins, and graph visualization.

# K-D-H (K-Pop Demon Hunters)
[GitHub](https://github.com/tsarkr/K-D-H)

유튜브 플레이리스트 댓글을 수집해 팬덤 반응을 분석합니다.

- 수집: YouTube Data API
- 분석: VADER 감정 분석, 키워드 동시출현 네트워크, BERTopic + UMAP 토픽 모델링(시드 고정)
- 결과: 감정 분포 도넛 차트, 주요 토픽 바 차트, 키워드 네트워크 그래프(Gephi용 GEXF)
- 관련 논문: [경계의 상상력, K-콘텐츠의 미래를 열다 (디아스포라연구 제19권 제2호)](./경계의%20상상력,%20K-콘텐츠의%20미래를%20열다.pdf)

English: Collects YouTube playlist comments and analyzes fandom reactions with VADER sentiment analysis, keyword co-occurrence networks, and BERTopic.

# K-Heritage
[GitHub](https://github.com/tsarkr/k-heritage)

국가유산채널(K-heritage.tv) 유튜브 댓글 분석

- 수집: YouTube API로 영상별 댓글 수집
- 분석: 자연어 처리 기반 텍스트 분석, 키워드 및 주제 추출
- 시각화: 분석 결과 그래프·차트
- 관련 논문: [텍스트마이닝을 이용한 국가유산채널 영상 콘텐츠 수용자 반응 분석 (미디어융합연구 제38집)](./텍스트마이닝을%20이용한%20국가유산채널%20영상콘텐츠%20수용자%20반응%20분석.pdf)

English: Comment analysis of the K-heritage.tv YouTube channel — comment collection, text mining, keyword and topic extraction, and visualization.

# KCI Scrape
[GitHub](https://github.com/tsarkr/kci_scrape)

KCI 논문 데이터를 수집해 "문화유산 큐레이션" 분야의 연구 동향과 저자 네트워크를 분석합니다.

- 논문 상세 정보 스크래핑(제목, 저자, 초록, 키워드, 발행년도)
- 키워드(예: AI/XR) 포함 논문의 연도별 비율 등 연구 동향 분석
- 공저 네트워크 및 기간별(2019년 이전/2020년 이후) 비교, 단독·공저 논문 수 비교

English: Scrapes KCI paper data and analyzes research trends and co-authorship networks in cultural heritage curation.

# RedditGo
[GitHub](https://github.com/tsarkr/redditgo)

Reddit의 한국·중국·일본 관련 게시물과 댓글을 대상으로 COVID-19 전후의 감정 변화를 비교합니다.

- 7가지 감정 분류(기쁨, 슬픔, 분노, 두려움, 혐오, 놀람, 중립)
- 토픽 모델링: SentenceTransformer + UMAP + HDBSCAN 기반 BERTopic
- TF-IDF 키워드 추출, 토픽·감정별 시각화

English: Sentiment analysis and BERTopic topic modeling of Korea/China/Japan-related Reddit posts and comments, comparing pre- and post-COVID-19 periods.

# Shortener 11e
[GitHub](https://github.com/tsarkr/shortener_11e) | [Service](https://11e.kr)

PHP 기반 URL 단축 서비스입니다. QR 코드 생성(endroid/qr-code)을 지원하며, 11e.kr에서 운영 중입니다. 다른 사이트에서 쓰려면 도메인과 광고(Kakao AdFit) 설정을 수정해야 합니다.

English: A PHP-based URL shortener with QR code generation, running at 11e.kr.

---

[back](./)
