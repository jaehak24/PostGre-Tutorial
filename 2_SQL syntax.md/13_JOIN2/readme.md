### Right join

이전에 left 조인과 반대된다고 생각하면 된다. right 쪽에 있는 테이블을 기준으로 왼쪽에 테이블이 하나 붙는다고 생각하면 된다.

>SELECT<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    a,<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    fruit_a,<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    b,<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    fruit_b;<br>
FROM<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    basket_a<br>
RIGHT JOIN basket_b ON fruit_a = fruit_b;

![Alt text](image.png)

 출력 결괄르 보면 