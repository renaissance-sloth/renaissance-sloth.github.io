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
at_least는 숫자를 최솟값으로 제한한다. 숫자만을 포함한 문자열에도 작동한다.

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
at_most는 숫자를 최댓값으로 제한한다. 숫자만을 포함한 문자열에도 작동한다.

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
ceil은 정수로 올림한다. 숫자만을 포함한 문자열에도 작동한다.

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
divided_by는 숫자를 다른 숫자로 나눈다. 숫자만을 포함한 문자열에도 작동한다.

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
minus는 숫자에서 다른 숫자를 뺀다. 숫자만을 포함한 문자열에도 작동한다.

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
modulo는 숫자에서 다른 숫자를 나누고 남은 나머지를 반환한다. 숫자만을 포함한 문자열에도 작동한다.

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
plus는 숫자에서 다른 숫자를 더한다. 숫자만을 포함한 문자열에도 작동한다.

예시:
{% raw %}
  ```javascript
{{ 4 | plus: 2 }}
{{ 16 | plus: 4 }}
{{ 183.357 | plus: 12 }}
```
{% endraw %}

결과:
  ```javascript
{{ 4 | plus: 2 }}
{{ 16 | plus: 4 }}
{{ 183.357 | plus: 12 }}
```

## prepend
prepend는 지정된 문자열을 다른 문자열의 앞에 추가한다. 변수를 사용할 수 있다.

예시:
{% raw %}
  ```javascript
{{ "apples, oranges, and bananas" | prepend: "Some fruit: " }}
{% assign url = "example.com" %}
{{ "/index.html" | prepend: url }}
```
{% endraw %}

결과:
  ```javascript
{{ "apples, oranges, and bananas" | prepend: "Some fruit: " }}
{% assign url = "example.com" %}
{{ "/index.html" | prepend: url }}
```

## remove
remove는 문자열에서 지정된 문자열을 모두 제거한다.

예시:
{% raw %}
  ```javascript
{{ "I strained to see the train through the rain" | remove: "rain" }}
```
{% endraw %}

결과:
  ```javascript
{{ "I strained to see the train through the rain" | remove: "rain" }}
```

## remove_first
remove_first는 문자열에서 첫번째 지정된 문자열만 제거한다.

예시:
{% raw %}
  ```javascript
{{ "I strained to see the train through the rain" | remove_first: "rain" }}
```
{% endraw %}

결과:
  ```javascript
{{ "I strained to see the train through the rain" | remove_first: "rain" }}
```

## remove_last
remove_last는 문자열에서 마지막 지정된 문자열만 제거한다.

예시:
{% raw %}
  ```javascript
{{ "I strained to see the train through the rain" | remove_last: "rain" }}
```
{% endraw %}

결과:
  ```javascript
{{ "I strained to see the train through the rain" | remove_last: "rain" }}
```

## replace
replace는 문자열에서 첫 번째 인수를 모두 두 번째 인수로 바꾼다.

예시:
{% raw %}
  ```javascript
{{ "Take my protein pills and put my helmet on" | replace: "my", "your" }}
```
{% endraw %}

결과:
  ```javascript
{{ "Take my protein pills and put my helmet on" | replace: "my", "your" }}
```

## replace_first
replace_first는 문자열에서 첫 번째 인수를 첫번째만 두 번째 인수로 바꾼다.

예시:
{% raw %}
  ```javascript
{{ "Take my protein pills and put my helmet on" | replace_first: "my", "your" }}
```
{% endraw %}

결과:
  ```javascript
{{ "Take my protein pills and put my helmet on" | replace_first: "my", "your" }}
```

## replace_last
replace_last는 문자열에서 첫 번째 인수를 마지막만 두 번째 인수로 바꾼다.

예시:
{% raw %}
  ```javascript
{{ "Take my protein pills and put my helmet on" | replace_last: "my", "your" }}
```
{% endraw %}

결과:
  ```javascript
{{ "Take my protein pills and put my helmet on" | replace_last: "my", "your" }}
```

## reverse
reverse는 배열에 있는 항목의 순서를 뒤집는다.

예시:
{% raw %}
  ```javascript
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array | reverse | join: ", " }}
{{ "Ground control to Major Tom." | split: "" | reverse | join: "" }}
```
{% endraw %}

결과:
  ```javascript
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array | reverse | join: ", " }}
{{ "Ground control to Major Tom." | split: "" | reverse | join: "" }}
```

## round
round는 숫자를 가장 가까운 정수로 반올림하거나, 숫자가 인수로 전달된 경우 해당 소수 자릿수까지 반올림한다.

