---
layout: post
title:  "[수리통계학 I] 3, 4강 요약 정리"
author: becky
categories: [ datascience ]
tags: [수리통계학, data science]
image: https://images.unsplash.com/photo-1523961131990-5ea7c61b2107?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
use_math: true
---

## [수리통계학 I] Random Variables  
### 3, 4강 요약 정리  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[3강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=0eb108cf6ad31136)  
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

### Random variables  

* Random: **일정한 규칙(확률)과 매치된**  
* Random variable: **확률 변수**  


* Random variable(r.v.): 각 요소 $c \in \mathscr{C}$이고 일대일 대응되는 (one and only one) $X(c)= x$인 function X  
* 도메인 $\mathscr{D} = \lbrace x: x= X(c), c \in \mathscr{C} \rbrace$  

* $\mathscr{D}$가 countable set일 때: discrete random variables  
* $\mathscr{D}$가 interval of real numbers일 때: continuous random variables  


![이미지](https://i.imgur.com/izXqMaM.jpeg)  

* Probability function $P$가 $\mathscr{B}$에서 정의되었다고 하면, $\mathscr{F}$에서 정의된 probability function $P_X$를 정의할 수 있다. $P_X$는 $r.v. X$에 의해 induced 된 probability function으로 불린다.  

* 즉, $P(C), C \in \mathscr{B}, P_X(B), B \in \mathscr{F}$  
   i.e. $P_X(B)= P\[c \in \mathscr{C} : X(c) \in B\], B \in \mathscr{F}$  
   
   
---  

### Probability Functions  
* Probability Mass Function (PMF): $P_X(d_i) = P(X= d_i), i=1, \cdots, m$  
* PMF: <u>이산 확률 변수</u>에서 특정 값에 대한 확률을 나타내는 함수  

* Cumulative Distribution Function (CDF): $F_X(x)= P_X((-\infty, x\])= P(X \leq x)$  

* Probability Density Function (PDF): $f_X(x) = \frac{d}{dx} F_X(x)$  
* PDF: <u>연속 확률 변수</u>에서 특정 구간에 속할 확률을 계산하기 위한 함수  


#### Example 1  

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

$F_X(x) = \begin{cases}
0 & \text{if } x < 0 \\ ,  
x & \text{if } 0 \leq x < 1 \\  ,  
1 & \text{if } x \geq 1  
\end{cases} $  

* 이 CDF는 continuous uniform distribution이라고 한다.  


### Theorem  

* Properties of CDF  
  1. $F(a) \leq F(b), \forall a < b$ (non-decreasing)  
  2. $\lim_{x\to-\infty} F(x) = 0$  
  3. $\lim_{x\to\infty} F(x) = 1$  
  4. $\lim_{x \to x_0+} F(x) = F(x_0)$ (right continuous)  

* $P(a < X \leq b)= F_X(b) - F_X(a)$, $\forall a < b$  

* $P(X= x) = F_X(x) - F_X(x-)$, $F_X(x-) = \lim_{z\to x-} F_X(z)$  


---   

### Discrete Random Variables  

* Discrete Random Variable: its space is either **finite** or **countable**  

* Probability Mass Function (PMF) of a discrete r.v. $X$ with space $\mathscr{D}$: $P_X(x)= P(X=x), x \in \mathscr{D}$  

* Support of X: $S_X= \lbrace x: P_X(x) > 0 \rbrace$  


* $X$의 PMF를 알고 있고, $g$가 일대일 대응일 때, $Y= g(X)$의 PMF를 구해보자.  
$P_Y(y)= P(Y=y) = P\[g(X)=y\] = P(X= g^{-1}(y)) = P_X(g^{-1}(y))$  



#### Example 1  

Fair coin을 던진다고 하고, X를 앞면이 나오는 경우의 수라고 하자. 이때 X의 PMF는,  
$P(X=x) = (\frac{1}{2})^{x-1} (\frac{1}{2}) = (\frac{1}{2})^x$ , $x= 1, 2, 3, \cdots $  

+ 이는 $2^{-x} I(x=1, 2, 3, \cdots)$ 으로 표현할 수 있다. $I(x)$는 indicator function이다.  


#### Example 2  

20개의 흰 공, 80개의 검은 공으로 총 100개의 공이 있다고 하자. 우리가 5개 공을 뽑을 때 흰 공의 개수를 X라고 하면, X의 PMF는  
$P_X(x) = \frac{\binom{20}{x} \binom{80}{5-x}}{\binom{100}{5}} , x= 0, 1, 2, 3, 4, 5$  


#### Example 3  

$Y= X-1$이고 $P_X(x) = (\frac{1}{2})^x, x=1,2,\cdots$일 때 PMF를 구해보자.  

$g(x)= x-1 \Rightarrow g^{-1}(y) = y+1$ 이므로, $P_Y(y) = P_X(y+1) = (\frac{1}{2})^{y+1}, y= 0,1,2,\cdots$  

* y의 범위를 잊지 말자!  
* 이 분포를 geometric distribution이라 한다.  


---  

### Continuous Random Variables  

* Continuous random variable: <u> CDF $F_X(x)$ is continuous </u>, $\forall x \in R$  

* CDF $F_X(x)= \int_{-\infty}^{x} f_X(t) \, dt$ 이고, $f_X(t)$는 probability density function (PDF)로 불린다.  

* $f_X(x) = \frac{d}{dx} F_X(x)$  

* Continuous variable에서, $P(X=x) = F_X(x) - F_X(x-) = 0$  
* Continuous variable에서, $P(a < X \leq b) = F_X(b) - F_X(a) = \int_{a}^{b} f_X(t) \, dt$  
* 또한, $P(a < X \leq b) = P(a \leq X \leq b) = P(a \leq X < b) = P(a < X < b)$  


* $F_X(x)$의 특성에 의해 유도되는 성질  
  1. $f_X(x) \geq 0$ ($F_X(x)$ is non-decreasing)  
  2. $\int_{-\infty}^{\infty} f_X(t) \, dt = 1$ ($F_X(\infty) = 1$)  


#### How to compute the PDF of Y=g(x), where g is differentiable and the PDF of X is known?  
1. CDF of Y $\leftarrow$ PDF ($f_Y(y)$): CDF technique  
2. Transformation technique (Jacobian)  


#### Example 1  

지름이 1인 원이 있고, 내부 영역에서 랜덤하게 점을 고른다고 하자. X가 원점에서 해당 점까지의 거리를 의미할 때, X의 PDF를 구해보자.  

$0 \leq x \leq 1$이며, $F_X(x)= P(X \leq x) = \frac{\pi x^2}{\pi 1^2} = x^2$이다.  
$P(X \geq 0)=0$, $P(X \geq 1)= 1$이므로,  
$F_X(x) = \begin{cases}
0 & \text{if } x < 0 \\ ,  
x^2 & \text{if } 0 \leq x < 1 \\  ,  
1 & \text{if } x \geq 1  
\end{cases} $  

따라서 $f_X(x) = \begin{cases}
2x & \text{if } 0 \leq x \leq 1 \\  ,  
0 & \text{otherwise}  
\end{cases} $  


#### Example 2  

위 Example 1에 이어, $Y= X^2$의 PDF를 구해보자.  

$F_Y(y)= P(Y \leq y) = P(X^2 \leq y)$,  $y>0$  
$= P(-\sqrt{y} \leq X \leq \sqrt{y} $  
$= P(0 \leq X \leq \sqrt{y}) = F_X(\sqrt{y}) - F_X(0) $  
$= (\sqrt{y})^2 = y$ ,  $0<y<1$  

따라서 $f_Y(y)= I(0<y<1)$  


#### Example 3  

$f_X(x)= \frac{1}{2} I(-1 < x < 1)$일 때, $Y= X^2$의 PDF를 구해보자.  

$F_Y(y) = P(Y \leq y) = P(X^2 \leq y)$,  $y>0$  
$= P(-\sqrt{y} \leq X \leq \sqrt{y} $  
$= \int_{-\sqrt{y}}^{\sqrt{y}} f_X(x) \, dx$  
$= \int_{-\sqrt{y}}^{\sqrt{y}} \frac{1}{2} \, dx$  
$= \sqrt{y}$  

따라서 $f_Y(y)= \frac{1}{2\sqrt{y}} I(0 \leq y \leq 1)$  


---  

### Theorem_transformation technique  

X를 PDF로 $f_X(x)$를 가지고 support는 $S_X$를 가지는 연속 확률 변수라 하자. $Y= g(X)$라고 하고, 이 $g(X)$가 일대일 대응 미분 가능 함수일 때, Y의 PDF는 다음과 같다.  

$f_Y(y) = f_X(g^{-1}(y)) \vert \frac{dx}{dy}\vert$,  $y \in S_Y$ 이며,  
$S_Y= \lbrace y= g(x) : x \in S_X \rbrace$ 이다.  


<span style='color: #A2A2A2'> [pf] $g(X)$를 increasing 한다고 가정해보자.  
  $F_Y(y)= P(g(X) \leq y)$  
  $=P(X \leq g^{-1}(y)) = F_X(g^{-1}(y))$  
  $\therefore f_Y(y) = \frac{d}{dy} F_Y(y)$  
  $= f_X(g^{-1}(y))\frac{dx}{dy}$  
  
  $g(X)$가 decreasing해도 증명 방식은 똑같다.</span>  
  
  
  #### Example 1  
  
  $f_X(x)= I(0<x<1)$일 때, $Y= -2 \log{x}$의 PDF를 구해보자.  
  
  $g^{-1}(y)= e^{-\frac{y}{2}}$,  $\frac{dx}{dy}= -\frac{1}{2} e^{-\frac{y}{2}}$  
  
  $\therefore f_Y(y)= \frac{1}{2}{-\frac{y}{2}}$,  $y>0$  
  
  
  #### Example 2  
  
  










[Scroll to top ↑](#){: .btn .btn--primary }  

