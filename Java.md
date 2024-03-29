# Java
## Java의 장단점

- 장점
    - 운영체제에 독립적
        - JVM에서 동작하기 때문에 플랫폼에 종속적이지 않다.
    - 객체지향 언어로
        - 캡슐화, 상속, 추상화, 다형성 등을 지원하여 객체 지향 프로그래밍이 가능
    - 동적 로딩을 지원
        - 애플리케이션이 실행될 때 모든 객체가 생성되지 않고, 각 객체가 필요한 시점에 클래스를 동적 로딩해서 생성된다. 또한 유지보수 시 해당 클래스만 수정하면 되기 때문에 전체 애플리케이션을 다시 컴파일할 필요가 없다. 따라서 유지보수가 쉽고 빠르다.
- 단점
    - 비교적 느림
        - 한번의 컴파일링으로 실행 가능한 기계어가 만들어지지 않고 JVM에 의해 기계어로 번역되고 실행되는 과정을 거치기 때문에 조금 느리다.

## OOP 의 4가지 특징은 무엇인가요?

객체 지향 프로그래밍이란 

**프로그램 구현에 필요한 객체를 파악하고 객체들 간의 상호작용을 통해 프로그램을 만드는 것** 을 말한다.

- 캡슐화
    - 정보 은닉 : 필요 없는 정보는 외부에서 접근하지 못하도록 제한
    - 높은 응집도, 낮은 결합도로 유연함과 유지보수성 증가
- 추상화
    - 사물들의 공통적인 특징을 파악해서 하나의 개념(집합)으로 다루는 것
    - 목적과 관련이 없는 부분을 제거하여 필요한 부분만을 표현하기 위한 개념
- 상속
    - 기존 상위클래스에 근거하여 새롭게 클래스와 행위를 정의할 수 있게 도와주는 개념
- 다형성
    - **형태가 같은데 다른 기능을 하는 것을 의미**
    - 오버라이딩, 오버로딩

## OOP의 5대 원칙 (SOLID)에 대해서 설명해주세요.

- S : 단일 책임 원칙(Single Responsible Principle)
    - 객체는 단 하나의 책임만을 가져야한다.
    - 어떤 변화에 의해 클래스를 변경해야 하는 이유는 오직 하나뿐이어야 한다.
- O : 개방 폐쇄 원칙(Open Closed Principle)
    - 확장에는 열려(Open) 있으나, 변경에는 닫혀(Closed)있어야 한다.
    - 기존 코드를 변경하지 않으면서 기능을 추가할 수 있도록 설계되어야 한다.
- L : 리스코프 치환 원칙
    - 자식 클래스는 최소한 자신의 부모 클래스에서 가능한 행위는 수행할 수 있어야한다.
    - 부모 클래스를 카리키는 포인터에 해당 클래스를 상속하는 자식 클래스를 할당하더라도 모든 기능이 정상적으로 작동해야 하며자식 클래스의 상세 내부를 부모 클래스는 알 필요가 없다는 뜻입니다
- I : 인터페이스 분리 원칙
    - 특정 클라이언트를 위한 인터페이스 여러 개가 범용 인터페이스 하나보다 낫다.
    - 인터페이스가 명확해지고, 대체 가능성이 높아진다.
- D : 의존관계 역전 원칙 (Dependency Inversion Principle)
    - 의존 관계를 맺을 때 변화하기 쉬운 것 또는 자주 변화하는 것보다는 변화하기 어려운 것, 거의 변화가 없는 것에 의존하라는 것이다.
    - 쉽게 이야기하면, 구현 클래스에 의존하지 말고, 인터페이스에 의존하라는 뜻

## 객체 지향 프로그래밍 vs 절차 지향 프로그래밍

- 절차 지향 프로그래밍
    - 실행하고자 하는 절차를 정하고, 순차적으로 프로그래밍 하는 방식으로 빠르다.
    - 엄격하게 순서가 정해져 있기에 비효율적이고 유지보수가 어렵다.
    - 목적을 달성하기 위한 일의 흐름에 중점을 둔다.
