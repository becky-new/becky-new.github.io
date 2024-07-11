---
layout: post
title: '[수리통계학 I] 6강 요약 정리'
author: becky
categories:
  - datascience
tags:
  - 수리통계학
  - data science
image: >-
  https://images.unsplash.com/photo-1523961131990-5ea7c61b2107?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] Important Inequalities & Multivariate Distribution  
### 6강 요약 정리  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[6강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=82ee00e4daaee27b)  
[4강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=8aec1210d15581cd)  


**목차**  
[1. Theorem 1](#theorem-1)  
[2. Markov's Inequality](#markovs-inequality)  
[3. Chebyshev Inequality](#chebyshev-inequality)  
[4. Theorem 2](#theorem-2)  
[5. Jensen's Inequality](#jensen-s-inequality)  
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

* ![dlalwl](https://i.imgur.com/FSoWJBs.jpeg)  


---  

### Chebyshev Inequality  

* Markov's 부등식의 특수한 경우!  

* $P(\vert X-\mu \vert \geq k\sigma) \leq \frac{1}{k^2}$,  $\forall k>0$  
* ![dlalwl](https://i.imgur.com/E1Utj2x.jpeg)  

---  

### Theorem 2  

* $\phi$가 $(a, b)$에서 정의된 함수이고, $-\infty \leq a < b \leq \infty$라고 하자.  
  + $\phi\[\gamma x + (1-\gamma)y \leq \gamma\phi(x) + (1-\gamma)\phi(y)$,  $\forall x, y$  in $(a,b)$  and  $0<\gamma<1$  
  + 위 식을 만족할 때, $\phi$는 convex 되었다고 한다.  
  + 부등호가 $<$이면 strictly convex 되었다고 한다.  
  
  + ![이미지](https://i.imgur.com/oBH4xiZ.jpeg)  
  
  
* Assume $\phi$ is differentiable on $(a,b)$  
  1. $\phi$: convex iff $\phi'(x) \leq \phi'(y)$,  $\forall a<x<y<b$  
  2. $\phi$: strictly convex iff $\phi'(x) < \phi'(y)$,  $\forall a<x<y<b$  
  3. $\phi$가 $(a,b)$에서 2번 미분이 가능할 때: $\phi$ is convex iff $\phi''(x) \geq 0$,  $\forall a<x<b$  
  4. $\phi$가 $(a,b)$에서 2번 미분이 가능할 때: $\phi$ is strictly convex iff $\phi''(x) > 0$,  $\forall a<x<b$  
  
  
---  

### Jensen's Inequality  

* $\phi$ is convex on an open interval $I$  
* $X$ is r.v. with support $S \subset I$ and $E(X) < \infty$  
* then, $\phi\[E(X)] \leq E\[\phi(X)]$  

* ![dlalwl](https://i.imgur.com/dCqRehN.jpeg)  


#### Example 1  

$\lbrace a_1, \cdots, a_n\rbrace$ : set of positive numbers.  
$X$를 $P(X= a_i) = \frac{1}{n}$,  $i=1,\cdots,n$에 대한 r.v.라고 하자.  

1. $E(X) = \sum_{i=1}^{n} a_i\frac{1}{n} = \bar{a}$ : Arithmetic mean (AM, 산술 평균)  

2. $-\log{x}$가 convex이므로, Jensen's ineq.를 사용할 수 있다.  
  + $-\log{\[E(X)]} = -\log{\bar{a}} \leq E\[-\log{X}]$  
  $= -\frac{1}{n}\sum\log{a_i} = -\log{(a_1,\cdots,a_n)}^{\frac{1}{n}}$  
    * i.e. $(a_1,\cdots,a_n)^{\frac{1}{n}}$: geometric mean (GE, 기하 평균) $\leq \bar{a} = \frac{1}{n}\sum a_i$  

3. $a_i$를 $\frac{1}{a_i}$로 대체하면, $(\frac{1}{a_1\cdots a_n})^{\frac{1}{n}} \leq \frac{1}{n}\sum \frac{1}{a_i}$  
  * i.e. $(a_1,\cdots,a_n)^{\frac{1}{n}} \geq \frac{1}{\frac{1}{n}\sum \frac{1}{a_i}}$ : harmonic mean (HM, 조화 평균)  
  
따라서, **$HM \leq GM \leq AM$**  


---  
















[Scroll to top ↑](#){: .btn .btn--primary }
