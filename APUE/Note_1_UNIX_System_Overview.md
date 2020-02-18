# UNIX System Overview

## 1.1 Intro
没啥奇怪的知识

## 1.2 UNIX Architecture
一些奇怪的知识：
- __OS__ regarded as __Software__
- __Kernel__ is small
- __Ring-0__ concept belong to 分级保护域 (英语：hierarchical protection domains)
![protectiondomains](./Note_1_img/450px-Priv_rings.svg.jpg "Hierarchical Protection Domains")
- __Kernel__ in __Ring-0__
- __System Call__ between kernel and application/software
![ArchitectureUNIXOS](./Note_1_img/Architecture_of_the_UNIX_operating_system.jpg "Architecture of the UNIX operating system")
- __System Call(系统调用)__ regarded as __Interface__ of Kernel
- __Library Routines(公用函数库)__ base on System Call
- Application could call __"System Call" and "Library Routines"__
- 应用层软件可以调用系统调用与公用函数库
- __Shell__ is __special__ application as interface between application and system
- __OS__ including kernel & software in broad sense
__(software: system utility+app+shell+library routines)__

奇怪且刷新认知：
- GNU是操作系统（系列）
- Linux是GNU的kernel
- Linux的严格称呼GNU/Linux
- 不严格也是OK的
__(It  also  hasthe advantage of being moresuccinct.) I like it !__

## 1.3 Logging in
总觉得登录没啥奇怪的知识：

> We need what ?
> - login name
> - password
### 1.3.1 Logging Name

已存密码放在 /etc/passwdzhong

> It's composedof  seven  colon-separated  fields:  
> - __the  login  name__ (登录名)
> - __encrypted  password__ (加密过的密码)
> - __numeric  user  ID(205)__ (用户ID)
> - __numeric group ID(105)__ (用户组ID)
> - __acomment field__ (注释字段 啥玩意啊？？？)
> - __home directory (/home/sar)__  (开始目录)
> - __shellprogram (/bin/ksh)__  (选定启用哪个shell)
> - ___sar:x:205:105:Stephen Rago:/home/sar:/bin/ksh___

### 1.3.2 Shell (其实我不喜欢他command-line-type)

只要用户登陆了，不管接下来显示什么系统信息等，之后一定会以shell提示结束并等待用户输入。
> Shell is what ???
> - A command-line interpreter
> - It could read user input
> - Execute command(shell script)->app/system call/library routines

我只认__(ba)sh__，__(t)csh__ 花里胡哨特性增增减减，source环境和bash等经常冲突，javaVM也踩csh坑，别那么乱七八糟求你了md，你在干活不是在自己玩。蛇皮（

__各种shell历史轨迹（包袱）：__
> - The C shell, developed by Bill Joy at Berkeley, is provided with all the BSD releases.Additionally,the  C  shell  was  provided  by  AT&T  with  System  V/386  Release  3.2  andwas  also  included  in  System  V  Release  4(SVR4). 
>> 所以这也是一方面我不用bsd的原因虽然现在也没有这方面的问题了

>> CSH: Its control flow looks morelike the C language 但好的feature还是得品的，短程作业控制我用过

> - The  Bourne-again  shell  is  the  GNU  shell  provided  with  all  Linux  systems.  It  wasdesigned  to  be  POSIX  conformant,  while  still  remaining  compatible  with  the  Bourneshell.  It supports features from both the C shell and the Korn shell.
>> 总之一句话：__POSIX 1003.2__ 规范化是真的好，bash天下第一




