# DAO DTO VO ENTITY

### DAO(Data Access Object)

- DAO는 DB의 data에 접근하기 위한 객체로 직접 DB에 접근하여 데이터를 삽입, 삭제, 조회 등 조작할 수 있는 기능을 수행한다.

- DataBase 접근을 하기 위한 로직과 비지니스 로직을 분리하기 위해 사용한다.


### DTO(Data Transfer Object)

- DTO는 로직을 가지지 않는 데이터 객체이고 getter/setter메소드만 가진 클래스를 의미한다.

- DTO(Data Transfer Object)는 데이터 전송(이동) 객체라는 의미를 가지고 있다.

- DTO는 주로 비동기 처리를 할 때 사용한다.

- 계층간 데이터 교환을 위한 객체(Java Beans)이다.

### VO(Value Object)

- DTO와 달리 VO는 Read-Only속성을 값 오브젝트이다.

- 자바에서 단순히 값 타입을 표현하기 위해 불변 클래스(Read-Only)를 만들어 사용한다.

- 예를 들면 빨강은 Color.RED, 초록은 Color.GREEN 이렇게 단순히 값만 표현하기 위해 getter기능만 존재한다.

- VO 내부에 선언된 속성(필드)의 모든 값들이 VO 객체마다 값이 같아야, 똑같은 객체라고 판별한다.

### Entity

- 실제 Database 테이블과 1 : 1로 Mapping 되는 클래스
- DB의 테이블내에 존재하는 컬럼만을 속성(필드)으로 가져야 한다.
- 상속을 받거나 구현체여서는 안된다.
- 테이블내에 존재하지 않는 컬럼을 가져서도 안된다
