### [장명훈]

<details>
  <summary> Q. 멀티 코어와 멀티 스레드의 차이를 설명하시오.  </summary>

- 멀티 코어
  - 코어를 여러 개 포함하고 있는 CPU

- 멀티 스레드 
  - 하나의 코어로 여러 명령어를 동시에 처리하는 CPU
  
</details>

<details>
  <summary> Q. 명령어 파이프라인의 위험성 3가지를 설명하시오. </summary>

  - 데이터 위험(data hazard)
    - 명령어 간 <ins>데이터 의존성</ins>에 의해 발생함
  
  - 제어 위험(control hazard)
    - 분기 등으로 인한 <ins>프로그램 카운터의 갑작스러운 변화</ins>로 발생

  - 구조적 위험(structural hazard)
    - 서로 다른 명령어가 <ins>동시에 같은 ALU, 레지스터 등의 CPU 부품에 접근</ins>할 때 발생함

</details>

---