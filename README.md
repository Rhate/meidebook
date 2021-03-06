# 美德公益读书（网站已经暂停运营）
  [活动详情](http://meidebook.com/about)

# 功能展示
  包含“注册、登录、搜索图书、查看图书信息、评论图书、发表读书心得、上传图片、验证码等”功能。

  请访问[美德公益图书 - 首页](http://meidebook.com)体验相关功能（更侧重手机访问体验）。

# 安装本项目
  采用[Sinatra](www.sinatrarb.com)架构搭建本项目，数据库操作用[Sequel](http://sequel.jeremyevans.net/)，数据库用[SQLite](http://sqlite.com/)，界面用[WeUI](http://weui.github.io/weui/)，模板引擎用[Slim](http://slim-lang.com/)。

## 安装Ruby
### 安装[rbenv](https://github.com/rbenv/rbenv) 
  相比RVM，我更喜欢rbenv。RVM中我想要的功能，rbenv都有。用了rbenv，你会发现一些RVM的不便之处。

### 安装[rbenv-gemset](https://github.com/jf/rbenv-gemset)

## 安装其它软件
  [ImageMagick](http://www.imagemagick.org/) 用于图片处理。

## 安装本程序
```bash
$ git clone git@github.com:gazeldx/meidebook.git
$ cd /path/to/meidebook
$ gem install bundler
$ bundle install
$ sequel -m db/migrations sqlite://db/book_development.db -E # 创建数据库
$ puma # 启动项目，这时可以访问 http://localhost:9292/ 了
```

## 代码说明
[./config.ru](./config.ru)是第一个被加载的文件，[./controllers/application_controller.rb](./controllers/application_controller.rb)是一个很重要的文件。

## 安装Nginx并运行程序在80端口
  详见[./deploy/README.md](./deploy/README.md)

  其它使用帮助见[Wiki](https://github.com/gazeldx/meidebook/wiki)