예시:
{% raw %}
  ```javascript
{{ 1.2 | round }}
{{ 2.7 | round }}
{{ "183.357" | round: 2 }}
```
{% endraw %}

결과:
  ```javascript
{{ 1.2 | round }}
{{ 2.7 | round }}
{{ "183.357" | round: 2 }}
```

## rstrip
rstrip은 문자열 **오른쪽**의 모든 공백(탭, 공백, 줄바꿈)을 제거한다.

예시:
{% raw %}
  ```javascript
{{ "      공백이      너무        많다       " | rstrip }}!
```
{% endraw %}

결과:
  ```javascript
{{ "      공백이      너무        많다       " | rstrip }}!
```

## size
size는 문자열의 문자 수 또는 배열의 항목 수를 반환한다.

태그 내부에서 사용해야 하는 경우 점 표기법을 사용할 수 있다.

예시:
{% raw %}
  ```javascript
{{ "Ground control to Major Tom." | size }}
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}
{{ my_array.size }}
```
{% endraw %}

결과:
  ```javascript
{{ "Ground control to Major Tom." | size }}
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}
{{ my_array.size }}
```

## slice
slice는 첫 번째 인수 인덱스에서부터의 배열 또는 문자열을 반환한다. 선택적인 두 번째 인수는 길이 또는 개수를 지정한다.

문자열이나 배열 인덱스는 0부터 센다.

첫 번째 인수가 음수이면 인덱스는 문자열 끝에서부터 계산한다.

예시:
{% raw %}
  ```javascript
{{ "Liquid" | slice: 0 }}
{{ "Liquid" | slice: 2 }}
{{ "Liquid" | slice: 2, 5 }}
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}
{{ beatles | slice: 1, 2 }}
{{ "Liquid" | slice: -3, 2 }}
```
{% endraw %}

결과:
  ```javascript
{{ "Liquid" | slice: 0 }}
{{ "Liquid" | slice: 2 }}
{{ "Liquid" | slice: 2, 5 }}
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}
{{ beatles | slice: 1, 2 }}
{{ "Liquid" | slice: -3, 2 }}
```

## sort
sort는 대소문자를 구분하여 배열의 항목을 정렬한다. 선택적 인수는 정렬에 사용할 배열 항목의 속성을 지정한다.

예시:
{% raw %}
  ```javascript
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}
{{ my_array | sort | join: ", " }}
```
{% endraw %}

결과:
  ```javascript
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}
{{ my_array | sort | join: ", " }}
```

## sort_natural
sort_natural은 대소문자를 구분하여 배열의 항목을 정렬한다. 선택적 인수는 정렬에 사용할 배열 항목의 속성을 지정한다.

예시:
{% raw %}
  ```javascript
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}
{{ my_array | sort_natural | join: ", " }}
```
{% endraw %}

결과:
  ```javascript
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}
{{ my_array | sort_natural | join: ", " }}
```

## split
split은 인수를 구분 기호로 사용하여 문자열을 배열로 나눈다.

예시:
{% raw %}
  ```javascript
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{% for member in beatles %}
  {{ member }}
{% endfor %}
```
{% endraw %}

결과:
  ```javascript
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{% for member in beatles %}
  {{ member }}
{% endfor %}
```

## strip
strip은 문자열 **양쪽**의 모든 공백(탭, 공백, 줄바꿈)을 제거한다.

예시:
{% raw %}
  ```javascript
{{ "      공백이      너무        많다       " | strip }}!
```
{% endraw %}

결과:
  ```javascript
{{ "      공백이      너무        많다       " | strip }}!
```

## strip_html
strip_html은 문자열에서 모든 HTML 태그를 제거한다.

예시:
{% raw %}
  ```javascript
{{ "Have <em>you</em> read <strong>Ulysses</strong>?" | strip_html }}
```
{% endraw %}

결과:
  ```javascript
{{ "Have <em>you</em> read <strong>Ulysses</strong>?" | strip_html }}
```

## strip_newlines
strip_newlines은 문자열에서 줄 바꿈 문자(줄 바꿈)를 제거한다.

예시:
{% raw %}
  ```javascript
{% capture string_with_newlines %}
Hello
there
{% endcapture %}

{{ string_with_newlines | strip_newlines }}
```
{% endraw %}

결과:
  ```javascript
{% capture string_with_newlines %}
Hello
there
{% endcapture %}

{{ string_with_newlines | strip_newlines }}
```

## sum
sum은 배열에 있는 모든 항목을 더한다.

문자열이 인수로 전달되면 속성 값을 더한다.

## times
times
/TODO()
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
