## JVM (Java Virtual Machine) 
 - 바이트코드라고 하는 컴파일된 프로그램을 실행할 수 있는 환경 제공
 - 다양한 플랫폼에 대한 다양한 벤더의


![image](https://github.com/Tech-Stack-Tree/Tech-Stack/assets/49936027/c2f49c97-ac30-4d21-85f7-8cd0556b47a9)
- 자바 소스 코드를 바이트코드로 컴파일 한다. JVM은 모든 구현에서 동일한 바이트 코드를 실행할 수 있다. 위 그림은 다양한 플랫폼에서 Java 바이트코드를 한번 작성하고 어디서나 실행할 수 있다는 개념이다.


![image](https://github.com/Tech-Stack-Tree/Tech-Stack/assets/49936027/f419b01b-067c-4dc4-9357-bdea47d35524)
* #### Class Loader Subsystem
 컴파일 된 클래스는 `.class` 파일로 저장되고, 클래스를 사용하려고 하면 Java `ClassLoader`가 해당 클래스를 메모리에 로드한다. 클래스는 이미 실행 중인 클래스에서 이름으로 참조될 때 Java 환경에 도입된다. 첫 번째 클래스가 실행되면 클래스 로드에 대한 향후 시도는 클래스 로더에 의해 수행된다. 첫번째 클래스 실행은 일반적으로 정적 main() 메서드를 선언하고 사용하여 수행된다.

 



- 참고 :  https://youtu.be/AWXPnMDZ9I0

