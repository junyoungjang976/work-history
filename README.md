# busungtk-work-history

부성티케이 작업 히스토리 대시보드 — GitHub 활동을 자동 수집하여 시각화하는 정적 대시보드

## 기술 스택

| 항목 | 기술 |
|------|------|
| 프론트엔드 | 순수 HTML + Tailwind CSS (CDN) |
| 차트 | Chart.js (CDN) |
| 데이터 수집 | Python 3.11 + requests (GitHub API) |
| 자동화 | GitHub Actions (매일 09:00 KST) |
| 배포 | GitHub Pages |

## 주요 기능

- GitHub 생산성 대시보드 (커밋, PR, 이슈) — busungtk 전체 레포 대상
- 주간 목표 달성률 추적
- 작업 유형별 파이 차트
- 시간대별 활동 히트맵
- 레포별 커밋 타임라인 필터링

## 프로젝트 구조

```
index.html                — 대시보드 UI
data.json                 — 자동 생성된 GitHub 활동 데이터
scripts/fetch_activity.py — GitHub API 데이터 수집 스크립트
.github/workflows/        — 매일 자동 실행 + GitHub Pages 배포
```

## 사용법

```bash
# 데이터 수동 업데이트
GITHUB_TOKEN=xxx python scripts/fetch_activity.py

# 로컬 확인
open index.html
```

CI가 매일 자동으로 데이터를 수집하고 GitHub Pages에 배포합니다.
