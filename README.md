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
0. JavaScriptを使った全文検索  
[JavaScriptを使ってHugoサイト内に全文検索を取り付けてみた](https://snap.textgh.org/201801152012/)  
[Hugo に全文検索を取り付けた](http://rs.luminousspice.com/hugo-site-search/)

## 書いておくべきconfig.toml
```
baseURL = "/"
title = "doshirouto3"
languageCode = "ja-JP"
HasCJKLanguage = true
[taxonomies]
tag = "tags"
[params]
favicon = ""
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

## サイト内の全文検索を有効にするには
2つの投稿(Markdownファイル)を用意しておく必要がある  
1. full_text_index.md  
全文検索用のインデックスファイルを生成するため 
```
+++
date = "2018-01-01T00:00:00+09:00"
type = "full_text_index"
url = "full_text_index.txt"
+++

``` 

2. full_text_search.md  
全文検索用のページを生成するため 
```
+++
date = "2018-01-01T00:00:00+09:00"
type =  "full_text_search"
url =  "search"
title =  "サイト内を全文検索します"
+++

```

## 使い方
```
$ hugo new site doshirouto
$ cd doshirouto/themes/
$ git clone https://github.com/TakeuchiDensetsu/doshirouto3.git
$ cd ..
$ nano config.toml
```