## Coroutine?
- 코루틴은 비동기적으로 실행되는 코드를 간소화하기 위해 Android에서 사용할 수 있는 동시 실행 설계 패턴
-  코루틴은 Kotlin 버전 1.3에 추가됨.
-  다른 언어에서 확립된 개념을 기반으로 함.
-  기본 스레드를 차단하여 앱이 응답하지 않게 만들 수도 있는 장기 실행 작업을 관리하는데 도움이 됨.



### 기능?
: 코루틴은 Android의 비동기 프로그래밍에 권장되는 솔루션
- **경량** : 코루틴을 실행 중인 스레드를 차단하지 않는 **정지**를 지원 -> 단일 스레드에서 많은 코루틴 실행 가능
  - 정지는 많은 작업을 동시 진행하면서도 차단보다 메모리를 절약함.
- **메모리 누수 감소** : 구조화된 동시 실행을 사용하여 범위 내에서 작업을 실행함.
- **기본으로 제공되는 취소 지원** : 실행 중인 코루틴 계층 구조를 통해 자동으로 취소가 전달
- **Jetpack 통합** : 많은 Jetpack 라이브러리에 코루틴을 완전히 지원하는 확장 프로그램이 포함되어 있음    
     
       
### 사용하기
- 코루틴을 사용하기 위해서는 앱의 build.gradle 파일에 종속 항목을 추가해야 함

```java
dependencies {
    implementation("org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.9")
}
```
