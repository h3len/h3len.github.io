---
title: hexo next主题文章版权信息配置
date: 2017-09-05 01:26:43
tags:
- next
- Hexo
categories:
- Diary
---
Hexo的next主题可通过配置在文章底部增加版权信息，另外通过修改让部分文章能不显示版权信息
## 默认文章底部增加版权信息
> themes/next/_config.yml 文件

```yaml
# Declare license on posts
post_copyright:
  enable: true
  license: CC BY-NC-SA 4.0
  license_url: https://creativecommons.org/licenses/by-nc-nd/4.0/
```
达到效果如下图：
![20170905013206](http://ovsdspcnp.bkt.clouddn.com/20170905013206.png)
## 允许部分文章不显示版权信息
> themes/next/layout/_macro/post-copyright.swig 文件中

* 在开头加上
```
{% if not page.disable_copyright %}
```
* 在结尾加上
```
{% endif %}
```
  
如下：
```yaml
{% if not page.disable_copyright %}
<ul class="post-copyright">
  <li class="post-copyright-author">
    <strong>{{ __('post.copyright.author') + __('symbol.colon') }}</strong>
    {{ config.author }}
  </li>
  <li class="post-copyright-link">
    <strong>{{ __('post.copyright.link') + __('symbol.colon') }}</strong>
    <a href="{{ post.permalink }}" title="{{ post.title }}">{{ post.permalink }}</a>
  </li>
  <li class="post-copyright-license">
    <strong>{{ __('post.copyright.license_title') + __('symbol.colon') }} </strong>
    {{ __('post.copyright.license_content', theme.post_copyright.license_url, theme.post_copyright.license) }}
  </li>
</ul>
{% endif %}
```
某文章如不需要添加末尾版权信息，可在.md文件开头添加：
```md
---
disable_copyright: true
```

