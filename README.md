#천우성 202430134
## 3월 20일(목)

## 3월 27일(목)
# 식별자 (identifier) – 명명 규칙 (Naming Convention)

식별자란? 클래스, 변수, 상수, 메소드 등에 붙이는 이름

식별자의 원칙
✓ '@', '#', '!'와 같은 특수 문자, 공백 또는 탭은 식별자로 사용불가. '', '$'는 사용 가능
✓ 유니코드 문자 사용 가능. 한글 사용 가능. * 한글은 사용하지 마세요.
✓ 자바 언어의 키워드는 식별자로 사용불가.
✓ 식별자의 첫 번째 문자로 숫자는 사용불가.
✓ '' 또는 '$'를 식별자 첫 번째 문자로 사용할 수 있으나 일반적으로 잘 사용하지 않는다.
✓ 불린 리터럴 (true, false)과 널 리터럴(null)은 식별자로 사용불가
✓ 길이 제한 없음
✓ 대소문자 구별 : barChart와 barchart는 다른 식별자

# 참조 자료형 (Reference Type)
포인터는 임의의 메모리 주소를 저장하는 반면, 참조 자료형은 주소를 저장할 수 없습니다.

직접 주소를 갖고 있지는 않지만, JVM이 해당 주소로 안내해 주게 됩니다.

객체를 참조하는 변수 유형으로, 힙(Heap) 영역에 저장된 객체의 메모리 주소를 가리킵니다.
* 참고로 기본 자료형은 스택(Stack) 영역에 저장됩니다.

New 키워드로 객체(인스턴스)를 생성하는 것이 바로 참조 자료형을 선언하는 것입니다.

이렇게 선언된 참조 자료형은 JVM이 대신 객체의 주소를 저장합니다.

**배열(Array), 인터페이스(Interface) 혹은 열거형(Enum)**도 객체이기 때문에 참조 자료형입니다.

객체를 참조하지 않을 때 null 값을 가질 수 있습니다.

같은 객체를 여러 변수가 참조할 수 있고, == 연산자로 객체의 주소를 비교할 수도 있습니다.

일반적으로 '레퍼런스'라고 부르면 되지만, 레퍼런스형, 레퍼런스 자료형, 참조형, 참조 자료형, 래퍼런스 변수, 참조 변수 등 다양하게 부릅니다.

# Java는 왜 참조(Reference) 자료형을 사용할까?
1. 메모리 안전성(Safety)

포인터를 사용하면 직접 메모리 주소를 조작할 수 있기 때문에 잘못된 메모리 접근(Invalid Memory Access) 문제가 발생할 가능성이 높습니다.

Java는 포인터를 허용하지 않음으로써 이런 위험한 동작을 원천적으로 차단하기 때문에 메모리 충돌이나 해제된 메모리 접근 문제가 발생하지 않습니다.

2. Garbage Collection(가비지 컬렉션) 지원

C++에서는 new를 활용한 메모리는 delete로 직접 해제해야 하지만, Java에서는 **Garbage Collector(GC)**가 필요 없는 객체를 자동으로 정리해 줍니다.

Java에서 포인터를 허용하면, 개발자가 직접 메모리를 관리해야 하므로 GC가 동작할 수 없게 됩니다.

3. 코드의 단순화 및 가독성 향상

포인터를 사용하면 코드가 복잡해지고 실수할 가능성이 커지게 됩니다.

Java는 포인터 연산 없이 객체를 다룰 수 있기 때문에 코드가 훨씬 간결하여 가독성이 높습니다.

4. 보안(Security) 강화
포인터를 사용하면 특정 메모리 주소를 직접 조작할 수 있기때문에, 버퍼 오버플로우(Buffer Overflow)같은 보안 취약점이 생길 가능성이 높습니다.
포인터를 활용한 해킹 기법(버퍼 오버플로우, 스택 오버플로우 등)이 Java에서는 불가능합니다.
*보안이 중요한 웹 서버, 금융 시스템, 앱 개발 등에서 Java가 많이 사용되는 이유중 하나입니다.
 
5. 다중 플랫폼 지원(Portable)
java는 JVM(Java Virtual Machine)에서 실행되기 때문에, OS에 따라 메모리 관리 방식이 달라지더라도 영향을 받지않습니다.

*래퍼런스를 사용하면 JVM이 메모리를 관리해주므로, OS에 관계없이 같은 코드가 실행 가능합니다.





## 4월 3일(목)

## 4월 10일(목)
세상 모든 것이 객체다.

