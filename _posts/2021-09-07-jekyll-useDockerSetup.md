---
title: 使用Docker架設Jekyll theme
author: JackLiang
layout: post
---
<h2>Local端使用Docker架設Jekyll theme專案</h2>


# 1.安裝Docker
* *[安裝教學](https://docs.docker.com/get-docker/){:target="_blank"}*

# 2.選擇jekyll theme使用
* *[theme主題](https://jekyllthemes.io/free){:target="_blank"}*
* git clone下來並cd到該專案中
```js
git clone https://github.com/chrisbobbe/jekyll-theme-prologue.git
cd jekyll-theme-prologue
```
# 3.在Docker hub中找尋合適的Jekyll version
* *[Docker Jekyll](https://hub.docker.com/r/jekyll/jekyll/tags){:target="_blank"}*
* 建議使用 jekyll/jekyll:4.0

# 4.Docker指令架設Jekyll專案
```js
docker run --volume="$PWD:/srv/jekyll" -p 4000:4000 -it jekyll/jekyll:4.0.0 jekyll serve
```
* --volume (本地端啟動資料位置 : container端虛擬機專案  位置)
* $PWD (cmd現在路徑位置)
* -p (對應port號)
* jekyll serve (jekyll架設專案指令)

# 其他基本Docker 指令
* docker ps (列出Docker container列表)
* docker kill [CONTAINER ID] (停止並刪除container,CONTAINER ID : 從docker ps取得)

# 參考資料:
*[影片教學](https://www.youtube.com/watch?v=ZHQ3IwIL590){:target="_blank"}*
