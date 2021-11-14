## 短代码
贴心の小功能


### 博客内文章跳转

格式示例

```
[art]cid[/art]
```

cid为文章id

![文章跳转](https://cdn.exia.xyz/img/G_Doc/G_theme_art2art.png)

### 提示栏

格式示例

```html
[notice]哟哈[/notice]
```

![提示栏](https://cdn.exia.xyz/img/G_Doc/G_theme_shortcode_notice2.png)

### 警告栏

格式示例

```html
[warn]哟哈[/warn]
```

![警告栏](https://cdn.exia.xyz/img/G_Doc/G_theme_shortcode_warn2.png)



### 标签

格式示例

```html
[tag]哦哦[/tag] [tag type="red"]嘿嘿[/tag] [tag type="black"]哈哈[/tag]
```

type控制颜色，默认为蓝色(`#07F`)，目前仅支持`red` `black`

![警告框](https://cdn.exia.xyz/img/G_Doc/G_themes_shortcode_tags.png)

### DPlayer

格式示例

```html
[dplayer id="xxx" url="demo.mp4" pic="demo.png"]随便写点（建议空格）不写会出事[/dplayer]
```

id处填写视频id，**必须填写**

url处填写视频链接，**必须填写**

pic处填写封面链接，可选

**注意！**一定要在内容中随便写点东西，建议空格

![DP](https://cdn.exia.xyz/img/G_Doc/G_themes_shortcode_dplayer.png)



### B站视频

格式示例

```
[bili]av号[/bili]
```



### 折叠框

格式示例

```html
[collapse title="标题"]
我是内容
[/collapse]
```

![](https://cdn.exia.xyz//img/G_Doc/20210508232744.png)

![](https://cdn.exia.xyz//img/G_Doc/20210508232727.png)

### 相册

格式示例

```html
[photos]
首页,https://cdn.exia.xyz/img/blog/588/20201127084700.png|
管理页,https://cdn.exia.xyz/img/blog/588/20201127084808.png|
详情页,https://cdn.exia.xyz/img/blog/588/20201127084900.png|
黑色呢？,https://cdn.exia.xyz/img/blog/447/deepink1.jpg|
[/photos]
```

外层用`[photos][/photos]`包裹，里面的图片按照

```html
图片名,图片链接|
```

的格式一行一行添加。

相册不会自动换行，如果想使用多行的相册请使用多个`[photos]`短代码。

![](https://cdn.exia.xyz//img/G_Doc/20210508233154.png)

