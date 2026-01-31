# 작업 히스토리 대시보드 - 이어서 할 작업

## 현재 상태
- ✅ 레포 생성 완료: https://github.com/junyoungjang976/work-history
- ✅ 대시보드 URL: https://junyoungjang976.github.io/work-history/
- ✅ GitHub Actions 워크플로우 설정 완료
- ✅ Public 레포 수집 작동 중
- ⏳ **Private 레포 접근 설정 필요**

## 남은 작업: PAT 설정

### 1. Personal Access Token 생성
1. https://github.com/settings/tokens?type=beta 접속
2. "Generate new token" 클릭
3. 설정:
   - Token name: `work-history-bot`
   - Expiration: 90 days
   - Repository access: "All repositories"
   - Permissions: Contents (Read), Metadata (Read)
4. 토큰 복사

### 2. Repository Secret 추가
1. https://github.com/junyoungjang976/work-history/settings/secrets/actions 접속
2. "New repository secret" 클릭
3. Name: `PAT_TOKEN`, Secret: 복사한 토큰
4. Add secret

### 3. 워크플로우 실행
```bash
gh workflow run update-history.yml --repo junyoungjang976/work-history
```

## 추적 대상 레포
- sales-pipeline, order-tracker, busung-as, field-check
- equipment-manager, call-manager
- busungtk-docs, portal, hvac-mentor

## 제외
- JND-dashboard-PM-, jnd-portal (JND 관련)
- work-history, oh-my-claudecode
