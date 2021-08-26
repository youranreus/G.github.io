# 你来了

如果想要追求更好的效果请继续看下去吧。



# 1.主题的进阶配置



# 2.使用独立页面做首页

### 2.1设置外观的位置
![](https://goojoe.cc/img/Gthemedoc/2-1.png)

![](https://goojoe.cc/img/Gthemedoc/2-2.png)

### 2.2打开设置

首先请到 **控制台->更换外观->设置外观** 处打开这个选项（cool为打开，nope为关闭）

![独立首页.PNG](https://cdn.exia.xyz//img/G_Doc/20210101122018.png)

### 2.3新增页面作为首页

### 2.4独立界面位置

![](https://goojoe.cc/img/Gthemedoc/2-3.png)

然后可以在**独立页面**新增一个页面作为首页，内容可以自定义（奇奇怪怪的问候啊，歌词啊...）

![](https://goojoe.cc/img/Gthemedoc/2-4.png)

然后到**设置->阅读**处按照下图设置

![](https://goojoe.cc/img/Gthemedoc/2-5.png)

如果设置了伪静态，可以在主题设置中将头部文章路径设置为blog。如果你不知道伪静态是什么或者没有设置伪静态就不用修改这一项。

![](https://cdn.exia.xyz//img/G_Doc/20210508195239.png)

# 3.伪静态

没有伪静态的话你的链接会是这样的：域名/index.php/blog，这对用户非常不友好，看着也不好看所以只要开启伪静态就可以看起来完全消失

## 3.1宝塔面板

![](https://goojoe.cc/img/Gthemedoc/2-6.png)

![](https://goojoe.cc/img/Gthemedoc/2-7.png)

![](https://goojoe.cc/img/Gthemedoc/2-8.png)

其他的我不知道，这是最简单的，若不行请百度吧

## 3.2永久链接设置

![](https://goojoe.cc/img/Gthemedoc/2-9.png)

![](https://goojoe.cc/img/Gthemedoc/2-10.png)



# 4.更改字体

到网站路径

``` markdown
www/wwwrooot/域名/usr/themes/G/CSS
```

![](https://goojoe.cc/img/Gthemedoc/2-11.png)

![](https://goojoe.cc/img/Gthemedoc/2-12.png)

修改完后过一会应该可以生效，若你的网站加了CDN缓存可能需要更久，建议清理浏览器缓存TTL

## 友情链接

### 插件

作者首推使用[寒泥大佬](http://www.imhan.com/archives/typecho-links/)的[links插件](http://www.imhan.com/archives/typecho-links/)，使用了此插件的话，通过插件添加友情链接即可

![友情链接.PNG](https://cdn.exia.xyz//img/G_Doc/20210101123106.png)

就像这样



### 非插件版

~~**1.5**版本后不再支持非插件模式。望周知。~~

现在可以通过**后台->外观->设置外观**->**友情链接**处按照以下格式添加。

> **链接名称,链接地址,链接描述,链接分类,头像链接**
> 不同信息之间用英文逗号“,”分隔，例如：
> **季悠然,https://gundam.exia.xyz/,寻找有趣的灵魂,好朋友,https://xxx.xxx.com/avatar.jpg**
> 多个链接换行即可，一行一个

**注意！**当启用友情链接插件后，该方式添加的友链不会生效。

#### 最终效果

![展示](https://cdn.exia.xyz//img/G_Doc/20210101123145.png)

## 文章头图

当发布文章时，请在自定义字段中添加`imgurl`字段，就像这样

![](https://cdn.exia.xyz//img/G_Doc/20210101123457.png)







## 独立页面启用评论

模板默认关闭独立页面的评论功能，如果要启用，请在自定义字段中添加`enableComment`字段并赋值`1`，就像这样

![开启评论](https://cdn.exia.xyz/img/G_Doc/G_theme_enableComment.png)

## 搜索

此功能需要插件[ExSearch](https://github.com/AlanDecode/Typecho-Plugin-ExSearch)支持

当启用ExSearch插件时，会在footer处生成一个搜索按钮



## 打赏

设置位置**后台->外观->设置外观**->**打赏二维码图片**

![赞赏设置](https://cdn.exia.xyz/img/G_Doc/G_theme_feed_option.png)

若这一栏被填写，将在文章页生成赞赏按钮

![赞赏按钮](https://cdn.exia.xyz/img/G_Doc/G_theme_btn_feed.png)

## 更多自定义选项

### 背景图片

设置位置**后台->外观->设置外观**->背景图片

请填入背景图片链接



### 网站运行时间

设置位置**后台->外观->设置外观**->运行时间

格式YYYY-MM-DD



### 半透明

设置位置**后台->外观->设置外观**->半透明开关



### 平滑滚动开关

设置位置**后台->外观->设置外观**->平滑滚动开关



### 文章单双排显示

设置位置**后台->外观->设置外观**->**开启文章页双排显示**



### ~~罗德岛限定图标~~

~~设置位置**后台->外观->设置外观**->**罗德岛纪念图标**~~



### 自定义logo

设置后会在头部右上角显示

设置位置**后台->外观->设置外观**->**头部logo**



### 自定义头部背景颜色

设置位置**后台->外观->设置外观**->头部背景颜色



### 自定义CSS

设置位置**后台->外观->设置外观**->**自定义CSS**



### 自定义JS

设置位置**后台->外观->设置外观**->**自定义JS**

分为头部和尾部JS，按需添加即可。

**注意！本主题已包含JQ，无需再次引入。**



### 自定义头部文章路径

默认index.php/blog

设置位置**后台->外观->设置外观**->**头部文章路径**



### 文章默认头图

设置位置**后台->外观->设置外观**->**没有设置文章头图的就用这里的图片啦**

ps.如果单单填写张图片的地址可能略显枯燥。可以在此处填写你的随机图片api以达到更加美观的效果。



### 备份主题数据

设置位置**后台->外观->设置外观**->**备份**



### 开启加载进度条

设置位置**后台->外观->设置外观**->**开启加载进度条**



### 开启侧边栏小相框

设置位置**后台->外观->设置外观**->**启用侧边栏小相框**

![](https://cdn.exia.xyz//img/G_Doc/20210508232241.png)

之后再填写下面的两个设置就完成辣。

效果展示：

![](https://cdn.exia.xyz//img/G_Doc/20210508232435.png)

![](https://cdn.exia.xyz//img/G_Doc/20210508232414.png)



