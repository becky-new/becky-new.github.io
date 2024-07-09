---
layout: post
title:  "[수리통계학 I] 3강 요약 정리"
author: becky
categories: [ datascience ]
tags: [수리통계학, data science]
image: https://images.unsplash.com/photo-1523961131990-5ea7c61b2107?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] Random Variables  
### 3강 요약 정리  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[3강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=0eb108cf6ad31136)  


**목차**  
[1. 기본 개념](#기본-개념)  
[2. Set theory](#set-theory)  
[3. Integral](#integral)  
[4. Probability Set Function](#probability-set-function)  
[5. Conditional Probability](#conditional-probability)  
[6. Bayes Theorem](#bayes-theorem)  
[7. Independent](#independent)  

---  

### Random variables  

* Random: **일정한 규칙(확률)과 매치된**  
* Random variable: **확률 변수**  


* Random variable(r.v.): 각 요소 $c \in \mathscr{C}$이고 일대일 대응되는 (one and only one) $X(c)= x$인 function X  
* 도메인 $\mathscr{D} = \{x: x= X(c), c \in \mathscr{C}\}$  

* $\mathscr{D}$가 countable set일 때: discrete random variables  
* $\mathscr{D}$가 interval of real numbers일 때: continuous random variables  


![이미지](https://i.imgur.com/izXqMaM.jpeg)  

* Probability function $P$가 $\mathscr{B}$에서 정의되었다고 하면, $\mathscr{F}$에서 정의된 probability function $P_X$를 정의할 수 있다. $P_X$는 $r.v. X$에 의해 induced 된 probability function으로 불린다.  

* 즉, $P(C), C \in \mathscr{B}, P_X(B), B \in \mathscr{F}$  
   i.e. $P_X(B)= P\[c \in \mathscr{C} : X(c) \in B\], B \in \mathscr{F}$  
   
   
---  

### Probability Functions  
* Probability Mass Function (PMF): $P_X(d_i) = P(X= d_i), i=1, \cdots, m$  

* Cumulative Distribution Function (CDF): $F_X(x)= P_X((-\infty, x\])= P(X \leq x)$  


#### Example  

Fair dice를 던지는 경우를 X라고 해보자. X의 CDF는 어떻게 될까?   
* Fair dice: $P_X(1)= P_X(2)= \cdots = P_X(6)= \frac{1}{6}$  

$\textit{Sol}$  
![dlalwl](https://i.imgur.com/NxGugvt.jpeg)  

![dlalwl](https://i.imgur.com/7tdiBI6.jpeg)  

이러한 CDF를 step function이라 부르고, 이는 non-decreasing 하는 특징이 있다. (일정한 구간이 있으므로 increasing은 아니다!)  


위 경우의 PMF는 아래 그래프와 같다.  

![이미지](https://i.imgur.com/NME75wE.jpeg)  


#### Example 2  

X는 (0,1)의 continuous variable이라고 하고, $P_X\[(a,b)\] = b-a$  for, $0 < a < b < 1$이라 할 수 있다.  
r.v. $X$의 CDF를 구하면 아래와 같다.

$F_X(x)= 0 & \text{if } x < 0 \\ x & \text{if } 0 \leq x < 1 \\ 1 & \text{if } x \geq 1 \end{cases} $






[Scroll to top ↑](#){: .btn .btn--primary }  

