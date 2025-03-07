---
title: "Liquid 필터"
excerpt: 
tags: liquid filter grammer
header:
  teaser: https://cdn.shopify.com/shopifycloud/brochure/assets/brand-assets/shopify-logo-primary-logo-456baa801ee66a0a435671082365958316831c9960c480451dd0330bcdae304f.svg
---

필터는 Liquid 객체나 변수의 출력을 변경한다. 이중 중괄호 `{% raw %}{{{% endraw %}` `{% raw %}}}{% endraw %}`와 할당된 변수와 함께 사용되며 파이프 문자 `{% raw %}|{% endraw %}`로 구분한다. 여러 필터를 하나의 출력에 사용할 수 있으며 왼쪽에서 오른쪽으로 적용된다.


## abs
abs는 숫자의 절댓값을 반환한다. 숫자만을 포함한 문자열에도 작동한다.

예시:
{% raw %}
  ```javascript
{{ -17 | abs }}
{{ 4 | abs }}
{{ "-19.86" | abs }}
```
{% endraw %}

결과:
  ```javascript
{{ -17 | abs }}
{{ 4 | abs }}
{{ "-19.86" | abs }}
```

## append
append는 문자열을 다른 문자열의 끝에 추가한다. 변수를 사용할 수도 있다.

예시:
{% raw %}
  ```javascript
{{ "/my/fancy/url" | append: ".html" }}
{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }}
```
{% endraw %}

결과:
  ```javascript
{{ "/my/fancy/url" | append: ".html" }}
{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }}
```

## at_least
at_least는 숫자를 최솟값으로 제한한다.

예시:
{% raw %}
  ```javascript
{{ 4 | at_least: 5 }}
{{ 4 | at_least: 3 }}
```
{% endraw %}

결과:
  ```javascript
{{ 4 | at_least: 5 }}
{{ 4 | at_least: 3 }}
```

## at_most
at_most는 숫자를 최댓값으로 제한한다.

예시:
{% raw %}
  ```javascript
{{ 4 | at_most: 5 }}
{{ 4 | at_most: 3 }}
```
{% endraw %}

결과:
  ```javascript
{{ 4 | at_most: 5 }}
{{ 4 | at_most: 3 }}
```

## capitalize
capitalize는 문자열의 첫 번째 문자를 대문자로 만들고 나머지 문자는 소문자로 바꾼다.

예시:
{% raw %}
  ```javascript
{{ "my GREAT title" | capitalize }}
```
{% endraw %}

결과:
  ```javascript
{{ "my GREAT title" | capitalize }}
```

## ceil
ceil은 정수로 올림한다.

예시:
{% raw %}
  ```javascript
{{ -1.2 | ceil }}
{{ 2.0 | ceil }}
{{ "183.357" | ceil }}
```
{% endraw %}

결과:
  ```javascript
{{ -1.2 | ceil }}
{{ 2.0 | ceil }}
{{ "183.357" | ceil }}
```

## compact
compact는 배열에서 모든 `nil` 값을 제거한다.

## concat
concat는 여러 배열을 병합한다. 결과 배열에는 입력 배열의 모든 항목이 포함된다. 여러번 사용하여 두 개 이상의 배열을 결합 할 수 있다.

예시:
{% raw %}
  ```javascript
{%- assign fruits = "apples, oranges, peaches" | split: ", " -%}
{%- assign vegetables = "carrots, turnips, potatoes" | split: ", " -%}
{%- assign furniture = "chairs, tables, shelves" | split: ", " -%}

{%- assign everything = fruits | concat: vegetables | concat: furniture -%}

{% for item in everything %}
- {{ item }}{% endfor %}
```
{% endraw %}

결과:
  ```javascript
{%- assign fruits = "apples, oranges, peaches" | split: ", " -%}
{%- assign vegetables = "carrots, turnips, potatoes" | split: ", " -%}
{%- assign furniture = "chairs, tables, shelves" | split: ", " -%}

{%- assign everything = fruits | concat: vegetables | concat: furniture -%}

{% for item in everything %}
- {{ item }}{% endfor %}
```

