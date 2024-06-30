---
layout: post
title:  "[깃 블로그] 1: 생성해보자"
author: becky
categories: [ tip ]
tags: [git, blog]
image: https://images.unsplash.com/photo-1505330622279-bf7d7fc918f4?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
description: "Github blog making #1"
---

## [깃 블로그]를 생성해보자 \#1  


여러 블로그를 참고하여 깃 블로그를 개설하고 이것저것 만져보았다. 깃 블로그는 처음 가공이 좀 어려운 편이지만, 만들고 나면 마크다운 파일을 작성하거나 일부 편집은 다른 블로그와 난이도가 비슷하다.  

> 참조 블로그: [깃 블로그 만들기](https://velog.io/@pyk0844/%EA%B9%83-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0%EC%89%BD%EA%B2%8C-%EA%B4%80%EB%A6%AC-%ED%95%98%EA%B8%B0)  



### 1. 깃허브 가입하기  

깃 블로그는 깃 레포지토리를 이용하기 때문에, [Github](https://github.com/) 계정이 있어야 사용할 수 있다. 물론 깃 블로그를 생각하는 사람 대부분은 계정이 있겠지만, 없다면 위 하이퍼링크에서 가입하자.  

![dl](https://i.imgur.com/RjgQNsv.jpeg)  

나중에 이렇게 레포지토리를 만들 수 있다.  
(왜 두 개인가요?: 테마 가져와서 블로그 개설할 때부터 애를 많이 먹어서... 블로그 지웠다 만들었다 했었기 때문...)  

참고로, 뒷부분에서 언급하겠지만 블로그 주소는 아이디? 닉네임?을 그대로 적는 경우가 많으므로 계정을 새로 생성한다면 이름 적을 때 참고하자.  




### 2. Jekyll 테마 찾기  

Jekyll은 텍스트 파일을 블로그 형식으로 바꾸어주는 사이트 같은 것이다. Jekyll 테마는 정\~~말 많다. 취향인 걸 골라서 쓰면 되는데, 이때 예쁘기만 하다고 받기보다는 가공하기 좋은 걸 다운받는 게 낫다.  
가공하기 좋은 건 어떤 테마냐 하면... ... 그냥 여러 개 받고 판단해보자. 나도 이 블로그 테마와 shell 컨셉 테마를 받았었는데, 결국은 이게 더 좋아서 이걸 쓰고 있다.  


Jekyll 테마 사이트는 아래와 같다.  

* [http://jekyllthemes.org/](http://jekyllthemes.org/)  
* [https://jekyllthemes.io/](https://jekyllthemes.io/)  
* 이건 다른 분이 정리해둔 추천 테마 10가지 [https://imsoftpro.tistory.com/74](https://imsoftpro.tistory.com/74)  

나는 3번째 링크의 Mediumish 테마를 사용하고 있다. 물론 다른 Jekyll 테마 사이트를 찾아보다가 발견한 것이지만, 깔끔하고 보기 좋아서 사용하게 되었다.  

어쨌든, 마음에 드는 Jekyll 테마를 찾자!  





### 3. 레포지토리 복사하기  

마음에 드는 테마를 찾으면, 이제 내 레포지토리에 복사할 차례이다.  

![이미지](https://i.imgur.com/zVi9Ujt.png)  


위 이미지처럼 내 깃허브에 folk를 만들거나, 다운로드 후 레포지토리를 추가하는 방식으로 테마를 가져올 수 있다.  





### 4. 레포지토리 이름 수정하기  


![dlalwl](https://i.imgur.com/irXrapO.png)  

우선은 내 깃허브에 생긴 레포지토리가 `public`인지 확인하자. `private`이라면 공개로 바꿔주어야 남들이 블로그를 볼 수 있다. (아니어도 볼 수 있는 것 같긴 하던데, 그냥 우리도 공개 테마를 가져오는 거라면 많이 수정하지 않는 이상 비공개로 둘 이유가 있나 싶기도 하다...)  


레포지토리 이름은 setting → repository name 에서 수정할 수 있다.  

![이미지](https://i.imgur.com/6um1wfu.png)  

![이미지](https://i.imgur.com/HxBRKsY.png)  

이렇게 바꿀 수 있는데, 보통은 **계정명.io**로 많이 사용한다고 한다. 나는 계정명이 아니라 다른 주소로 해보려고 시도했었는데, 오류는 크게 없던 것 같지만 결국 남들이 주로 하는 방식을 따르기로 했다. 어차피 레포지토리는 삭제하고 다시 folk 해와도 되니 편하게 이것저것 해봅시다.  

**이것이 나의 깃 블로그 주소가 된다!**  





### 5. 사이트 배포  

이름을 수정하면, 이제 공개적으로 블로그를 운영하기 위해 페이지를 배포해야 한다.  

![이미지](https://i.imgur.com/0l6kMfo.png)  

Pages 설정에 들어가면,


![이미지](https://i.imgur.com/1EQCU5i.png)  

이런 페이지를 볼 수 있다.  
visit site로는 내 블로그를 직접 볼 수 있다. (물론 주소로도 들어갈 수 있다!) 그 전에 아래 빨간 상자도 저렇게 되도록 체크해준다.  





### 6. 깃 블로그 개설 완료!  

깃 블로그가 개설되었다!  

하지만 완전 초기 단계로 복사해온 레포지토리를 그대로 보여주기 때문에, 샘플 포스트나 레이아웃들을 수정하고 싶을 수도 있다.  


내 블로그 역시 Mediumish 테마에서 이것저것 수정한 결과이므로, 다음 포스트에서는 자잘한 팁을 정리하겠다.  






[Default Button](#){: .btn .btn--primary }