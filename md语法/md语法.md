标题语法：
---------------

Setext 形式
A First Level Header
====================
A Second Level Header
---------------------
atx 形式
# Header 1 
## Header 2
### Header 3
#### Header 4
##### Header 5


区块语法：
---------------------
> This is a blockquote.
> 
> This is the second paragraph in the blockquote.
> >这是嵌套
> ## This is an H2 in a blockquote

这是一个普通段落：

    这是一个代码区块。
    #include <stdio.h>

分割线语法：
---------------------
* * *

***

*****

- - -

---------------------------------------

标记语法：
---------------
Some of these words *are emphasized*.
Some of these words _are emphasized also_.
Use two asterisks for **strong emphasis**.
Or, if you prefer, __use two underscores instead__.

I strongly recommend against using any `<blink>` tags.

``There is a literalbacktick (`) here.``

I wish SmartyPants used named entities like `&mdash;`
instead of decimal-encoded entites like `&#8212;`.

If you want your page to validate under XHTML 1.0 Strict,
you've got to put paragraph tags in your blockquotes:

<blockquote>
<p>For example.</p>
</blockquote>

列表语法：
---------------------------
* Candy.
* Gum.
* Booze.
+ Candy.
+ Gum.
+ Booze.
- Candy.
- Gum.
- Booze.
1. Red
2. Green
3. Blue
*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.
    
*   一列表项包含一个列表区块：

        <代码写在这>
        #include <stdio.h>
1986\. What a great season.

链接语法：
--------------------------
This is an [example link](http://example.com/).

This is an [example link](http://example.com/ "With a Title").

This is [an example] [id] reference-style link.
[id]: http://example.com/  "Optional Title Here"
[id]: <http://example.com/>  "Optional Title Here"

[百度][]
[百度]: http://www.baidu.com
I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"

图片语法：
----------------------
![Alt text](./002.jpg)