실세계 객체의 특징
객체마다 고유한 특성(state) 과 행동(behavior) 을 가짐

다른 객체들과 정보를 주고 받는 등, 상호작용 하면서 살아감

컴퓨터 프로그램에서 객체 사례
테트리스 게임의 각 블록들

한글 프로그램의 메뉴나 버튼들

자바의 객체 지향 특성 : 캡슐화
캡슐화 : 객체를 캡슐로 싸서 내부를 볼 수 없게 하는 것
객체의 가장 본질적인 특징
외부의 접근으로부터 객체 보호

자바의 캡슐화
클래스(class): 객체 모양을 선언한 틀(캡슐화하는 툴)
객체: 생성된 실체(instance): 클래스 내에 메소드와 필드 구현

자바의 객체 지향 특성 : 상속

상속

상위 객체의 속성이 하위 객체에 물려 줌

하위 객체가 상위 객체의 속성을 모두 가지는 관계

실제계의 상속 사례

나무는 식물의 속성과 생물의 속성을 모두 가짐

사람은 생물의 속성은 가지지만 식물의 속성은 가지고 있지 않음

자바의 상속

상위 클래스의 멤버들 하위 클래스가 물려받음

상위 클래스 : 슈퍼 클래스

하위 클래스 : 서브 클래스, 슈퍼 클래스 코드의 재사용, 새로운 특성 추가 가능

자바의 객체 지향 특성 : 다형성
다형성

같은 이름의 메서드가 클래스 혹은 객체에 따라 다르게 구현되는 것

다형성 사례

메서드 오버로딩: 한 클래스 내에서 같은 이름이지만 다르게 작동하는 여러 메서드

메서드 오버라이딩: 슈퍼 클래스의 메서드를 동일한 이름으로 서브 클래스마다 다르게 구현

객체 지향 언어의 목적
1. 소프트웨어의 생산성 향상
컴퓨터 산업 발전에 따라 소프트웨어의 생명 주기(life cycle) 단축

소프트웨어를 빠른 속도로 생산할 필요성 증대

객체 지향 언어
상속, 다형성, 객체, 캡슐화 등 소프트웨어 재사용을 위한 여러 장치 내장

소프트웨어의 재사용과 부분 수정 빠름

소프트웨어를 다시 만드는 부담 대폭 줄임

소프트웨어 생산성 향상

객체 지향 언어의 목적

2. 실세계에 대한 쉬운 모델링

초기 프로그래밍
✓ 수학 계산/통계 처리를 하는 등 처리 과정, 계산 절차 중요

현대 프로그래밍
✓ 컴퓨터가 산업 전반에 활용
✓ 실세계에서 발생하는 일을 프로그래밍
실세계에서는 절차나 과정보다 물체(객체)들의 상호 작용으로 묘사하는 것이 용이

객체 지향 언어
실세계의 일을 보다 쉽게 프로그래밍하기 위한 객체 중심적 언어

절차 지향 프로그래밍과 객체 지향 프로그래밍

절차 지향 프로그래밍

작업 순서를 표현하는 컴퓨터 명령 집합

함수들의 집합으로 프로그램 작성

객체 지향 프로그래밍

컴퓨터가 수행하는 작업을 객체들 간의 상호 작용으로 표현

클래스 혹은 객체들의 집합으로 프로그램 작성

클래스와 객체

클래스 : 객체의 속성(state)과 행위(behavior) 선언. 객체의 설계도 혹은 틀.

객체 : 클래스의 틀로 찍어낸 실체

프로그램 실행 중에 생성되는 실체

메모리 공간을 갖는 구체적인 실체

인스턴스(instance)라고도 부름

사례

클래스: 소나타자동차, 객체: 출고된 실제 소나타 100대

클래스: 벽시계, 객체: 우리집 벽에 걸린 벽시계들

클래스: 책상, 객체: 우리가 사용중인 실제 책상들

자바 클래스 구성

클래스

class 키워드로 선언

멤버 : 클래스 구성 요소. 필드(멤버 변수)와 메소드(멤버 함수)

클래스에 대한 public 접근 지정 : 다른 모든 클래스에서 클래스 사용 허락

멤버에 대한 public 접근 지정 : 다른 모든 클래스에게 멤버 접근 허용

public class Circle {
    int radius;
    String name;

    public double getArea() {
        return 3.14 * radius * radius;
    }
}

생성자
객체가 생성될 때 초기화 목적으로 실행되는 메소드
객체가 생성되는 순간에 자동 호출

## 4월 17일(목)
