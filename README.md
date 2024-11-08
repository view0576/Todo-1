### [Spring 7기] CH 3 일정 관리 앱 만들기

## 1. API 설계


| API | Method| URL | request | response | 응답코드 |
| --- | --- | --- |  --- |  --- |  --- | 
| 일정생성 | Post | /api/todos | {"title": "string","userName": "string","contents": "string","userId":"string","password": "string"}| {"id: 1, "title": "string","userName": "string","contents": "string","userId":"string","createdAt":"string",} | 200: 정상등록 400: Bad Request
| 일정단건조회 | Get |  /api/todos/{id} |-| {"id: 1, "title": "string","userName": "string","contents": "string","userId":"string","createdAt":"string","updatedAt": "string"} | 200: 정상조회 404: Not Found
| 전체일정조회 | Get |  /api/todos |-| {"id: 1, "title": "string","userName": "string","contents": "string","userId":"string","createdAt":"string","updatedAt": "string"} | 200: 정상조회
| 일정수정 | Put | /api/todos/{id} |{"title":"string","userName":"string","password":"string"| {"id: 1, "title": "string","userName": "string","contents": "string","userId":"string","createdAt":"string","updatedAt": "string"} | 200: 정상수정 400: Bad Request 404: Not Found
| 일정삭제 | Delet | /api/todos/{id} |{password":"string"}|-| 200: 정상삭제 404: Not Found

![todo](https://github.com/user-attachments/assets/e8e743fd-dc44-49cb-a587-596fac46f26d)

<details><summary>SQL 쿼리
</summary>
create table todos<br/> 
(title varchar(20), contents varchar(200), username varchar(10), <br/> password varchar(20), createat datetime, updateat datetime)
<br/> <br/> 
insert into todos<br/> 
values(..., ..., ...) <br/> <br/> 

select *<br/> 
from todos

select *<br/> 
from todos<br/> 
where id=1

delete from todos<br/> 
where id=1<br/> 

update todos <br/> 
set title= ... <br/> 
,userName= ... <br/> 
,contents= ... <br/> 
,userId= ... <br/> 
,password= ... <br/> 
where id=1 <br/> 


</details>
