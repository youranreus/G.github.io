## 安装

1. 下载主题包并解压
2. 将文件夹**重命名为G** ，上传至typecho主题文件夹下。
3. 启用主题**后台设置—>控制台—>外观**

至此主题已经安装完毕，但是离使用还有一段距离，请继续阅读[进阶配置]

安装以下插件可以获取更好的使用体验

- [ExSearch](https://github.com/AlanDecode/Typecho-Plugin-ExSearch)

## 基本配置

### 页面设置

首先至少设置以下三个独立页面，分别作为**友情链接页面** 、**关于页面**和**归档页面**，名称可以自定义

![pages](https://cdn.exia.xyz/img/G_theme_page_option.png)

注意独立页面链接的配置(下图中黄色区域)

![links](https://cdn.exia.xyz/img/G_theme_page_option_links.png)

![archive](https://cdn.exia.xyz/img/G_theme_page_option_archive.png)

![about](https://cdn.exia.xyz/img/G_theme_page_option_about.png)



那么基本的页面设置完毕。

### 评论设置

前往**设置**->**评论**->**评论显示**处选择 `将较新的评论显示在前面`

![comment](https://cdn.exia.xyz/img/G_theme_comment_option.png)



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



## 更新

1. 下载新版完整主题包
2. 解压，将原本的主题文件夹清空，再将此主题包内的文件移入主题文件夹

> 常见问题：
>
> - Q：更新后css混乱怎么办？
>
> A：请刷新**浏览器缓存（以及cdn等）**

## 最后

**强烈建议继续阅读[进阶配置]**