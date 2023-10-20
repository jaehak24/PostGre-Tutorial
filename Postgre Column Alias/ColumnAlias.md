# column을 설정했는데 뭔가 이름이 마음에 안들어...
alias를 사용한다면 이 문제를 해결해준다. 다음 문장을 보면서 이해해보자.

>![Alt text](image.png)

이 구문을 실행할 경우 column_name으로 명명된 column은 alias_name으로 설정된다.

여기서 alias는 as라고 생각 하면 된다. 이 때, 또 alias의 특징이 하나 더 있는데, as를 다음과 같이 생략해도 해당 절은 문제없이 돌아간다.
![Alt text](image-3.png)

실습을 한번 해보자. 다음과 같이 성과 이름을 불러오는 SELECT절이 있다고 해보자.

<실습 테이블>

![Alt text](image-4.png)


![Alt text](image-1.png)

조금 더 격식 있는 형태로 성을 surname으로 바꾸고 싶다면 다음과 같이 절을 변경하면 된다.

![Alt text](image-2.png)

이 절이 시행된다면 테이블은 다음과 같이 바뀌게 된다.

![Alt text](image-5.png)

아까도 말했듯이, as를 생략할 수도 있다.

![Alt text](image-6.png)