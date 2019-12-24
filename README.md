# JAVA-SPRING
자바, 스프링 공부
## JAVA
### Singleton pattern
- 하나만 존재해야하는 객체를 만들때 사용
- instance 를 저장할 static 변수 하나 선언
- new instance
- getInstance 로 객체 주소값 리턴
- 이러한 방식으로 객체를받는 예 -> 캘린더(날짜는 딱 하나만 존재해야함)


### Factory Method Pattern
- 객체간 연관성을 줄일려고 쓰는것 같음
- 아직 잘 모르겠음

### Templete Method Pattern
- 객체의 흐름은 이미 정의되어 있음, 구현만 각자 알아서 해서 사용
- 추상클래스 안에 공통적인 부분은 일반 메서드로 구현하고 하위클래스 마다 다른 기능은 추상메서드를 활용하여 선언
- 하위 클래스는 시나리오대로 구현만 할 뿐
- 프레임워크의 개념을 몰랐는데 비슷한 개념임

### Strategy Pattern
- 인터페이스를 활용하면 다양한 정책이나 알고리즘을 프로그램은 큰 수정없이 적용 확장 할 수 있음

### 상속
- A : 부모객체, B : 자식객체
- A a = new B() => 업캐스팅 가능
- 힙 메모리 구조는 부모객체 생성자가 먼저 호출되어 할당되고 자식객체 생성자가 호출되어 할당
- a.method() : 재정의 된 메서드는 b 메서드 호출, 재정의 안된 메서드는 a 메서드 호출
- 하나의 메서드는 고유한 주소를 가짐, 동일한 이름의 메서드는 존재할수 없음(오버로딩은 이름이 조금씩 바뀜)
- 오버라이딩시 가상함수로 새로운 주소로 할당

- IS-A 관계 : 동물 >>> 사람 >>> 호랑이, 추상적인것이 구체화되는경우
- HAS-A 관계 : 학생 >>> 과목, 객체가 객체를 소유한경우

### 다형성
- 동물클래스에서 사람, 호랑이, 새 클래스를 상속한경우 자료형을 동물 인스턴스를 사람, 호랑이, 새 로하면 하나의 자료형으로 다른 결과를 얻어 낼 수 있음으로 다형성이다.
- 다형성이 있음으로서의 장점 : 사람 호랑이 새 인스턴스를 동물이라는 자료형 하나로 다룰 수 있다, 만약 다형성이 없다면 우리는 매서드 안에 수많은 if 문을 사용하여 인스턴스를 구분해야 할것이다.

### 다운캐스팅
- 업캐스팅한 인스턴스를 다시 다운캐스팅 할 수 있음
- instanceof 키워드를 사용하는것이 바람직 ex> if(animal instanceof human){ Human human = (Human)animal; human.readBooks();}
- 다운캐스팅은 오버라이딩이 불가피한경우 사용하는것이 좋다

### static
- 공유의 개념, 메모리를 중복해서 할당하지 않고 같은 주소를 참조함

### final
- 변수 : 값이 변하지 않음
- 메서드 : 오버라이딩 불가
- 클래스 : 상속 불가능

### interface
- 인터페이스는 명세다
- JDBC를 예로 들면, 자바에서 Connection 이라는 인터페이스를 만들어 놓으면 Oracle, Mysql, MongoDB등 이런 회사에서 자기 디비에 맞는 코드로 인터페이스를 구현하고 클라이언트들은 그냥 그 내부적인 소스를 이해하고 사용하는게 아니라 자바가 선언한 인터페이스만을 보고 사용하는거임.
- 설계에서 아주 중요한 개념, 추상클래스와의 차이는 명세, 그리고 모든 메소드가 다 추상메소드 라는점(추상클래스는 일부만 추상 메소드)
- 인터페이스에서의 변수는 상수에 해당한다
