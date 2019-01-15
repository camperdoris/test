# gitbook
## gitbook
## gitbook
<br>
```
標題一，在文字前面加上#
標題二，在文字前面加上##
標題三，在文字前面加上###
```
<br>

## 安裝
<font color="FF0088">要使用gitbook，要先安裝 Node.js 並通過 npm 來安裝</font>
<br>
```
npm install gitbook-cli -g
```
<br>
<br>
<br>
## 指令
1、初始化書藉目錄      gitbook init<br>
2、編譯和執行         gitbook serve<br>
3、開啟本地4000端口   http://localhost:4000/<br>
<br>
<br>
<br>
## 改變電子書目錄結構
1、在桌面新增一個資料夾test<br>
2、使用編輯器開啟test文件夾<br>
3、SUMMARY.md  這個是存放書的目錄結構<br>
4、book.json   這個是放入插件的json檔<br>
<br>
<br>
<br>
## 增加圖片與影片方法
1、可以至https://imgur.com/  找圖，複製Markdown link，貼上連結後，最前面需要加上符號"!"，執行刷新 'gitbook serve'
<br>
```
![Imgur](https://i.imgur.com/ZPYcvnu.jpg)
```
![Imgur](https://i.imgur.com/ZPYcvnu.jpg)
<br>
<br>
<br>
<hr size="5" align="center" noshade width="90%" color="#AAAAAA">
<br>
2、可以使用html標籤崁入圖片
```
<img src="https://i.imgur.com/ZPYcvnu.jpg" width="100%" height="100%">
```
<img src="https://i.imgur.com/ZPYcvnu.jpg" width="100%" height="100%">
<br>
<br>
<br>
<hr size="5" align="center" noshade width="90%" color="	#AAAAAA">
<br>
3、崁入影片
<br>
<br>
<br>
狗狗影片
<br>
```
<iframe width="560" height="315" src="https://www.youtube.com/embed/1ZWLTt8Hgiw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/1ZWLTt8Hgiw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<br>
<br>
貓咪影片
<br>
```
<iframe width="560" height="315" src="https://www.youtube.com/embed/wtQuGwDWlpo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/wtQuGwDWlpo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br>
<br>
<br>
<hr size="5" align="center" noshade width="90%" color="	#AAAAAA">
<br>
4、崁入連結
```
[google](https:\\google.com)
```
[google](https:\\google.com)
<br>
<br>
<br>
<hr size="5" align="center" noshade width="90%" color="	#AAAAAA">
<br>



5、插件
<font color="FF0088">Github Button插件</font>
<font color="FF0088">通過 npm 來安裝</font>
<br>
```
npm install gitbook-plugin-github-buttons
```
<br>
<font color="FF0088">將二段程式碼分別加入book.json中並存檔</font>
<br>
```
{
  "plugins": [
    "github-buttons"
  ],
  "pluginsConfig": {
    "github-buttons": {
      "buttons": [{
        "user": "azu",
        "repo": "JavaScript-Plugin-Architecture",
        "type": "star",
        "size": "small"
        }]
    }
  }
}
```
<br>
<font color="FF0088">gitbook install-只要有修改到json檔都要重新安裝</font>
<font color="FF0088">gitbook serve</font>
<br>


6、將電子書部署到GitHub中
    a)下載安裝git
        https://git-scm.com/downloads
        在test資料夾中點擊右鍵，選擇Git bash here
        並執行gitbook serve
        開啟電子書  http://localhost:4000
    b)  進入 github.com 網站
        Create a new repository   
        name：test
        Description：電子書測試
        選擇public免費，如果選私人要付錢
        建立

    b)第一次使用需初始化
    git init   會生成一個隱藏的文件夾.git，可使用ls-la查看
    git remote add origin https://github.com/camperdoris/test.git
    git add .
    git commit -m 'up'
    git push -u origin master

    c)master 分支保存書藉
    gh-pages 分支保存書職編譯後的 HTML 文件
    先將TEST資料夾中的_book資料整個複製備份
    然後輸入 git checkout -b gh-pages
    此時原本（master）會改為（gh-pages）