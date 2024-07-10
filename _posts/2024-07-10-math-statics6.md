---
layout: post
title:  "[수리통계학 I] 6강 요약 정리"
author: becky
categories: [ datascience ]
tags: [수리통계학, data science]
image: https://images.unsplash.com/photo-1523961131990-5ea7c61b2107?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] Important Inequalities & Multivariate Distribution  
### 6강 요약 정리  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[6강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=82ee00e4daaee27b)  
[4강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=8aec1210d15581cd)  


**목차**  
[1. Random Variables](#ramdon-variables)  
[2. Probability Functions](#probability-functions)  
[3. Theorem](#Theorem)  
[4. Discrete Random Variables](#discrete-random-variables)  
[5. Continuous Random Variables](#continuous-random-variables)  
[6. Bayes Theorem](#bayes-theorem)  
[7. Independent](#independent)  

---  

### Theorem 1  

$E(X^m)$이 존재한다면 $k \leq m$에 대해 $E(X^k)$도 존재한다.  
  * <span style='color:#A2A2A2'> prove: $\int (\vert x \vert)^kf(x) \, dx &lt; \infty$ </span>  
  

---  

### Markov's Inequality  

* $u(X)$: r.v.$X$의 non-negative function  
* $E\[u(X)]$가 존재한다고 하면, $\forall c > 0$,  $P\[u(X) \geq c] \leq \frac{E\[u(X)]}{c}$  

* ![dlalwl](https://i.imgur.com/DlHmO9r.jpeg)  
* <span style='color:#A2A2A2'>$E\[u(X)] = \int u(x)f(x) \, dx = \int_{A} u(x)f(x) \, dx + \int_{A^C} u(x)f(x) \, dx = \cdots$ </span>  

---  

### Chebyshev Inequality  















[Scroll to top ↑](#){: .btn .btn--primary }  







