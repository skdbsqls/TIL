# git revert

### git revert란?
특정 commit을 없었던 일로 만드는 작업

### revert 명령어
`git revert <commit id>`

### git revert의 작동 원리
- 재설정
- 단일 commit을 실행 취소 하는 것
- 프로젝트 기록에서 commit을 없었던 일로 처리 후 그 결과를 새로운 commit으로 추가함
- 특정 commit을 제거하고, 그 commit을 제거했음을 다시 commit으로 추가!
- 특정 commit에 있었던 일(변경 사항)만 사라지고, 특정 commit은 그대로 남겨짐~

### revert 주의사항
revert에서도 conflict가 생길 수 있음
- 1 commit에서 1 2 3
- 2 commit에서 같은 라인의 코드를 11 22 33으로 변경하고
- 1 commit을 지우려고 한다면 충돌 발생!

### revert 정리
- 변경 사항을 안전하게 실행 취소할 수 있도록 도와주는 순방향 실행 취소 작업
- commit 기록에서 커밋을 삭제하거나 분리하는 대신, 지정된 변경 사항을 반전시키는 새 commit을 생성
- git에서 기록이 손실되는 것을 방지하며 기록의 무결성과 협업의 신뢰성을 높임
