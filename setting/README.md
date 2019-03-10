## 你来了

如果想要追求更好的效果请继续看下去吧。



## 主题的进阶配置

只是把安装主题的话是无法驾驭主题G的，需要进一步配置。



首先至少设置以下两个独立页面，分别作为**友情链接页面**和**关于页面**，名称可以自定义

![pages](https://i.loli.net/2019/02/12/5c62404b4bb0b.png)

注意独立页面链接的配置(途中黄色区域)

![slugs](https://i.loli.net/2019/02/12/5c624205590ed.jpg)

那么基本的两个页面设置完毕。

### 常见问题



​	Q:设置了之后从前台访问页面显示404（明明链接是对的）

​	A:请前往**[后台->设置->永久链接]**处启用**地址重写功能**

​	Q:我已经启用了地址重写功能，为什么还是不行

​	A:那么多半是伪静态出了问题

如果网站环境为APACHE，请在typecho根目录下新建`.htaccess`文件，文件内容如下

```apache
<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteBase /
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^(.*)$ index.php [L,E=PATH_INFO:$1]
</IfModule>
```



如果环境为nginx，代码则为

```nginx
location / {
index index.html index.php;
if (-f $request_filename/index.html) {
rewrite (.*) $1/index.html break;
}
if (-f $request_filename/index.php) {
rewrite (.*) $1/index.php;
}
if (!-f $request_filename) {
rewrite (.*) /index.php;
}
}
```

具体操作请到百度查找，关键词为`typecho伪静态`。



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

如果不想安装插件，则需手动代码添加

1.前往友情链接页面编辑页面

2.按照以下格式添加友链

**请注意务必在页面头部和尾部加上`!!!`**

```html
!!!
<li class='clear hoverup'>
    <a href='{url}' target='_blank'><img src='{image}' alt='{name}'/></a>
    <div class='link-item-content'>
        <h3>{name}</h3>
	<span>{sort}</span>
	<p>{description}</p>
    </div>
</li>

!!!
```

3.将主题文件夹下的link.php文件中如下字段删去

```php
<?php Links_Plugin::output("
    <li class='clear'>
        <a href='{url}' target='_blank'><img src='{image}' alt='{name}'/></a>
        <div class='link-item-content'>
            <h3>{name}</h3>
            <span>{sort}</span>
            <p>{description}</p>
        </div>
    </li>
", 0); ?>
```



第二步中的短代码含义如下

> {url}=>链接
>
> {name}=>名称
>
> {sort}=>分类
>
> {description}=>描述
>
> {image}=>头像

### 最终效果

![展示](https://i.loli.net/2019/02/12/5c624a187a2c7.png)

## 文章头图

当发布文章时，请在自定义字段中添加`imgurl`字段，就像这样

![文章头图](https://i.loli.net/2019/02/12/5c624d23716e0.png)



## 短代码

### 博客内文章跳转

格式示例

```
[art]cid[/art]
```

cid为文章id

### 下载按钮

格式示例

```
[dl href="gundam.exia.xyz"]blog.zip[/dl]
```

href为目标地址,中间的`blog.zip`可替换成相应文件名

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