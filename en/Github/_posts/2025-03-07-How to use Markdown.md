---
title: "How to write Markdown"
excerpt: "How to write Markdown"

tags: markdown
header:
  teaser: 
---

# How to write Markdown

> if you feel that Markdown alone is not enough, you can also use HTML tags.

# 1. About Markdown
## 1.1. What is Markdown?
[**Markdown**](https://www.markdownguide.org/getting-started/) is a text-based markup language created by John Gruber in 2004. It is easy to write and read and can be converted to HTML. It uses a very simple grammar structure using special characters and letters to create content faster and more intuitively on the web. The reason why Markdown has recently come into the spotlight is because of [GitHub](https://github.com). README.md, which records information about GitHub's repository, was the first Markdown document that anyone using GitHub would encounter. As Markdown's strengths of being able to simply record installation methods, source code descriptions, issues, etc. and improve readability were highlighted, it gradually spread to various places.

## 1.2. Pros and Cons of Markdown
### 1.2.1. Pros
1. Concise.
2. Can be written without a separate tool.
3. Can be converted into various forms.
4. Since it is saved as text, it is easy to store because it takes up little space.
5. Since it is a text file, you can manage the change history using a version control system.
6. Supports by various programs and platforms.

### 1.2.2. Disadvantages
1. There is no standard.
2. Since there is no standard, the conversion method or result is different depending on the tool.
3. It does not replace all HTML markup.

---

# 2. How to use Markdown (grammar)
## 2.1. Headers
* Headings: Only 1~6 are supported
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### This is a H7(not supported)
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### This is a H7(not supported)

## 2.2. BlockQuote
Use the `>` block quote character used in email.
```
> This is a first blockqute.
> > This is a second blockqute.
> > > This is a third blockqute.
```
> This is a first blockqute.
> > This is a second blockqute.
> > > This is a third blockqute.

You can include other markdown elements inside this.
> ### This is a H3
> * List
> ```
> code
> ```

## 2.3. List
### Ordered list (number)
Ordered lists use numbers and periods.
```
1. First
2. Second
3. Third
```
1. First
2. Second
3. Third

**Currently, the order is defined as descending order, no matter what number you enter.**
```
1. First
3. Third
2. Second
```
1. First
3. Third
2. Second

It doesn't seem like it will improve much. John Gruber doesn't care...

### Unordered list (supports bullets: `*`, `+`, `-`)
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

You can also mix

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

## 2.4. Code
When it encounters an indentation of 4 spaces or a tab, it starts to be converted and continues until it encounters an unindented line.

### 2.4.1. Indentation
```
This is a normal paragraph:

    This is a code block.

end code block.
```

Actually applying it,

Application example:

---

This is a normal paragraph:

    This is a code block.

end code block.

---

> If you don't leave a space on the line, the recognition problem will not occur properly.

```
This is a normal paragraph:
    This is a code block.
end code block.
```

Application example:

---

This is a normal paragraph:
    This is a code block.
end code block.

---

### 2.4.1. Code block
Code block can be used in two ways as follows:

* `<pre><code>{code}</code></pre>` Usage method

```
<pre>
<code>
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, Honeymon"); }

}
</code>
</pre>
```

---
<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, Honeymon"); }

}
</code>
</pre>
</div>
</div>
---

* How to use code block code ("\```")

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

```
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, Honeymon");
    }
}
```

