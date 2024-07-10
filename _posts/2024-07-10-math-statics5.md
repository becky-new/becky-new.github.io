---
layout: post
title:  "[수리통계학 I] 5강 요약 정리"
author: becky
categories: [ datascience ]
tags: [수리통계학, data science]
image: https://images.unsplash.com/photo-1523961131990-5ea7c61b2107?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] Expectation of a Random Variable  
### 4, 5강 요약 정리  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[4강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=8aec1210d15581cd)  
[5강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=5bc0510cab27c26c)  


**목차**  
[1. Expectation of a Random Variable](#expectation-of-a-random-variable)  
[2. Some special Expectations](#some-special-expectations)  
[3. Theorem](#Theorem)  
[4. Discrete Random Variables](#discrete-random-variables)  
[5. Continuous Random Variables](#continuous-random-variables)  

---   

### Expectation of a Random Variable  

* $E(x)= \int_{-\infty}^{\infty} xf_X(x) \, dx$,  $if \int_{-\infty}^{\infty} \vert x \vert f_X(x) \, dx < \infty (conti.)$  
* $E(x)= \sum_{x \in S_X} x p_X(x)$,  $if \sum \vert x \vert p(x) < \infty (discrete)$  


* $Y= g(X)$의 expectation은 다음과 같다.  
  1. $E\[g(X)]= \int_{-\infty}^{\infty} g(x)f_X(x) \, dx$  $if \int_{-\infty}^{\infty} \vert g(x) \vert f_X(x) \, dx < \infty (conti.)$  
  2. $E\[g(X)]= \sum_{x \in S_X} g(x) p_X(x)$  $if \sum \vert x \vert p(x) < \infty (discrete)$  

* Linear property of expectation: $E\[k_1 g_1(X) + k_2 g_2(X)] = k_1E\[g_1(X)] + k_2E\[g_2(X)]$,  if $E\[g_1(X)]$ and $E\[g_2(X)]$ exist  


<span style='color:#A2A2A2'> Triangular inequality: $\vert a+b \vert \leq \vert a \vert + \vert b \vert$ </span>



---  

### Some special Expectations  

1. $\mu = E(X)$ : **population** mean of r.v. $X$  
2. $\sigma^2 = E(X-\mu)^2$ : variance of r.v. $X$  
  * $\sigma^2 = E(X^2) - (\lbrace E(X) \rbrace)^2$  
3. $\sigma = \sqrt{\sigma^2}$ : standard variation  
4. Moment Generating Function (mgf, 적률 생성 함수): $M_X(t) = E(e^{tX}) = \int_{\infty}^{\infty} e^{tx}f(x) \, dx$  
  * <span style='color:#A2A2A2'> $E(e^{tX}) &lt; \infty$,  $\vert t \vert &lt; h$ for some $h&gt;0$ </span>  


* $E(x^k)$ : k-th moment (k차 적률)  
* $E\[(x-k)^k]$ : k-th central moment  
* Uniqueness of mgf: $F_X(z) = F_Y(z)$,  $\forall z \in R$,  
$iff M_X(t) = M_Y(t)$,  $\forall t \in (-h,h)$, $h>0$  


---  

### Taylor Expansion  

"**다항식의 합의 모양**으로 나타낼 수 있다!"  

i. 1차원: $f: R^1 \rightarrow R^1$,  infinitely differentiable at $x= x_0$  
  + $f(x)= f(x_0) + \frac{f'(x_0)}{1!}(x-x_0)^1 + \frac{f''(x_0)}{2!}(x-x_0)^2 + \cdots$  
  $= \sum_{j=0}^{\infty} \frac{f^{(j)}(x_0)}{j!}(x-x_0)^j$  
  
  + As a special case: $f(x)= \sum_{j=0}^{k} \frac{f^{(j)}(x_0)}{j!}(x-x_0)^j + \frac{f^{(k+1)}(\xi)}{(k+1)!}(x-x_0)^{k+1}$ = **leading term + remainder term**  
  + $\xi$: $x$와 $x_0$ 사이의 값  
  
ii. d차원 $\rightarrow$ 1차원: $f: R^d \rightarrow R^1$,  infinitely differentiable at $\mathbf{x}= \mathbf{x_0}$  
  + $f(\mathbf{x})= f(\mathbf{x_0}) + \nabla f(\mathbf{x_0})^T (\mathbf{x}-\mathbf{x_0}) + \frac{1}{2!} (\mathbf{x}-\mathbf{x_0})^T H(\mathbf{x}-\mathbf{x_0}) + R_n$  
  where $\nabla f(x) = \frac{\partial f(x)}{\partial x}$,  $H= \frac{\partial^2 f(x)}{\partial x \partial x^2}$  
  
iii. d차원 $\rightarrow$ p차원: $f: R^d \rightarrow R^1$,  infinitely differentiable at $\mathbf{x}= \mathbf{x_0}$  
  + ii와 비슷하게 진행  
  
  
---  

### Remark   

1. mgf may not exist : example pdf $f(x) = \frac{1}{x^2} I(x>1)$  

2. Sometimes, pdf can be found from the mgf  
  * $M_X(t)= \frac{1}{10} e^t + \frac{2}{10} e^{2t} + \frac{3}{10} e^{3t} + \frac{4}{10} e^{4t}$ 이라고 하자.  
  * $M_X(t) = \sum e^{tx}p(x) = p(1)e^t + p(2)e^{2t} + p(3)e^{3t} + p(4)e^{4t}$  
  * by the uniqueness of polynomial coeff $\rightarrow p(x)= \frac{x}{10}$,  $x= 1,2,3,4$  
    + <span style='color:#A2A2A2'> uniqueness of polynomial coefficient: $a_0 + a_1x + a_2x^2 + \cdots = b_0 + b_1x + b_2x^2 + \cdots$,  $\forall x \Rightarrow a_i = b_i$,  $i= 0,1,2,\cdots,n$ </span>  
    
    
3. mgf를 이용해 $E(X^m)$을 계산할 수 있다.  
  * $M_X(t) = E(e^{tX}) = E\[1 + tX + \frac{t^2 X^2}{2!} + \frac{t^3 X^3}{3!} + \cdots]$  
  $= 1+ tE(X) + \frac{t^2}{2!} E(X^2) + \cdots$  
  * $\therefore M_X^{(m)}(0) = E(X^m)$  













[Scroll to top ↑](#){: .btn .btn--primary }  



