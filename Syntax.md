# Markdown Syntax
## 一、标题类
### 1.类Setext
= (最高阶标题)和 - (第二阶标题)
**例：**
```
This is an H1
=======
This is an H2
----------
```
**效果如下：**

This is an H1
=======
This is an H2
----------

任何数量的 = 和 - 都可以有效果。
>注意：由于分割线也是 “----”， 因此在使用分割线时，一定要空一行，不然会把上方的文字识别为第二阶标题。原因会在后面的段落和换行中说到。

### 2.类Atx
在行首插入1到6个 # ，对应到标题1到6阶
**例：**
```
# this is H1
## this is H2
###### this is H6
```
>注意：标准语法一般在 # 后跟个空格再写文字，不然可能会无法识别。
## 二、强调
Markdown 使用星号（*）和底线（_）作为标记强调字词的符号，你可以随便用你喜欢的样式，唯一的限制是，你用什么符号开启标签，就要用什么符号结束。
**例：**
```
*这是倾斜*
_这也是倾斜_
**这是加粗**
__这也是加粗__
***这是加粗倾斜***
___这也是加粗倾斜___
~~这是加删除线~~
```
**效果如下：**
*这是倾斜*
_这也是倾斜_
**这是加粗**
__这也是加粗__
***这是加粗倾斜***
___这也是加粗倾斜___
~~这是加删除线~~
>注意：强调也可以直接插在文字中间，但是如果你的 * 和 _ 两边都有空白的话，它们就只会被当成普通的符号。 如果要在文字前后直接插入普通的星号或底线，你可以用反斜线 \ 。
## 三、列表
无序列表使用星号、加号或是减号作为列表标记。
**例：**
```
- 列表内容
+ 列表内容
* 列表内容
```
**效果如下：**
- 列表内容
+ 列表内容
* 列表内容
>注意：- + * 跟内容之间都要有一个空格

有序列表则使用数字接着一个英文句点作为标记。
**例：**
```
1. 列表内容
2. 列表内容
3. 列表内容
```
>注意：序号跟内容之间要有空格

**效果如下：**
1. 列表内容
2. 列表内容
3. 列表内容

列表可以嵌套，上一级和下一级之间敲三个空格即可。
**例：**
```
* 一级无序列表内容
   * 二级无序列表内容
   * 二级无序列表内容
   * 二级无序列表内容
```
**效果如下：**
* 一级无序列表内容
   * 二级无序列表内容
   * 二级无序列表内容
   * 二级无序列表内容
## 四、引用
在引用的文字前加 > 即可。 在 Markdown 文件中建立一个区块引用，那会看起来像是你自己先断好行，然后在每行的最前面加上 > 
**例：**
```
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.
```
**效果如下：**
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.
> 
Markdown 也允许你偷懒只在整个段落的第一行最前面加上 > 
**例：**
```
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.
```
**效果如下：**
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing.

区块引用可以嵌套（例如：引用内的引用），只要根据层次加上不同数量的 > 
**例：**
```
> This is the first level of quoting.
>
> > This is nested blockquote.
>
> > > > Back to the first level.
```
**效果如下：**

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> > > > Back to the first level.

>引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等。
## 五、代码
在Markdown中加入代码块有两种方式： 第一种，只要简单地缩进 4 个空格或是 1 个制表符就可以，
```
这是一个普通段落：

    这是一个代码区块。

(当然，前面要有一个空行和前面的文字分隔开)
```
效果如下：

这是一个普通段落：

    这是一个代码区块。
第二种方法似乎是更为常用， 单行代码：代码之间分别用一个反引号包起来即可；
```
这里有一句代码`代码内容`。
```
**效果如下：**
这里有一句代码`代码内容`。
代码块：代码之间分别用三个反引号包起来，且两边的反引号单独占一行
```
\```
  代码...
  代码...
  代码...
\```
\ 是为了防止转译，实际是没有的。
```
**效果如下：**
```
  代码...
  代码...
  代码...
```
>还可以在上面的 ``` 后面注明你的代码类型，可以产生相应的代码高亮。
## 六、链接
`[链接名称](链接地址)`
**例：**
`[example](https://www.example.com)`
**效果如下**
[example](https://www.example.com)

<链接地址>
**例：**
`<http://www.example.com>`
**效果如下：**
<http://www.example.com>

```
[链接名称]
[链接名称]: 链接地址
```
**例：**
```
I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"
```
**效果如下：**
I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"

## 七、图片
```
![alt 属性文本](图片地址)
![alt 属性文本](图片地址 "可选标题")
```
**例：**
```
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png)

![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")
```
**效果如下：**
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png)

![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")