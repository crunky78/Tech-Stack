## JVM (Java Virtual Machine) 
 - 자바 바이트 코드를 실행할 수 있는 주체
 - 자바 바이트 코드는 운영체제(OS)에 독립적이며 모든 JVM은 규격에 정의된 대로 자바 바이트 코드를 실행
 - 자바 애플리케이션을 클래스 로더를 통해 읽어 JAVA API와 함께 실행

<br/>

## JVM의 메모리 구조

![image](https://github.com/Tech-Stack-Tree/Tech-Stack/assets/49936027/c2f49c97-ac30-4d21-85f7-8cd0556b47a9)
- 자바 소스 코드를 바이트코드로 컴파일 한다. JVM은 모든 구현에서 동일한 바이트 코드를 실행할 수 있다. 위 그림은 다양한 플랫폼에서 Java 바이트코드를 한번 작성하고 어디서나 실행할 수 있다는 개념이다.


![image](https://github.com/Tech-Stack-Tree/Tech-Stack/assets/49936027/f419b01b-067c-4dc4-9357-bdea47d35524)
* #### Class Loader Subsystem
  컴파일 된 클래스는 `.class` 파일(ByteCode)로 저장되고, 클래스를 사용하려고 하면 Java `ClassLoader`가 해당 클래스를 메모리에 로드한다. 이렇게 생성된 `.class` 파일들을 엮어서 JVM이 운영체제로 할당 받은 메모리 영역인 Runtime Data Area로 적재(Loading)한다.
* #### Runtime Data Area
  JVM의 메모리 영역으로 자바 애플리케이션을 실행할 때 사용되는 데이터들을 적재하는 영역으로, 이 영역은 크게 Method Area, Heap Area, Stack Area, PC Register, Native Method Stack으로 나눌 수 있다.
* #### Excution Engine
  Class Loader에 의해 메모리에 로드된 바이트 코드를 실행하는 요소로, Class Loader에 의해 Runtime Data Area에 배치된 바이트코드는 Excution Engine에 의해 실행된다.
 또한 메모리에 적재된 클래스(ByteCode)들을 기계어(BinaryCode)로 변경하여 명령어 단위로 실행하는 역할을 한다
  ##### Interpreter : 명령어를 하나씩 실행하는 대화형식 컴파일. 파이썬이 대표적인 인터프리터 언어.
  ##### JIT(Just-In-Time) Compiler : 적절한 시간에 전체 바이트 코드를 네이티브 코드로 변경해서 실행하므로 성능이 인터프리터보다 속도 면에서 성능이 더 좋다.
* #### Garbage Collector
  Heap 메모리 영역에 적재된 객체들 중 더이상 사용하지 않는 객체들을 탐색 후 제거하는 역할을 한다. 또한 Garbage Collector를 수행하는 동안 Garbage Collector를 수행하는 쓰레드가 아닌 다른 모든  쓰레드가 일시 정지된다.
* #### Java Native Interface (JNI)
  JNI는 기본 메서드 라이브러리와 상호 작용하고 실행 엔진에 필요한 기본 라이브러리를 제공한다.
* #### Native Method Libraries
  실행 엔진에 필요한 기본 라이브러리 모음
  


- 참고 :  https://youtu.be/AWXPnMDZ9I0

