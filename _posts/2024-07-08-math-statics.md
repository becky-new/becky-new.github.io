---
layout: post
title:  "[수리통계학 I] 1~2강 요약 정리"
author: becky
categories: [ datascience ]
tags: [수리통계학, data science]
image: https://images.unsplash.com/photo-1523961131990-5ea7c61b2107?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] 1, 2강  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[강의 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=ab9a991198792450)  


---  

### 기본 개념  

* Statistical(Random) experiment: 실험 수행 전 결과를 100% 확신할 수 없는 실험. 동전을 던진다고 했을 때, 확률이 얼마가 될지는 예측할 수 있어도 반드시 앞면이 나올 것이라 말할 수는 없다.  
* Sample space $\Omega$: 표본 공간. Random experiment의 가능한 모든 경우를 모아둔 집합이다.  
* Event: sample의 부분 집합.  


### Set Theory  

* $C_1 \subset C_2$: $C_1$은 $C_2$의 subset(부분집합).  
* Null(empty) set: $\emptyset$으로 표현되며, set C가 아무 요소가 없을 때 공집합이라고 한다.  
---
* $C_1 \cup C_2$: $C_1$과 $C_2$의 합집합.  
  + $\bigcup_{k=1}^{\infty} C_k = C_1 \cup C_2 \cup C_3 \cdots \cup C_n$  
  
  + $C_k= {x: 1/(k+1) \leq x \leq 1}$일 때, $\bigcup_{k=1}^{\infty} C_k= {x: 0 < x \leq 1}$  
    - 임의의 k에 대해 $1/(k+1) > 0$이므로 0과 같을 수는 없다.  
    
    
---
* $C_1 \cap c_2$: $C_1$과 $C_2$의 교집합.  
  + $\bigcap_{k=1}^{\infty} C_k = C_1 \cap C_2 \cap C_3 \cdots \cap C_n$  
  
  + $C_k= {x: 0 < x < 1/k}$일 때, $\bigcap_{k=1}^{\infty} C_k= \emptyset$  
    - 임의의 x에 대해, $1/k < x$인 0보다 큰 k가 존재한다. (x를 아무리 작게 해도 그것보다 작아지도록 만드는 k는 존재한다.)  
    
---
* $\overline{C}$: 표본 공간 $\Omega$의 부분 집합 C의 여집합(여사건)  

* Point function: 정의역이 point일 때.  
* Set function: 정의역이 set일 때.  


### Integral  

* $\iint_C f(x,y) \, dxdy$  
* k-fold integration: $\iint \cdots \int f(x_1,x_2,\cdots,x_k) \, dx_1,dx_2,\cdotsdx_k$  
* 






[Scroll to top ↑](#){: .btn .btn--primary }   


