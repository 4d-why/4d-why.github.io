---
layout: post
title: "[GitHub] 폰트 변경하기"
date: 2021-08-28 17:24:18 +0200
image: 12.jpg
tags: [jekyll, docs]
categories: jekyll
---
<div markdown="1" style="overflow: auto; height: 300px">
***#목차 <br/>***
*[(1) 무료 폰트 찾기](#1-무료-폰트-찾기)<br/>
[(2) 폰트 적용](#2-폰드-적용) <br/>
[(3) (활용) 코드 블록에 D2Coding 폰트 적용](#3-활용-코드-블록에-d2coding-폰트-적용) <br/>*
</div>


##### 1. 무료 폰트 찾기
> 무료 폰트 사이트에서 사용하고 싶은 폰트를 찾아 적용 파일 형식에 따라 코드 복사하기

- 무료 폰트 사이트 목록
    - 눈누 : [https://noonnu.cc/index](https://noonnu.cc/index)
    - 구글 폰트 : [https://fonts.google.com/](https://fonts.google.com/)
    
- CSS 파일
    - 눈누 (CSS파일용 코드만 제공)
![noonnu](\assets\images\gitHub\noonnu.png){: width="100%"}
    - 구글 폰트
![googleFonts_css](\assets\images\gitHub\googleFonts.png){: width="100%"}

- HTML 파일
    - 구글 폰트
![googleFonts_html](\assets\images\gitHub\googleFonts_html.png){: width="100%"}


<br/>
##### 2. 폰트 적용
> CSS / HTML 파일에 코드 작성

- 폰트 import
    - CSS 파일 : [gitblog 파일 경로]/assets/css/[css파일명].css

    ```ruby
    @font-face {
        font-family: 'Pretendard-Regular';
        src: url('https://cdn.jsdelivr.net/gh/Project-Noonnu/noonfonts_2107@1.1/Pretendard-Regular.woff') format('woff');
        font-weight: 400;
        font-style: normal;
    }

    ```

    - HTML 파일 : 적용 원하는 html파일 `<header>` 블록 안

    ```ruby
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@100&display=swap" rel="stylesheet">

    ```

- 폰트 적용
    - 방법 1: 직접 적용
    
    ```ruby
    body {
      line-height: 1.2;
      font-family: 'Pretendard-Regular';
      -webkit-font-smoothing: antialiased;
      font-size: 15px;
      color: $text-color;
    }

    ```
    
    - 방법 2: 전역 변수 설정하여 적용       
        - `_variable.scss`파일에서 변수 만들기
    
        ```ruby
        $primary-font: 'KOTRA_GOTHIC', 'Roboto', sans-serif;

        ```

        - 폰트 적용
        
        ```ruby
        body {
          line-height: 1.2;
          font-family: $primary-font;
          -webkit-font-smoothing: antialiased;
          font-size: 15px;
          color: $text-color;
        }

        ```  
        
    📌'직접 적용'과 '전역변수 설정하여 적용'의 차이점
    - 직접 적용: 일회성
    - 전역 변수 설정하여 적용: 재사용성 높음
    
<br/>
##### 3. (활용) 코드 블록에 D2Coding 폰트 적용
1. 무료 폰트 사이트에서 'D2Coding'폰트 코드 복사
![noonnu_D2Coding](\assets\images\gitHub\noonnu_D2Coding.png){: width="100%"}

2. css파일에 D2Coding 폰트 import

    ```ruby
    @font-face {
        font-family: 'D2Coding';
        src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_three@1.0/D2Coding.woff') format('woff');
        font-weight: normal;
        font-style: normal;
    }

    ```

3. D2Coding 폰트 변수 만들기 (_variable.scss 파일에서)

    ```ruby
    $code-font: 'D2Coding', "Consolas", monospace; 

    ```

4. `<code>` 태그에 D2Coding 폰트 적용

    ```ruby
    code {
        font-family: $code-font; 
    }

    ```




<br/>
<details>
    <summary>더보기</summary>
    <div>
        <strong>출처</strong>
        - 평생 공부 블로그  <a href="https://ansohxxn.github.io/blog/font/">https://ansohxxn.github.io/blog/font/</a><br/>
        - 눈누  <a href="https://noonnu.cc/index">https://noonnu.cc/index</a><br/>
        - 구글 폰트  <a href="https://fonts.google.com/">https://fonts.google.com/</a><br/>
    </div>
</details>
