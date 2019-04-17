# HTML 标签

  * br 
    * break
    * 换行
    * 自闭合标签
  * hr
    * horizontal
    * 水平线分隔
    * 自闭合标签
    * 强行写作`<hr>some text</hr>`的话里面的内容会被移出标签
      - 可以理解为没有</hr>标签
  * font/marquee
    * 几乎是不用了,早些年不用css时可以使用这些标签指定字体等
    * deprecates 不推荐使用
  * em 
    * emphasis
    * 语义为强调
    * 斜体
  * strong
    * 强调，比em强调更重一些
    * 粗体
  * b
    * bold
    * 只是样式上的加粗
  * 可访问性 accessibility
    * 读屏软件
    * 比如，windows 高对比度主题，方便色弱的人能更容易识别
    * a r i a
  * u underline
    * 下划线
  * i
    * italic，斜体的，一般编辑器（如word）的斜体按钮就是用的一个斜着的I图标来表示
    * 在以前，这个标签就是表示斜体文字的
    * 但html5中对其语义进行了明确
      * 用来表示由于某些原因需要与普通文本区分的文本
    * 因为跟icon这个单词的首字母一样，很多人/框架/库也用这个标签来表示图标
      * http://fontawesome.io/
        
        ```html
        <i class="fa fa-star"></i>
        ```
  * `<!-- asdfghjkl-->`
    <!--注释-->
    * **注释是对程序本身的解释，几乎不会对程序的行为造成任何的影响**
    * 基本上所有的语言都是有注释的
    * css中可以在属性前面加一个“x”来把该属性去掉，类似注释的功能
  * pre
    * 表示有预定义格式的文本
      * 里面的内容的回车跟空格都会被保留
    * 本来有个width属性，表示每行最多的字符
      * 本来支持度也不好，然后在html5中被弃用了，因为可以用css更为精确的控制
    * 常与code标签`配合`使用，用来在页面里显示高亮过的代码
      * pre标签里面嵌套code标签来表示代码块
  * 列表类标签
    - ol,ul
      + Ordered List, Unordered List
      + 有序列表和无序列表
      + 其直接子节点必须只能是li标签
        - li内可以是任意其它标签
      + 默认会在每多一层级的列表中缩进
      + 并带有列表项符号，有序和无序的
      + `多个同类项的重复，就应该使用列表标签`
    - dl 描述性列表
      + description list
      + dt
        * description term
      + dd
        * description description
      + 一个列表项是**一个dt**和**一个或多个dd**一起算一组
      + 此标签与ol/ul有些区别，在于
        + 一个dt可以对应多个dd
        ```html
          <dl>
            <dt>帅哥</dt>
            <dd>宋泽民</dd>

            <dt>丑女</dt>
            <dd>边晓菲</dd>
            <dd>邓凯丽</dd>
            <dd>武晓春</dd>

          </dl>
        ```
---
# html标签到这里暂时告一段落，未完待续......