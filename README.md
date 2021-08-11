Table of Contents
---

- Operating System(운영체제)
- System Programing(시스템 프로그래밍)
- Computer Architecture(컴퓨터 구조)
- Network(네트워크)
- Database(데이터베이스)
  

Operating System(운영체제)
---
[운영체제의 역할](https://yunsikus.github.io/cs/2021/07/21/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C%EC%9D%98%EC%97%AD%ED%95%A0/)
  
<details>
<summary>운영체제란 무엇입니까?</summary>
<div markdown="1">       

응용 프로그램이 요청하는 시스템 리소스를 효율적으로 분배하고 지원하는 소프트웨어

</div>
</details> 

<details>
<summary>운영체제의 주요 목적은 무엇입니까?</summary>
<div markdown="1">       

시스템 자원 관리, 사용자와 컴퓨터간의 커뮤니케이션 지원, 응용프로그램 관리

</div>
</details> 

[운영체제 구조 - 시스템콜, 사용자 모드, 커널](https://yunsikus.github.io/cs/2021/07/29/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C_%EA%B5%AC%EC%A1%B0_%EC%8B%9C%EC%8A%A4%ED%85%9C%EC%BD%9C/)
  
<details>
<summary>커널, API, 시스템콜이란?</summary>
<div markdown="1">       

커널 : 커널은 하드웨어와 응용프로그램 사이에서 인터페이스(System Call)를 제공하여 응용 프로그램이 하드웨어에서부터 오는 자원(CPU, 메모리, 저장장치, 모니터)을 관리하고 사용할 수 있게 해준다. 즉, OS의 API기능을 담당하는 부분.

API : 응용프로그램이 OS와 요청을 주고 받는 인터페이스를 API라고 함.

시스템콜 : OS가 제공하는 서비스를 어플리케이션에 제공하는 인터페이스로, API 내부에는 시스템콜을 호출하는 형태로 만들어진다. 시스템콜의 종류로는 프로세스 제어(생성, 종료, 시그널), 파일 및 IO 관리, 통신 등이 있다.

</div>
</details> 

[운영체제 구조 - 배치 처리 시스템, 멀티 태스킹, 멀티 프로그래밍](https://yunsikus.github.io/cs/2021/07/29/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C_%EB%B0%B0%EC%B9%98%EC%B2%98%EB%A6%AC_%EC%8B%9C%EB%B6%84%ED%95%A0/)

<details>
<summary>질문 1 배치처리시스템은 무엇이고 어떤 단점이 있는가?</summary>
<div markdown="1">       

배치처리 시스템은 등록된 여러 프로그램들을 컴퓨터 프로그램의 실행 요청 순서에 따라 순차적으로 실행하는 방식. 

단점 : 만약 어떤 프로그램이 실행 시간이 너무 많이 걸린다면, 다음 프로그램이 실행되는데 너무 많이 기다려야 한다. 동시에 여러 프로그램을 실행 시킬 수 없으며 다중 사용자의 지원이 어렵다. 

</div>
</details> 

<details>
<summary>시분할 시스템이란?</summary>
<div markdown="1">       

시분할 시스템은 다중 사용자 지원을 위해 컴퓨터 응답시간을 최소화하는 시스템. 각 어플리케이션이 실행될수 있도록 잘게 잘라서 배치하는 것.

</div>
</details> 

<details>
<summary>멀티 태스킹과 멀티 프로세싱의 차이점은?</summary>
<div markdown="1">       

멀티 태스킹은 단일 CPU에서 여러개의 쪼개진 프로세스가 실행되도록 하는 갓. 반면 멀티 프로세싱은 여러 CPU에 하나의 프로그램을 병렬로 실행해서 실행속도를 극대화 시키는 시스템. 

</div>
</details> 

[운영체제 구조 - 선점형/비선점형 스케줄러](https://yunsikus.github.io/cs/2021/08/06/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C-%EC%84%A0%EC%A0%90%ED%98%95-%EB%B9%84%EC%84%A0%EC%A0%90%ED%98%95/)

<details>
<summary>선점 스케줄링과 비선점 스케줄링의 차이점은?</summary>
<div markdown="1">       

선점 스케줄링은 높은 우선순위의 프로세스가 들어올 경우 현재 프로세스를 중지시키고, 높은 우선순위의 프로세스를 처리.
비선점 스케줄링은 한번 할당하면 끝날때까지 다른 프로세스가 들어오지 못하는 스케줄링
엄격한 비선점식 스케줄링을 사용하지 않는 이유는 짧은 프로세서가 오랫동안 대기하게 될 경우 비효율적이고, 기아상태가 발생할 수 있다. 

</div>
</details>


[운영체제 구조 - 프로세스 스케줄링](https://yunsikus.github.io/cs/2021/08/06/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C-%EC%84%A0%EC%A0%90%ED%98%95-%EB%B9%84%EC%84%A0%EC%A0%90%ED%98%95/)


<details>
<summary>스케줄링이 필요한 이유?</summary>
<div markdown="1">       

한정적인 메모리(자원)를 효율적으로 관리하기 위해, 공정성을 주기 위해 필요하다.

</div>
</details>


<details>
<summary>스케줄러와 CPU 스케줄러의 차이에 대하여 설명해보세요.</summary>
<div markdown="1">       

스케줄러(=Job Scehduler, 장기 스케줄러)는 디스크와 메모리 간 스케줄링을 담당한다.

CPU 스케쥴러(= 단기 스케줄러)는 메모리와 CPU 간 스케줄링을 담당한다.

</div>
</details>


<details>
<summary>FCFS 스케줄링을 개선한 스케줄링 방식에 대하여 설명해보세요..</summary>
<div markdown="1">       

FCFS는 먼저 도착한 프로세스에게 CPU를 할당하는 기법이다.

하지만 먼저 도착한 프로세스가 실행 시간이 긴 경우 나중에 도착한 프로세스들의 대기 시간이 길어지는 Convoy Effect 라는 문제점을 가지고 있다.

이를 개선한 SJF(Shortest Job First) 기법이 있다.

SJF는 짧은 실행시간을 갖는 프로세스에게 CPU를 먼저 할당하는 기법이다.

Convoy Effect는 해결하였지만, 실행시간이 긴 프로세스는 계속 CPU를 할당받지 못하는 Starvation 현상이 일어날 수 있다.

</div>
</details>


<details>
<summary>Round Robin 스케줄링 방식에서 time quantum 설정에 따른 결과를 설명해보세요.</summary>
<div markdown="1">       

타임퀀텀이 긴 경우: 타임퀀텀이 프로세스의 실행시간과 비슷해진다면 FCFS랑 다를 바 없어진다.

타임퀀텀이 짧은 경우: 타임퀀텀이 짧아 Context Switching이 자주 일어나게 되어 오버헤드가 발생한다.

</div>
</details>

<details>
<summary>오버헤드가 어떤건가요?.</summary>
<div markdown="1">       

프로그램의 실행 흐름 도중에 동떨어진 위치의 코드를 실행시켜야 할 때, 추가적으로 시간, 메모리, 자원이 사용되는 현상을 오버헤드라 한다.

</div>
</details>

<details>
<summary>다음 스케줄링 알고리즘을 설명하시오 - FCFS.</summary>
<div markdown="1">       
- 특징 
    - 먼저 온 고객을 먼저 서비스해주는 방식. 먼저 온 순서대로 차리
    - 가장 간단한 스케줄러(배치처리시스템)
    - FCFS(First Come First Served)
    - 비선점형 스케줄링
      - 일단 CPU를 잡으면 CPU burst가 완료될 때까지CPU를 반환하지 않는다. 할당되었던 CPU가 반환될때만 스케줄링이 이루어짐
- 문제점
    - 실행시간 큰 프로세스로 다른 프로세스들이 딜레이가 생길 수 있음
</div>
</details>


<details>
<summary>다음 스케줄링 알고리즘을 설명하시오 - SJF.</summary>
<div markdown="1">       
- 특징
  - 가장 프로세스 실행시간이 짧은 프로세스부터 먼저 실행을 시키는 알고리즘
  - 다른 프로세스가 먼저 도착했어도 CPU burst time이 짧은 프로세스에게 선 할당
  - FIFO와 마찬가지로 비선점형 스케줄링
  - 응답시간이 짧지만 수행기산을 다 알아야함
- 문제점
  - 효율성을 추구하는게 가장 중요하지만 특정 프로세스가 지나치게 차별받으면 안된다. 이 스케줄링은 극단적으로 CPU 사용이 짧은 job을 선호. 그래서 사용이 긴 프로세스는 거의 영원한 CPU를 할당받을 수 없다. 
</div>
</details>

<details>
<summary>다음 스케줄링 알고리즘을 설명하시오 - SRT.</summary>
<div markdown="1">       
- 특징
  - 새로운 프로세스가 도착할 때마다 새로운 스케줄링이 이루어진다
  - 선점형 스케줄링
    - 현재 수행중인 프로세스의 남은 burst time보다 더 짧은 CPU burst time을 가지는 새로운 프로세스가 도착하면 CPU를 뺏긴다
- 문제점
  - 새로운 프로세스가 도달할 때마다 스케줄링을 다시하기 때문에 CPU burst time(CPU 사용시간)을 측정할 수가 없다. 
</div>
</details>

<details>
<summary>다음 스케줄링 알고리즘을 설명하시오 - Priority Scheduling.</summary>
<div markdown="1">       
- 특징
  - 우선순위가 가장 높은 프로세스에게 CPU를 할당 우선순위란 정수로 표현하게 되고 작은 숫자가 우선순위가 높다. 
  - 선점형 스케줄링 방식
    - 더 높은 우선순위의 프로세스가 도착하면 실행중인 프로세스를 멈추고 CPU를 선점
  - 비선점형 스케줄링 방식
    - 더 높은 우선순위의 프로세스가 도착하면 Ready Queue의 Head에 넣는다
- 문제점
  - 실행 준비는 되어있으나 CPU를 사용 못하는 프로세스를 CPU가 무기한 대기하는 상태. 아무리 우선순위가 낮은 프로세스라도 오래 기다리면 우선순위를 높여주어 해결 가능

</div>
</details>

<details>
<summary>다음 스케줄링 알고리즘을 설명하시오 - Round Robin.</summary>
<div markdown="1">       
- 특징
  - 현대적인 CPU 스케줄링. 시분할 시스템을 위해 설계됨
  - 각 프로세스는 동일한 크기의 할당 시간(time quantun)을 갖게 된다. 
  - 할당 시간이 지나면 프로세스는 선점 당하고 ready queue의 제일 뒤에 가서 다시 줄을 선다
  - `RR`은 CPU 사용시간이 랜덤한 프로세스들이 섞여있을 경우에 효율적
  - `RR`이 가능한 이유는 프로세스의 context를 save할 수 있기 때문
- 장점
  - Response time이 빨라진다. 
    - n개의 프로세스가 ready queue에 있고 할당시간이 q(time quantun)인 경우 각 프로세스는 q 단위로 CPU 시간의 1/n을 얻는다. 즉, 어떤 프로세스도 (n-1)q time unit 이상 기다리지 않는다.
  - 프로세스가 기다리는 시간이 CPU를 사용할 만큼 증가한다. 
    - 공정한 스케줄링이라고 할 수 있다. 
- 주의할 점
  - 설정한 `time quantum`이 너무 커지면 FCFS와 같아진다. 또 너무 작아지면 스케줄링 알고리즘의 목적에는 이상적이지만 잦은 context switch로 overhead가 발생한다. 그렇기 때문에 적당한 `time quantun`을 설정하는 것이 중요
</div>
</details>

[운영체제 구조 - 인터럽트](https://yunsikus.github.io/cs/2021/08/06/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C-%EC%9D%B8%ED%84%B0%EB%9F%BD%ED%8A%B8/)

<details>
<summary>인터럽트란?</summary>
<div markdown="1">       

CPU가 프로그램을 실행하고 있을 때, 입출력 **하드웨어 장치와 커뮤니케이션 할때나, 예외상황이 발생하여 처리가 필요할 경우가 생길 수 있다. 이때 CPU에 알려서 처리하는 기술을 인터럽트라고 한다.**

</div>
</details>

<details>
<summary>내부/외부 인터럽트는 어떤 상황들이 있는지?</summary>
<div markdown="1">       

내부 인터럽트는 하드웨어 고장, 실행할 수 없는 명령어, 명령어 실행 오류, 사용 권한 위배 등이 있다. 

- 하드웨어 고장은 컴퓨터 고장 또는 비트 오류
- 명령어 실행 오류는 나누기 0과 같은 경우
- 사용 권한 위배는 말 그대로 사용자가 OS만 접근 가능한 곳에 엑세스 한 경우

외부인터럽트는 보통 외부 입력장치에 의해 발생

- 컴퓨터 종료(전원버튼누르기)
- 타이머 인터럽트(타이머가 일정 시간 간격으로 인터럽트 요청)
- 입출력 인터럽트(입출력 장치가 입출력 완료를 알리기 위해 인터럽트 요청)

</div>
</details>

[운영체제 구조 - 프로세스 구조, 컨텍스트 스위칭](https://yunsikus.github.io/cs/2021/08/11/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4%EC%99%80%EC%BB%A8%ED%85%8D%EC%8A%A4%ED%8A%B8%EC%8A%A4%EC%9C%84%EC%B9%AD/) 


<details>
<summary>컨텍스트 스위칭이란?</summary>
<div markdown="1">       

멀티 프로세스 환경에서 CPU가 어떤 하나의 프로세스를 실행하고 있는 상태에서 인터럽트 요청에 의해 다음 우선 순위의 프로세스가 실행되어야 할 때 기존의 프로세스의 상태 또는 레지스터 값을 저장하고 CPU가 다음 프로세스를 수행하도록 개로운 프로세스의 상태 또는 레지스터 랎을 교체하는 작업을 Context Switching이라고 한다. 

</div>
</details>


<details>
<summary>프로세스 제어 블록이란?</summary>
<div markdown="1">       
PCB는 특정 프로세스에 대한 중요한 정보를 저장하고 있는 운영체제의 자료구조. 운영체제는 프로세스를 관리하기 위해 프로세스의 생성과 동시에 고유한 PCB를 생성. 프로세스는 CPU를 할당받아 작업을 처리하다가도 프로세스 전환이 발생하면 진행하던 작업을 저장하고 CPU를 반환해야 하는데, 이때 작업의 진행 상황을 모두 PCB에 저장하게 된다. 그리고 다시 CPU를 할당받게 되면 PCB에 저장되어있던 내용을 불러와 이전에 종료됐던 시점부터 다시 작업을 수행한다.
PCB에 저장되는 정보는 프로세스 ID, Register 값(PC, SP), 스케줄링 정보, 메모리 관리 정보등이 있다. 

</div>
</details>