---
title:  "Linux 명령어 정리"
excerpt: "Linux를 사용하면서 사용되는 명령어를 정리해놓은 페이지"
toc: true
toc_sticky: true

categories:
  - Linux
tags:
  - Linux
  - command
last_modified_at: 2021-07-28T21:52:00
---

## A

* alias : 명령어를 간소화하여 다른 이름으로 사용할 수 있도록 해주는 쉘 내부 명령어

```bash
# 현재 등록되어 있는 alias 목록 
alias

# alias 등록
alias [alias_name]='[command_name]'
```

* apt-cache : 패키지 검색 도구

```bash
# 패키지 검색
apt-cache search [package_name]

# 패키지 정보 보기
apt-cache show [package_name]

# 패키지 의존성 확인
apt-cache depends [package_name]

# 패키지 역 의존성 확인
apt-cache rdepends [package_name]
```

* apt, apt-get : 데비안 계열의 리눅스에서 쓰이는 패키지 관리 명령어 도구

```bash
# 패키지 인덱스 업데이트(/etc/apt/source.list의 인덱스 정보 이용)
sudo apt-get update

# 설치된 패키지 업그레이드
sudo apt-get upgrade
sudo apt-get upgrade [package_name]

# 패키지 설치
sudo apt-get install [package_name]

# 패키지 재설치
sudo apt-get --reinstall install [package_name]

# 패키지 삭제
sudo apt-get remove [package_name]

# 패키지 완전 삭제(구성 파일 포함)
sudo apt-get purge [package_name]

# 패키지 소스코드 다운로드
sudo apt-get source [package_name]
```

## B

* bg : "background"를 나타내며, 작업을 백그라운드로 보내는 명령어, "foreground"에 해당하는 fg와 반대되는 명령어

## C

* cal : 캘린더를 띄우는 명령어

```bash
# 서버시간 기준의 연,월,일이 표시된 해당 월의 달력 표시
cal

# 해당 연도의 모든 월의 달력 표시
cal -y

# 특정 연 월 출력
cal 8 2021
```

* cat : 파일의 내용을 화면에 출력하거나 파일을 만듦

```bash
# 파일의 내용 출력
cat [fileName]
cat [fileName1] [fileName2] [fileName3] ...

# 파일의 내용 합치기(1,2,3번을 합쳐서 4번 파일을 만듦)
cat [fileName1] [fileName2] [fileName3] > [fileName4]

# 파일 내용 덧붙이기(2번의 끝에 1번을 덧붙임)
cat [fileName1] >> [fileName2]

# 새로운 파일을 만들기
cat > [new_file]
```

* cd : 해당 경로의 디렉토리로 이동함.

```bash
# path에 해당하는 위치로 이동
cd [path]

# 현재 디렉토리로 이동
cd .

# 한 단계 상위 디렉토리로 이동
cd ..

# 최상위 디렉토리로 이동
cd /
```

* chmod : 파일의 권한 변경. 숫자로 변경하는 방법만 간단하게 정리

```bash
# 모든 사용자의 모든 권한 제거
chmod 000 FILE

# 사용자(읽기+쓰기), 그룹(읽기+쓰기), 그 외 사용자(읽기)
chmod 664 FILE

# 사용자에게 모든 권한 추가
chmod 700 FILE

# 사용자(읽기+쓰기+실행), 그룹(읽기), 그 외 사용자(읽기)
chmod 744 FILE

# 사용자(읽기+쓰기+실행), 그룹(읽기+실행), 그 외 사용자(읽기+실행)
chmod 755 FILE

# 모든 사용자에 모든 권한 추가.
chmod 777 FILE
```

* chown : 파일이나 디렉터리의 소유자를 변경하는 명령어

```bash
# 파일이나 디렉토리의 소유자 변경
chown user /path/to/file_or_directory

# 파일이나 디렉토리의 소유자 및 그룹 변경
chown user:group /path/to/file_or_directory

# symbolic link의 소유자 변경
chown -h user /path/to/symboli_link

# symbolic link를 포함한 파일이나 디렉토리의 소유자와 그룹 변경
chown -hR user:group /path/to/file_or_dir
```

* cp : 파일을 복사하는 데 사용

```bash
# filename1을 복사하여 filename2를 만듦
cp [filename1] [filename2] 

# filename을 복사하여 directory안에 filename을 만듦 (directory가 존재한다고 가정)
cp [filename] [directory]
```

## D

* date : 날짜 출력 명령어

```bash
# 현재 시간 출력
date

# 표준 시간 표시하기
date -u

# format 지정 출력(YYYY-MM-DD)
date "+%Y-%m-%d"

# format 지정 출력(YYYY-MM-DD 24시간 표시,분,초)
date "+%Y-%m-%d %H:%M:%S"

# format 지정 출력(12시간 표시,분,초 오전/오후 출력)
date "+%Y-%m-%d %I:%M:%S %p"

# unix time stamp
data +%s

# 시스템 시간 설정
sudo date  "+%Y-%m-%d %H:%M:%S" -s "20200412-13:24:50"
```

* df : 시스템 전체의 디스크 여유 공간 확인

```bash
# 디스크 공간 확인
df

# 모든 파일 시스템 출력
df -a

# total 추가
df --total

# 용량 크기로 출력
df -h
```

* dmesg : 


* dpkg

* du

## E

* echo :

* exit :

## F

* fg

* find

* finger 

* free

## G

* grep

* gzip

## H

* head :

## I

* id

## J

* join

## K

* kill

## L

* lf

* ll

* ln

* locate :

* ls : 현재 디렉토리 위치의 파일 목록을 조회


## M

* man : 

* make :

* mkdir : 새로운 디렉토리를 만듬

```bash
# directoryname의 새로운 디렉토리 생성
mkdir [directoryname]

# 디렉토리를 만들 때, 하위 디렉토리까지 만들 때 사용
mkdir -p [directoryname1]/[directoryname2]
```

* more : 

* mount :

* mv : 파일을 이동시킴

## N

* nslookup

## O

* od

## P

* ps :

* pwd :

* ping :

## Q

* quit 

## R

* rm : 파일을 제거함

* rpm :

## S

* sh

* source : bash 명령어로, bash 쉘이 작동 중일 때만 동작함. filename 안의 환경설정 내용을 즉시 적용하기 위해 사용됨

```bash
source [filename]
```

* ssh

* sudo :

## T

* tail :

* tar :

* top : 

* touch : 0바이트 파일을 생성함

```bash
# filename의 0바이트 파일을 생성
touch [filename]
```

## U

* uname

* uptime 

## V

* vi

## W

* w

* wget

* whereis

* which

* whois

## X

* xdm

## Z

* zcat