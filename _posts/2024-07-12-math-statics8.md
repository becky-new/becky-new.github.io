---
layout: post
title:  "[수리통계학 I] 8, 9강 요약 정리"
author: becky
categories: [ datascience ]
tags: [수리통계학, data science]
image: https://images.unsplash.com/photo-1523961131990-5ea7c61b2107?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] Conditional Distribution ~ Extension      
### 8, 9강 요약 정리  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[8강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=2cea1b5099b279f6)  
[9강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=3f6f08d56688f46b)  


**목차**  
[1. Conditional Distribution](#conditional-distribution)  
[2. Correlation Coefficient](#correlation-coefficient)  
[3. Indepentent Random Variables](#indepentent-random-variables)  
[4. Extension to Several Random Variables](#extension-to-several-random-variables)  
[5. Continuous Random Variables](#continuous-random-variables)  
[6. Bayes Theorem](#bayes-theorem)  
[7. Independent](#independent)  

---  

### Conditional Distribution  

* $p_{X_2 \vert X_1}(x_2 \vert x_1) = \frac{p_{X_1}(x_1)}{p_{X_1, X_2}(x_1, x_2)}$ : conditional pmf of $X_2$ given $X_1= x_1$  
* $f_{X_2 \vert X_1}(x_2 \vert x_1) = \frac{f_{X_1}(x_1)}{f_{X_1, X_2}(x_1, x_2)}$ : conditional pdf of $X_2$ given $X_1= x_1$  

* 분자: joint / 분모: marginal  

-

* $P(a < X_2 < b \vert X_1=x_1) = \int_{a}^{b} f(x_2 \vert x_1) \, dx_2$  


* conditional mean of $u(X_2)$: $E\[u(X_2)\vert x_1]= \int_{-\infty}^{\infty} u(x_2)f(x_2\vert x_1) \, dx_2$  
* conditional var. of $X_2$: $Var(X_2\vert X_1)= E\[\lbrace X_2 - E(X_2\vert x_1)\rbrace^2 \vert x_1] = E({X_2}^2 \vert x_1) - E^2(X_2 \vert x_1)$  

-

* Double expectation theorem: $E\[E(X_2 \vert X_1)] = E(X_2)$  

* $Var\[E(X_2\vert X_1)] \leq Var(X_2) = Var\[E(X_2\vert X_1)] + E\[Var(X_2\vert X_1)]$  


---  

### Correlation Coefficient  

* $Cov(X, Y) := E\[(X_1-\mu_1)(Y-\mu_2)] = E(XY) - E(X)E(Y)$ : covariance(공분산) between X and Y  

* Corr. coef.: $\rho := \frac{Cov(X, Y)}{\sigma_1\sigma_2} = \frac{E\[(X-\mu_1)(Y-\mu_2)]}{\sigma_1\sigma_2}$  



* if $E(X\vert Y)$ is linear in $X$  
  + $E(Y\vert X) = \mu_2 + \rho\frac{\sigma_2}{\sigma_1}(X-\mu_1)$  
  + $E\[Var(Y\vert X)]= {\sigma_2}^2(1-\rho^2)$  
  

---  

### Indepentent Random Variables  

* $X$와 $Y$가 독립이다: $f_{X,Y}(x,y)= f_X(x)f_Y(y)$  

* $X$ and $Y$ is indep. $\Leftrightarrow f_{X,Y}(x,y)= g(x)h(y)$, $g(x)$와 $h(y)$가 각각 x와 y에 대한 함수  


* $X$ and $Y$ is indep. $\Leftrightarrow F_{X,Y}(x,y) = F_X(x)F_Y(y)$  


* $X$ and $Y$ is indep. $\Leftrightarrow P(a < X \leq b, c < Y \leq d) = P(a < X \leq b)P(c < Y \leq d)$  


* $X$ and $Y$ is indep. $\Rightarrow E\[u(X)v(Y)] = E\[u(X)]E\[v(Y)]$  

* $X$ and $Y$ is indep. $\Leftrightarrow M(t_1, t_2)= M(t_1,0)M(0,t_2)$  


---  

### Extension to Several Random Variables  

$\mathbf{X} = (X_1, \cdots, X_n)^T$: n-dim random vector  

* $F_{\mathbf{X}}(\mathbf{x}) = P(\mathbf{X} \leq \mathbf{x}) = P(X_1 \leq x_1, \cdots, X_n \leq x_n)$ : joint cdf  

* $Y= u(X_1, \cdots, X_n) \Rightarrow E(Y)= \int \cdots \int u(x_1,\cdots,x_n)f_{X_1,\cdots,X_n}(x_1,\cdots,x_n) \, dx_1\cdots dx_n$  
  + f_{2,\cdots,n\vert1}(x_2,\cdots,x_n \vert x_1) = \frac{f_{X_1,\cdots,X_n}(x_1,\cdots,x_n)}{f_1(x_1)}$  
  + f_{1\vert 2,\cdots,n}(x_1 \vert x_2,\cdots,x_n) = \frac{f_{X_1,\cdots,X_n}(x_1,\cdots,x_n)}{f_{X_2,\cdots,X_n}(x_2,\cdots,x_n)}$  

-
* mutually indep.이면 반드시 pairwise indep.이지만, 반대는 성립하지 않음.  

* iid: independent and identically distributed  

* $E(\mathbf{X}) = (E(X_1),\cdots,E(X_n))^T$  
* $E(\mathbf{W}) = \[E(W_{ij})]$, where $\mathbf{W}$ is mxn matrix of r.v.s  














---  


[Scroll to top ↑](#){: .btn .btn--primary }  





