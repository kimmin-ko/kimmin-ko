# GitHub 활동 기록 (자동 갱신)

이 README는 개인 소개 없이 오로지 GitHub 활동(커밋·PR·기여)만 집중적으로 보여주도록 설계되었습니다.
아래 섹션은 자동화 스크립트와 워크플로를 통해 정기적으로 갱신됩니다.

---

## 실시간 위젯
아래 위젯을 사용하면 프로필 통계와 활동 그래프를 시각적으로 노출할 수 있습니다.

- GitHub Readme Stats
```md
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=kimmin-ko&show_icons=true&theme=tokyonight)
```

- 커밋 활동 그래프
```md
![Activity Graph](https://activity-graph.herokuapp.com/graph?username=kimmin-ko&theme=react-dark)
```

- Streak / 연속 활동
```md
![Streak](https://github-readme-streak-stats.herokuapp.com/?user=kimmin-ko&theme=dark)
```

---

## 최근 주요 커밋 (자동 갱신)
아래 목록은 스크립트가 자동으로 갱신합니다. (최신 커밋 → 오래된 순, 최대 20개)

<!--START_ACTIVITY-->
- 이 섹션은 자동으로 업데이트됩니다. 스크립트와 워크플로가 설정되면 최신 커밋 목록이 들어옵니다.
<!--END_ACTIVITY-->

---

## 자동 갱신 설정 개요
1. scripts/update-activity.js — GitHub API로 사용자 커밋을 수집해 README의 위 마커(<!--START_ACTIVITY--> / <!--END_ACTIVITY-->) 사이를 대체합니다.
2. .github/workflows/update-activity.yml — 매일(또는 수동) 실행되어 README를 갱신하고 변경 사항을 푸시합니다.

설정 방법
1. 리포지토리에 `scripts/update-activity.js`와 `.github/workflows/update-activity.yml`를 추가하세요.
2. workflow는 기본 제공되는 `GITHUB_TOKEN`으로 커밋/푸시합니다(권한이 필요할 경우 Settings → Actions → Workflow permissions 확인).
3. 필요 시 스크립트의 `ACTIVITY_USERNAME` 변수(기본: kimmin-ko)와 출력 개수(limit)를 조정하세요.

---

## 권장 커스터마이징
- 공개 레포만 포함하거나, 특정 레포(예: 작업중인 개인 레포) 제외 필터를 적용할 수 있습니다.
- 출력 포맷(날짜 형식, 항목 수, 메시지 길이)을 수정할 수 있습니다.
- 대표 커밋 대신 PR 목록을 보이도록 변경도 가능합니다.
