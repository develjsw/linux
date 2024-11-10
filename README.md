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
        $ shift + v  →  방향키로 여러 줄 선택  →  d(삭제)
        ~~~
  - $ shift + insert
    - 윈도우에서 복사한 내용을 vim에서 붙여넣기 할때 사용
        ~~~
        EX)
        $ shift + insert
        ~~~
- Docker
  - $ docker inspect < 컨테이너명입력 > | grep "< 키워드입력 >"
    - 특정 컨테이너의 키워드에 해당되는 모든 설정정보 JSON 형식으로 출력
        ~~~
        EX)
        $ docker inspect < 컨테이너명입력 > | grep "Env" -- = $ docker exec -it < 컨테이너명입력 > /bin/bash 후 $ env 입력 
        $ docker inspect < 컨테이너명입력 > | grep "NetworkSettings"
        $ docker inspect < 컨테이너명입력 > | grep "IPAddress"
        ~~~
- ETC
  - $ tr -d '[:space:]' < 파일명입력 > temp_file && mv temp_file 파일명입력
    - 파일에서 모든 공백(스페이스, 탭, 줄 바꿈 등) 제거 후, 그 결과를 원본 파일에 덮어 씌우는 명령어
        ~~~
        EX)
        $ tr -d '[:space:]' < db_secret_key > temp_file && mv temp_file db_secret_key       
        ~~~
  - $ find /< 경로입력 > -name "< 파일/폴더명입력 >"
    - 파일/폴더명 찾을 때 사용하는 명령어
        ~~~
        EX) 
        $ find /data/www -name "nest-api" -- nest-api 파일/폴더 찾기
        $ find /data/www -name "*api*" -- api라는 키워드가 들어간 파일/폴더 찾기
        $ find /data/www -iname "*api*" -- 대소문자 구분없이 api라는 키워드가 들어간 파일/폴더 찾기
        ~~~
  - $ grep "< 찾을문자열 >" /< 경로입력 >
    - 문자열 찾을 때 사용하는 명령어
        ~~~
        EX) 
        $ grep "failed" /var/log/* -- 해당경로 디렉토리 내에 모든 파일에서 특정 문자열 찾기
        $ grep -i "failed" /var/log/* -- 대소문자 구분없이 해당경로 디렉토리 내에 모든 파일에서 특정 문자열 찾기
        $ grep -r "failed" /var/log/* -- 하위 디렉토리를 포함하여 문자열 찾기
        ~~~
---