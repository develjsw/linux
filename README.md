## Linux 명령어
- 자주 잊어버리거나 사용되는 명령어
---
### [ Linux 공통 ]
- GIT
  - $ git checkout -- 파일명
    - git이 연결되어 있는 상태에서 특정 파일에 대한 수정된 내용을 취소하고 가장 최근의 커밋 내용으로 되돌리는데 사용
        ~~~
        EX)
        $ git checkout -- text.txt
        ~~~
      
- Vim 편집기
  - $ shift + v, 방향키/PageUp/PageDown
    - 라인 단위로 영역을 선택하여 여러 줄을 한 번에 선택 가능
    - 선택한 영역을 지우거나, 복사, 들여쓰기/내어쓰기 작업을 할 때 유용
        ~~~
        EX)
        shift + v  →  방향키로 여러 줄 선택  →  d(삭제)
        ~~~
- ETC
  - $ tr -d '[:space:]' < 파일명입력 > temp_file && mv temp_file 파일명입력
    - 파일에서 모든 공백(스페이스, 탭, 줄 바꿈 등) 제거 후, 그 결과를 원본 파일에 덮어 씌우는 명령어
        ~~~
        EX)
        $ tr -d '[:space:]' < db_secret_key > temp_file && mv temp_file db_secret_key       
        ~~~
---