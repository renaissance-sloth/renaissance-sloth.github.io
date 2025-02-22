---
title: "Introduction"
excerpt: Liquid uses a combination of objects, tags, and filters inside template files to display dynamic content.
tags: liquid basic introduction
header:
  teaser: https://cdn.shopify.com/shopifycloud/brochure/assets/brand-assets/shopify-logo-primary-logo-456baa801ee66a0a435671082365958316831c9960c480451dd0330bcdae304f.svg
---
# Introduction

Liquid uses a combination of [objects]({{page.url | append:"#objects"}}), [tags]({{page.url | append:"#tags"}}), and [filters]({{page.url | append:"#filters"}}) inside **template files** to display dynamic content.

## Objects
**Objects** contain the content that Liquid displays on a page. Objects and variables are displayed when enclosed in double curly braces: 
`{% raw %}{{{% endraw %}`
and 
`{% raw %}}}.{% endraw %}`

{% raw %}
  ```javascript
//input
{{ page.title }}
```
{% endraw %}

  ```javascript
//Output
{{ page.title }}
```

In this case, Liquid is rendering the content of the `title` property of the `page` object, which contains the text `Introduction`.

## Tags
**Tags** create the logic and control flow for templates. The curly brace percentage delimiters `{% raw %}{%{% endraw %}` and `{% raw %}%}{% endraw %}` and the text that they surround do not produce any visible output when the template is rendered. This lets you assign variables and create conditions or loops without showing any of the Liquid logic on the page.

{% raw %}
  ```javascript
//input
{% if page %}
  Welcome to {{ page.title }}!
{% endif %}
```
{% endraw %}

  ```javascript
//Output
{% if page %}
  Welcome to {{ page.title }}!
{% endif %}
```
Tags can be categorized into various types:

- [Control flow]({{ '/' | relative_url | append:page.language | append:"/liquid/tags/control-flow" }})
- [Iteration]({{ '/' | relative_url | append:page.language | append:"/liquid/tags/iteration" }})
- [Template]({{ '/' | relative_url | append:page.language | append:"/liquid/tags/template" }})
- [Variable assignment]({{ '/' | relative_url | append:page.language | append:"/liquid/tags/variable" }})

You can read more about each type of tag in their respective sections.

## Filters
**Filters** change the output of a Liquid object or variable. They are used within double curly braces `{% raw %}{{{% endraw %}` `{% raw %}}}{% endraw %}` and variable assignment, and are separated by a pipe character `|`.

{% raw %}
  ```javascript
//input
{{ "/my/fancy/url" | append: ".html" }}
```
{% endraw %}

  ```javascript
//Output
{{ "/my/fancy/url" | append: ".html" }}
```

Multiple filters can be used on one output, and are applied from left to right.

{% raw %}
  ```javascript
//input
{{ "adam!" | capitalize | prepend: "Hello " }}
```
{% endraw %}

  ```javascript
//Output
{{ "adam!" | capitalize | prepend: "Hello " }}
```