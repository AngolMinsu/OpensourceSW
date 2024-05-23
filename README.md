# OpensourceSW
This is HomeWork README.md
## top
현재 OS의 상태를 나타내주는 CLI 어플리케이션
![image](https://github.com/AngolMinsu/OpensourceSW/assets/106021108/5db70e6e-cb1d-4e29-b6a4-a50695baff43)
맨 윗줄부터

`시스템 현재시간, OS가 살아있는 시간, 유저 세션 수`

`총 작업수, 현재 실행중인 작업수, 자고있는 작업수, 멈춘 작업수, 좀비작업수`

`CPU 점유율`

`메모리 점유율`

로 구분되어있다.
윈도우 OS의 작업관리자에서 나오는 목록과 비슷하다고 보면 된다

## ps
Process Status
현재 구동중인 프로세스 정보를 확인할 수 있다.
![image](https://github.com/AngolMinsu/OpensourceSW/assets/106021108/e580ca6b-f8d1-4d27-ac3d-77d40efb785c)
* 옵션
*  
  `-e` : 모든 사용자가 구동시킨 프로세스를 보여줌
  
  `-f` : 자세한 내용을 보여줌

  `-l `: -f 보다 더 자세히 보여줌

* ps -efl 실행 예시
![image](https://github.com/AngolMinsu/OpensourceSW/assets/106021108/419c1a47-6e96-4839-8c18-bc7c9018c5b8)
* F : 프로세스 플래그
* 
  `4: used super-user privileges`

  `1: forked ut didn't exec`
  
  `5 : 4,1 둘 다 아님`
  
  `0 : 어느 플래그도 아님`
  
* S : 프로세스의 현재 상태
* 
  `R: 실행 중 혹은 실행 가능 상채`
  
  `S: 대기`

  `I: 짧은 대기`

  `T: 작업 제어에 의한 정지`

  `D: 디스크 관련 대기`

  `P: 페이지 관련 대기 `

  `X: 메모리 확보를 위한 대기`

  `>: 인위적으로 우선순위가 높아짐`

  `Z: 좀비 프로세스`

## jobs
쉘에서 실행한 프로세스 목록을 확인하는 명령어
![Pasted image 20240520135334](https://github.com/AngolMinsu/OpensourceSW/assets/106021108/313f19da-29e9-40d8-ac1e-96aea01359d5)

그냥 실행하면 아무것도 안나온다

백그라운드에 ss.sh를 실행시킨 후 jobs를 실행
![image](https://github.com/AngolMinsu/OpensourceSW/assets/106021108/ff69d082-8383-44f4-b622-342606c72188)

jobs /option/ /job/ 으로 사용한다
*  `-l` 옵션: 프로세스 ID와 함께 작업 목록을 출력
- `-n` 옵션: 마지막로 알림 이후 변경된 작업 출력
- `-p` 옵션: 작업 프로세스 ID만 출력
- `-r` 옵션: 실행 중인 작업만 출력
- `-s` 옵션: 중지된 작업만 출력
## kill
프로세스를 종료하는 명령어
kill /option/ PID로 사용한다
 * 옵션

 `-s : 특정 시그널을 사용하여 프로세스를 종료`

 `-l, --list : 지원되는 시그널 목록을 출력`

 `-a, --all : 현재 사용자에 속한 모든 프로세스를 종료`

 `-q, --queue : 프로세스에 시그널을 보내는 대신 시그널을 대기열에 추` 
* 신호
* ![Pasted image 20240520140034](https://github.com/AngolMinsu/OpensourceSW/assets/106021108/87b7631c-89f9-47d8-895d-ca40b6415168)

*kill을 사용하여 아까 실행시킨 ss.sh를 종료*
![image](https://github.com/AngolMinsu/OpensourceSW/assets/106021108/a465bca2-2b92-4e1b-8b22-c1c007a210be)

*kill을 사용하여 python3(PID : 553)을 종료*
![Pasted image 20240520140303](https://github.com/AngolMinsu/OpensourceSW/assets/106021108/513111ae-2f4a-4474-bcc0-8bd3928a1b9e)

*kill을 사용하여 gitstatusd-linu를 종료*
![Pasted image 20240520140441](https://github.com/AngolMinsu/OpensourceSW/assets/106021108/65c3b126-7cd5-4415-9409-c73a11295b30)
