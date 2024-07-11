---
layout: post
title:  "[수리통계학 I] 6, 7강 요약 정리"
author: becky
categories: [ datascience ]
tags: [수리통계학, data science]
image: https://images.unsplash.com/photo-1523961131990-5ea7c61b2107?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] Multivariate Distributions  
### 6, 7강 요약 정리  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[6강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=82ee00e4daaee27b)  
[7강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=884678081d449e34)  


**목차**  
[1. Distributions of Two Random Variables](#distributions-of-two-random-variables)  
[2. Probability Functions](#probability-functions)  
[3. Theorem](#Theorem)  
[4. Discrete Random Variables](#discrete-random-variables)  
[5. Continuous Random Variables](#continuous-random-variables)  
[6. Bayes Theorem](#bayes-theorem)  
[7. Independent](#independent)  

---   

### Distributions of Two Random Variables  

1. $(X_1, X_2)$: random vector  
  + $\mathscr{D}= \lbrace(x_1, x_2): x_1= X_1(c), x_2= X_2(c), c\in\mathscr{C}\rbrace$  
  + vector notation $\mathbf{X} = {X_1\choose X_2} = (X_1, X_2)' = (X_1, X_2)^T$  
  
  + cdf of $\mathbf{X}$  
    * $F_{X_1,X_2}(x_1, x_2) = P(X_1 \leq x_1, X_2 \leq x_2)$  
    * $P(a_1 < X_1 \leq b_1, a_2 < X_2 \leq b_2)$  
      $= F_{X_1,X_2}(b_1, b_2) - F_{X_1,X_2}(a_1, b_2) - F_{X_1,X_2}(b_1, a_2) + F_{X_1,X_2}(a_1, a_2)$  
    * ![dlalwl](https://i.imgur.com/Vu01lCi.jpeg)  
    
  
  + joint prob. mass function if $\mathbf{X}$ is discrete: $p_{X_1,X_2}(x_1, x_2) = P(X_1= x_1, X_2= x_2)$  
  + joint pdf for continuous r.v.: $f_{X_1,X_2}(x_1, x_2) = \frac{\partial^2 F_{X_1,X_2}(x_1, x_2)}{\partial x_1 \partial x_2}$  
    * $F_{X_1,X_2}(x_1, x_2) = \int_{-\infty}^{x_2} \int_{-\infty}^{x_1} f_{X_1,X_2}(w_1, w_2) \, dw_1 dw_2$  
    
  
  + Marginal of $X_1$  
    * cdf: $F_{X_1}(x_1)= \lim_{x_2 \to \infty} F_{X_1,X_2}(x_1, x_2)$  
    * pmf: $p_{X_1}(x_1)= \sum_{x_2} p_{X_1,X_2}(x_1, x_2)$  
    * pdf: $f_{X_1}(x_1)= \int_{-\infty}^{\infty} f_{X_1,X_2}(x_1, x_2) \, dx_2$  
    
    -
  
  + continuous: $E\[g(X_1, X_2)]= \iint g(x_1, x_2)f(x_1, x_2) \, dx_1 dx_2$  
    * <span style='color:#A2A2A2'> $\iint \vert g(x_1, x_2)\vert f(x_1, x_2) \, dx_1 dx_2 &lt; \infty$ </span>  
  
  + discrete: $\sum_{x_1} \sum_{x_2} g(x_1, x_2)p(x_1, x_2)$  
    + <span style='color:#A2A2A2'> $\sum_{x_1} \sum_{x_2} \vert g(x_1, x_2)\vert p(x_1, x_2) &lt; \infty$ </span>  
  
    
  + Linearity property of expectation: $E\[k_1g_1(X_1, X_2) + k_2g_2(X_1, X_2)] = k_1E\[g_1(X_1, X_2)] + k_2E\[g_2(X_1, X_2)]$  
  
  -
  
  + $M_{\mathbf{X}}(\mathbf{t}) = E\[e^{\mathbf{t}'\mathbf{X}}]$,  $\mathbf{t}= (t_1, t_2)^T$,  $||\mathbf{t}|| < h$,  $h>0$  
    $= M_{X_1, X_2}(t_1, t_2)= E\[e^{t_1X_1 + t_2X_2}]$  
    : mgf of $\mathbf{X}$  
    
    
  
#### Example 1  

$f_{X_1,X_2}(x_1, x_2)= x_1 + x_2$,  $0 < x_1 < 1$,  $0 < x_2 < 1$이다.  
$P(X_1 \leq \frac{1}{2})$와 $P(X_1 + X_2 \leq 1)$을 구해보자.  

1. $P(X_1 \leq \frac{1}{2})$  
  * $P(X_1 \leq \frac{1}{2})= P(X_1 \leq \frac{1}{2}, 0 \leq x_2 \leq 1)$  
    $= \int_{0}^{\frac{1}{2}} f_1(x_1) \, dx_1$  
  * $f_{X_1}(x_1) = \int f_{X_1,X_2}(x_1, x_2) \, dx_2$  
    $= \int_{0}^{1} (x_1 + x_2) \, dx_2 = x_1 + \frac{1}{2}$  
  
    * $\therefore P(X_1 \leq \frac{1}{2}) = \int_{0}^{\frac{1}{2}} (x_1 + \frac{1}{2}) \, dx_1= \frac{3}{8}$  
  

2. $P(X_1 + X_2 \leq 1)$  
  * $P(X_1 + X_2 \leq 1)= \int_{0}^{1} \int_{0}^{1-x_2} f_{X_1,X_2}(w_1, w_2) \, dw_1 dw_2$  
    $= \int_{0}^{1} \int_{0}^{1-x_2} (x_1+x_2) \, dw_1 dw_2 = \frac{1}{3}$  
  


#### Example 2  

$f(x_1, x_2)= 8x_1x_2I(0 < x_1 < x_2 < 1)$일 때, $E(X_1{X_2}^2)$와 $E(X_2)$ 그리고 $E\[7X_1{X_2}^2 + 5X_2]$를 구해보자.  

1. $E(X_1{X_2}^2) = \int_{0}^{1} \int{0}^{x_2} x_1{x_2}^2 8x_1 x_2 \, dx_1 dx_2 = \frac{8}{21}$  
2. $E(X_2)= \int_{0}^{1} x_2 f_{x_2}(x_2) \, dx_2 = \int_{0}^{1} x_2 \[\int_{0}^{x_2} 8x_1 x_2 \, dx_1] \, dx_2 = \frac{4}{5}$  
3. $E\[7X_1{X_2}^2 + 5X_2]= \frac{20}{3}$  










---  

[Scroll to top ↑](#){: .btn .btn--primary }  







