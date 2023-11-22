# markdown笔记  参考：[择势量投](https://www.jianshu.com/p/ebe52d2d468f)

## 随用随记 [markdown官方教程](https://markdown.com.cn/extended-syntax/tables.html)

### 注意

markdown语法中的标题/项目符号需要顶格写不然可能出错

### 新东西

!!! note "def a title"

    note is awesome!

???+ note "okay"

    notitle, also can be hided

!!! info inline end "Lorem ipsum"

    Lorem ipsum dolor sit amet, consectetur
    adipiscing elit. Nulla et euismod nulla.
    Curabitur feugiat, tortor non consequat
    finibus, justo purus auctor massa, nec
    semper lorem quam in massa.

???+ tip "admotions_type"

    note  
    abstract  
    info  
    tip  
    success  
    question  
    warning  
    failure  
    danger  
    bug  
    example  
    quote  


``` python
""" Bubble sort """
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

[代码高亮](https://squidfunk.github.io/mkdocs-material/setup/extensions/python-markdown-extensions/?h=highlight#highlight)

[提示框](https://juejin.cn/post/7066641709198737416)

==bright==

*xieti*

**jiacu**

<u>xiahuaxian</u>

> yinyong recite

无序列表:  要空行

- kajsbd,jsnd kakjdbnj,ddadklmaldkqsajashdbzx dwdhlad qwdhihdbc bk.saqbdw 
  wqdhifchjbfwjbfkwj 

unordered list:

- Nulla et rhoncus turpis. Mauris ultricies elementum leo. Duis efficitur
  accumsan nibh eu mattis. Vivamus tempus velit eros, porttitor placerat nibh
  lacinia sed. Aenean in finibus diam.

    * Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    * Nam vulputate tincidunt fringilla.
    * Nullam dignissim ultrices urna non auctor.

ordered list 开头使用tab区分

1.  Vivamus id mi enim. Integer id turpis sapien. Ut condimentum lobortis
    sagittis. Aliquam purus tellus, faucibus eget urna at, iaculis venenatis
    nulla. Vivamus a pharetra leo.

    1.  Vivamus venenatis porttitor tortor sit amet rutrum. Pellentesque aliquet
        quam enim, eu volutpat urna rutrum a. Nam vehicula nunc mauris, a
        ultricies libero efficitur sed.

    2.  Morbi eget dapibus felis. Vivamus venenatis porttitor tortor sit amet
        rutrum. Pellentesque aliquet quam enim, eu volutpat urna rutrum a.

        1.  Mauris dictum mi lacus
        2.  Ut sit amet placerat ante
        3.  Suspendisse ac eros arcu

definition list

`Lorem ipsum dolor sit amet`

:   Sed sagittis eleifend rutrum. Donec vitae suscipit est. Nullam tempus
    tellus non sem sollicitudin, quis rutrum leo facilisis.

`Cras arcu libero`

:   Aliquam metus eros, pretium sed nulla venenatis, faucibus auctor ex. Proin
    ut eros sed sapien ullamcorper consequat. Nunc ligula ante.

    Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    Nam vulputate tincidunt fringilla.
    Nullam dignissim ultrices urna non auctor.


分隔符等于三个-

---

:cat:

:heart:   :birthday:

:smile:

task list  方括号一定要打空格

- [ ] as

- [x] bs

- [x] cs


 - [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque


脚注[^tiaozhuan]

[^tiaozhuan]: tag.md

嵌入视频
<iframe src="//player.bilibili.com/player.html?aid=327623069&bvid=BV1JA411h7Gw&cid=171385214&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>


### 改行
* 文末に半角空白スペースを2つつける

* 1行空白の行を入れる

* &lt;br>タグを使う

* markdown中&lt;和&amp;需要特殊转译，输入时输入`&lt;` `&amp;`

* 根据上一条的经验 使用 `` 可以强制表示文本  或 &lt;code>  &lt;/code>

    `比如这样`   <code> 或者这样 </code>

### 表格
语法说明： 

不管是哪种方式，第一行为表头，第二行分隔表头和主体部分，第三行开始每一行为一个表格行。
列于列之间用管道符|（mac键盘shift加\）隔开。原生方式的表格每一行的两边也要有管道符。
第二行还可以为不同的列指定对齐方向。默认为左对齐，在-右边加上:就右对齐。
- 左对齐， :-: 中心对齐，-: 右对齐

| 学号 | 姓名 | 序号 |
|: --- | --- :|: --- :|
| 小明 | 男 | 5 |
| 小红 | 女 | 79 |
| 小陆 | 男 | 192 |

快速生成 [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)



### 转义字符一览 

[一览表](https://juejin.cn/post/6870818926561853453)




