# git reset

### git reset이란?
특정 commit으로 되돌아가는 작업

### reset 명령어
`git reset [옵션] <commit id>`

### git reset의 작동 원리
- 되돌리기
- 시계를 마치 과거로 돌리는 듯한 행위
- 특정 commit으로 되돌아 갔을 때, 되돌아간 commit 이후의 커밋은 모두 삭제

### reset의 3가지 옵션
- `--soft`: 삭제된 commit의 기록을 staging area에 남김
- `--mixed`: 삭제된 commit의 기록을 working directory에 남김 (기본 옵션 값)
- `--hard`: 삭제된 commit의 기록을 남지기 않음

### reset 주의사항
- 강력한 명령어라  confilct도 일어나지 않음..
- push하기 전, 로컬에서 reset을 한다고 해서 원격에서 reset이 되는 것은 아님
- 즉, push가 된 커밋은 더 복잡한 과정을 거쳐야...