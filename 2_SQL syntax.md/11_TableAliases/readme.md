# Table aliases
테이블 이름이 안에 있는 데이터를 위해서 길게 작성돼었다면  aliases를 사용해서, 다음과 같이 간편하게 사용할 수 있다.

> 다음과 같이 긴 이름이 있다고 가정해 보면,
> #### a_very_long_table_name
>  해당 테이블의 컬럼을 다음과 같이 불러오기보다는
> #### a_very_long_table_name.column_1
> #### a_very_long_table_name as table 
> 같이 별칭을 지어준 후 호출하는 것이 확장성면이나 편이성에서 용이하다.
> #### table.column1

이전에 aliases를 배웠다면 as는 생략이 가능하다는 것을 배웠을 거시앋.

## table aliases의 사용예제

### 1. 긴 이름의 테이블일 경우 aliases를 사용해서 가독성 있게 쿼리문을 작성 가능

### 2. JOIN을 사용할 떄 aliases를 사용해서 가능케 할 수 있다.
일반적으로, 같은 이름의 컬럼을 가지고 있는 테이블들이 많을 경우 그 테이블을 JOIN 시켜준다.
보통 컬럼 이름이 같을 경우 테이블명에서 별칭을 주어 syntax 오류를 피할 수 있다.

>SELECT<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c.customer_id,<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;first_name,<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;amount,<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;payment_date<br>
FROM<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;customer c<br>
INNER JOIN payment p <br> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ON <u>p.customer_id = c.customer_id</u><br>
ORDER BY <br>
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;payment_date DESC;<br>

다음 쿼리문을 보면 customer_id가 customer과 payment 테이블에 같은 이름의 컬럼으로 존재하게 되는데, 이를 JOIN에서 테이블명 없이 사용하게 된다면 오류가 뜰 것이 자명하다. 그렇기 때문에 customer 테이블을 c로 alias로 두고 payment를 p로 별칭을 두어 INNER JOIN 해서 syntax 오류를 회피할 수 있다.

### 3.SELF-JOIN 구문에서 사용
자기 스스로에게 JOIN을 사용할 때 별칭을 두어, 쿼리문에 두 개의 같은 컬러명이 나와  syntax 오류가 나오는 것을 피할 수 있다. 
>SELECT<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;e.first_name employee,<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;m .first_name manager<br>
FROM<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<u>employee e</u><br>
INNER JOIN <u>employee m</u> <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ON <u>m.employee_id = e.manager_id</u><br>
ORDER BY manager;

employee 테이블을 m으로 별칭을 두어 employee를 id를 기준으로 INNER JOIN 시키는 쿼리문