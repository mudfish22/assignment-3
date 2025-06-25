## assignment-3
# 리눅스 명령어(top, ps, jobs, kill)

### 1. top
 - 현재 OS의 상태를 실시간으로 보여줌
 - git-bash 환경에서는 테스트 할 수 없음
![스크린샷 2025-06-25 143414](https://github.com/user-attachments/assets/8e21efd6-63d4-4dce-9d87-ca57cb594e49)
[tasks, cpu, memory 등의 정보를 확인할 수 있음]


#### 단축키를 통해 여러 명령어를 실행해볼 수 있음
 - k - 프로세스 종료
 - 1 - CPU 코어별 사용 현황
 - m - 메모리 사용률 시각화 표시
 - ...

<https://sabarada.tistory.com/146>
<https://blog.naver.com/hongganz/222456616664>
---

### 2. ps
 - top와 비슷하세 현재 실행중인 정보를 확인함
 - 실시간으로 갱신하는 top와 달리 명령어 실행 시점의 정보에 대해서만 한번 보여줌
 - git-bash 환경에서도 일부 기능만 테스트 해볼 수 있음..(추가 옵션 사용 안됨)
![스크린샷 2025-06-25 144914](https://github.com/user-attachments/assets/0abc0dfa-74db-46dd-8223-2f2a58858d11)
[PID - 프로세스 아이디, PPID - 부모 프로세스 아이디, PGID 프로세스 그룹 아이디, 등의 정보]

*git-bash에선 cpu 사용량 등에 대한 정보는 표시되지 않음*

#### 주요 옵션
 - -e : 현재 사용자가 구동시킨 모든 프로세스 표시
 - -f : 상세한 정보 표시
 - -l : -f보다 더 상세한 정보 표시

<https://tigris-data-science.tistory.com/entry/Linux-ps-%EB%AA%85%EB%A0%B9%EC%96%B4>
---

### 3. jobs
 - 셀에서의 처리 단위를 뜻하는 *잡(job)*
 - 현재 셀에서 처리 중인 백그라운드 작업 목록에 대해 보여줌(실행 중인 게 없다면 아무것도 안보여줌)
 - git-bash에서도 사용 가능!!
![스크린샷 2025-06-25 150306](https://github.com/user-attachments/assets/a68f37de-3f4a-4938-86a2-e3d8cabc8a9e)
[작업 번호와 상태(stopped - 정지, Running - 실행 중, Done - 작업 완료), 실행한 명령어를 보여줌]

#### 주요 옵션 
 - -l : PID(프로젝트 아이디)까지 출력
 - -r/-s, : 실행중인/일시 정지 상태의 작업만 출력
 - 아래 설명할 kill로 작업 중지 가능
![image](https://github.com/user-attachments/assets/913a3073-35d2-4562-b4ba-deadf36b3e67)

<https://gymdev.tistory.com/82>
---

### 4. kill
 - 특정 프로세스를 종료하는 데 사용
 - kill [시그널 또는 옵션] PID
 - git-bash에서 사용 가능!!
![image](https://github.com/user-attachments/assets/87543e20-ab93-41d1-a5cd-8bb00f9353cc)
[kill이 사용가능한 목록]

#### 주요 옵션
 - -l : 사용가능한 목록 표시
 - -s : 보낼 시그널 지정
![image](https://github.com/user-attachments/assets/407b0d8f-1556-4b96-ac6f-be21a6c5ae46)
[위의 실행을 kill로 종료한 모습]