- 객체 지향 프로그래밍
    - 객체를 만들고 객체들 간의 상호작용을 통해 로직을 구성하는 프로그래밍하는 방식으로 상속, 다형성, 추상화, 캡슐화를 통해 결합도를 낮추고 응집도를 높일 수 있으며 코드의 재사용성도 높일 수 있다.

## JVM 구성요소

JVM : 시스템 메모리를 관리하면서, 자바 기반 애플리케이션을 위해 이식 가능한 실행 환경을 제공함

- 자바 프로그램을 실행하는 역할
    - 컴파일러를 통해 바이트 코드로 변환된 파일을 JVM에 로딩하여 실행
- Class Loader : JVM 내(Runtime Data Area)로 Class 파일을 로드하고 링크
- Execution Engine : 메모리(Runtime Data Area)에 적재된 클래스들을 기계어로 변경해 실행
- Garbage Collector : 힙 메모리에서 참조되지 않는 개체들 제거
- Runtime Data Area : 자바 프로그램을 실행할 때, 데이터를 저장


### JVM 실행 과정
![JVM](https://user-images.githubusercontent.com/47858282/225517496-f976b76a-bd55-4557-a8f5-8ba5b9b91ace.png)
1. JVM은 OS로부터 메모리(Runtime Data Area)를 할당 받음
2. 컴파일러(javac)가 자바 소스코드(.java)를 읽어 바이트 코드(.class)로 변환
3. Class Loader를 통해 Class파일을 JVM내 JVM 메모리 영역(Runtime Data Area)로 로딩
4. 로딩된 Class 파일을 Execution Engine을 통해 해석 및 실행

### JVM 메모리(Runtime Data Area) 구조
![jvm_ele](https://user-images.githubusercontent.com/47858282/225517625-197d498d-a186-4e83-a982-4fbcbb96844f.png)
- 메서드(static) 영역
    - 클래스가 사용되면 해당 클래스의 파일(.class)을 읽어들여, 클래스에 대한 정보(바이트 코드)를 메서드 영역에 저장
    - 클래스와 인터페이스, 메서드, 필드, static 변수, final 변수 등이 저장되는 영역입니다.
- JVM 힙 영역
    - 런타임 시 동적으로 할당하여 사용하는 영역
    - new 연산자로 생성된 객체와 배열 저장
    - 참조가 없는 객체는 GC(가비지 컬렉터)의 대상
- JVM 스택 영역
    - 스레드마다 존재하여 스레드가 시작할 때마다 할당
    - 지역변수, 매개변수, 연산 중 발생하는 임시 데이터 저장
    - 메서드 호출 시마다 개별적 스택 생성
- pc register
    - 쓰레드가 현재 실행할 스택 프레임의 주소를 저장
- Native Method Stack
    - C/C++ 등의 Low level 코드를 실행하는 스택

## Java의 가비지 컬렉션(Garbage Collection) 처리 방법

가비지 컬렉션

가비지 컬렉터:**동적으로 할당한 메모리 영역 중 사용하지 않는 영역을 탐지하여 해제하는 역할**

**실행순서**
: 참조되지 않은 객체들을 탐색 후 삭제 → 삭제된 객체의 메모리 반환 → 힙 메모리 재사용


## string vs char

Char은 내용물이 1개인 문자로 제한되는 반면에 String은 문자열을 담을 수 있다.

Char의 경우 변수 안에 직접적으로 문자를 가지고 있지만 String은 reference 타입으로 실질적인 문자열이 아니라 주소값을 가지고 있다.

이 때문에 비교 방식에 차이가 있다.

Char의 경우 값이 같다면 ==(동일성) 비교를 사용할 수 있지만, String의 경우 내용이 같더라도 생성되는 주소가 다르기 때문에 == 비교를 사용하면 다른 결과가 나오게 되고 equals를 사용해야 한다.


## == 과 equals (동일성과 동등성)

- ==
    - 참조 비교로 두 객체가 같은 메모리 공간을 가리키는지 확인
- equals
    - 두 객체의 내부 값이 같은지 내용을 비교한다.
    - 기본 타입(Primitive Type)에 대해서는 적용할 수 없다.
    - 객체 비교시 override해서 원하는 방식으로 수정할 수 있다.


## 데이터 타입에 대해서 설명해주세요.

- 기본형과 참조형의 차이점
- Value Type
    - **기본 Primitive 타입으로 int, char 등이 있다.**
    - 기본 타입의 크기가 작고 고정적이기 때문에 **메모리 Stack 영역** 에 저장된다.
    - 정수형 : byte, short, int, long
    - 실수형 : float, double
    - 논리형 : boolean
    - 문자형 : char
- 참조 타입(Reference Type)
    - **기본형을 제외하고는 모두 참조형이다.**
    - String과 박싱 타입인 Integer 등이 있다.
    - 참조 타입은 데이터의 크기가 가변적이고, 동적이므로**Heap 영역**에서 관리된다.
    - **데이터는 Heap 영역에서 관리되지만 메모리의 주소값은 Stack 영역에 담긴다.**
    - new 키워드를 이용해 객체를 생성하여 데이터가 생성된**주소를 참조하는 타입**
    - String과 배열은 일반적인 참조 타입과 달리 new 없이 생성 가능하지만 참조타입이다.
    - 더이상 참조하는 변수가 없을 때 GC에 의해 삭제된다.

## call by value vs call by reference

- Call By Value(값에 의한 호출)
    - 함수 호출 시 인자로 전달되는**변수의 값을 복사하여 함수의 인자로 전달**한다.
    - 따라서,**함수 안에서 인자의 값이 변경되어도, 외부의 변수의 값은 변경되지 않는다.**
- Call by Reference(참조에 의한 호출)
    - **함수 호출 시 인자로 전달되는 변수의 레퍼런스를 전달한다.**
    - 따라서 **함수 안에서 인자의 값이 변경되면, 인자로 전달된 변수의 값도 함께 변경된다.**

자바는 새롭게 지역 변수(다른 주소)를 만들어서 값만 복사하고 할당한다. 따라서 자바는 Call By Value에 해당한다.

자바의 경우 해당 객체의 주소 값을 그대로 넘기는게 아닌 객체를 보는 또다른 주소값을 만들어서 넘긴다.


## 박싱, 언박싱 (wrapper class)

wrapper class: 데이터를 객체로 표현해야 할 때 쓰이는 것

래퍼 클래스는 산술 연산을 위해 정의된 클래스가 아니므로,**인스턴스에 저장된 값을 변경할 수 없다.** 단지, 값을 참조하기 위해 새로운 인스턴스를 생성하고, 생성된 인스턴스의 값만을 참조할 수 있다.기본 타입을 래퍼클래스의 인스턴스로 변환하는 과정을 **박싱**, 래퍼클래스의 인스턴스에 저장된 값을 다시 기본 타입으로 꺼내는 과정은 **언박싱** 이라고 한다.

## Java의 non-static 멤버와 static 멤버의 차이는?

- Java의 main 메서드가 static인 이유

  클래스가 메모리에 올라갈 때 정적 메소드가 자동적으로 생성됩니다. 그렇기에 **정적 메소드는 인스턴스를 생성하지 않아도 호출**
  을 할 수 있습니다.

- non-static
    - 공간적 특성
        - 객체마다 별도로 존재하고 인스턴스 변수라고 부른다.
    - 시간적 특성
        - 객체와 생명주기가 동일하다.
- static
    - 공간적 특성
        - **클래스당 하나만 생성된다.**
        - **동일한 클래스의 모든 객체들에 의해 공유된다.**
    - 시간적 특성
        - 객체가 생기기 전에 이미 생성되어 객체를 생성하지 않아도 사용 가능하다.
        - 객체가 사라져도 사라지지 않는다.
        - 프로그램 종료시에 사라진다.

## Mutable 객체와 Immutable 객체의 차이점에 대해 설명해주세요.

Mutable 객체는 변경 가능 객체이고, Immutable 객체는 불변 객체라고 흔히들 말합니다.

Immutable

- multi-thread 환경에서 동기화 처리 없이 객체를 공유 가능하다.(쓰레드에 안전하다 라고함)

Mutable

- multi-thread 환경에서 사용하려면 별도의 동기화 처리를 해줘야한다.


## final vs finally vs finalize

- final 키워드
    - 변수, 메서드, 클래스가 **변경 불가능**하도록 만든다.
    - 기본 타입 변수에 적용 시
        - 해당 변수의 값 변경 불가능하다.
    - 참조 변수에 적용 시
        - 참조 변수가 힙 내의 다른 객체를 가리키도록 변경할 수 없다.(final Person같이 객체를 생성할 때, 어떤 값이 변경이 불가능 한걸까? 안에 내부 변수를 변경할 수 있을까?)
    - 메서드에 적용 시
        - 해당 메서드를 오버라이드할 수 없다.(오버로딩은 가능)
    - 클래스에 적용 시
        - 해당 클래스를 상속 받아서 사용할 수 없다.
- finally 키워드
    - try catch 블록 뒤에서 항상 실행될 코드 블록을 정의하기 위해 사용한다.
- finalize 메서드
    - 가비지 컬렉터가 더 이상의 참조하지 않는 객체,배열을 메모리에서 삭제하겠다고 결정하는 순간 호출된다.
    - 시점은 알 수 없다.

## try with resources

자바 7 이전에는 try-catch-finally에서 리소스의 생성을 try 구문에서 리소스의 반납은 finally 구문에서 하다보니 실수가 발생할 여지가 있었다.

자바 7 이후에는 try with resources 구문이 나오게 됬는데 try 옆 괄호 안에서 리소스를 생성해주면 따로 반납하지 않아도 리소스를 자동으로 반납해주게 된다.

아래와 같이 작성한 것이 try with resources 구문이고, 만약 try-catch-finally를 사용했다면 finally 구문에서 scanner을 close하는 내용이 있어야 한다.

`public class ResourceClose {
public static void main(String[] args) {
try (Scanner scanner = new Scanner(new File("input.txt"))) {
System.out.println(scanner.nextLine());
} catch (FileNotFoundException e) {
e.printStackTrace();
}
}
}`

## 제네릭은 무엇인가요?

- **클래스나 메서드 내부에서 지정하는 것이 아닌 외부에서 사용자에 의해 지정되는 것을 의미**
  한다. 한마디로 특정(Specific) 타입을 미리 지정해주는 것이 아닌 필요에 의해 지정할 수 있도록 하는 일반(Generic) 타입
- 잘못된 타입이 들어올 수 있는 것을 컴파일 단계에서 방지할 수 있다.
- 불필요한 타입 변환을 제거할 수 있다.
- 컴파일 시점에 검사되어 타입 변환된다.

## 오버로딩, 오버라이딩

- 오버로딩
    - 두 메서드가 같은 이름을 갖고 있으나 인자의 수나 자료형이 다른 경우
    - 리턴타입은 상관이 없다.
- 오버라이딩
    - 하위 클래스에서 상위 클래스의 메서드와 일치하는 함수를 재정의하는 것

## 추상 클래스 vs 인터페이스
- 추상 메서드
    - abstract 키워드와 함께 원형만 선언되고 코드는 작성하지 않은 메서드
- 추상 클래스
    - 개념 : abstract 키워드로 선언된 클래스
        - 반드시 하나 이상의 추상 메서드를 가진다. (추상 메서드가 최소 한 개 이상을 가진 abstract 클래스)
        - 추상 메서드 이외의 다른 것들도 추가 가능
        - 추상메서드는 선언만되고 구현이 되지 않은 불완전한 메서드이므로 객체로 생성되어서는 안됩니다.
          이런 클래스(추상메서드가 포함된 클래스)는 추상클래스로 선언하여 객체 생성을 금지시킵니다.
    - 목적
        - **관련성이 높은 클래스 간의 코드를 공유하고 확장하고 싶은 목적**

  →**추상클래스는 반드시 하나 이상의 추상메서드를 가지며, 객체를 생성할 수 없습니다. 하지만 슈퍼클래스로 사용할 수는 있으며 추상메서드를 사용하기 위해서는 반드지 해당 메서드를 재정의 해야만 합니다.**

- 인터페이스
    - 개념 : default와 static 을 제외하고는 추상 메서드와 상수만을 포함하여, interface 키워드를 사용하여 선언
        - 모든 메서드는 추상 메서드로, public abstract이 생략되어 있다.
        - 상수 필드는 public static final이 생략되어 있다.
        - 다중상속이 가능하다.
    - 목적
        - **관련성이 없는 클래스들의 논리적으로 같은 기능을 자신에 맞게 구현을 강제하는데 목적**

정리하자면, 구조상 차이로 추상 클래스는 abstract 키워드가 붙고 추상 메서드뿐만 아니라 다른 변수, 메서드도 선언이 가능하고, 인터페이스는 추상 메서드와 상수만 선언 가능하다.(자바 8부터는 default 메서드 선언 가능)목적의 차이로 추상 클래스는 관련성이 높은 클래스 간의 코드 공유(재사용)와 확장을 목적으로 하고, 인터페이스는 관련성이 없는 클래스들의 같은 기능을 자신에 맞게 구현하는데 목적이 있다.


## Collection

컬렉션이란 무엇인가?

다수의 데이터를 쉽고 효과적으로 처리할 수 있는 표준화된 방법을 제공하는 클래스의 집합

- java Map 인터페이스 구현체의 종류

대표적인 구현체로 `HashMap`이 존재한다. (밑에서 살펴볼 멀티스레드 환경에서의 개발 부분에서 HashTable 과의 차이점에 대해 살펴본다.) key-value 의 구조로 이루어져 있으며 key 를 기준으로 중복된 값을 저장하지 않으며 순서를 보장하지 않는다.

- java Set 인터페이스 구현체의 종류

대표적인 구현체로 `HashSet`이 존재한다.객체(데이터)를 중복으로 저장할 수 없으며 저장 순서과 보장되지 않는다.

- java List 인터페이스 구현체의 종류

`List`인터페이스를 직접`@Override`를 통해 사용자가 정의하여 사용할 수도 있으며, 대표적인 구현체로는`ArrayList`가 존재한다. 이는 기존에 있었던`Vector`를 개선한 것이다. 이외에도`LinkedList`등의 구현체가 있다.

### `HashTable` vs `HashMap`

Java에서 Hash Table과 Hash Map의 차이는 동기화 지원 여부이다. 

key에 대한 hash값을 사용하여 값을 저장,조회하는 것은 동일하다.

- HashTable
  - 병렬 처리를 할 때(동기화를 고려해야하는 상황)
  - Null값을 허용하지 않는다.

- HashMap
    - 병렬 처리를 하지 않을 때(동기화를 고려하지 않는 상황)
    - Null값을 허용한다.(단 하나의 NULL 값을 Key 값으로 가질 수 있고, 여러 NULL 값을 Value 값으로 가질 수 있다.)

### `HashSet` vs `TreeSet`
![hashset_vs_treeset](https://user-images.githubusercontent.com/47858282/225520230-0dcd9400-a986-414f-b75d-6dad3c6de59a.png)

### `HashMap` vs `HashSet`

- HashMap

    - Map인터페이스의 구현체
    
    - key-value 쌍 형태로 데이터를 저장한다.
    
    - put() 메서드를 사용하여 데이터를 삽입하는데, Key-Value 쌍 데이터의 형태를 저장하기 때문에 삽입 연산 동안 **단 하나의 객체가 생성**된다.

- HashSet

  - Set인터페이스의 구현체

  - 객체 그 자체를 저장한다.

  - add() 메서드로 데이터를 삽입하는데,객체 그 자체를 저장하고 내부적으로 HashMap을 사용하기 때문에 삽입되는 **객체(Key값)**와 **dummy 객체(Value 값)로 총 두개의 객체가 삽입 연산 동안 생성된다.**