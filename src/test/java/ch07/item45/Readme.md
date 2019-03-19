## 스트림은 주의해서 사용하라
---
#### 스트림을 과용하면 프로그램이 읽거나 유지보수하기 어려워진다.

#### 스트림으로 할 수 없는일

 - 코드 블록에서의 범위 안의 지역변수를 수정할 경우, 수정하는 건 불가능하다.(Atomic 종류(AtomicInteger, AtomicBoolean..)는 가능)
 - break, continue 문으로 종료하거나, skip하는 작업.
 - 내부 로직에서 예외를 던지는 작업.
 

#### 스트림으로 하기 좋은 작업 
 - 원소들의 시퀀스를 일관되게 변환한다.
 - 원소들의 시퀀스를 필터링한다.
 - 원소들의 시퀀스를 하나의 연산을 사용해 결합한다.(더하기, 연결하기, 최소값 구하기 등.)
 - 원소들의 시퀀스를 컬렉션에 모은다.
 - 원소들의 시퀀스에서 특정 조건을 만족하는 원소를 찾는다. 

#### 스트림으로 하기 어려운 작업
 - 파이프라인의 여러 단계를 통과할 때 이 데이터의 각 단계에서의 값들에 동시에 접근하기는 어려운
 경우다. 스트림 파이프라인은 일단 한 값을 다른 값에 매핑하고 나면 원래의 값은 잃기 때문이다.
 
---
### 요약
`
스트림을 사용해야 더 알맞거나, 반복 방식을 해야 더 알맞을 경우가 있다.
어느 쪽이 나은지가 확연히 드러나는 경우가 많겠지만, 확신하기 어려운 경우라면 
둘 다 해보고 더 나은 쪽을 선택하라.
`