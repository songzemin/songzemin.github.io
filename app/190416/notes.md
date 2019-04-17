# 引入HTML

* 缩进 indent
    * 一般来说，现在前端社区里面都是缩进**两个空格**
        * 一个标签如果被一个标签包含在内，则它相对于这个标签缩进一个层级
        ```html
        <html>
          <div>
            <ul>
              <li>
                <a>
                  <img src="1.jpg">
                </a>
              </li>
              <li></li>
              <li></li>
              <li></li>
            </ul>
          </div>
        </html>
        ```
        * 如果一个标签里面只有纯文字，则可以直接把文字包含在标签内而不缩进
---
* 语义化
    * 什么样的内容用什么样的标签来表达

* 属性
    * 每个标签可以接受一个或多个属性
    * 属性可以有值，也可以没有（required）
    * 属性名不区分大小写，属性值区分大小写
    * 属性的值一般使用双引号或单引号包起来
    * 但当属性的值里没有空格，引号等特殊字符时，属性值是**完全可以**不用引号包起来的
    * 如下列出一些，用用/全局属性（Global Attributes）**eg：title**，即可以用在所有元素上面且有实际意义
        + id属性，在不学js的情况下，也可以有很多地方要用到
            * 标签在整个页面唯一的值
            * 一般来说起成一个单一的单词，不以数字开头，没有空格
        + name属性，标签的名字，现在主要用在表单类标签上面
        + title属性，鼠标在上面时显示的tooltip文本
        + alt属性，主要用在img标签上
            * 指定在图片加载失败的时候的替换文本
        + class属性，用于给标签制定内联样式
            * 多个值用**空格**分割
        + tabindex属性，用于指定表单顺序
            ```html 
            <input type="text" tabindex="1">
            <input type="text" tabindex="3">
            <input type="text" tabindex="2">
            ```
        + data-***
            * <div data-isbn="56789">书籍详情</div>
            * 杜撰一个属性
        + contenteditable标签，用于内容可编辑
            * <div contenteditable></div>
* HTML实体
  * 转义（escape）：html entity HTML实体
    + 引号 &qout; 
    + 小于号 &lt;
    + 大于号 &gt;
    + 空格 &nbsp;
    + & &amp;
    + 版权符 &copy;
    + **html entity**上有所有的转移符号。
    + [square braccket]
    + {curly braces}
    + (parentheses)
    + ; semicolon
    + : colon
    + , comma
    + . period
    + / slash
    + \ backslash
    + ? question mark
    + +plus
    + *times stark  
    + | vertical bar
    + ! exclaimation
* 对空白字符的忽略
  * pre标签，预定义格式，里边的内容不会被更改
  * 默认情况下浏览器忽略文字与文字之间多于一个的空格，换行符会被全部忽略
    * 当然css可以改变这种行为
  * 所以下面的写法其实是一样的
    ```html
    abc <p>
      <span> abc       def   </span>




      a  <i>  foo bar 

      </i>
    </p>
    <pre>
      这里你输入的空格   是完全不会被更改的，因为在`pre`里边
    </pre>
    ```
  * 上边的写法相当于下边的写法，【严格注意】空格
    ```html
      <p><span>abc def </span><i>foo bar</i></p><pre>这里你 舒服的空格  是完全不会被更改的，因为你在`pre`里边</pre>
    ```
  * 如何不用`css`让空格不被合并呢？
