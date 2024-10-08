---
layout: post
title: '[수리통계학 I] 1, 2강 요약 정리'
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

## [수리통계학 I] 1, 2강  

**부산대학교 김충락 교수님의 2020년 1학기 KOCW 강의를 들으며 요약하는 글입니다.**  

[1강 링크](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=7c789810ade43386&lid=ab9a991198792450)  


**목차**  
[1. 기본 개념](#기본-개념)  
[2. Set theory](#set-theory)  
[3. Integral](#integral)  
[4. Probability Set Function](#probability-set-function)  
[5. Conditional Probability](#conditional-probability)  
[6. Bayes Theorem](#bayes-theorem)  
[7. Independent](#independent)  

---  

### 기본 개념  

* Statistical(Random) experiment: 실험 수행 전 결과를 100% 확신할 수 없는 실험. 동전을 던진다고 했을 때, 확률이 얼마가 될지는 예측할 수 있어도 반드시 앞면이 나올 것이라 말할 수는 없다.  
* Sample space $\Omega$ (혹은 $\mathscr{C}$): 표본 공간. Random experiment의 가능한 모든 경우를 모아둔 집합이다.  
* Event: sample의 부분 집합.  


### Set Theory  

* $C_1 \subset C_2$: $C_1$은 $C_2$의 subset(부분집합).  
* Null(empty) set: $\emptyset$으로 표현되며, set C가 아무 요소가 없을 때 공집합이라고 한다.  

---
* $C_1 \cup C_2$: $C_1$과 $C_2$의 합집합.  
  + $\bigcup_{k=1}^{\infty} C_k = C_1 \cup C_2 \cup C_3 \cdots \cup C_n$  
  
  + $C_k= \lbrace x: \frac{1}{k+1} \leq x \leq 1 \rbrace$일 때, $\bigcup_{k=1}^{\infty} C_k= \lbrace x: 0 < x \leq 1 \rbrace$  
    - 임의의 k에 대해 $\frac{1}{k+1} > 0$이므로 0과 같을 수는 없다.  
    
    
---
* $C_1 \cap C_2$: $C_1$과 $C_2$의 교집합.  
  + $\bigcap_{k=1}^{\infty} C_k = C_1 \cap C_2 \cap C_3 \cdots \cap C_n$  
  
  + $C_k= \lbrace x: 0 < x < \frac{1}{k} \rbrace$일 때, $\bigcap_{k=1}^{\infty} C_k= \emptyset$  
    - 임의의 x에 대해, $\frac{1}{k} < x$인 0보다 큰 k가 존재한다. (x를 아무리 작게 해도 그것보다 작아지도록 만드는 k는 존재한다.)  
    
---
* $\overline{C}$: 표본 공간 $\Omega$의 부분 집합 C의 여집합(여사건)  

* Point function: 정의역이 point일 때.  
* Set function: 정의역이 set일 때.  


### Integral  

* $\iint_C f(x,y) \, dxdy$  
* k-fold integration: $\iint \cdots \int f(x_1,x_2,\cdots,x_k) \, dx_1dx_2 \cdots dx_k$  

* $Q(C)= \int_c \cdots \int \, dx_1dx_2 \cdots dx_n$이라고 하자. $C= \lbrace(x_1,x_2, \cdots, x_n): 0 \leq x_1 \leq x_2 \leq \cdots \leq x_n \leq 1 \rbrace$이면, $Q(C)= \int_{0}^{1} \int_{0}^{x_n} \cdots \int_{0}^{x_3} \int_{0}^{x_2} \, dx_1dx_2 \cdots dx_{n-1}dx_n = \frac{1}{n!}$  


### Probability Set Function  

* $\sigma$\_field의 조건 3가지  
  1. $\emptyset \in \mathscr{B}$  
  2. $C \in \mathscr{B} \Rightarrow C^C \in \mathscr{B}$ (closed under complement)   
  3. $C_1,C_2, \cdots \in \mathscr{B} \Rightarrow \bigcup_{i=1}^{\infty} C_i \in (B)$ (closed under countable union)  
    * countable: 정수와 1:1 매핑이 가능함.  
    
* Borel $\sigma$\_field: $\Re$의 모든 열린 구간의 집합 $\mathscr{I}$($\mathscr{I}$를 포함하는 가장 작은 $\sigma$\_field 집합)에 의해 생성된 $\sigma$\_field    


* Probability set function의 조건 3가지  
  1. $P(C) \geq 0, \forall C \in  \mathscr{B}$ (non-negativity)  
  2. $P(\mathscr{C}) = 1$ (normality)  
  3. $C_1, C_2, \cdots \in \mathscr{B}  s.t.  C_m \cup C_n = \emptyset, \forall m \ne n$일 때, $P(\bigcup_{i=1}^{\infty} C_n) = \sum_{i=1}^{\infty} P(C_i)$ (countable additivity)  


* Theorem  
  1. $P(C) = 1- P(C^C), \forall C \in \mathscr{B}$  
    * <span style="color:#A2A2A2"> $C \cup C^C = \mathscr{C}  and  C \cap C^C = \emptyset$ </span>  
    
  2. $P(\emptyset) = 0$  
    * <span style="color:#A2A2A2"> $C= \emptyset \Rightarrow C^C = \mathscr{C}$ </span>  
    
  3. $C_1 \subset C_2 \Rightarrow P(C_1) \leq P(C_2)$  
    * <span style="color:#A2A2A2"> $C_2 = C_1 \cup (C_1^C \cap C_2)$ </span>  
    
  4. $0 \leq P(C) \leq 1, \forall C \in \mathscr{B}$  
    * <span style="color:#A2A2A2"> $\emptyset \subset C \subset \mathscr{C}$ </span>  
    
  5. $P(C_1 \cup C_2) = P(C_1) + P(C_2) - P(C_1 \cap C_2)$  
    * <span style="color:#A2A2A2"> $C_1 \cup C_2 = C_1 \cup (C_1^C \cap C_2),  C_2= (C_1 \cap C_2) \cup (C_1^C \cap C_2)$ </span>  
  
  6. $\lbrace C_n \rbrace$이 increasing sequence라고 할 때, $\lim_{n\to\infty} P(C_n) = P(\lim_{n\to\infty} C_n) = P(\bigcup_{n=1}^{\infty} C_n)$  
  7. $\lbrace C_n \rbrace$이 decreasing sequence라고 할 때, $\lim_{n\to\infty} P(C_n) = P(\lim_{n\to\infty} C_n) = P(\bigcap_{n=1}^{\infty} C_n)$  


  8. $\lbrace C_n \rbrace$을 arbitrary sequence라고 하면, $P(\bigcup_{n=1}^{\infty} C_n) \leq \sum_{n=1}^{\infty} P(C_n)$  


* Inclusion-exclusion formula  

  + $P(C_1 \cup C_2 \cup \cdots \cup C_k) = p_1 - p_2 + p_3 - \cdots + (-1)^{k-1}p_k$  


### Conditional Probability  

* 조건부 확률 (Conditional Probability): $C_1, C_2 \subset \mathscr{C}$일 때, $P(C_2 \mid C_1) = \frac{P(C_2 \cap C_1)}{P(C_1)}$, if $P(C_1) > 0$


* 조건부 확률의 3가지 성질
  1. $P(C_2 \mid C_1) \geq 0$ (non-negativity)
  2. $P\left(\bigcup_{i=2}^{\infty} C_i \mid C_1\right) = \sum_{i=2}^{\infty} P(C_i \mid C_1)$ if $C_2, C_3, \cdots$ are mutually disjoint (countable additivity)
  3. $P(C_1 \mid C_1) = 1$ (normality)


#### Example  

4가지 모양이 13개씩 있는 덱에서 비복원 추출로 카드를 뽑는다고 생각해보자. 6번째 추출에서 3번째 스페이드를 뽑을 확률을 구하라.  

$\textit{Sol}$  
$C_1$: 5번째까지의 추출에서 스페이드 2개가 나오는 경우.  
$C_2$: 6번째 추출에서 스페이드가 나오는 경우.  

우리는 $P(C_1 \cap C_2)$를 구해야 하고 $P(C_1 \cap C_2) = P(C_2 \mid C_1)P(C_1)$이므로,  
$P(C_1)= \frac{\binom{13}{2} \binom{39}{3}}{\binom{52}{5}} = 0.2743$,  $P(C_2 \mid C_1)= \frac{11}{47} = 0.234 \Rightarrow P(C_1 \cap C_2) = 0.064$  


#### In general  

$P(C_1 \cup C_2 \cup C_3 \cup \cdots) = P(C_1)P(C_2 \mid C_1)P(C_3 \mid {C_1 \cap C_2})P(C_4 \mid {C_1 \cap C_2 \cap C_3}) \cdots$  



### Bayes Theorem  

* 베이즈 정리: $P(C_j \mid C)$를 구하기 힘들지만, $P(C \mid C_j)$와 $P(C)$를 구하기 쉬울 때 (알고 있을 때) 유용하게 사용하며, 여러 분야에 응용된다.  

* $P(C_j \mid C) = \frac{P(C_j) P(C \mid C_j)}{\sum_{i=1}^{k} P(C_i) P(C \mid C_i)} = \frac{P(C_j) P(C \mid C_j)}{P(C)}, \quad j= 1, \cdots, k$  

* $P(C_j)$ : Prior probability  
* $P(C_j \mid C)$ : Posterior probability  


### Independent  

* $C_1$과 $C_2$가 independent하다: $P(C_1 \mid C_2) = P(C_1) \Rightarrow P(C_1 \cap C_2) = P(C_1)P(C_2)$  

* In general: $P(C_{i_1} \cap C_{i_2} \cap \cdots \cap C_{i_k}) = P(C_{i_1}) \cdots P(C_{i_k}) = \prod_{j=1}^{k} P(C_{ij})$이라면 $C_1, C_2, \cdots, C_n$은 independent  


* Pairwise independent: $P(C_i \cap C_j) = P(C_i)P(C_j), \forall i \ne j$  
  
  

---  

[Scroll to top ↑](#){: .btn .btn--primary }