**GitHub** allows [syntax highlighting](https://docs.github.com/en/github/writing-on-github/creating-and-highlighting-code-blocks#syntax-highlighting) by declaring the language used at the beginning of the code block code ("\```").

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

```java
public class BootSpringBootApplication {
    public static void main(String[] args) {
        System.out.println("Hello, Honeymon");
    }
}
```

## 2.5. Horizontal line `<hr/>`
The lines below all create horizontal lines. They are often used for *page breaks* when previewing a markdown document.

```
* * *

***

*****

- - -

---------------------------------------
```

* Application examples

* * *

***

*****

- - -

---------------------------------------

## 2.6. Link
* Reference link

```
Usage: 
[link keyword][id]

[id]: URL "Optional Title here"

Example: 
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"
```

Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"

* External link

```
Usage: [Title](link)
Example: [Google](https://google.com, "google link")
```
Link: [Google](https://google.com, "google link")

* Automatic link

```
If it is a general URL or email address, form a link in the appropriate format.

* External link: <http://example.com/>
* Email link: <address@example.com>
```

* External link: <http://example.com/>
* Email link: <address@example.com>

## 2.7. Emphasis
```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~cancelline~~
```

* *single asterisks*
* _single underscores_
* **double asterisks**
* __double underscores__
* ~~cancelline~~

`When used in the middle, **spac**ing is recommended.`

When used in the middle, **spac**ing is recommended.

## 2.8. Image
```
![Alt ​​text](/path/to/img.jpg)
![Alt ​​text](/path/to/img.jpg "Optional title")
```
![Seokchon Lake Rubber Duck](http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0)
![Seokchon Lake Rubber Duck](http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0 "RubberDuck")

Since there is no size adjustment function, use ```<img width="" height=""></img>```.

Example:
```
<img src="/path/to/img.jpg" width="450px" height="300px" title="Set px(pixel) size" alt="RubberDuck"><br/>
<img src="/path/to/img.jpg" width="40%" height="30%" title="Set px(pixel) size" alt="RubberDuck">
```

<img src="http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0" width="450px" height="300px" title="Set px(pixel) size" alt="RubberDuck"><br/>
<img src="http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0" width="40%" height="30%" title="%(ratio) size setting" alt="RubberDuck">

## 2.9. Line break
If you leave more than 3 spaces (` `), the line will break.

```
* To break a line, you must leave more than 3 spaces at the end of the sentence.
Like this

* To break a line, you must leave more than 3 spaces at the end of the sentence. ___\\ Space
Like this
```

* To break a line, you must leave more than 3 spaces at the end of the sentence. Like this

* To break a line, you must leave more than 3 spaces at the end of the sentence.   
Like this

---

# 3. Markdown Usage
## 3.1. WYSIWYG Editor
Most of the editors we commonly use on the web (Naver, Daum, Google, etc.) are WYSIWYG editors, and basically use HTML to apply styles and decorate sentences. Therefore, when you copy and paste the contents of the View area of ​​a Markdown editor such as Harupad, they are generally copied as they appear in the View area. However, there is a problem when you try to edit the sentences after pasting, because the tags containing the style are transformed during the editing process and affect the overall effect. It is not easy on Tistory blogs... In the case of WordPress, it is recommended to utilize the function that converts posts written in Markdown to HTML.
The conclusion is, **If you copy and paste, it is better not to edit the main text if possible.**

## 3.2. Github, Bitbucket, Yobi, etc.
In the case of recently popular collaborative development platforms, they have a converter function that converts Markdown, so you can apply Markdown by simply copying and pasting or uploading text written in Markdown grammar.

---

# 4. Summary
Markdown is a markup language that can be easily written in a general text editor as long as you know the basic grammar. Since it is currently supported by various tools and platforms, it is becoming more and more widely used because it allows you to write styled documents more easily.

> Try writing styled documents easily and quickly by understanding and using Markdown.

---

## ○ References
* [[Common] How to write markdown](https://gist.github.com/ihoneymon/652be052a0727ad59601)
* [78 Tools for writing and previewing Markdown](http://mashable.com/2013/06/24/markdown-tools/)
* [John gruber Markdown translation](http://nolboo.github.io/blog/2013/09/07/john-gruber-markdown/)
* [GitHub-flavored Markdown translation](http://nolboo.github.io/blog/2014/03/25/github-flavored-markdown/)
* [Honeymon's Markdown writing method](http://www.slideshare.net/ihoneymon/ss-40575068)