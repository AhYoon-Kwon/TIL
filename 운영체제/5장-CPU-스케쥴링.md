## [CPU 스케쥴링 #1](https://core.ewha.ac.kr/publicview/C0101020140328151311578473?vmode=f)

## [CPU 스케쥴링 #2, 프로세스 동기화 #1](https://core.ewha.ac.kr/publicview/C0101020140401134252676046?vmode=f)

### 멀티 프로세스 스케쥴링 (Multi-Processing Scheduling)

- CPU가 여러 개인 경우 스케줄링은 더욱 복잡해짐
  <br/>
- Homogeneous processor인 경우 (동일한 성격의 코어를 모은 프로세서; 멀티코어 CPU)
  - Queue에 한줄로 세워서 각 프로세서가 알아서 꺼내가게 할 수 있다
  - 반드시 특정 프로세서에서 수행되어야 하는 프로세스가 있는 경우에는 문제가 더 복잡해짐
- Load sharing
  - 일부 프로세서에 job이 몰리지 않도록 부하를 적절히 공유하는 메커니즘 필요
  - (각각의 CPU마다) 별개의 큐를 두는 방법 vs 공동 큐를 사용하는 방법
- Symmetric Multiprocessing (SMP)
  - 각 프로세서가 각자 알아서 스케줄링 결정
- Asymmetric multiprocessing
  - 하나의 프로세서가 시스템 데이터의 접근과 공유를 책임지고 나머지 프로세서는 거기에 따름

### 실시간 스케쥴링 (Real-time Scheduling)

- **Hard real-time systems**
  - Hard real-time task는 정해진 시간 안에 반드시 끝내도록 스케줄링해야 함
  - 정해진 task의 처리 시간(dead line)을 넘기면 실패하는 경우
  - ex. 자동차의 에어백 등
- **Soft real-time computing**
  - Soft real-time task는 일반 프로세스에 비해 높은 priority를 갖도록 해야 함
  - 정해진 task 처리 시간을 넘기면 성능이 감소하는 경우
  - 최대한 빨리 끝낼 수 있도록 함. dead line이 있긴 하지만 조금 넘어도 상관은 없음.
  - ex. streaming video 등

<!-- ### 스레드 스케줄링 (Thread Scheduling) -->
