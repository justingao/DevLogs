# 如何使用 markdown 语法


## 段落、标题、区块代码
markdown 支持两种标题的语法：Setext 和 atx。
Setext 是采用底线的方式：= 代表最高阶标题，- 代表第二阶标题。（任意数量的 = 和 - 都有一样的效果）
atx 是在行首插入 1~6 个 # 表示标题的 1~6 阶。

区块引用是在行首增加 >（与 email 的引用一样）。


    A First Level Header
    ====================
    A Second Level Header
    ---------------------
    
    Now the file content.
    
    ### Header 3
    
    > This is a blockquote.
    >
    > ## This is an H2 in a blockquote.
链接到[横线](#hr)。


## 修辞和强调
markdown 使用 * 和 _ 表示修辞和强调。
*/_ 会生成 <em></em> 标记对（HTML展示出来是斜体的效果），**/__ 会生成 <strong></strong> 标记对（HTML展示出来是加粗的效果）。 
~~ 表示删除线。
Some of these words *are emphasized*.
Some of these words _are emphasized also_.
Use two asterisks for **strong emphasized**.
Or, if you prefer, __use two underscores instead__.



## 列表

无序列表使用 *、+、- 表示。
有序列表使用 `数字.` 表示。
有序列表中，数字不必完全按照数字顺序标记，但是第一个数字条目最好是 1。
列表的标记不必写在行首，前面可以有最多 3 个空格（4 个空格就表示源代码了）。
如果在列表的项目之间插入空行，那么项目的内容会用 <p> 包起来，你也可以在一个项目内放上多个段落，只要在它前面缩排 4 个空格或 1 个 Tab。



## 链接
markdown 语法支持两种链接方式：行内、参考。
链接标识的文字需要用 [] 括起来。
行内的方式，直接在链接文字后面用 () 接上链接地址：
This is an [example link](http://leigao.org/).
也可以给链接选择性的加上 title 属性：
This is an [example link](http://leigao.org/ "Link Title").

参考的方式，可以给链接指定一个名称，后面可以在文件的其它地方定义该链接的内容：
I get 10 times more traffic from [Google][1] than from [MSN][2].
[1]: http://google.com/
[2]: http://msn.com/
也可以选择性的加上 title 属性，title 可以使用字母、数字和空格，但是不区分大小写：
I start my morning with a cup of coffee and [The New York Times][NY Times].
[ny times]: http://nytimes.com/



## 图片
markdown 中图片和链接的方式一样的：
行内方式：
![alt text for the image](/path/to/the/image "Option Title")
参考方式：
![alt text for the image][id]
[id]: /path/to/the/image "Option Title"



## 代码
markdown 中使用 ` （反引号）表示代码。代码块中的 &、>、< 会被自动转换为 HTML 实体。
I strongly recommend aginst using any `<blink>` tags.

如果要插入一大段代码，只要每行都缩进 4 个空格或者一个 Tab 就可以了。代码块中的 &、>、< 会被自动转换为 HTML 实体。



## 自动链接
markdown 支持一些比较简单的 url 或者 email 地址被自动转换为链接方式，只要用 <> 括起来即可：
<http://example.com>
<address@example.com>
会被自动转换为 http 链接和 mailto 邮件地址链接。



## 字符转义
如果期望上面的这些关键字符不被转义，在其前面加上 \ 就可以了，markdown 中的保留字符有：
    \
    `
    *
    _
    {}
    []
    ()
    #
    +
    -
    .
    !



## 换行与分段
空一行（也就是两个回车）代表分段（<p>）；
行末尾加上两个或者更多空格代表换行（<br/>），一个空格会被当做普通空格处理。



## <a id="hr"></a>横线
3 个或者更多个 *、- 或者 _ 单独放在一行就可以生成一条横线（<hr/>）。
例如：    
    * * *
    ***
    - - - - - -
    ______________




