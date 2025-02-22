---
title: "Control flow"
excerpt: Control flow tags create conditions that decide whether blocks of Liquid code get executed.
tags: liquid tags control flow
header:
  teaser: https://cdn.shopify.com/shopifycloud/brochure/assets/brand-assets/shopify-logo-primary-logo-456baa801ee66a0a435671082365958316831c9960c480451dd0330bcdae304f.svg
---
# Control flow
Control flow tags create conditions that decide whether blocks of Liquid code get executed.

## if
Executes a block of code only if a certain condition is `true`.

{% raw %}
  ```javascript
//input
{% if product.title == "Awesome Shoes" %}
  These shoes are awesome!
{% endif %}
```
{% endraw %}

  ```javascript
//Output
These shoes are awesome!
```

## unless
The opposite of `if` – executes a block of code only if a certain condition is **not** met.

{% raw %}
  ```javascript
//input
{% unless product.title == "Awesome Shoes" %}
  These shoes are not awesome.
{% endunless %}
```
{% endraw %}

  ```javascript
//Output
These shoes are not awesome.
```

This would be the equivalent of doing the following:

{% raw %}
  ```javascript
{% if product.title != "Awesome Shoes" %}
  These shoes are not awesome.
{% endif %}
```
{% endraw %}

## elsif / else
Adds more conditions within an `if` or `unless` block.


{% raw %}
  ```javascript
//input
<!-- If customer.name = "anonymous" -->
{% if customer.name == "kevin" %}
  Hey Kevin!
{% elsif customer.name == "anonymous" %}
  Hey Anonymous!
{% else %}
  Hi Stranger!
{% endif %}
```
{% endraw %}

  ```javascript
//Output
Hey Anonymous!
```

## case/when
Creates a switch statement to execute a particular block of code when a variable has a specified value. `case` initializes the switch statement, and `when` statements define the various conditions.

A `when` tag can accept multiple values. When multiple values are provided, the expression is returned when the variable matches any of the values inside of the tag. Provide the values as a comma-separated list, or separate them using an `or` operator.

An optional `else` statement at the end of the case provides code to execute if none of the conditions are met.

{% raw %}
  ```javascript
//input
{% assign handle = "cake" %}
{% case handle %}
  {% when "cake" %}
     This is a cake
  {% when "cookie", "biscuit" %}
     This is a cookie
  {% else %}
     This is not a cake nor a cookie
{% endcase %}
```
{% endraw %}

  ```javascript
//Output
This is a cake
```