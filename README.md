# 一、乐优商城门户

门户系统面向的是用户，安全性很重要，而且搜索引擎对于单页应用并不友好。因此门户系统不再采用与后台系统类似的SPA（单页应用）。
依然是前后端分离，不过前端的页面会使用独立的html，在每个页面中使用vue来做页面渲染。采用live-server热部署方式

安装live-server
npm install live-server -g 

运行命令：
live-server --port=9002

修改C:\Windows\System32\drivers\etc下hosts文件：
```$xslt
  127.0.0.1 api.leyou.com          #网关Zuul
  127.0.0.1 manage.leyou.com       #后台系统地址
  127.0.0.1 www.leyou.com          #前端网站
  192.168.19.128 image.leyou.com   #文件上传
```

运行windows本地nginx域名跳转：
./nginx.exe -s reload 

浏览器访问：www.leyou.com
