# mkdocs入门   [b站教程](https://www.bilibili.com/video/BV1JW411p7Tw/?spm_id_from=333.337.search-card.all.click&vd_source=3b45457b6248a7de8acbfc264432895d)  

## 安装

  [官方教程](https://www.mkdocs.org/getting-started/)  

* mac自带了python2 但并没有什么用
* 需要先安装好Python3 [这个教程](https://phoenixnap.com/kb/install-pip-mac)比官方更易懂一些

## 新建mkdocs方法  

   1.mac终端执行cd命令进入桌面，参考b站教程  
   2.执行 `mkdocs new 文件夹名` 创建文件夹  
   3.cd 进入新文件夹  
   4.执行mkdocs serve命令建立本地网站  
   【md后缀意味着markdown文件，yml后缀意味着编程语言】  
   5.使用一些文本编辑软件开始网页的制作  
   友情建议：b站教程中使用的sublime text貌似要收license的费用（99$），可以用[vscode](https://azure.microsoft.com/ja-jp/products/visual-studio-code/)   

   

## 插入超链接、图片

   语法：`[显示名称](超链接地址)`

   加入在线图片需在中括号前加感叹号 网址是照片链接  
   ![neko](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/A_cat_on_a_motorcycle_in_the_medina_of_Tunis_20171017_131525.jpg/300px-A_cat_on_a_motorcycle_in_the_medina_of_Tunis_20171017_131525.jpg)

   语法：`![显示名称](超链接地址)`

   本地添加图片在docs文件夹创建img文件夹 图片存至里面  
   ![fucku](/img/fuck U .png)  

   语法：`![显示名称](文件地址)`

   * 插入视频 [详见](https://fabacademy.org/2022/labs/kannai/Instruction/tips/embed_videos/)

  
## 输入公式

   想要输入公式可以安装插件mathjax  

   [安装地址](https://docs.mathjax.org/en/v2.7-latest/start.html)

   使用到的代码  
   ![代码](/img/mathjax.png)  

   $$
  a^2 + b^2 = c^2
   $$

## 新建标签
    1.在docs文件夹下新建文档 文件名保存为XX.md格式  
    2.在mkdocs.yml中添加（pages：）一行  
    如果使用了下面的网站主题，需要将 pages: 改成 nav：
    3.输入 - "index": index.md   
          -"xinjian": xinjian.md  

## 新建外部标签
   nav:
    - Introduction: 'index.md'
    - 'about.md'
    - 'Issue Tracker': 'https://example.com/'

* 终端中mac键盘的control+c 可以停止本地服务器  

## 更换网站主题
   [推荐主题](https://squidfunk.github.io/mkdocs-material/getting-started/)  
   在终端使用pip安装主题后，在mkdocs.yml页输入theme name语句  
   `pip install mkdocs-material`  
   `theme:  name: 'material'`


   TEST:Please see the [markdown](markdown笔记.md###转义字符一览 ) for further details.

## 打包网站

    1.执行mkdocs build命令，生成一个包含html文件的文件夹  
    2.将文件夹压缩zip，打包网站上传：[bitballon](https://app.netlify.com/signup/start)  

## Commands
For full documentation visit [mkdocs.org](https://www.mkdocs.org).
* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


| ステップ | チェックリスト | 計画 |
| --- | --- | --- |
| 1. 味方になると考える | 氏名、組織、権限・・・ |  |
| 2. 目標を定める | 承認、リソース、意思決定 自律性、情報提供・・・ |  |
| 3. 「心の的」を見つける | キャリアの経歴と目標 仕事の目標 上司、同僚、など関係者 抱えている懸念 |  |
| 4. 照準を合わせる | 気分を高めるカレンシー 仕事に役立つカレンシー 立場に関するカレンシー 人間関係に関するカレンシー 個人的なカレンシー |  |
| 5. 交換を始める | いかに交換するか |  |
| 6. 目的を見失わない | 目的は何か |  |

   

<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}
});
</script>
 



