---
layout: post
title:  "[수리통계학 I] 10, 11강 요약 정리"
author: becky
categories: [ datascience ]
tags: [수리통계학, data science]
image: https://images.unsplash.com/photo-1596495577886-d920f1fb7238?q=80&w=2074&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] Some Special Distributions        
### 10, 11강 요약 정리  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[10강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=dcb7e91e6ff7098b)  
[11강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=3a6402010717e725)  


**목차**  
[1. Binomial Distribution](#binomial-distribution)  
[2. Correlation Coefficient](#correlation-coefficient)  
[3. Independent Random Variables](#independent-random-variables)  
[4. Extension to Several Random Variables](#extension-to-several-random-variables)  
[5. Transformation of Random Vectors](#transformation-of-random-vectors)  

---   

### Binomial Distribution  

1. Binomial equation  
  * $(a+b)^n = \sum_{x=0}^{n} {n\choose x} b^x a^{n-x}$  
  
  
2. Bernoulli trial (베르누이 시행)  
  * 매 결과가 S 혹은 F이며 $p= P(S)$의 확률이 일정하고, 각 시행이 독립인 일련의 실험.  
  
  * $P(X_i= 1) = p$, P(X_i= 0) = 1-p$,  $0 \leq p \leq 1$  
  * $X_i ~ B(n,p)$ 라고 부르고, n은 시행 횟수, p는 성공 확률이다.  
  
  
  * $E(X_i)= \sum_{x_i=0}^{1} X_if(x_i) = 0(1-p) + p = p$  
  * $Var(X_i)= E(X_i^2)-E^2(X_i) = p(1-p)$  
  
  * pmf of X: $P_X(x)= p^x(1-p)^{1-x} I(x=0, 1)$  
  
  
3. Pmf of binomial distribution  
  * $X_1, \cdots, X_n$을 bernoulli trials이라고 하자.  
  * $X= \sum_{i=1}^{n} X_1$는 n번 시행 중 성공의 횟수를 의미한다.  
  
  * $p(x)= {n\choose x}p^x (1-p)^{n-x} I(x= 0, 1, 2, \cdots, n)$  
  
  
  
4. mgf  
  * $M(t)= E\[e^{tX}]$  
        $= \sum_{x=0}^{n} e^{tx}{n\choose x} p^x(1-p)^{n-x}= \sum_{x=0}^{n}{n\choose x} (pe^t)^x(1-p)^{n-x}$  
        $= \[(1-p) + pe^t]^n$  
   













[Scroll to top ↑](#){: .btn .btn--primary }  







