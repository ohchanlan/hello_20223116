## 20223116 오찬란
---
- 리눅스 명령어 top
- 리눅스 명령어 ps
- 리눅스 명령어 jobs
- 리눅스 명령어 kill
- vim 에디터에서의 매크로 사용법
---
**리눅스 명령어 top**

실시간으로 CPU 사용률을 체크해주는 명령어 (윈도우의 작업관리자와 비슷)

리눅스를 사용하는 서버의 성능이나 현재 돌아가고 있는 상황을 볼 때 사용

***top 명령어 옵션***

shift + p : CPU 사용률이 높은 프로세스 순서대로 표시

shift + m : 메모리 사용률이 높은 프로세스 순서대로 표시

shift + t : 프로세스가 돌아가고 있는 시간 순서대로 표시

a : 메모리 사용량에 따라 정렬

b : Batch 모드 작동

c : 명령행 / 프로그램 이름 토글

s : 보안 모드 작동

S : 누적 시간 모드 토글

등등...

**리눅스 명령어 ps**

현재 실행중인 프로세스 목록을 보여주는 명령어

아파치, 오라클 등 프로그램 프로세스가 정상적인지 확인하거나 비정상적인 프로세스가 올라왔는지 확인하는 등 리눅스 관리 전반적으로 많이 사용되는 명령어

주로 파이프라인, grep 명령어와 함께 사용하여 특정 프로세스를 확인하는 데 사용됨

***ps 명령어 옵션***

-A : 모든 프로세스 출력

a(BSD계열) : 터미널과 연관된 프로세스 출력, 보통 x 옵션과 연계하여 모든 프로세스를 출력할 때 사용

-a : 세션 리더를 제외하고 데몬 프로세스처럼 터미널에 종속되지 않은 모든 프로세스 출력

-e : 커널 프로세스를 제외한 모든 프로세스 출력

-f : 풀 포맷으로 보여줌, 유닉스 스타일로 출력해주는 옵션으로 UID, PID, PPID 등이 함께 표시됨

-M : 64비트 프로세스들을 보여줌

-p : 특정 PID를 지정할 때 사용

-u : 특정 사용자의 프로세스 정보를 확인할 때 사용, 사용자를 지정하지 않으면 현재 사용자를 기준으로 정보 출력

System V 계열에서는 'ps -ef'를 가장 많이 사용

BSD 계열에서는 'ps aux'를 가장 많이 사용

**리눅스 명령어 jobs**

현재 세션의 작업 상태(작업이 중지된 상태, 백그라운드로 진행 중인 상태 등)를 출력하는 명령어

***jobs 명령어 옵션***

-l : 프로세스 그룹 ID를 state 필드 앞에 출력

-n : 프로세스 그룹 중에 대표 프로세스 ID를 출력

-p : 각 프로세스 ID에 대해 한 행씩 출력

command : 지정한 명령어를 실행

**리눅스 명령어 kill**

프로세스를 죽이는(종료시키는) 명령어

프로세스에 시그널을 보내 원하는 작업을 하게 하는 명령어

시그널 : 인터럽트의 일종으로 어떤 이벤트의 발생을 프로세스에게 알려주는 것, 리눅스에서 프로세스끼리 통신할 때 사용

***kill 명령어 옵션***

-l : 시그널의 종류 출력

-s signal : 시그널의 이름 지정

-s 옵션으로 시그널을 지정하지 않으면 기본 시그널 값이 정상종료(SIGTERM,15)

프로세스를 안전하게 종료하기 위해서는 'kill -9 pid', 'kill -SIGKILL pid' 형태의 프로세스 강제종료를 권장하지 않음 (데이터 유실 위험)



