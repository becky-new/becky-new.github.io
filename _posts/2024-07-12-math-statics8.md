---
layout: post
title:  "[수리통계학 I] 8강 요약 정리"
author: becky
categories: [ datascience ]
tags: [수리통계학, data science]
image: https://images.unsplash.com/photo-1523961131990-5ea7c61b2107?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] Conditional Distribution and Expectation    
### 8강 요약 정리  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[8강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=2cea1b5099b279f6)  


**목차**  
[1. Conditional Distribution](#conditional-distribution)  
[2. Probability Functions](#probability-functions)  
[3. Theorem](#Theorem)  
[4. Discrete Random Variables](#discrete-random-variables)  
[5. Continuous Random Variables](#continuous-random-variables)  
[6. Bayes Theorem](#bayes-theorem)  
[7. Independent](#independent)  

---  

### Conditional Distribution  

* $p_{x_2 \vert x_1}(x_2 \vert x_1) = \frac{p_{x_1}(x_1)}{p_{x_1, x_2}(x_1, x_2)}$ : conditional pmf of $X_2$ given $X_1= x_1$  
* $f_{x_2 \vert x_1}(x_2 \vert x_1) = \frac{f_{x_1}(x_1)}{f_{x_1, x_2}(x_1, x_2)}$ : conditional pdf of $X_2$ given $X_1= x_1$  

* 분자: joint / 분모: marginal  


* $P(a < X_2 < b \vert X_1=x_1) = \int_{a}^{b} f(x_2 \vert x_1) \, dx_2$  


* conditional mean of $u(X_2)$: $E\[u(X_2)\vert x_1]= \int_{-\infty}^{\infty} u(x_2)f(x_2\vert x_1) \, dx_2$  
* conditional var. of $X_2$: $Var(X_2\vert X_1)= E\[\lbrace X_2 - E(X_2\vert x_1)\rbrace^2 \vert x_1] = E({X_2}^2 \vert x_1) - E^2(X_2 \vert x_1)$  


* Double expectation theorem: $E\[E(X_2 \vert X_1)] = E(X_2)$  

* $Var\[E(X_2\vert X_1)] \leq Var(X_2) = Var\[E(X_2\vert X_1)] + E\[Var(X_2\vert X_1)]$  


---  

### Correlation Coefficient  

* $Cov(X, Y) := E\[(X_1-\mu_1)(Y-\mu_2)] = E(XY) - E(X)E(Y)$ : covariance(공분산) between X and Y  

* Corr. coef.: $\rho := \frac{Cov(X, Y)}{\sigma_1\sigma_2} = \frac{E\[(X-\mu_1)(Y-\mu_2)]}{\sigma_1sigma_2}$  











---  


[Scroll to top ↑](#){: .btn .btn--primary }  





