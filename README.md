## Welcome to GitHub Pages


[使用 GitHub, Jekyll 打造自己的免费独立博客](http://blog.csdn.net/on_1y/article/details/19259435)


I'd like to add something here. 中文是否支持？ 

H1 :# Header 1
H2 :## Header 2
H3 :### Header 3
H4 :#### Header 4
H5 :##### Header 5
H6 :###### Header 6

链接 :[Title](URL)
加粗 :**Bold**
斜体字 :*Italics*
*删除线 :~~text~~
*高亮 :==text==
段落 : 段落之间空一行
换行符 : 一行结束时输入两个空格
列表 :* 添加星号成为一个新的列表项。
引用 :> 引用内容
内嵌代码 : `alert('Hello World');`
画水平线 (HR) :--------


You can use the [editor on GitHub](https://github.com/QuantumZhang/QuantumZhang.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/QuantumZhang/QuantumZhang.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.









# Programming-Collective-Intelligence-Source-Code_by Toby Segaran

[*英文版官方*](http://pan.baidu.com/s/1ntKHRPB)
[*中文版PDF电子书免费下载地址*](http://pan.baidu.com/s/1ntKHRPB)


***
# 阅读记录

#### Chapter 2 Making recommendations
1. 相似性度量方法，or 机器学习中的距离度量 
	[机器学习算法 原理、实现与实践 —— 距离的度量](http://www.cnblogs.com/ronny/p/4080442.html)

	[漫谈：机器学习中距离和相似性度量方法](http://www.cnblogs.com/daniel-D/p/3244718.html)

	==目标： 从样本空间、行业知识以及计算效率的角度，理解不同距离度量方法的适用性和区别。==


2. 计算效率
3. 待定


***
- one
- two
- three


***
-[] to do
-[x] Done


***
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

 

***
# Programming-Collective-Intelligence-Source-Code_by Toby Segaran

[*英文版官方*](http://pan.baidu.com/s/1ntKHRPB)
[*中文版PDF电子书免费下载地址*](http://pan.baidu.com/s/1ntKHRPB)


***
# Programming-Collective-Intelligence-Source-Code_by Toby Segaran

[*英文版官方*](http://pan.baidu.com/s/1ntKHRPB)
[*中文版PDF电子书免费下载地址*](http://pan.baidu.com/s/1ntKHRPB)


***
# 阅读记录

#### Chapter 2 Making recommendations
1. 相似性度量方法，or 机器学习中的距离度量 
	[机器学习算法 原理、实现与实践 —— 距离的度量](http://www.cnblogs.com/ronny/p/4080442.html)

	[漫谈：机器学习中距离和相似性度量方法](http://www.cnblogs.com/daniel-D/p/3244718.html)

	==目标： 从样本空间、行业知识以及计算效率的角度，理解不同距离度量方法的适用性和区别。==


2. 计算效率
3. 待定


***
#### Chapter 4 Searching and Ranking
#### 搜索和排名

- Ｇoogle ＰageRank 算法思想简述
-- 0. Ｒeference： 《数学之美》 by 吴军

-- 1. **ＰageRank的核心思想**
	在互联网上，如果一个网页被很多其他网页所链接，说明它受到普遍的承认和信赖，那么他的排名就高。举例，一个网页y的排名应该来自于所有指向这个网页的其他网页x~1~,x~2~,x~3~,...,x~k~的权重之和。至于x~i~的权重分别是多少，如何度量，及网页本身的网页排名。
	
-- 2. **迭代算法**
	“计算搜索结果的网页排名的过程中需要用到网页本身的排名，这不成了’先有鸡还是先有蛋‘的问题了吗？" 解决的办法是通过矩阵相乘的迭代，即先假设所有网页排名相同，作为初始值，算出哥哥网页的第一次迭代排名，然后根据第一次迭代排名算出第二次的排名，布林和佩奇二人从理论上证明了无论初始值如何选取，此算法总是能收敛到真实值，并不需要人工干预。 
	
-- 3.  **工程问题**
	互联网上网页的数量是巨大的，假定有十亿个网页，矩阵就有一百亿个元素。佩奇和布林利用稀疏矩阵计算的技巧，大大简化了计算量，实现了网页排名算法。
	
-- 4. **并行计算**
	2003年，Ｇoogle工程师Ｊeffrey Dean和Ｓanjay Ghemawat发明了并行计算工具ＭapReduce，实现ＰageRank的并行计算。
	
-- 5. **ＰageRank的计算方法**
--- 迭代方法，获得收敛结果；
--- 数学上，等效为平稳马尔可夫过程 (stationary Markov process)
---**tip** 迭代方法，数学上可以表示成算子的指数运算，即Ｐ~n~=H^n^P~0~


-- 6. **Learning from Clicks**
	==提高搜索结果的核心——利用用户点击查询结果的信息。
	构造ＡＮＮ==
	
-- 7. **更具体的讨论**
[PageRank算法--从原理到实现](http://www.cnblogs.com/rubinorth/p/5799848.html)
博文中附有较为专业的资料

	
-- 6. 怎么想到ＰageRank算法的？ 
	据《数学之美》中叙述，佩奇讲起他当年和布林是怎么想到网页排名算法的，他说：”当时我们觉得整个互联网就像一张大的图，每个网站就像一个节点，而每个网页的链接就像一个弧。我想，互联网可以用一个图或者矩阵描述，我也许可以用这个发现做篇博士论文。“	
	






