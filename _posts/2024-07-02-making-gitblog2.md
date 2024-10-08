---
layout: post
title: '[Github blog] 2: 글을 작성해보자 (Markdown 마크다운 편)'
author: becky
categories:
  - tip
tags:
  - git
  - blog
image: >-
  https://images.unsplash.com/photo-1607799279861-4dd421887fb3?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
description: 'Github blog making #2'
---

## [깃 블로그]에 글을 작성해보자 \#2  

> [깃 블로그]를 생성해보자 1편: [여기](https://becky-new.github.io/making-gitblog1/)  


깃 블로그를 생성했다면 글을 써보자!  



### Prose.io 사이트  

[Prose.io](https://prose.io/)는 깃과 연동하여 포스트를 쉽게 작성할 수 있도록 해둔 사이트이다. 초보자에 맞추어 기본적인 헤더, 링크, 볼드, 리스트 등 간단한 마크다운 버튼이 있어 클릭만 하면 문법을 몰라도 사용할 수 있게 되어 있다.    
물론 Git 레포지토리나 비주얼 스튜디오 등 직접 문서를 작성해 커밋하거나 푸시하여 포스팅할 수도 있고, Prose를 사용하여 포스팅할 수도 있다. 하지만 나도 아직 외부에서 푸시하거나 깃 자체에서 포스팅하는 건 익숙하지 않아 Prose를 사용하고 있다.  
참고로 이미지 같은 건 Prose에서 업로드하는 것보다 **깃 레포지토리의 /assets/ 폴더에 해당하는 곳에 직접 업로드하는 게 속 편하다.** 이미지 포스팅도 이어지는 포스팅에서 정리해 업로드하겠다!  



## 마크다운 (Markdown)  

Jekyll을 활용한 깃 블로그에 작성되는 글은 대부분 **Markdown** 문법을 활용한다. 실제로 이 포스트 역시 .md 파일 형식을 사용한다. 따라서 이번 포스트에서는 아주 기본적인 마크다운 문법에 대해 정리하고자 한다.  

마크다운 문법은 여기서만 쓰이는 게 아니라 전반적으로 다 쓰인다. 나는 디스코드 메시지를 치거나 R 보고서를 작성하면서 마크다운에 익숙해졌는데, 이렇게 깃 블로그 작성하면서 또 써먹게 될 줄은 몰랐다.ㅋㅋ 어쨌든 알아두면 굉장히 유용하다!  

-where-  
- [줄바꿈](#줄바꿈)  
- [헤더](#헤더)  
- [볼드, 이텔릭체](#볼드체-이텔릭체-기울임)  
- [취소선, 밑줄, 글자색](#취소선-밑줄-글자색)  
- [하이퍼링크](#하이퍼링크)  
- [이미지 첨부](#이미지-첨부)  
- [인용문](#인용문)  
- [리스트](#리스트)  
- [이스케이프 문자](#이스케이프-문자)  
- [코드 블럭](#코드-블럭)
- [구분선](#구분선)  
- [추가 문법 참고](#추가-문법-참고)  



---
### 줄바꿈  

마크다운에서 줄바꿈은 엔터만 하는 게 아니라 **스페이스바 2번**을 한 뒤 엔터를 해야 줄이 바뀐다!  


---  
### 헤더  

`#`은 Header를 나타낼 때 사용된다. 1개에서 6개까지 `#`, `##`, `###`, `####` 등으로 붙여 사용할 수 있고, 이 문자 뒤에 띄어쓰기를 한 번 한 다음 글자를 쓰면 자동으로 크기 조절과 볼드 처리가 된다.  \#의 개수가 많아질수록 글자 크기가 작아진다.  
`#`이 제일 큰 바운더리, `##`이 그 다음으로 비중이 큰 헤더이다. 이 포스트에서 예를 들면 '깃 블로그에 글을 작성해보자'는 `##`를 사용하였고, '헤더'는 `###`를 사용하였다.  


---  
### 볼드체, 이텔릭체 (기울임)  

볼드체는 `*`를 2번 사용하고, 이텔릭체는 `*`를 1번 문자 앞뒤로 사용하면 된다.  
예를 들어, '\*\*이건 볼드체고요\*\*, \*이건 이텔릭체입니다*'라고 작성한다면 **이건 볼드체고요**, *이건 이텔릭체입니다*라고 나오게 된다. 참고로 `*`를 3번 쓰면 볼드 겸 이텔릭체가 된다. ***이렇게***.   

```  
**이건 볼드체고요**  
*이건 이텔릭체입니다*  
***이건 전부 다.***  
```  


---  
### 취소선, 밑줄, 글자색  

취소선은 `~~`를 글자 앞뒤로 붙여 '~\~취소하세요~\~' ~~취소하세요~~ 로 만들 수 있다.  
밑줄은 '\<u>밑줄</u>' <u>밑줄</u> 로 만들 수 있다.  

글자 색은 CSS를 사용해야 한다!  
'\<span style="color:green">색 넣기</span>' <span style="color:green">색 넣기</span> 로 적용이 가능하다. 여기서 **color는 컬러코드로 지정해줄 수 있다.**   
\#888888로 지정해보자. <span style="color:#888888">이렇게!</span>

```  
~~취소합시다~~  
<u>밑줄입니다</u>  
<span style="color:#888888">색 넣기입니다</span>  
```  


---  
### 하이퍼링크  

링크 삽입은 **\[어쩌고](링크)** 형식으로 할 수 있다.  
예를 들어, '\[내 깃블로그 주소](https://becky-new.github.io/)' 이렇게 작성한다면 [내 깃블로그 주소](https://becky-new.github.io/)가 이렇게 하이퍼링크로 삽입되어 나타난다.  

참고로, 그냥 링크만 붙여 넣고 싶다면 <링크>로 넣을 수도 있다.


```  
<링크입니다>  
[링크 설명입니다](링크)  
```  


---  
### 이미지 첨부  

본문에 이미지를 첨부하고 싶다면 하이퍼링크와 비슷하게 할 수 있다.  
형식은 하이퍼링크와 똑같이 하되, **앞에 '!'를 붙여야 한다.** 즉, '!\[이미지](링크)' 형태가 되는 것이다.  
예를 들어, `![출처 unsplash](https://images.unsplash.com/photo-1427501482951-3da9b725be23?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)` 라고 작성한다면  

![이미지](https://images.unsplash.com/photo-1427501482951-3da9b725be23?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)  

이런 이미지가 나타나게 된다.  

```  
![이미지](이미지링크)  
```  


---  
### 인용문  

인용문은 `>`로 이루어진다.  
'\> 안녕하세요' 라고 쓰게 되면,  
> 안녕하세요  

이렇게 나온다.  

```  
> 안녕하세요? 인용문입니다.  
```  

---  
### 리스트  

리스트는 `-`, `*`, `+`를 쓰거나, 번호를 붙여주면 된다.  
- 이렇게    * 이렇게    + 이렇게  
1. 이렇게  
2. 이렇게    + 이렇게  


---  
### 이스케이프 문자  

가끔 `~`을 두 번 쓰고 싶은데 두 번은 취소선 표현이라 곤란하거나... 이런 '문자를 문자 그대로 쓰지 못해서' 발생하는 상황들이 있다. 이럴 때 사용하면 좋은 것이 **이스케이프 문자**이다. 정규표현식을 아는 분이라면 익숙하실 수도 있다.  

`\` 이것, 혹은 백슬래시로 불리는 문자이다.  
이 문자를 사용하고자 하는 문자 앞에 붙여주면, 시스템이 뒤의 문자를 특수 문자처럼 취급해서 기존의 효과를 무시하게 된다.  
예를 들어, '\\~\~안녕하세요~\\\~'라고 작성하면 \\~\~안녕하세요~\\\~로 출력된다.  


---  
### 코드 블럭  

'\`' 문자는 `이렇게 블럭을 만들 때 쓴다.`   
'\`\`\`' 3개를 연달아 사용하면,  
```
이렇게 문단이나
긴 문자열도
블럭으로 묶어서 
사용할 수 있다.
```  



---  
### 구분선  

구분선은 `***`, `---` 로 만들어진다.  
그냥 저렇게 쳐주고 스페이스 두 번, 엔터를 누르면 위에 구분선이 생긴다.  


---  
### 추가 문법 참고  

내가 아는 마크다운 문법은 여기까지이다.  
추가로 궁금한 사항이 있다면 아래 선생님의 블로그에 정리가 굉장히 잘 되어 있으므로 링크를 달아두겠다.  

> <https://ansohxxn.github.io/blog/markdown/>  





[Scroll to top ↑](#){: .btn .btn--primary }
