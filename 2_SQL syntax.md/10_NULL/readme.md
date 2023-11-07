# ISNULL
value의 값이 null인지를 확이하는 syntax로 IS NULL이 있다.
해당 syntax의 사용은 다음과 같이 where 의 조건부 느낌으로 들어오게 됀다.

다음과 같이 Contact 테이블에서 연락처가 없는 사람의 행을 찾으려면 다음과 같이 쿼리문을 작성하면된다
>SELECT<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    first_name,<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    last_name,<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    email,<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    phone;<br>
FROM<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    contacts<br>
WHERE<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    phone <u><b>IS NULL;</u></b><br>

출력 결과>

![Alt text](image.png)

## IS NOT NULL
IS NULL 문도 다른 syntax들과 같이 부정문으로 들어와서 사용이 가능하다.
