---
title: Jekyll(1)-環境安裝
author: JackLiang
layout: post
---
<h2>在Github使用Jekyll&SEO(1)  Ruby & Jekyll安裝</h2>

# 1.要先安裝  *[Ruby](https://rubyinstaller.org/downloads/){:target="_blank"}* 
* 安裝好exe後在Ruby Installer(自動挑出)照指令順序輸入1、2、3
* 跑完1後不需要執行Run MSYS2
* 安裝完成1、2、3步驟後關掉Installer 開啟cmd 或 cmder
* 輸入ruby -v確定一下版本(要2.0以上)

# 2.使用cmder安裝Jekyll與bundler
```js
gem install jekyll bundler
```

# 3.創立Jekyll專案並cd帶該目錄中
```js
jekyll new test1
cd test1
```

# 4.執行專案
* 第一次用
```js
bundle exec jekyll
```
* 之後都用
```js
jekyll serve
```
