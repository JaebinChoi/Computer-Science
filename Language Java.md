# Java

### JVM (Java Virtual Machine)
- Java와 OS 사이의 중계자 역할
- Java가 OS에 구애받지 않고 사용하게 해줌
- 메모리 관리, 가비지 컬렉션
- 스택 기반
---
### JVM을 알아야 하는 이유
#### 한정된 메모리를 효율적으로 관리하여 최고의 성능을 내기 위해
---
### 자바 프로그램 실행 과정
1. 프로그램을 실행하면 JVM이 OS로부터 프로그램에 필요한 메모리를 할당
2. 자바 컴파일러(Java Compiler)는 자바 소스파일(.java)을 읽어 자바 바이트코드(.class)로 변환
3. 클래스 로더는 자바 클래스 파일들을 JVM에 로딩
4. 실행 엔진(Execution Engine)은 로딩된 자바 클래스 파일들을 해석
5. 해석된 바이트코드는 메모리 영역에 배치, 수행
---
![image](https://user-images.githubusercontent.com/51224070/110293483-fa897f80-8031-11eb-8555-98ef8b9b109b.png)
---
### Java 메모리 영역
1. 스택
  - 데이터 임시 저장 영역
  - 지역 변수, 매개 변수
2. 메소드 (스태틱)
  - 초기화되는 대상 저장 영역
  - 전역 변수, static 변수, 바이트코드
3. 힙
  - 객체 저장 영역
  - new로 생성된 객체, 배열
---
### 가비지 컬렉션 (Garbage Collection)
#### 유효하지 않은 메모리를 정리해주는 프로그램 => 힙 메모리 재활용 가능
#### 프로그래머가 직접 메모리를 관리하지 않아도 됨 => 개발 속도 상승
---
### Vector VS ArrayList
#### Vector : 동기식, 한 스레드가 Vector 작업 중이면 다른 스레드는 작업 불가능
#### ArrayList : 비동기식, 여러 스레드가 ArrayList에서 동시 작업 가능
---
### String VS StringBuffer VS StringBuilder
#### String : 불변, 문자열을 수정하려면 다시 생성해야 함(new) => 문자열 연산이 많으면 비효율적
#### StringBuffer : 가변, 문자열 변경이 용이, 동기화 O, 멀티스레드 환경에 적합
#### StringBuilder : 가변, 동기화 지원 X, 멀티스레드 환경에 부적합 => 싱글스레드에서 StringBuffer보다 효율적
---
### 오버라이딩 (Overriding) VS 오버로딩 (Overloading)
#### 오버라이딩 : 부모 클래스에서 상속받은 메소드를 재정의 하는 것
#### 오버로딩 : 메소드 이름은 같고, 매개 변수는 다르게 해서 여러 메소드를 만드는 것
---
### 추상클래스 (Abstract Class) VS 인터페이스 (Interface)
#### 추상클래스 : extends를 통해 기능 이용, 확장
#### 인터페이스 : implements를 통해 다중 상속 가능, 모든 클래스를 구현해야 함
---
### 제네릭 (Generic)
#### 클래스 안에서 사용할 타입을 클래스 외부에서 설정하는 것
#### <> 안에는 참조자료형(Reference Type)만 가능
---
### 접근 지정자
- public : 모든 접근 허용
- protected : 상속 받은 메소드, 같은 패키지만 접근 허용
- default : 기본 제한자, 자신 클래스 내부, 같은 패키지만 접근 허용
- private : 외부 접근 불가능, 해당 클래스 내에서만 접근 허용
---
### 값에 의한 호출 (Call by Value) VS 참조에 의한 호출 (Call by Reference)
#### 값에 의한 호출 : 값을 복사해서 새로운 함수로 넘기는 호출 방식, 원본 값 변경 X
#### 참조에 의한 호출 : 주소 값을 인자로 전달하는 호출 방식, 원본 값 변경 O
---

### 기본형 타입 (Primitive Type) VS 참조형 타입 (Reference Type)
- 기본형 타입
  -  8개 (boolean, char, byte, short, int, long, float, double)
  -  사용 전 반드시 선언되어야 함
  -  비객체 타입 -> null을 가질 수 없음, null을 사용하고 싶으면 Wrapper Class 활용
  -  스택 메모리에 저장
- 참조형 타입
  - 힙 메모리에 저장
  - 빈 객체인 null을 가질 수 있음
  - 클래스(Class) 타입, 인터페이스(Interface) 타입, 배열(Array) 타입, 열거(Enum) 타입이 있음
