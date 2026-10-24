---
layout: default
---

## 박사과정생 연구기록

[back](./)

---

## GitHub — 주요 프로젝트 (tsarkr)

다음은 GitHub 계정 `tsarkr`의 주요 저장소입니다. 각 링크의 README를 참고하면 설치 및 사용법을 확인할 수 있습니다.

- [shortener_11e](https://github.com/tsarkr/shortener_11e) — PHP 기반 URL 단축기(11e.kr). 간단한 리다이렉트 및 통계 기능 제공.
- [k-heritage](https://github.com/tsarkr/k-heritage) — 국가유산 채널 댓글 텍스트 마이닝 및 분석 파이프라인.
- [redditgo](https://github.com/tsarkr/redditgo) — 한국어·중국어·일본어 Reddit 데이터 수집 및 감성 분석 도구.
- [kci_scrape](https://github.com/tsarkr/kci_scrape) — KCI 논문 메타데이터 스크래핑 및 공저 네트워크 시각화 스크립트.
- [K-D-H](https://github.com/tsarkr/K-D-H) — K-pop 관련 데이터 분석 및 실험 프로젝트.
- [D-CENT](https://github.com/tsarkr/D-CENT) — 3·1운동 기록을 PostgreSQL, TEI, CIDOC-CRM, Neo4j로 연결하고 질문별 역사 서사를 재구성하는 연구 프레임워크.
- [darkstar](https://github.com/tsarkr/darkstar) — Rust 기반 전문 OWL 2 RL 온톨로지 편집기이자 추론 엔진.

원하시면 특정 저장소의 요약이나 사용 예시, README 주요 내용을 더 추가해드리겠습니다.
 
English — GitHub project highlights
- `shortener_11e` — PHP-based URL shortener powering 11e.kr; simple redirect and demo analytics.
- `k-heritage` — YouTube comment text-mining and analysis pipeline for the K-Heritage channel.
- `redditgo` — Reddit data collection and multilingual sentiment analysis toolkit (KR/JP/CN).
- `kci_scrape` — Scrapers for KCI metadata and co-authorship network visualization scripts.
- `K-D-H` — K-pop related analysis and experimental datasets.
- `D-CENT` — Digital Contextualized Entity & Narrative Technology, a research framework that connects March First Movement records through PostgreSQL, TEI, CIDOC-CRM, and Neo4j to reconstruct dated narratives.
- `darkstar` — A professional Rust-based OWL 2 RL ontology editor and inference engine with SPARQL/DL queries, explanation tools, plugin support, and graph visualization.


# Shortener 11e
[Short URL service](https://11e.kr)

Shortener 11e is a URL shortening service initially developed with ChatGPT and enhanced with GitHub Copilot.
It provides a service that converts long URLs into shorter, memorable links.

Features
- 간단한 단축 URL 생성 및 리다이렉트
- 커스텀 키 지정(중복 검사 포함)
- 간단한 방문 통계(클릭 수, 생성일)
- 보안: 입력 URL 검증 및 악성 URL 차단(기본 수준)

Tech / Deployment
- 구현: (예) Flask 또는 FastAPI 기반 API, SQLite 또는 간단한 Key-Value 스토어
- 배포: Heroku, Netlify Functions, 또는 간단한 VPS에 컨테이너 배포 가능

English summary
- Shortener 11e is a lightweight URL shortening service that creates short redirects for long URLs.
- Features: short URL creation and redirect, custom key support with collision checks, basic visit statistics (click counts, creation date), and basic URL validation/security checks.

English tech notes
- Implementation: Example implementations use Flask or FastAPI with SQLite or a simple key-value store.
- Deployment: Can be deployed to Heroku, Netlify Functions, or a containerized VPS for a simple demo or production use.


# K-Heritage
[K-Heritage](https://github.com/tsarkr/k-heritage)

Comment Analysis of the K-heritage.tv YouTube Channel

[텍스트마이닝을 이용한 국가유산채널 영상콘텐츠 수용자 반응 분석.pdf](https://tsarkr.github.io/텍스트마이닝을%20이용한%20국가유산채널%20영상콘텐츠%20수용자%20반응%20분석.pdf)

Project Notes
- 목적: 국가유산 채널의 댓글을 통해 시청자 반응(감성, 관심사, 피드백 유형)을 파악합니다.
- 데이터: 채널 영상별 댓글 수집 및 전처리(불용어 제거, 형태소 분석 등).
- 분석기법: 감성분석, 토픽모델링, 빈도 기반 키워드 분석.
- 산출물: 논문 및 리포트, 재현 가능한 분석 파이프라인(스크립트 포함).

English summary
- Purpose: Analyze audience reactions (sentiment, interests, feedback types) from comments on the national heritage channel.
- Data: Collected and preprocessed comments per video (stopword removal, morphological analysis).
- Methods: Sentiment analysis, topic modeling, and frequency-based keyword analysis.
- Deliverables: Academic paper and reports, along with reproducible analysis pipelines and scripts.


# RedditGo
[RedditGo](https://github.com/tsarkr/redditgo)

**RedditGo** is a project that gathers posts and comments from Korean, Chinese, and Japanese communities on Reddit,  
providing a multifaceted analysis of sentiment changes during the COVID-19 pandemic.

- **Multi-language Support**: Focused on Korean, Chinese, and Japanese sentiment analysis
- **Sentiment Shift Detection**: Compares pre-/post-data to track emotional trends
- **Extensibility**: Easily integrate additional languages or modules for enhanced functionality

Notes
- 데이터 수집: Reddit API(PRAW 등)로 서브레딧별 게시글/댓글 수집 및 언어별 필터링
- 전처리: 언어별 토크나이저/형태소분석기(예: KoNLPy, Jieba, MeCab) 적용
- 분석: 시계열 감성 추적, 이벤트 기반 변화 탐지(예: 주요 뉴스·정책 발표 전후)
- 확장 아이디어: 시각화 대시보드, 경향 알림(임계값 기반), 추가 언어 지원

English notes
- Data collection: Use Reddit API (PRAW or equivalent) to collect posts and comments per subreddit with language filtering.
- Preprocessing: Apply language-specific tokenizers and morphological analyzers (e.g., KoNLPy, Jieba, MeCab).
- Analysis: Track sentiment time series and detect event-driven changes (e.g., before/after major news or policy announcements).
- Extensions: Visualization dashboards, trend alerts (threshold-based), and support for additional languages.

---

[back](./)