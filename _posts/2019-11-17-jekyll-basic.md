---
title: Jekyll(2)-基本架構
author: JackLiang
layout: post
---
<h2>在Github使用Jekyll&SEO(2)  Jekyll基本架構</h2>

# 1._includes資料夾
* 是存放重複使用元素(Dom/html)的地方，通常是header/footer之類的

```js
% include header.html %(整段放在{}裡/在html使用這樣載入header.html)
```

# 2._layout資料夾
* 是用來存放頁面版型的地方，ex:post.html(_post的每筆資料都是套用post.html)

```html
---
layout: default(把這行拿掉可以取消原本theme套用的一些版型)
---
<p>Hi<p>
```

# 3._post資料夾
* 是放blog檔案的地方，md/html檔案都可，是很好新增文章的系統

```html
---
title: Jekyll-環境安裝
author: JackLiang
layout: post(使用_layout -> post.html來render這筆資料)
---
<h2>我是POST</h2>
```

# 4._site資料夾
* 是jekyll serve執行時繪製的整個網站，修改這裡面內容是沒有作用的(重新serve時 還是照其他資料夾的內容繪製)

# 5._config.yml
* 這是jekyll中很重要的文件，會在這裡設定許多東西，也可以自己新增參數來存取。
* title:首頁的標題 SEO關鍵字會找尋
* description: 詳細網站解釋 SEO關鍵字會找尋
* url:架站的網域(ex:github架站 https://github.com/myID)(看theme是否要設置，有些不用設置)
* baseurl: /blog (ex:github 自己架站的repository名字) 在local serve開啟也要加上

```html
title: My blog
subtitle: Web/Unity/AR
description: 
  網頁、Unity、Spark AR技術紀錄
author: Jack Liang
email: test0@gmail.com
avatar: assets/images/avatar.jpg
url: "http://example.com"
baseurl: "/blog"
```

# 6.Gemfile
* 用來存放用到的bundle/套件 可以在這裡調整套件版本

# 7.一些code應用範例-->下面()都等於{}
* 載入圖片  site.baseurl=這網站跟目錄

```html
<img src="(( site.baseurl ))/public/img/h01.png" alt=""> 
```

* 使用if判斷render

```html
<p>(% if page.author %)(( page.author ))</p>
```

* Markdown超連結(blank) -->下面的()不變
<br>*[Ruby](https://rubyinstaller.org/downloads/){:target="_blank"}*

```html
*[Ruby](https://rubyinstaller.org/downloads/){:target="_blank"}* 
```