## date
date는 타임스탬프를 다른 날짜 형식으로 바꾼다.

페이지가 마지막으로 생성된 현재 시간이 특수 단어 "now"(또는 "today")의 값이 된다.

예시:
{% raw %}
  ```javascript
{{ "now" | date: "%a, %b %d, %y" }}
{{ "today" | date: "%Y" }}
{{ "오늘은 2025/03/07입니다." | date: "%b %d, %y" }}
이 페이지는 마지막으로 {{ "now" | date: "%Y년 %m월 %d일 (%A) %H시 %M분 %S초" }}에 생성되었습니다.
```
{% endraw %}

결과:
  ```javascript
{{ "now" | date: "%a, %b %d, %y" }}
{{ "today" | date: "%Y" }}
{{ "오늘은 2025/03/07입니다." | date: "%b %d, %y" }}
이 페이지는 마지막으로 {{ "now" | date: "%Y년 %m월 %d일 (%A) %H시 %M분 %S초" }}에 생성되었습니다.
```

## default
default는 값이 할당되지 않은 모든 변수에 대한 기본값을 설정한다. 입력값이 `nil`이나 `false` 또는 비어있다면 기본값을 표시한다.

예시:
{% raw %}
  ```javascript
{{ product_price | default: 2.99 }}
{% assign product_price = 4.99 %}
{{ product_price | default: 2.99 }}
{% assign product_price = "" %}
{{ product_price | default: 2.99 }}
```
{% endraw %}

결과:
  ```javascript
{{ product_price | default: 2.99 }}
{% assign product_price = 4.99 %}
{{ product_price | default: 2.99 }}
{% assign product_price = "" %}
{{ product_price | default: 2.99 }}
```

## divided_by
divided_by는 숫자를 다른 숫자로 나눈다.

정수끼리 나눈다면 나머지는 버린다.

예시:
{% raw %}
  ```javascript
{{ 16 | divided_by: 4 }}
{{ 5 | divided_by: 3 }}
{{ 5 | divided_by: 3.0 }}
{{ 5.0 | divided_by: 3 }}
{{ 5 | times: 1.0 | divided_by: 3 }}
```
{% endraw %}

결과:
  ```javascript
{{ 16 | divided_by: 4 }}
{{ 5 | divided_by: 3 }}
{{ 5 | divided_by: 3.0 }}
{{ 5.0 | divided_by: 3 }}
{{ 5 | times: 1.0 | divided_by: 3 }}
```

## downcase
downcase는 문자열의 각 문자를 소문자로 만든다.

예시:
{% raw %}
  ```javascript
{{ "1. LaTeX은 멋지다." | downcase }}
```
{% endraw %}

결과:
  ```javascript
{{ "1. LaTeX은 멋지다." | downcase }}
```

## escape
escape는 문자를 이스케이프 시퀀스로 대체한다. (URL에 사용할 수 있다.)

예시:
{% raw %}
  ```javascript
{{ "Have you read 'James & the Giant Peach'?" | escape }}
```
{% endraw %}

결과:
  ```
{{ "Have you read 'James & the Giant Peach'?" | escape }}
```

## escape_once
escape_once는 기존 이스케이프된 시퀀스를 변경하지 않고 문자열을 이스케이프한다.

예시:
{% raw %}
  ```javascript
{{ "1 < 2 & 3" | escape_once }}
{{ "1 &lt; 2 &amp; 3" | escape_once }}
{{ "1 &lt; 2 &amp; 3" | escape }}
```
{% endraw %}

결과:
  ```
{{ "1 < 2 & 3" | escape_once }}
{{ "1 &lt; 2 &amp; 3" | escape_once }}
{{ "1 &lt; 2 &amp; 3" | escape }}
```

