---
title: Jekyll-Github+SEO
author: JackLiang
layout: post
---
<h2>在Github使用Jekyll&SEO(4) 上傳到Github+設定SEO</h2>


# 1.設定好_config.yml中網域
* baseurl:Repository名稱
* url:自己Github主頁網址

```js
baseurl: "/blog" 
url: "https://github.com/JackLiangTW"
```
# 2.在Github上建立新的Repository
* 建議不要勾選Initialize this repository with a README
* cmd cd到自己專案夾中
```html
git init
```
* 設定新的branch gh-pages(建置到github.io必須要以gh-pages這個命名)
```html
git checkout --orphan gh-pages
```
* 所有加入追蹤(除了.gitignore中) / 建立push的連結 / commit並註解這次的上傳內容
```html
git add .
git remote add origin https://github.com/JackLiangTW/blog.git
git commit -m "first commit"
```

# 3.到Google Search Console得到憑證
* *[GoogleSearchConsole](https://search.google.com/search-console/about){:target="_blank"}*
* https://jackliangtw.github.io/

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
