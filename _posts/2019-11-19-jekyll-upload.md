---
title: Jekyll(4)-Github+SEO
author: JackLiang
layout: post
---
<h2>在Github使用Jekyll&SEO(4) 上傳到Github+設定SEO</h2>


# 1.設定好_config.yml中網域
* baseurl:Repository名稱
* url:自己Github主頁網址(看該theme是否要設置)

```js
baseurl: "/blog" 
url: "https://XXX.github.io"
```
# 2.在Github上建立新的Repository並push上去
* 建議不要勾選Initialize this repository with a README
* cmd cd到自己專案夾中並
```html
git init
```
* 設定新的branch gh-pages(建置到github.io必須要以gh-pages這個命名)
```html
git checkout --orphan gh-pages
```
* 所有加入追蹤(除了.gitignore中)
* 建立push的連結(2.的Repository)
* commit(提交)並註解這次的上傳內容
* push上傳上去
```html
git add .
git remote add origin https://github.com/JackLiangTW/blog.git
git commit -m "first commit"
git push -u origin gh-pages
```

# 3.到Google Search Console得到憑證(網頁可以被SEO到)
* *[GoogleSearchConsole](https://search.google.com/search-console/about){:target="_blank"}*
* 登入後->新增資源

```html
EX:網域:
jackliangtw.github.io

EX:網址前置字元
https://jackliangtw.github.io/blog
```

* 輸入完案繼續 會得到幾種憑證方式(要github上面有上傳好憑證方式才能點選驗證)
* 自己這裡是使用meta憑證方式 
* 在_includes的head.html貼上驗證<meta> 並重新push到github上 ->GSC點擊驗證

```html
EX:
<meta name="google-site-verification" content="XXXXXXXXXXXXXXXXXX" />
```
* SEO設置完成會有一段時間等Google重新刷新才能搜尋到