## first
first는 배열의 첫 번째 항목을 반환한다. 태그 내부에서 사용해야 하는 경우 점 표기법을 사용할 수 있다.

예시:
{% raw %}
  ```javascript
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}
{{ my_array | first }}
{{ my_array.first }}
```
{% endraw %}

결과:
  ```javascript
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}
{{ my_array | first }}
{{ my_array.first }}
```

## floor
floor는 정수로 버림한다.

예시:
{% raw %}
  ```javascript
{{ -1.2 | floor }}
{{ 2.0 | floor }}
{{ "183.357" | floor }}
```
{% endraw %}

결과:
  ```javascript
{{ -1.2 | floor }}
{{ 2.0 | floor }}
{{ "183.357" | floor }}
```

## join
join은 인수를 구분 기호로 사용하여 배열에 있는 항목을 단일 문자열로 결합한다.

예시:
{% raw %}
  ```javascript
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}
{{ beatles | join: " and " }}
```
{% endraw %}

결과:
  ```javascript
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}
{{ beatles | join: " and " }}
```

## last
last는 배열의 마지막 항목을 반환한다. 태그 내부에서 사용해야 하는 경우 점 표기법을 사용할 수 있다.

예시:
{% raw %}
  ```javascript
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}
{{ my_array | last }}
{{ my_array.last }}
```
{% endraw %}

결과:
  ```javascript
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}
{{ my_array | last }}
{{ my_array.last }}
```

## lstrip
lstrip 문자열 **왼쪽**의 모든 공백(탭, 공백, 줄바꿈)을 제거한다.

예시:
{% raw %}
  ```javascript
{{ "      공백이      너무        많다       " | lstrip }}!
```
{% endraw %}

결과:
  ```javascript
{{ "      공백이      너무        많다       " | lstrip }}!
```

## map
map은 다른 객체에서 명명된 속성의 값을 추출하여 값의 배열을 생성한다.

## minus
minus는 숫자에서 다른 숫자를 뺀다.

예시:
{% raw %}
  ```javascript
{{ 4 | minus: 2 }}
{{ 16 | minus: 4 }}
{{ 183.357 | minus: 12 }}
```
{% endraw %}

결과:
  ```javascript
{{ 4 | minus: 2 }}
{{ 16 | minus: 4 }}
{{ 183.357 | minus: 12 }}
```

## modulo
modulo는 숫자에서 다른 숫자를 나누고 남은 나머지를 반환한다.

예시:
{% raw %}
  ```javascript
{{ 3 | modulo: 2 }}
{{ 24 | modulo: 7 }}
{{ 183.357 | modulo: 12 }}
```
{% endraw %}

결과:
  ```javascript
{{ 3 | modulo: 2 }}
{{ 24 | modulo: 7 }}
{{ 183.357 | modulo: 12 }}
```

## newline_to_br
newline_to_br은 문자열의 각 줄바꿈(`\n`) 앞에 HTML 줄 바꿈(`<br />`)을 삽입한다.

예시:
{% raw %}
  ```javascript
{% capture string_with_newlines %}
Hello
World!
{% endcapture %}

{{ string_with_newlines | newline_to_br }}
```
{% endraw %}

결과:
  ```javascript
{% capture string_with_newlines %}
Hello
World!
{% endcapture %}

{{ string_with_newlines | newline_to_br }}
```

## plus
plus/TODO()

## prepend
prepend

## remove
remove

## remove_first
remove_first

## remove_last
remove_last

## replace
replace

## replace_first
replace_first

## replace_last
replace_last

## reverse
reverse

## round
round

## rstrip
rstrip

## size
size

## slice
slice

## sort
sort

## sort_natural
sort_natural

## split
split

## strip
strip

## strip_html
strip_html

## strip_newlines
strip_newlines

## sum
sum

## times
times

## truncate
truncate

## truncatewords
truncatewords

## uniq
uniq

## upcase
upcase

## url_decode
url_decode

## url_encode
url_encode

## where
where
