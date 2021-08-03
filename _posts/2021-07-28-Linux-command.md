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

* alias

* apt, apt-get

## C

* cat : 파일의 내용을 화면에 출력하거나 파일을 만듦

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

* chmod :

* cp : 파일을 복사하는 데 사용

```bash
# filename1을 복사하여 filename2를 만듦
cp [filename1] [filename2] 

# filename을 복사하여 directory안에 filename을 만듦 (directory가 존재한다고 가정)
cp [filename] [directory]
```

## E

* echo :


## F

* find

## G

* grep

## L

* ll

* ln

* locate :

* ls : 현재 디렉토리 위치의 파일 목록을 조회


## M

* mkdir : 새로운 디렉토리를 만듬

```bash
# directoryname의 새로운 디렉토리 생성
mkdir [directoryname]

# 디렉토리를 만들 때, 하위 디렉토리까지 만들 때 사용
mkdir -p [directoryname1]/[directoryname2]
```

* mv : 파일을 이동시킴

## P

* pwd :

## R

* rm : 파일을 제거함

## S

* source : bash 명령어로, bash 쉘이 작동 중일 때만 동작함. filename 안의 환경설정 내용을 즉시 적용하기 위해 사용됨

```bash
source [filename]
```

* sudo :

## T

* tar :

* touch : 0바이트 파일을 생성함

```bash
# filename의 0바이트 파일을 생성
touch [filename]
```

## W

* wget