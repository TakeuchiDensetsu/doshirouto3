# Hugoのテーマ 「doshirouto3」
HugoとBootStrapの初心者がHugoのテーマ「doshirouto3」を書きました

## 使っているもの
1. Hugo(Hugo Static Site Generator v0.32.4 linux/amd64 BuildDate: 2018-01-11T17:58:37+09:00)
0. Bootstrap(bootstrap-4.0.0-dist.zip)  
[Download](https://github.com/twbs/bootstrap/releases/download/v4.0.0/bootstrap-4.0.0-dist.zip)
0. jquery(jquery-3.3.1.min.js)  
[Download](https://jquery.com/download/)
0. Font Awesome(font-awesome-4.7.0.zip)  
[Download](https://fontawesome.com/v4.7.0/)
0. highlight.js(highlight.js 9.12.0)  
[Download](https://highlightjs.org/download/)
0. Lightbox(Lightbox 2.10.0)  
[Download](http://lokeshdhakar.com/projects/lightbox2/)

## 書いておくべきconfig.toml
```
baseURL = "/"
title = "doshirouto3"
languageCode = "ja-JP"
HasCJKLanguage = true
[taxonomies]
tag = "tags"
[params]
enumerate = "page"
tracking_id = ""
avatar_url = "/image/profile/avatar.png"
description = "Site Description"
copyright = " TakeuchiDensetsu; all rights reserved."
[[menu.navbar]]
    name = "Home"
    weight = -10
    pre = "<i class='fa fa-home'></i>"
    identifier = ""
    url = "/"
```
enumerateにはlist.htmlで列挙するContentTypeを指定する
例えば"page"や"post"など

## ショートコード
Fluid Imageな<img>タグを吐く
{{< img-fluid src="/image/source.png" alt="AlternateText" >}}

Overflow Imageな<img>タグを吐く
{{< img-overflow src="/image/source.png" alt="AlternateText" >}}

Fluid ImageでLightboxが効いた<img>タグを吐く
{{< img-lightbox src="/image/source.png" group="LightboxImageGroup" alt="AlternateText" >}}