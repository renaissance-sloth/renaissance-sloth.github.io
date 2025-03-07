---
title: "Markdown 어떻게 쓰지?"
excerpt: "Markdown을 작성하는 방법"

tags: markdown
header:
  teaser: 
---

# Markdown을 작성하는 방법

> 마크다운만으로는 부족하다고 생각되면 HTML 태그도 사용할 수 있다.

# 1. 마크다운에 대하여
## 1.1. 마크다운이란?
[**Markdown**](https://www.markdownguide.org/getting-started/)은 2004년 존 그루버가 만든 텍스트 기반 마크업 언어이다. 읽고 쓰기 쉽고 HTML로 변환할 수 있다. 특수 문자와 문자를 사용하여 매우 간단한 문법 구조를 사용하여 웹에서 콘텐츠를 더 빠르고 직관적으로 만든다. 마크다운이 최근 주목받게 된 이유는 [GitHub](https://github.com) 때문이다. GitHub의 저장소에 대한 정보를 기록한 README.md는 GitHub을 사용하는 모든 사람이 마크다운 문서를 마주하게 하였다. 설치 방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있는 마크다운의 장점이 부각되면서 점차 사용처가 늘어났다.

## 1.2. 마크다운의 장단점
### 1.2.1. 장점
1. 간결하다.
2. 별도의 도구 없이도 작성할 수 있다.
3. 다양한 형태로 변환 가능하다.
4. 텍스트로 저장되므로 공간을 거의 차지하지 않아 보관하기 쉽다.
5. 텍스트 파일이기 때문에 버전 관리 시스템을 사용하여 변경 내역을 관리할 수 있다.
6. 다양한 프로그램과 플랫폼에서 지원한다.

### 1.2.2. 단점
1. 표준이 없다.
2. 표준이 없으므로 도구에 따라 변환 방법이나 결과가 다르다.
3. 모든 HTML 마크업을 대체하지 못한다.

---

# 2. 마크다운 사용 방법 (문법)
## 2.1. 제목
* 헤더: 1~6까지만 지원
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### This is a H7(not supported)
```

* 적용 예시

# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### This is a H7(not supported)

## 2.2. 인용문
이메일에서 사용되는 `>` 블록 인용 문자를 사용한다.
```
> This is a first blockqute.
> > This is a second blockqute.
> > > This is a third blockqute.
```

* 적용 예시

> This is a first blockqute.
> > This is a second blockqute.
> > > This is a third blockqute.

다른 마크다운 요소를 포함할 수 있다.
> ### This is a H3
> * List
> ```
> code
> ```

## 2.3. 목록
### 순서가 있는 목록 (숫자)
순서가 있는 목록은 숫자와 마침표를 사용한다.
```
1. First
2. Second
3. Third
```

* 적용 예시:

1. First
2. Second
3. Third

**현재로서는 입력하는 숫자와 관계없이 내림차순으로 정의된다.**
```
1. First
3. Third
2. Second
```

* 적용 예시:

1. First
3. Third
2. Second

John Gruber는 신경 쓰지 않고 있기에 개선의 여지는 없어보인다.

### 순서 없는 목록 (글머리 기호 지원: `*`, `+`, `-`)
```
* Red
    * Green
        * Blue

+ Red
    + Green
        + Blue

- Red
    - Green
        - Blue
```

* Red
    * Green
        * Blue

+ Red
    + Green
        + Blue

- Red
    - Green
        - Blue

섞어서 사용할 수 있다.

```
* Step 1
    - Step 2
        + Step 3
            + Step 4
```

* Step 1
    - Step 2
        + Step 3
            + Step 4

## 2.4. 코드
4개의 공백이나 탭이 있는 들여쓰기부터 들여쓰기가 없는 줄까지 코드블록으로 변환한다.

### 2.4.1. 들여쓰기
```
This is a normal paragraph:

    This is a code block.

end code block.
```

* 적용 예시:

---

This is a normal paragraph:

    This is a code block.

end code block.

---

> 줄에 공백을 두지 않으면 인식 문제가 발생한다.

```
This is a normal paragraph:
    This is a code block.
end code block.
```

* 적용 예시:

---

This is a normal paragraph:
    This is a code block.
end code block.

---

### 2.4.1. 코드 블록
코드 블록은 두 가지 방법으로 사용할 수 있다.

* `<pre><code>{code}</code></pre>` 사용법

```
<pre>
<code>
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, World"); }

}
</code>
</pre>
```

---
* 적용 예시:

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, World"); }

}
</code>
</pre>
</div>
</div>
---

* 코드 블록 ("\```") 사용법

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>
```
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, Honeymon");
    }
}
```
</code>
</pre>
</div>
</div>
---

* 적용 예시:

```
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, Honeymon");
    }
}
```
---

**GitHub**에서는 코드 블록 코드의 시작 부분에 사용된 언어("\```")를 선언하여 [구문 강조](https://docs.github.com/en/github/writing-on-github/creating-and-highlighting-code-blocks#syntax-highlighting)를 허용한다.

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>
```java
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, Honeymon");
    }
}
```
</code>
</pre>
</div>
</div>
---

* 적용 예시:

```java
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, Honeymon");
    }
}
```
---

## 2.5. 가로줄 `<hr/>`
아래 줄은 모두 가로줄을 만든다. *페이지 나누기*에 주로 사용된다.

```
* * *

