## 你来了

如果想要追求更好的效果请继续看下去吧。



## 主题的进阶配置



## 使用独立页面做首页

首先请到**后台->外观->设置外观**处打开这个选项（cool为打开，nope为关闭）

![独立首页.PNG](https://i.loli.net/2019/03/10/5c84c5afa15a3.png)

然后新建一个页面作为首页，内容可以自定义（奇奇怪怪的问候啊，歌词啊...）

然后到**后台->设置->阅读**处按照下图设置

![独立首页](https://i.loli.net/2019/02/07/5c5c46e2d17ce.png)

大功告成！

## 友情链接

### 插件

作者首推使用[寒泥大佬](http://www.imhan.com/archives/typecho-links/)的[links插件](http://www.imhan.com/archives/typecho-links/)，使用了此插件的话，通过插件添加友情链接即可

![友情链接.PNG](https://i.loli.net/2019/03/10/5c84c730167c2.png)

![友情链接](https://i.loli.net/2019/02/12/5c6249ce21214.png)

就像这样



### 非插件版

**1.5**版本后不再支持非插件模式。望周知。



### 最终效果

![展示](https://i.loli.net/2020/02/16/3CmRafVSAlHjtrG.png)

## 文章头图

当发布文章时，请在自定义字段中添加`imgurl`字段，就像这样

![文章头图](https://i.loli.net/2019/02/12/5c624d23716e0.png)



## 搜索

此功能需要插件[ExSearch](https://github.com/AlanDecode/Typecho-Plugin-ExSearch)支持

当启用ExSearch插件时，会在footer处生成一个搜索按钮



## 打赏

设置位置**后台->外观->设置外观**->**打赏二维码图片**

![赞赏设置](https://cdn.exia.xyz/img/G_theme_feed_option.png)

若这一栏被填写，将在文章页生成赞赏按钮

![赞赏按钮](https://cdn.exia.xyz/img/G_theme_btn_feed.png)

## 更多自定义选项

### 背景图片

设置位置**后台->外观->设置外观**->背景图片

请填入背景图片链接



### 网站运行时间

设置位置**后台->外观->设置外观**->运行时间

格式YYYY-MM-DD



### 半透明

设置位置**后台->外观->设置外观**->半透明开关



### 文章单双排显示

设置位置**后台->外观->设置外观**->**开启文章页双排显示**



### 罗德岛限定图标

设置位置**后台->外观->设置外观**->**罗德岛纪念图标**



### 文章默认头图

设置位置**后台->外观->设置外观**->**没有设置文章头图的就用这里的图片啦**

ps.如果单单填写张图片的地址可能略显枯燥。可以在此处填写你的随机图片api以达到更加美观的效果。



## 短代码



### 博客内文章跳转

格式示例

```
[art]cid[/art]
```

cid为文章id

![文章跳转](https://cdn.exia.xyz/img/G_theme_art2art.png)



### 下载按钮

格式示例

```
[dl href="gundam.exia.xyz"]blog.zip[/dl]
```

href为目标地址,中间的`blog.zip`可替换成相应文件名

![下载按钮](https://cdn.exia.xyz/img/G_theme_btn_download.png)

### 提示框

格式示例

```html
[notice]哟哈[/notice]
```

![提示框](https://cdn.exia.xyz/img/G_themes_shortcode_notice.png)

### 警告框

格式示例

```html
[warn]哟哈[/warn]
```

![警告框](https://cdn.exia.xyz/img/G_themes_shortcode_warn.png)

### 标签

格式示例

```html
[tag]哦哦[/tag] [tag type="red"]嘿嘿[/tag] [tag type="black"]哈哈[/tag]
```

type控制颜色，默认为蓝色(`#07F`)，目前仅支持`red` `black`

![警告框](https://cdn.exia.xyz/img/G_themes_shortcode_tags.png)

