# Hugoのテーマ 「doshirouto3」
HugoとBootStrapの初心者がHugoのテーマ「doshirouto3」を書きました

## 使っているもの
1. Hugo(Hugo Static Site Generator v0.32.4 linux/amd64 BuildDate: 2018-01-11T17:58:37+09:00)
0. Bootstrap(bootstrap-4.0.0-dist.zip)  
[Download](https://github.com/twbs/bootstrap/releases/download/v4.0.0/bootstrap-4.0.0-dist.zip)
0. jquery(jquery-3.3.1.min.js)  
[Download](https://jquery.com/download/)

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
```