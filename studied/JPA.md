# JPA
**Java Persistence API**  
자바 ORM의 표준 인터페이스  
자바 클래스와 DB테이블을 매핑한다. (sql매핑이 아니다)  

## ORM  
**Object Relational Mapping**  
객체와 RDBMS를 자동으로 매핑해주는 것  

객체지향 프로그램은 클래스를 사용하고, 관계형 DB는 테이블을 사용하는데, 연동 시 불일치가 생김.  
ORM을 통해 객체간의 관계를 바탕으로 **SQL을 자동으로 생성**해주어 불일치를 해결해준다.  

### 장점
- 객체 지향적인 코드 -> 코더들에게 직관적이고 구현이 편함  
- 재사용 및 유지보수 편리 -> MVC패턴에 유리하다  
- DBMS에 대한 종속성이 줄어든다 -> DB교체 시에도 적용이 빠르다  

### 단점
- ORM은 편하지만 튜닝이 어렵다. -> 프로젝트가 복잡할수록 설계가 어렵다.  

## JPA
자바 어플리케이션과 JDBC사이에서 동작  
JPA호출시 JPA가 JDBC API를 사용해 SQL을 호출하고, DB와 통신함.  
![../img/jpa_arch.png]  
[JPA with sql](./jpa_query.md)
[연관관계 매핑](./jpa_relation.md)

### 프로세스
1. 개발자가 조작을 원하는 객체의 정보를 JPA에게 넘겨준다.  
2. JPA는 엔티티 분석 후 적절한 SQL(INSERT, SELECT 등)을 생성하여 DB에 보낸다.  
3. JPA가 DB로부터 결과를 받아와 객체에 매핑한다.  


