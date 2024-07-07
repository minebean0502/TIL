# 1장. 자바를 시작하기 전에

## 1.1 자바란?
- 자바는 "객체지향 프로그래밍 언어"
- 운영체제에 독립적임 → 운영체제의 종류에 관계없이 JVM 덕분에 실행이 가능하다

## 1.2 자바 언어의 특링
1. 운영체제에 독립적이다.
2. 객체지향 언어(OOP : Object-Oriented-Program)이다.
   - 상속, 캡슐화, 다형성 등이 적용되어 있다
3. 자동 메모리 관리 (Garbage Collection)
   - 가비지 컬렉터가 자동적으로 메모리를 관리해준다 → 프로그래머가 메모리를 따로 관리하지 않아도 된다.
4. 네트워크와 분산처리를 지원한다.
5. 멀티쓰레드를 지원한다
   - 여러 쓰레드에 대한 스케줄링을 자바 인터프리터가 담당하게 된다.
6. 동적 로딩 (Dynamic Loading)을 지원한다.
   - 어플리케이션은 여러 자바 클래스로 구성되어 있다.
   - 실행시에 "모든 클래스"가 로딩되지 않고, "필요한" 시점에 클래스를 로딩하여 사용 가능
   - 일부 클래스가 변경되어도, 전체 애플리케이션을 다시 컴파일 하지 않아도 된다.

## 1.3 JVM (Java Virtual Machine)
- 일반 애플리케이션 코드는 OS만 거치고 하드웨어로 전달되나, JAVA 애플리케이션은 JVM을 한번 거쳐 실행된다.
- 그렇기에 하드웨어에 맞게 완전히 컴파일된 상태가 아니고, 실행 시 해석(interpret)가 되기 때문에 속도가 비교적 느리다는 단점을 가지고 있다.
    - A) JAVA 애플리케이션 ↔ JVM ↔ OS(Windows) ↔ 컴퓨터(HW)
    - B) 일반 애플리케이션 ↔ OS ↔ 컴퓨터(HW)
- 일반 애플리케이션은 OS에 종속적이나, JAVA는 JVM과 상호작용만 하기 때문에 OS와 상관없이 실행이 가능하다
- 그러나 JVM는 OS에 종속적이다.

## 1.4 JDK (Java Development Kit)
- JDK = JRE + 개발에 필요한 실행파일 (javac.exe)
- JRE = JVM + 클래스 라이브러리 (Java API)

[JVM, JDK, JRE요약](https://github.com/minebean0502/TIL/blob/main/%EC%9E%90%EB%B0%94%EC%9D%98%EC%A0%95%EC%84%9D/1%EC%9E%A5/1%EC%9E%A5%20%EC%9D%B4%EB%AF%B8%EC%A7%80/JVM%2CJRE%2CJDK%20%EC%9A%94%EC%95%BD.PNG)

### 주요 키워드
- JVM
- 가비지 컬렉터
- 네트워크
- 분산처리
- 스케줄링
- 동적 로딩
- JDK, JRE

### 개인 메모
1. High Level Language
- High Level Language 자체를 CPU가 직접 실행할 수는 없다.
- Java를 비롯한 High Level Language로 작성된 코드는 어느 시점에 다시 기계어로 변환되어야 한다.
- !!특히 변환의 시점은 언어(의 구현체)마다 다르다
![컴파일_스크립트언어 사진](https://github.com/minebean0502/TIL/blob/main/%EC%9E%90%EB%B0%94%EC%9D%98%EC%A0%95%EC%84%9D/1%EC%9E%A5/1%EC%9E%A5%20%EC%9D%B4%EB%AF%B8%EC%A7%80/%EC%BB%B4%ED%8C%8C%EC%9D%BC_%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EC%96%B8%EC%96%B4.PNG)