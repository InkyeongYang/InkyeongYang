---
layout: post
title:  "C  개발환경 설정하기 (Visual Studio Code)"
date:   2021-02-22 00:48:10 +0530
categories: C VSCode CentOS7
---
C언어 공부를 위한 개발환경을 만들며 알게된 내용을 기록합니다. 

다음과 같은 조건으로 개발환경을 구축하였습니다.

- Cent OS 7
- gcc 4.8.5
- Visual Studio Code

C언어의 컴파일러인 gcc패키지를 설치합니다.

```bash
$ yum install -y gcc
```
gcc커맨드를 이용해서 버전을 확인해 봅니다.
```bash
$ gcc --version
gcc (GCC) 4.8.5 20150623 (Red Hat 4.8.5-44)
Copyright (C) 2015 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```
정상적으로 설치된 것은 확인하기 위해 "Hello C language world!"라는 문자열을 출력하는 간단한 코드를 작성합니다. C프로그램은 확장자 ".c"인 소스파일을 통해 만들어집니다.
```c++
#include <stdio.h>

int main(void)
{
    printf("Hello C language world!\n");

    return 0;
}
```
커맨드 라인에서 소스파일을 직접 컴파일 해 보면 컴파일러의 실행을 통해 "a.out"라는 목적파일이 생성되는 것을 확인할 수 있습니다. a.out이라는 파일명은 assempler output의 줄임말이다. [a.out위키페이지][a-out-wiki]

```bash
$ gcc smaple.c
$ ls
a.out	sample.c
```
다음의 커맨드를 실행해서 실행파일을 생성합니다.
```bash
$ gcc sample.c -o smaple
$ ls
a.out	sample	sample.c
```
실행파일을 실행해서 소스파일에 작성했던 문자열이 출력되는 것을 확인합니다.
```bash
$ ./sample
Hello C language world!
```

컴파일러가 문제없이 설치된 것을 확인했으니 다음은 에디터에 연결해서 빌드 하는 방법을 확인해 봅니다.
다양한 에디터를 취향에 맞게 선택해서 사용하시면 됩니다. 저는 VS Code를 사용하고 있기때문에, VS Code를 이용한 방법을 소개합니다.


[a-out-wiki]:https://ko.wikipedia.org/wiki/A.out
