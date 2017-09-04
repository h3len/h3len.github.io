---
title: 常用前端库CDN
date: 2017-09-04 20:45:21
tags:
- CDN
- Google
- fonts
categories:
- 资源 
---
## 前言 ##
打开网页经常遇到加载google字体慢或者失败的问题，严重影响体检，这里找到一些如下代理镜像或CDN加速服务
  
## CSS.NET常用前端公共库 CDN 服务
### CDNJS 前端公共库
[https://cdnjs.cat.net/ajax/libs/](https://cdnjs.cat.net/ajax/libs/ "https://cdnjs.cat.net/ajax/libs/")
### Google 公共库
[https://ajax.cat.net/](https://ajax.cat.net/ "https://ajax.cat.net/")
### Gravatar
[https://gravatar.cat.net/](https://gravatar.cat.net/ "https://gravatar.cat.net/")
### Google 字体库
[https://fonts.cat.net/](https://fonts.cat.net/ "https://fonts.cat.net/")
### 用法
参考：[https://sb.sb/css-cdn/](https://sb.sb/css-cdn/)
将域名替换即可
## 中科大 Google Fonts 加速服务
参考：[https://lug.ustc.edu.cn/wiki/lug/services/googlefonts](https://lug.ustc.edu.cn/wiki/lug/services/googlefonts "中科大GoogleFonts")
  
提供以下域名代理：

- ajax.googleapis.com => ajax.lug.ustc.edu.cn
- fonts.googleapis.com => fonts.lug.ustc.edu.cn
- themes.googleusercontent.com => google-themes.lug.ustc.edu.cn
  
## hexo next主题字体设置
参考：[http://theme-next.iissnan.com/theme-settings.html](http://theme-next.iissnan.com/theme-settings.html "http://theme-next.iissnan.com/theme-settings.html")
> themes/next/_config.yml中

```yaml
font:
  enable: true

  # Uri of fonts host. E.g. //fonts.googleapis.com (Default)
  host: //fonts.cat.net
```