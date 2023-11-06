# PostGre-Tutorial

Postgre SQL? 1996년 이름을 바꾸고 현재는 많은 분석 또는 웹 서비스에서 사용하고 있는 메인 데이터베이스로 사용되고 있다.

> 유닉스 베이스로 개발되었지만 현재는 IOS, Window, Solaris에서도 사요될 만큼 확장성을 높였다.

# PostGre의 활용 사례
1. LAPP stack에서 사용되는 안정성 높은 데이터베이스
LAPP(Linux, Apache, Postgre SQL, PHP) 로서 웹 서비스와 분석 서비스에서의 건장한 데이터베이스로서 동적으로 사용된다. 

2. <b>교환성 데이터베이스의 표준</b> :  많은 스타트업과 기업에서 데이터 거래가 이루어지는 데이터베이스를 사용할 때, postGre SQL을 <u>일반적</u>으로 사용하게 된다.

3. PostGIS(geographic Information system) System을 사용한다면 공간 데이터들을 활용할 수 있다.

<i>공간 데이터랑?(geographci data): 지도를 만들 때, 건물, 도로, 주소 같은 개념을 객체로 삼은 데이터를 일컫는다.</i>


#PostGRE 지원 언어
* python
* JAva
* C#
* C/C++
* Ruby
* Perl
* Javascript
* Go
* Tcl

# PostGre 주요 특징

* 사용자 정의 타입
* 테이블의 상속
* 복잡한 locking 메커니즘
* 외래 키를 참조하는 통합
* Views(포스트그레에서 테이블을 조회하는 방법), rules, subquery
* nested trasnsaction(transaction을 처리하는 와중에 transaction을 정의하는 기능)
* Multi-version concurrency control(동시에 여러개의 트랜스액션을 처리하는 기능) &rightarrow; MVCC
* Asynchronous replication(비동기 복제)

* native 윈도우 서버 버전에서도 사용할 수 있게 해줌
* TableSpace
* 깃처럼 한 시점에서 데이터를 복구해 줄 수 있는 기능

# 