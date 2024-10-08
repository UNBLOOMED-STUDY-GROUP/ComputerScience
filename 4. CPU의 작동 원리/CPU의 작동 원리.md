### [장명훈]

<details>
  <summary> Q. 레지스터란 무엇인가요? </summary>
  
  - CPU내부에 작은 임시 저장 장치
    - ALU의 결과값을 저장하는 공간
    - 읽고 쓰는 속도가 매우 빠르다.
      
</details>

<details>
  <summary> Q. 동기 인터럽트와 비동기 인터럽트를 설명해보세요. </summary>
  
  - 동기 인터럽트(synchronous interrupts)
    - <ins>CPU</ins>에 의해 발생하는 인터럽트
    - CPU가 명령어를 수행하면서 예상치 못한 상황이 생겼을 때 발생
    - 예외(exception)라고도 불림
  
  - 비동기 인터럽트(asynchronous interrupt): 
    - <ins>입출력장치</ins>에서 발생하는 인터럽트
    - 인터럽트 발생으로 입출력 작업 결과를 확인하여 CPU의 생산 효율을 높임
      
</details>

---

### [홍승현]

<details>
  <summary>Q1. 인터럽트를 처리할 때 CPU의 프로그램 카운터, 메모리 주소 레지스터, 메모리 버퍼 레지스터, 명령어 레지스터에 든 내용을 모두 어디에 백업할까요? </summary>
  
- 스택 메모리
</details>

<details>
  <summary>Q2. HW 인터럽트 처리 순서를 간단하게 설명해주세요 </summary>
  
- 입출력장치가 CPU에 인터럽트 요청 신호를 보내면 CPU는 플래그 레지스터에 있는 인터럽트 플래그를 통해 현재 인터럽트를 받아들일 수 있는지 여부를 확인하고 인터럽트를 받아들일 수 있다면 CPU는 지금까지의 작업을 백업합니다. 그리고 CPU는 인터럽트 벡터를 참조하여 인터럽트 서비스 루틴을 실행합니다. 인터럽트 서비스 루틴 실행이 끝나면 백업해둔 작업을 복구하여 실행을 재개합니다.

</details>

---

### [권영민]

<details>
  <summary>Q1. 인터럽트에 대해서 설명해보자 </summary>
  
- 컴퓨터 시스템에서 중요한 이벤트가 발생했을 때, CPU가 현재 실행 중인 작업을 중단하고 즉시 해당 이벤트를 처리하도록 하는 메커니즘이다.
</details>

<details>
  <summary>Q2. 인터럽트의 종류에 대해서 설명해보자 </summary>
  
- 하드웨어 인터럽트와 소프트웨어 인터럽트가 있다.
하드웨어 인터럽트는 외부 하드웨어 장치가 발생시키는 인터럽트이다.
소프트웨어 인터럽트는 프로그램 내에서 발생하는 인터럽트이다.

</details>

---

<details>
  <summary>Q1. 클럭에 대해서 설명해보자 </summary>
  
- 클럭이란 컴퓨터의 모든 부품을 일사분란하게 움직일 수 있게 하는 시간 단위이다.
</details>

<details>
  <summary>Q2. 인터럽트가 받아졌을 때, 인터럽트 서비스 루틴을 설명하라 </summary>
  
![image](https://github.com/user-attachments/assets/ba2beec4-fa4f-4970-a899-7450f0d0ea7d)

![image](https://github.com/user-attachments/assets/fe12baa2-329a-4564-9ef1-170c79237d30)

  1. 기존에 실행중이던 프로세스의 진행하여 캐싱한다.
  2. 인터럽트 서비스 루틴의 시작 주소로 이동한다
  3. 인터럽트 서비스 루틴을 진행한다.
  4. 인터럽트 서비스 루틴이 완료되면 원래의 프로세스로 이동한다.
  5. 기존의 프로세스를 진행한다.
</details>