***

*****

- - -

---------------------------------------
```

* 적용 예시

* * *

***

*****

- - -

---------------------------------------

## 2.6. 링크
* 참조 링크

```
사용법:
[링크 키워드][id]

[id]: URL "선택적 제목"

예시:
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"
```

Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"

* 외부 링크

```
사용법: [제목](링크)
예시: [Google](https://google.com, "google link")
```
Link: [Google](https://google.com, "google link")

* 자동 링크

```
일반 URL 또는 이메일 주소인 경우 적절한 형식으로 링크를 형성한다.

* 외부 링크: <http://example.com/>
* 이메일 링크: <address@example.com>
```

* 외부 링크: <http://example.com/>
* 이메일 링크: <address@example.com>

## 2.7. 강조
```
*별표 1개*
_밑줄 1개_
**별표 2개**
__밑줄 2개__
~~취소선~~
```

*별표 1개*
_밑줄 1개_
**별표 2개**
__밑줄 2개__
~~취소선~~

`중간에 사용할 경우 **띄어쓰기**를 사용하는 것이 좋다.`

중간에 사용할 경우 **띄어쓰기**를 사용하는 것이 좋다.

## 2.8. 이미지
```
![Alt ​​text](/path/to/img.jpg)
![Alt ​​text](/path/to/img.jpg "Optional title")
```
![text](/assets/favicon.ico/android-icon-192x192.png)
![text](/assets/favicon.ico/android-icon-192x192.png "나무늘보 아이콘")

크기 조절 기능이 없으므로 ```<img width="" height=""></img>```를 사용하라.

* 적용 예시:

```
<img src="/path/to/img.jpg" width="100px" height="100px" title="Set px(pixel) size" alt="나무늘보 아이콘"><br/>
<img src="/path/to/img.jpg" width="40%" height="30%" title="%(ratio) size setting" alt="나무늘보 아이콘">
```

* 적용 예시:

<img src="/assets/favicon.ico/android-icon-192x192.png" width="100px" height="100px" title="Set px(pixel) size" alt="나무늘보 아이콘"><br/>
<img src="/assets/favicon.ico/android-icon-192x192.png" width="40%" height="30%" title="%(ratio) size setting" alt="나무늘보 아이콘">

## 2.9. 줄바꿈
3개 이상의 공백(` `)을 남기면 줄이 바뀐다.

```
* To break a line, you must leave more than 3 spaces at the end of the sentence.
Like this

* To break a line, you must leave more than 3 spaces at the end of the sentence. ___\\ Space
Like this
```

* 적용 예시:

* To break a line, you must leave more than 3 spaces at the end of the sentence. Like this

* To break a line, you must leave more than 3 spaces at the end of the sentence.   
Like this

---

# 3. 마크다운 사용법
## 3.1. WYSIWYG 에디터
웹에서 흔히 사용하는 에디터(네이버, 다음, 구글 등)의 대부분은 WYSIWYG 에디터로, 기본적으로 HTML을 사용하여 스타일을 적용하고 문장을 꾸민다. 따라서 마크다운 에디터의 View 영역의 내용을 복사하여 붙여넣으면 일반적으로 View 영역에 나타나는 대로 복사된다. 하지만 붙여넣기 후 문장을 편집하려고 하면 문제가 있는데, 편집 과정에서 스타일이 포함된 태그가 변형되어 전체적인 효과에 영향을 미치기 때문이다. 티스토리 블로그에서는 편집이 쉽지 않다. 워드프레스의 경우 마크다운으로 작성된 게시물을 HTML로 변환하는 기능을 활용하는 것이 좋다.
결론은 **복사하여 붙여넣는 경우 가능하면 본문은 편집하지 않는 것이 좋다.**

## 3.2. Github, Bitbucket, Yobi 등
최근 인기 있는 협업 개발 플랫폼의 경우 마크다운을 변환하는 변환 기능이 있어 마크다운 문법으로 작성된 텍스트를 복사하여 붙여넣거나 업로드하기만 하면 마크다운을 적용할 수 있다.

---

# 4. 요약
마크다운은 기본 문법만 알면 일반 텍스트 편집기에서 쉽게 작성할 수 있는 마크업 언어이다. 현재 다양한 도구와 플랫폼에서 지원되고 있어 스타일이 적용된 문서를 더 쉽게 작성할 수 있기 때문에 점점 더 널리 사용되고 있다.

> 마크다운을 이해하고 사용하여 스타일이 적용된 문서를 쉽고 빠르게 작성해 보자.

---

## ○ 참고문헌
* [[공통] 마크다운 markdown 작성법](https://gist.github.com/ihoneymon/652be052a0727ad59601)
* [78 Tools for writing and previewing Markdown](http://mashable.com/2013/06/24/markdown-tools/)
* [존 그루버 마크다운 페이지 번역](http://nolboo.github.io/blog/2013/09/07/john-gruber-markdown/)
* [깃허브 취향의 마크다운 번역](http://nolboo.github.io/blog/2014/03/25/github-flavored-markdown/)
* [허니몬의 마크다운 사용기](http://www.slideshare.net/ihoneymon/ss-40575068)