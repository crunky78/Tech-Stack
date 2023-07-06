### *GC란?

자바 애플리케이션에서 사용하지 않는 메모리를 자동으로 수거하는 역할

자바에서 GC를 이용하여 개발자들이 메모리 관리를 비교적 신경쓰지 않는다.

***JVM의 메모리 영역**

→ Class영역, Java Stack, Heap, Native Method Stack

![GC](https://github.com/Tech-Stack-Tree/Tech-Stack/assets/79103761/2b50da0f-c7ec-4c21-90e4-ff3aa013c735)

이 **Heap영역은** 세 영역으로 나누어진다.

**1) Young 영역**

: 생성되지 얼마 되지 않은 객체들을 저장하는 장소

**2) Old 영역**

: 생성된지 오래된 객체를 저장하는 장소이다.

→ 시간이 지남에 따라 우선순위가 낮아지면 Old 영역으로 옮겨진다.

**3) Perm 영역**

: Class, Method 등의 코드가 저장되는 영역으로 JVM에 의해서 사용한다.
