---
title: Jekyll-套用主題
author: JackLiang
layout: post
plink: "/2019/12/17/jekyll-basic"
---
<h2>在Github使用Jekyll&SEO(3)  Jekyll套用主題</h2>

# 1.*[theme主題](https://jekyllthemes.io/free){:target="_blank"}*
* 有很多好用漂亮的主題，用Github clone下來或是下載zip檔案

# 2.cmd安裝版型套件
* 安裝該主題用到的套件

```html
gem install bundler
```
# 套件版本錯誤修改-jekyll版本不同
* 先用jekyll -v找到自己版本，再到到Gemfile或是.gemspec修改jekyll版本

# 套件版本錯誤修改-bundle版本不同
* 如果出現類似的錯誤 可以到Gemfile或是.gemspec修改套件版本

```html
Bundler could not find compatible versions for gem "bundler":
  In Gemfile:
    bundler (~> 2.02) x64-mingw32

  Current Bundler version:
    bundler (2.1.1)
This Gemfile requires a different version of Bundler.
Perhaps you need to update Bundler by running `gem install bundler`?

Could not find gem 'bundler (~> 2.02)' in any of the relevant sources:
  the local ruby installation
```
* Gemfile修改版本完成再次安裝

```js
bundle install
```

# 3.執行
```js
jekyll serve
```

# 修改theme內的資料內容
* theme大概的架構都在這篇 
*<a href="{{ site.baseurl }}{{page.plink}}">Jekyll基本結構</a>*