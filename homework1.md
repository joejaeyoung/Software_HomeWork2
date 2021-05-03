# 마크다운 기본 사용법

## HEADERS 제목
>총 6가지 크기 지원.  
공백에 유의.

# H1
## H2
### H3
#### H4
##### H5
###### H6
```
# H1  
## H2  
### H3
#### H4
##### H5
###### H6
```
***
  ***

## HILIGHT 강조
>#### BOLD 굵게
**굵은 강조** 입니다.  
__굵은 강조__ 입니다.  
```
**굵은 강조** 입니다.  
__굵은 강조__ 입니다.
```  
>#### Italic 기울임
*기울임* 텍스트 입니다.  
-기울임_ 텍스트 입니다.
```
*기울임* 텍스트 입니다.  
-기울임_ 텍스트 입니다.
```  
>#### 굵게 + 기울임
***매우 중요*** 텍스트입니다.  
___매우 중요___ 텍스트입니다.
```
***매우 중요*** 텍스트입니다.  
___매우 중요___ 텍스트입니다.
```

***
***

## 인용구
>지금까지 나온 기호(강조)들은 끼여있는 단어의 경우 _보다 *을 사용하는 것을 지향한다.
```
>지금까지 나온 기호(강조)들은 끼여있는 단어의 경우 _보다 *을 사용하는 것을 지향한다.
```  

#### 중첩 인용구
> 교수님께서 md문법을 익히라고 권장하셨다
>> md문법은 visual studio로 작업한다.

```
> 교수님께서 md문법을 익히라고 권장하셨다
>> md문법은 visual studio로 작업한다.
```
#### 다른요소가 포함된 인용구
> #### MD문법의 중요성은?
>> 1. ***reademe*** 파일을 작성할 수 있다.
>> 2. **다른 사람**에게 ~~나의 코드~~를 알아보기 쉽게 설명할 수 있다.  

```
> #### MD문법의 중요성은?
>> 1. ***reademe*** 파일을 작성할 수 있다.
>> 2. **다른 사람**에게 ~~나의 코드~~를 알아보기 쉽게 설명할 수 있다.
```

***
***

## 순서 목록
1. 숫자 뒤 마침표가 있게
2. 숫자 순서일 필요는 없지만
5. 시작은 1로 시작
5. 하면 완성  
    1. 들여쓰기도 가능
    3. 위에 주의사항과 같음  
```    
1. 숫자 뒤 마침표가 있게
2. 숫자 순서일 필요는 없지만
5. 시작은 1로 시작
5. 하면 완성  
    1. 들여쓰기도 가능
    3. 위에 주의사항과 같음  
```  

***
***

## 정렬되지 않은 목록
>-, *, + 기호 사용
- 기호를 섞어 사용하지 않는다.
- 들여쓰기 또한 지원된다.
  - 들여쓰기는 tab, 띄어쓰기 2번 

***
***

## 목록에 기타사항 추가
>공백 4개 또는 탭 1개
* 나는 점심에 찜닭을 먹었다.  
    
    내찜닭이었다. 
* 점심을 먹고 공부중이다.  
    소프트웨어 공학을 공부하고 있다.  
    * 이렇게 들여쓰기도 가능하다.
```
>공백 4개 또는 탭 1개
* 나는 점심에 찜닭을 먹었다.  
    
    내찜닭이었다. 
* 점심을 먹고 공부중이다.  
    소프트웨어 공학을 공부하고 있다.  
    *이렇게 들여쓰기도 가능하다.
```  

***
***

## 목록 겹치기
>순서있는 목록, 없는 목록 둘 다 겹쳐진다.  
1. 첫번째
3. 두번째  
    - 들여쓰기
4. 세번째
```
1. 첫번째
3. 두번째  
    - 들여쓰기
4. 세번째
```  

***
***

## 코드 블록
```
코드블록
```
    1. 코드블록 1  
    
    ```
    코드블록1
    ```  

    2. 코드블록2
    코드블록2 tab 또는 띄어쓰기 4번

***
***

## 이미지
1. 이미지 파일 오픈  
![logo.png](../UsingMarkDown/logo.png)
2. 이미지 파일 닫기
```
![logo.png](../UsingMarkDown/logo.png)
```

 ***
 *** 

## 백틱 탈출
>원하는 출력결과  

``코드 `사용`은 조심해야 한다.``
```
``코드 `사용`은 조심해야 한다.``
```

***
***

## 수평선 만들기
>수평선 앞뒤로 빈줄 넣기!
---
***
___
```
--- 마이너스 표기
*** 별 표기
___ 언더바 표기
```

  ***
  ***

## 하이퍼링크, 연결
>#### 제목없는 하이퍼링크  
저는 [VisualStudio](https://code.visualstudio.com/docs/languages/markdown)를 통해 공부합니다.
```
저는 [VisualStudio](https://code.visualstudio.com/docs/languages/markdown)를 통해 공부합니다.
```


>#### 제목 추가된 하이퍼링크
저는 [VisualStudio](https://code.visualstudio.com/docs/languages/markdown "VS Helper")를 통해 공부합니다.
```
저는 [VisualStudio](https://code.visualstudio.com/docs/languages/markdown "VS Helper")를 통해 공부합니다.
```

>#### URL 및 이메일 주소
<https://code.visualstudio.com/docs/languages/markdown>  
<wowhdud0303@gmail.com>


***
***

## 링크 서식
> 링크 강조
>>저는 **[VisualStudio](https://code.visualstudio.com/docs/languages/markdown "VS Helper")** 를 통해 공부합니다.  
```
저는 **[VisualStudio](https://code.visualstudio.com/docs/languages/markdown "VS Helper")** 를 통해 공부합니다.
```  
> 링크 기울이기
>> 저는 *[VisualStudio](https://code.visualstudio.com/docs/languages/markdown "VS Helper")* 를 통해 공부합니다.
```
저는 [VisualStudio](https://code.visualstudio.com/docs/languages/markdown "VS Helper")를 통해 공부합니다.
```
>코드 표시
>> 저는 [`code`](#code)를 통해 공부합니다.
```
저는 [`code`](#code)를 통해 공부합니다.
```

***
***

## 이스케이프 문자
> 서식을 지정하는데 사용하는 리터럴 문자 표시 위해 사용  

\* 역슬래쉬가 없으면 글머리 기호가 된다
```
\* 역슬래쉬가 없으면 글머리 기호가 된다
```
이스케이프 할 수 있는 문자들은  
![reference.png](../UsingMarkDown/reference.png)  
이다.

***
***

## 마크다운 & HTML
* 마크다운 안에서 HTML 사용가능
* HTML 안에서 마크다운은 사용불가

***
***
## 깃허브 주소
[GitHub](https://github.com/joejaeyoung/Software_Engineering "ReadMe Repo")에 확장기능 정리한 것들 올려놨습니다!

***
