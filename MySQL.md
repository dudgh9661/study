네이버 클라우드 플랫폼으로 만들어놓은 mysql서버에 원격 접속이 되지 않는 문제가 발생하였다.
아래 링크를 참조하여 my.cnf 설정값을 변경하였더니 해결되었다.

### 127.0.0.1로 설정되어 외부 접속이 차단되었던 것이 문제.

https://m.blog.naver.com/PostView.nhn?blogId=varkiry05&logNo=198610727&proxyReferer=https:%2F%2Fwww.google.com%2F


### foreign key가 설정되어 있는 table을 지우기 위해 

set foreign_key_checks=0; 
DROP table명 
set foreign_key_checks=1;

### 명령어를 적었다가 새로운 테이블을 만들 때 set foreign_key_checks=1;로 인하여 외래키가 생성이 안되는 오류가 발생. 

참고 자료 : https://c10106.tistory.com/4397
