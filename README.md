## 目录
- [3 构建页面](https://github.com/andy-love-coding/laravel1.7#3-%E6%9E%84%E5%BB%BA%E9%A1%B5%E9%9D%A2)
  - [3.2 创建应用](https://github.com/andy-love-coding/laravel1.7#32-%E5%88%9B%E5%BB%BA%E5%BA%94%E7%94%A8)
    - 修改 hosts 、新增站点
  - [3.3 静态页面布局](https://github.com/andy-love-coding/laravel1.7#33-%E9%9D%99%E6%80%81%E9%A1%B5%E9%9D%A2)
  - [3.4 Artisan 命令](https://github.com/andy-love-coding/laravel1.7#34-artisan-%E5%91%BD%E4%BB%A4)
- [4 优化页面](https://github.com/andy-love-coding/laravel1.7#4-%E4%BC%98%E5%8C%96%E9%A1%B5%E9%9D%A2)
  - [4.2 样式美化](https://github.com/andy-love-coding/laravel1.7#42-%E6%A0%B7%E5%BC%8F%E7%BE%8E%E5%8C%96)
    - 2.设置前端扩展包镜像
    - 3.安装 Bootstrap
  - [4.3 前端工作流](https://github.com/andy-love-coding/laravel1.7#43-%E5%89%8D%E7%AB%AF%E5%B7%A5%E4%BD%9C%E6%B5%81)
  - [4.4 浏览器缓存问题](https://github.com/andy-love-coding/laravel1.7#44-%E6%B5%8F%E8%A7%88%E5%99%A8%E7%BC%93%E5%AD%98%E9%97%AE%E9%A2%98)
  - [4.5 局部视图 (拆分布局视图)](https://github.com/andy-love-coding/laravel1.7#53-%E6%9F%A5%E7%9C%8B%E6%95%B0%E6%8D%AE%E5%BA%93%E8%A1%A8)
  - [4.6 布局中的链接(命名路由)](https://github.com/andy-love-coding/laravel1.7#46-%E5%B8%83%E5%B1%80%E4%B8%AD%E7%9A%84%E9%93%BE%E6%8E%A5%E5%91%BD%E5%90%8D%E8%B7%AF%E7%94%B1)
  - [4.7 用户注册页面](https://github.com/andy-love-coding/laravel1.7#47-%E7%94%A8%E6%88%B7%E6%B3%A8%E5%86%8C%E9%A1%B5%E9%9D%A2)
- [5 用户模型](https://github.com/andy-love-coding/laravel1.7#5-%E7%94%A8%E6%88%B7%E6%A8%A1%E5%9E%8B)
  - [5.1 章节说明](https://github.com/andy-love-coding/laravel1.7#51-%E7%AB%A0%E8%8A%82%E8%AF%B4%E6%98%8E)
  - [5.2 数据库迁移](https://github.com/andy-love-coding/laravel1.7#52-%E6%95%B0%E6%8D%AE%E5%BA%93%E8%BF%81%E7%A7%BB)
  - [5.3 查看数据库表（数据库查询工具 SequelPro）](https://github.com/andy-love-coding/laravel1.7#53-%E6%9F%A5%E7%9C%8B%E6%95%B0%E6%8D%AE%E5%BA%93%E8%A1%A8)
  - [5.4 模型文件](https://github.com/andy-love-coding/laravel1.7#54-%E6%A8%A1%E5%9E%8B%E6%96%87%E4%BB%B6)
    - 使用 `App\Models` 命名空间
  - [5.5 创建用户对象(Tinker)](https://github.com/andy-love-coding/laravel1.7#55-%E5%88%9B%E5%BB%BA%E7%94%A8%E6%88%B7%E5%AF%B9%E8%B1%A1tinker)
  - [5.6 查找用户对象(测试)](https://github.com/andy-love-coding/laravel1.7#56-%E6%9F%A5%E6%89%BE%E7%94%A8%E6%88%B7%E5%AF%B9%E8%B1%A1%E6%B5%8B%E8%AF%95)
  - [5.7 更新用户对象(测试)](https://github.com/andy-love-coding/laravel1.7#57-%E6%9B%B4%E6%96%B0%E7%94%A8%E6%88%B7%E5%AF%B9%E8%B1%A1%E6%B5%8B%E8%AF%95)
  - [5.8 小结](https://github.com/andy-love-coding/laravel1.7#58-%E5%B0%8F%E7%BB%93)
- [6 用户注册](https://github.com/andy-love-coding/laravel1.7#6-%E7%94%A8%E6%88%B7%E6%B3%A8%E5%86%8C)
  - [6.2 显示用户信息](https://github.com/andy-love-coding/laravel1.7#62-%E6%98%BE%E7%A4%BA%E7%94%A8%E6%88%B7%E4%BF%A1%E6%81%AF)
  - [6.3 注册表单](https://github.com/andy-love-coding/laravel1.7#63-%E6%B3%A8%E5%86%8C%E8%A1%A8%E5%8D%95)
  - [6.4 用户数据验证](https://github.com/andy-love-coding/laravel1.7#64-%E7%94%A8%E6%88%B7%E6%95%B0%E6%8D%AE%E9%AA%8C%E8%AF%81)
    - 1.表单数据验证
  - [6.5 错误消息](https://github.com/andy-love-coding/laravel1.7#65-%E9%94%99%E8%AF%AF%E6%B6%88%E6%81%AF)
    - 1.错误消息局部视图 (_errors.blade.php)
    - 3.添加语言包 laravel-lang:~3.0
  - [6.6 注册成功](https://github.com/andy-love-coding/laravel1.7#66-%E6%B3%A8%E5%86%8C%E6%88%90%E5%8A%9F)
    - 2.全局销售提示视图 (_messages.blade.php)
  - [6.7 在 Heroku 上使用 PostgreSQL](https://github.com/andy-love-coding/laravel1.7#67-%E5%9C%A8-heroku-%E4%B8%8A%E4%BD%BF%E7%94%A8-postgresql)
    - 1.使用多个数据库的配置
    - 3.自定义辅助函数
- [7.会话管理](https://github.com/andy-love-coding/laravel1.7#7-%E4%BC%9A%E8%AF%9D%E7%AE%A1%E7%90%86)
  - [7.2 会话](https://github.com/andy-love-coding/laravel1.7#72-%E4%BC%9A%E8%AF%9D)
  - [7.3 用户登录](https://github.com/andy-love-coding/laravel1.7#73-%E7%94%A8%E6%88%B7%E7%99%BB%E5%BD%95)
    - 1.伪造 DELETE 请求
    - 2.集成 Bootstrap 的 JavaScript 库
  - [7.4 退出](https://github.com/andy-love-coding/laravel1.7#74-%E9%80%80%E5%87%BA)
  - [7.5 记住我](https://github.com/andy-love-coding/laravel1.7#75-%E8%AE%B0%E4%BD%8F%E6%88%91)
- [8.用户 CRUD](https://github.com/andy-love-coding/laravel1.7#8-%E7%94%A8%E6%88%B7-crud)
  - [8.2 更新用户](https://github.com/andy-love-coding/laravel1.7#82-%E6%9B%B4%E6%96%B0%E7%94%A8%E6%88%B7)
  - [8.3 权限系统](https://github.com/andy-love-coding/laravel1.7#83-%E6%9D%83%E9%99%90%E7%B3%BB%E7%BB%9F)
    - 授权策略
    - 必须登录 必须为游客
    - 友好转向 intend()
  - [8.4 用户列表](https://github.com/andy-love-coding/laravel1.7#84-%E7%94%A8%E6%88%B7%E5%88%97%E8%A1%A8)
    - 分页
    - 填充假数据
  - [8.5 删除用户](https://github.com/andy-love-coding/laravel1.7#85-%E5%88%A0%E9%99%A4%E7%94%A8%E6%88%B7)
    - 1.用户迁移文件添加字段
- [9 邮件发送](https://github.com/andy-love-coding/laravel1.7#9-%E9%82%AE%E4%BB%B6%E5%8F%91%E9%80%81)
  - [9.2 账户激活](https://github.com/andy-love-coding/laravel1.7#92-%E8%B4%A6%E6%88%B7%E6%BF%80%E6%B4%BB)
    - 2.3.添加字段 boot()中的 creating 监听事件
    - 4.发送邮件
  - [9.3 密码重置](https://github.com/andy-love-coding/laravel1.7#93-%E5%AF%86%E7%A0%81%E9%87%8D%E7%BD%AE)
  - [9.4 生产环境中发送邮件](https://github.com/andy-love-coding/laravel1.7#94-%E7%94%9F%E4%BA%A7%E7%8E%AF%E5%A2%83%E4%B8%AD%E5%8F%91%E9%80%81%E9%82%AE%E4%BB%B6)
- [10 微博 CRUD](https://github.com/andy-love-coding/laravel1.7#10-%E5%BE%AE%E5%8D%9A-crud)
  - [10.2 微博模型](https://github.com/andy-love-coding/laravel1.7#102-%E5%BE%AE%E5%8D%9A%E6%A8%A1%E5%9E%8B)
    - 3.编写迁移文件(加索引)
    - 6.关联「微博」和「用户」（一对多）
  - [10.3 显示个人微博](https://github.com/andy-love-coding/laravel1.7#103-%E6%98%BE%E7%A4%BA%E4%B8%AA%E4%BA%BA%E5%BE%AE%E5%8D%9A)
    - 4.造微博假数据 (4.4 服务容器)
  - [10.4 发布微博](https://github.com/andy-love-coding/laravel1.7#104-%E5%8F%91%E5%B8%83%E5%BE%AE%E5%8D%9A)
  - [10.5 首页微博列表](https://github.com/andy-love-coding/laravel1.7#105-%E9%A6%96%E9%A1%B5%E5%BE%AE%E5%8D%9A%E5%88%97%E8%A1%A8)
  - [10.6 删除微博](https://github.com/andy-love-coding/laravel1.7#106-%E5%88%A0%E9%99%A4%E5%BE%AE%E5%8D%9A)
- [11 粉丝关系](https://github.com/andy-love-coding/laravel1.7#11-%E7%B2%89%E4%B8%9D%E5%85%B3%E7%B3%BB)
  - [11.2 粉丝数据表](https://github.com/andy-love-coding/laravel1.7#112-%E7%B2%89%E4%B8%9D%E6%95%B0%E6%8D%AE%E8%A1%A8)
    - 关联博主和粉丝 (多对多)
  - [11.3 社交信息统计](https://github.com/andy-love-coding/laravel1.7#113-%E7%A4%BE%E4%BA%A4%E4%BF%A1%E6%81%AF%E7%BB%9F%E8%AE%A1)
  - [11.4 粉丝页面](https://github.com/andy-love-coding/laravel1.7#114-%E7%B2%89%E4%B8%9D%E9%A1%B5%E9%9D%A2)
  - [11.5 关注按钮](https://github.com/andy-love-coding/laravel1.7#115-%E5%85%B3%E6%B3%A8%E6%8C%89%E9%92%AE)
  - [11.6 动态流（显示所有关注用户的微博动态）](https://github.com/andy-love-coding/laravel1.7#116-%E5%8A%A8%E6%80%81%E6%B5%81%E6%98%BE%E7%A4%BA%E6%89%80%E6%9C%89%E5%85%B3%E6%B3%A8%E7%94%A8%E6%88%B7%E7%9A%84%E5%BE%AE%E5%8D%9A%E5%8A%A8%E6%80%81)
## 3 [构建页面](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
### 3.2 [创建应用](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.做好准备
  ```
  > cd ~/Homestead && vagrant up
  > vagrant ssh
  ```
- 2.创建应用 
  ```
  $ cd ~/Code
  $ composer create-project laravel/laravel laravel1.7 --prefer-dist "6.*"
  ```
- 3.修改 hosts  
  Mac 下打开 Hosts 文件：
  ```
  subl /etc/hosts
  ```
  在 hosts 文件最后面新增下面一行以完成设置
  ```
  192.168.10.10   laravel1.7.test
  ```
- 4.新增站点  
  打开 Homestead.yaml 文件
  ```
  subl ~/Homestead/Homestead.yaml
  ```
  ```
  ---
  ip: "192.168.10.10"
  memory: 2048
  cpus: 1
  provider: virtualbox

  authorize: ~/.ssh/id_rsa.pub

  keys:
      - ~/.ssh/id_rsa
      - ~/.ssh/id_rsa.pub

  folders:
      - map: ~/Code
        to: /home/vagrant/Code

  sites:
      - map: note.test
        to: /home/vagrant/Code/note/public
      - map: laravel1.7.test
        to: /home/vagrant/Code/laravel1.7/public
      - map: laravel2.2.test
        to: /home/vagrant/Code/laravel3.0/public

  databases:
      - note
      - laravel1.7
      - laravel2.2
  ```
- 5.重启虚拟器
  ```
  > cd ~/Homestead && vagrant provision && vagrant reload
  ```
- 6.修改 `.env` 文件
  ```
  APP_NAME=Weibo
  APP_ENV=local
  APP_KEY=base64:dIAK2B7exLbY2S54RFQdI3c6vg9/qIWWjYy5M4ESa4A=
  APP_DEBUG=true
  APP_URL=http://laravel1.7.test

  DB_CONNECTION=mysql
  DB_HOST=127.0.0.1
  DB_PORT=3306
  DB_DATABASE=laravel1.7
  DB_USERNAME=homestead
  DB_PASSWORD=secret
  ```
- 7.统一代码风格
  .editorconfig
  ```
  root = true

  [*]
  charset = utf-8
  end_of_line = lf
  insert_final_newline = true
  indent_style = space
  indent_size = 4
  trim_trailing_whitespace = true

  [*.md]
  trim_trailing_whitespace = false

  [*.yml]
  indent_size = 2

  [*.{js,html,blade.php,css,scss}]
  indent_style = space
  indent_size = 2
  ```
- 8.Git代码版本控制
  ```
  $ cd ~/Code/laravel1.7
  $ git init
  $ git add -A
  $ git commit -m "3.2 创建应用 统一代码风格 Initial commit"

  $ git remote add origin git@github.com:andy-love-coding/laravel1.7.git
  $ git push -u origin master
  ```
### 3.3 [静态页面](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.新建分支
  ```
  $ git checkout master
  $ git checkout -b static-pages
  ```
  合并分支示例：
  ```
  $ git merge fake-branch
  ```
  删除分支示例：
  ```
  $ git branch -d fake-branch
  ```
- 2.移除无用视图
  ```
  rm resources/views/welcome.blade.php
  ```
- 3.配置路由 routes/web.php
  ```
  <?php

  Route::get('/', 'StaticPagesController@home');
  Route::get('/help', 'StaticPagesController@help');
  Route::get('/about', 'StaticPagesController@about');
  ```
- 4.生成静态页面控制器
  ```
  $ php artisan make:controller StaticPagesController
  ```
  app/Http/Controllers/StaticPagesController.php
  ```
  public function home()
  {
      return view('static_pages/home');
  }

  public function help()
  {
      return view('static_pages/help');
  }

  public function about()
  {
      return view('static_pages/about');
  }
  ```
- 5.使用通用视图 resources/views/layouts/default.blade.php
  ```
  <!DOCTYPE html>
  <html>
    <head>
      <title>@yield('title', 'Weibo App') - Laravel 新手入门教程</title>
    </head>
    <body>
      @yield('content')
    </body>
  </html>
  ```
- 6.添加静态页面视图  
  resources/views/static_pages/home.blade.php
  ```
  @extends('layouts.default')
  @section('content')
    <h1>主页</h1>
  @stop
  ```
  resources/views/static_pages/help.blade.php
  ```
  @extends('layouts.default')
  @section('title', '帮助')

  @section('content')
    <h1>帮助页</h1>
  @stop
  ```
  resources/views/static_pages/about.blade.php
  ```
  @extends('layouts.default')
  @section('title', '关于')

  @section('content')
    <h1>关于页</h1>
  @stop
  ```
- 7.Git代码版本控制
  ```
  $ git add -A
  $ git commit -m "3.3 基础页面 通用视图页面"
  ```
- 8.提交代码（合并分支）
  ```
  $ git checkout master
  $ git merge static-pages
  $ git push
  ```
### 3.4 [Artisan 命令](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- Artisan 是 Laravel 提供的 CLI（命令行接口）
  | 命令                         | 说明             |
  | ---------------------------- | ---------------- |
  | php artisan key:generate     | 生成 App Key     |
  | php artisan make:controller  | 生成控制器       |
  | php artisan make:model       | 生成模型         |
  | php artisan make:policy      | 生成授权策略     |
  | php artisan make:seeder      | 生成 Seeder 文件 |
  | php artisan migrate          | 执行迁移         |
  | php artisan migrate:rollback | 回滚迁移         |
  | php artisan migrate:refresh  | 重置数据库       |
  | php artisan db:seed          | 填充数据库       |
  | php artisan tinker           | 进入 tinker 环境 |
  | php artisan route:list       | 查看路由列表     |
- 查看 Artisan 命令帮助信息
  ```
  $ php artisan help migrate    
  ```
  或者
  ```
  $ php artisan migrate --help
  ```
## 4 [优化页面](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
### 4.2 [样式美化](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.新建分支
  ```
  $ git checkout master
  $ git checkout -b filling-layout-style
  ```
- 2.设置前端扩展包镜像
  ```
  $ npm config set registry=https://registry.npm.taobao.org
  $ yarn config set registry 'https://registry.npm.taobao.org'
  ```
- 3.安装 Bootstrap
  - 3.1 安装 laravel/ui
    ```
    $ composer require laravel/ui:^1.0 --dev
    ```
  - 3.2 引入 Bootstrap
    ```
    $ php artisan ui bootstrap
    ```
  - 3.3 修复漏洞：Bump lodash from 4.17.15 to 4.17.19  
    package.json
    ```
    "devDependencies": {
        "axios": "^0.19",
        "bootstrap": "^4.0.0",
        "cross-env": "^7.0",
        "jquery": "^3.2",
        "laravel-mix": "^5.0.1",
        "lodash": "^4.17.19",
        "popper.js": "^1.12",
        "resolve-url-loader": "^3.1.0",
        "sass": "^1.15.2",
        "sass-loader": "^8.0.0"
    }
    ```
  - 3.4 使用 Yarn 对扩展包进行安装
    ```
    $ yarn install --no-bin-links
    ```
  - 3.5 删除 `resources/sass/app.scss` 里的所有内容，只留下面一行，导入 Bootstrap：
    ```
    // Bootstrap
    @import '~bootstrap/scss/bootstrap';
    ```
  - 3.6 将 `.scss` 文件编译为 `.css`  
    前先安装 `vue-template-compiler` (vue模板编译需要这个)。
    ```
    $ yarn add vue-template-compiler --dev --production=false --no-bin-links
    ```
    - 如果没有先安装 `vue-template-compiler` 而直是直接执行 `npm run dev` 编译命令，那么会出现如下情况
      ```
      Additional dependencies must be installed. This will only take a moment. // 依然会要求安装 vue-template-compiler
      ERROR  Failed to compile with 1 errors  // 并且会一个错误，所以为了避免这个报错，还是先安装一下 vue-template-compiler 吧
      error  in ./resources/js/app.js
      Module build failed (from ./node_modules/babel-loader/lib/index.js):
      Error: Cannot find module '/home/vagrant/Code/laravel1.7/node_modules/schema-utils/src/index.js'. Please verify that the package.json has a valid "main" entry
      ```
    再执行编译命令
    ```
    $ yarn add cross-env // 先安装一下 cross-env 否则编译时报错提示：not found
    $ npm run dev
    ```
- 4.更改页面
  - 4.1 添加顶部导航和样式文件 resources/views/layouts/default.blade.php
    ```
    <!DOCTYPE html>
    <html>
      <head>
        <title>@yield('title', 'Weibo App') - Laravel 入门教程</title>
        <link rel="stylesheet" href="/css/app.css">
      </head>
      <body>
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
          <div class="container">
            <a class="navbar-brand" href="/">Weibo App</a>
            <ul class="navbar-nav justify-content-end">
              <li class="nav-item"><a class="nav-link" href="/help">帮助</a></li>
              <li class="nav-item" ><a class="nav-link" href="#">登录</a></li>
            </ul>
          </div>
        </nav>
        <div class="container">
          @yield('content')
        </div>
      </body>
    </html>
    ```
  - 4.2 修改主页 resources/views/static_pages/home.blade.php
    ```
    @extends('layouts.default')
    @section('content')
      <div class="jumbotron">
        <h1>Hello Laravel</h1>
        <p class="lead">
          你现在所看到的是 <a href="https://learnku.com/courses/laravel-essential-training">Laravel 入门教程</a> 的示例项目主页。
        </p>
        <p>
          一切，将从这里开始。
        </p>
        <p>
          <a class="btn btn-lg btn-success" href="#" role="button">现在注册</a>
        </p>
      </div>
    @stop
    ```
- 5.调整样式 resources/sass/app.scss
  ```
  // Bootstrap
  @import '~bootstrap/scss/bootstrap';

  body {
      font-size: 14px;
      font-weight: normal;
  }

  nav.navbar.navbar-expand-lg {
      margin-bottom: 20px;
  }
  ```
  编译样式
  ···
  $ npm run dev
  ···
- 6.Git版本控制
  ```
  $ git add -A
  $ git commit -m "4.2 初始化样式 集成 Bootstrap"
  ```
### 4.3 [前端工作流](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- [Laravel 前端工作流](https://learnku.com/courses/laravel-essential-training/6.x/laravel-front-end-workflow/5454)
  - SASS 语法基础
  - NPM, Yarn, Laravel Mix
### 4.4 [浏览器缓存问题](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.问题描述
  - 现代化的浏览器，会对静态文件进行缓存，静态文件在本课程的范畴内，指的是 .css 、.js 后缀的文件。开发时，你明明修改了样式，但是刷新浏览器却看不见变化，然后你就来回不断地修改你的样式文件，做各种测试，浏览器页面仍然一成不变。
- 2.解决方案  
  - 1.在 `webpack.mix.js` 中加 `.version()`
    ```
    const mix = require('laravel-mix');

    mix.js('resources/js/app.js', 'public/js')
      .sass('resources/sass/app.scss', 'public/css').version();
    ```
  - 2.用 `mix()函数来加载` resources/views/layouts/default.blade.php
    ```
    <link rel="stylesheet" href="{{ mix('css/app.css') }}">
    ```
- 3.Git版本控制
  ```
  $ git add -A
  $ git commit -m "4.4 静态文件浏览器缓存问题 .version() mix()"
  ```
### 4.5 [局部视图](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.头部和底部视图  
  resources/views/layouts/_header.blade.php
  ```
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container ">
      <a class="navbar-brand" href="/">Weibo App</a>
      <ul class="navbar-nav justify-content-end">
        <li class="nav-item"><a class="nav-link" href="/help">帮助</a></li>
        <li class="nav-item" ><a class="nav-link" href="#">登录</a></li>
      </ul>
    </div>
  </nav>
  ```
  resources/views/layouts/_footer.blade.php
  ```
  <footer class="footer">
    <img class="brand-icon" src="https://cdn.learnku.com/uploads/sites/KDiyAbV0hj1ytHpRTOlVpucbLebonxeX.png">
    <a href="https://learnku.com/laravel/courses" target=_blank>
      刻意练习，每日精进
    </a>

    <div class="float-right">
      <a href="/about" >关于</a>
    </div>
  </footer>
  ```
- 2.样式优化 resources/sass/app.scss
  ```
  /* footer */

  footer {
    margin-top: 45px;
    padding-top: 5px;
    border-top: 1px solid #eaeaea;
    color: #777;
    font-size: 13px;
    font-weight: bold;

    a {
      color: #555;
    }

    a:hover {
      color: #222;
    }

    img.brand-icon {
      width: 17px;
      height: 17px;
    }
  }
  ```
- 3.引入局部视图 resources/views/layouts/default.blade.php
  ```
  <!DOCTYPE html>
  <html>
    <head>
      <title>@yield('title', 'Weibo App') - Laravel 入门教程</title>
      <link rel="stylesheet" href="{{ mix('css/app.css') }}">
    </head>

    <body>
      @include('layouts._header')

      <div class="container">
        <div class="offset-md-1 col-md-10">
          @yield('content')
          @include('layouts._footer')
        </div>
      </div>
    </body>
  </html>
  ```
  编译样式
  ```
  $ npm run dev
  ```
- 4.Git版本控制
  ```
  $ git add -A
  $ git commit -m "4.5 切割头部和尾部子视图"
  ```
### 4.6 [布局中的链接(命名路由)](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.给路由命名 routes/web.php
  ```
  <?php

  Route::get('/', 'StaticPagesController@home')->name('home');
  Route::get('/help', 'StaticPagesController@help')->name('help');
  Route::get('/about', 'StaticPagesController@about')->name('about');
  ```
- 2.使用命名路由  
  - resources/views/layouts/_header.blade.php
    ```
    <a class="navbar-brand" href="{{ route('home') }}">Weibo App</a>
    <ul class="navbar-nav justify-content-end">
      <li class="nav-item"><a class="nav-link" href="{{ route('help') }}">帮助</a></li>
      <li class="nav-item" ><a class="nav-link" href="#">登录</a></li>
    </ul>
    ```
  - resources/views/layouts/_footer.blade.php
    ```
    <a href="{{ route('about') }}" >关于</a>
    ```
- 3.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "4.6 命名路由"
  ```
### 4.7 [用户注册页面](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.注册路由 routes/web.php
  ```
  Route::get('signup', 'UsersController@create')->name('signup');
  ```
- 2.生成用户控制器
  ```
  $ php artisan make:controller UsersController
  ```
  app/Http/Controllers/UsersController.php
  ```
  public function create()
  {
      return view('users.create');
  }
  ```
- 3.注册页面视图 resources/views/users/create.blade.php
  ```
  @extends('layouts.default')
  @section('title', '注册')

  @section('content')
  <h1>注册</h1>
  @stop
  ```
  给注册页面提供入口 resources/views/static_pages/home.blade.php
  ```
  <a class="btn btn-lg btn-success" href="{{ route('signup') }}" role="button">现在注册</a>
  ```
- 4.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "4.7 用户注册页面"
  ```
- 5.提交代码 (合并分支)
  ```
  $ git checkout master
  $ git merge filling-layout-style
  $ git push
  ```
## 5 [用户模型](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
### 5.1 [章节说明](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.准备好舞台
  ```
  $ git checkout master
  $ git checkout -b modeling-users
  ```
### 5.2 [数据库迁移](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.[数据库迁移](https://learnku.com/courses/laravel-essential-training/6.x/database-migration/5461)
  - [可用的字段类型](https://learnku.com/docs/laravel/6.x/migrations/5173#b419dd)
### 5.3 [查看数据库表](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.[数据库工具 SequelPro](https://learnku.com/courses/laravel-essential-training/6.x/check-the-database-table/5462#679a96)
- 2.执行迁移（生成表）
  ```
  $ php artisan migrate
  ```
### 5.4 [模型文件](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.使用 `App\Models` 命名空间
  - 1.1 新建文件夹，并移动 `User.php` 文件
    ```
    $ mkdir app/Models
    $ mv app/User.php app/Models/User.php
    ```
  - 1.2 修改 User.php 文件，更改 namespace  
    app/Models/User.php
    ```
    namespace App\Models;
    ```
  - 1.3 编辑器全局搜索 App\User 替换为 App\Models\User （共3个文件4处替换）
  - 1.4 因为上面的文件改动较大，因此我们需要进行一次 Git 提交，该改动的代码进行保存。
    ```
    $ git add -A
    $ git commit -m "5.4 Move user model to models folder"
    ```
- 2.操作 Article 模型(测试)
  - 2.1 生成模型
    ```
    $ php artisan make:model Article
    ```
  - 2.2 指定命名空间
    ```
    $ rm app/Article.php
    $ php artisan make:model Models/Article
    ```
  - 2.3 同时创建迁移文件
    ```
    $ rm app/Models/Article.php
    $ php artisan make:model Models/Article -m
    ```
  - 收拾舞台 (清除修改)
    ```
    // 当要撤销新增、修改等超时时，先添加文件到暂存区，然后强制检出，就相当于上都没做  
    $ git add -A                  // 添加所有 (工作区 → 暂存区)
    $ git checkout -f             // 放弃本地修改，强制检出代码（将修改内容从 暂存区 → 工作区）
    ```
- 3.Eloquent 表命名约定  
  - 模型**默认**情况下会使用类的「下划线命名法」与「复数形式名称」来作为数据表的名称
    - Article 数据模型类对应 articles 表；
    - User 数据模型类对应 users 表；
    - BlogPost 数据模型类对应 blog_posts 表
  - 如果你需要**指定**自己的数据表，则可以通过 table 属性来定义
    ```
    protected $table = 'my_articles';
    ```
### 5.5 [创建用户对象(Tinker)](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.进入 Tinker 环境
  ```
  $ php artisan tinker
  ```
- 2 创建一个用户对象
  ```
  >>> App\Models\User::create(['name'=> 'Summer', 'email'=>'summer@example.com','password'=>bcrypt('password')])
  ```
### 5.6 [查找用户对象(测试)](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.引用 `App\Models\User` Eloquent 模型类
  ```
  >>> use App\Models\User
  ```
- 2.查找一个 id 为 1 的用户
  ```
  >>> User::find(1)
  ```
  当 find 方法的 id 不存在时，Tinker 将会返回 null
  ```
  >>> User::find(5)
  => null
  ```
  在查询用户不存在时触发报错的话，可使用 findOrFail
  ```
  >>> User::findOrFail(5)
  Illuminate\Database\Eloquent\ModelNotFoundException with message 'No query results for model [App\Models\User] 5'
  ```
- 3.查找用户表中的首个用户
  ```
  >>> User::first()
  ```
- 4.取出所有的用户数据
  ```
  >>> User::all()
  ```
### 5.7 [更新用户对象(测试)](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.更新用户对象
  ```
  >>> $user = User::first()
  ```
  - 1.1 通过 save 方法更新
    ```
    >>> $user->name = 'Monkey'
    >>> User::first() // 查看：还未更新
    >>> $user->save() // 保存更新
    >>> User::first() // 查看：已经更新
    ```
  - 2.通过 update 方法更新
    ```
    >>> $user->update(['name'=>'Summer'])
    >>> User::first() // 查看：已经更新
    ```
### 5.8 [小结](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.将代码切回到主分支中进行合并，并提交
  ```
  $ git checkout master
  $ git merge modeling-users
  $ git push
  ```
## 6 [用户注册](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
### 6.2 [显示用户信息](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 0.新建一个分支
  ```
  $ git checkout master
  $ git checkout -b sign-up
  ```
- 1.路由 routes/web.php
  ```
  Route::resource('users', 'UsersController');
  ````
  以上代码等同于
  ```
  Route::get('/users', 'UsersController@index')->name('users.index');
  Route::get('/users/create', 'UsersController@create')->name('users.create');
  Route::get('/users/{user}', 'UsersController@show')->name('users.show');
  Route::post('/users', 'UsersController@store')->name('users.store');
  Route::get('/users/{user}/edit', 'UsersController@edit')->name('users.edit');
  Route::patch('/users/{user}', 'UsersController@update')->name('users.update');
  Route::delete('/users/{user}', 'UsersController@destroy')->name('users.destroy');
  ```
  | HTTP 请求 | URL                | 动作                    | 作用                   |
  | --------- | ------------------ | ----------------------- | ---------------------- |
  | GET       | /users             | UsersController@index   | 显示所有用户列表的页面 |
  | GET       | /users/{user}      | UsersController@show    | 显示用户个人信息的页面 |
  | GET       | /users/create      | UsersController@create  | 创建用户的页面         |
  | POST      | /users             | UsersController@store   | 创建用户               |
  | GET       | /users/{user}/edit | UsersController@edit    | 编辑用户个人资料的页面 |
  | PATCH     | /users/{user}      | UsersController@update  | 更新用户               |
  | DELETE    | /users/{user}      | UsersController@destroy | 删除用户               |
- 2.控制器 app/Http/Controllers/UsersController.php
  ```
  use App\Models\User;
  ...
    public function show(User $user)
    {
        return view('users.show', compact('user'));
    }
  ```
  - show() 方法传参时声明了类型 —— Eloquent 模型 User，对应的变量名 $user 会匹配路由片段中的 {user}，这样，Laravel 会自动注入与请求 URI 中传入的 ID 对应的用户模型实例
  - 此功能称为 [『隐性路由模型绑定』](https://learnku.com/docs/laravel/6.x/routing/5135#cbc0a0)，是『约定优于配置』设计范式的体现
- 3.用户视图 resources/views/users/show.blade.php
  ```
  @extends('layouts.default')
  @section('title', $user->name)

  @section('content')
  <div class="row">
    <div class="offset-md-2 col-md-8">
      <div class="col-md-12">
        <div class="offset-md-2 col-md-8">
          <section class="user_info">
            @include('shared._user_info', ['user' => $user])
          </section>
        </div>
      </div>
    </div>
  </div>
  @stop
  ```
- 4.用户局部视图 resources/views/shared/_user_info.blade.php
    ```
    <a href="{{ route('users.show', $user->id) }}">
      <img src="{{ $user->gravatar('140') }}" alt="{{ $user->name }}" class="gravatar"/>
    </a>
    <h1>{{ $user->name }}</h1>
    ```
- 5.Gravatar 头像和左边栏  
  - 4.1 模型中 app/Models/User.php
    ```
    public function gravatar($size = '100')
    {
        $hash = md5(strtolower(trim($this->attributes['email'])));
        return "http://www.gravatar.com/avatar/$hash?s=$size";
    }
    ```
- 6.样式优化 resources/sass/app.scss
  ```
  /* User gravatar */

  section.user_info {
    padding-bottom: 10px;
    margin-top: 20px;
    text-align: center;
    .gravatar {
      float: none;
      max-width: 70px;
    }
    h1 {
      font-size: 1.4em;
      letter-spacing: -1px;
      margin-bottom: 3px;
      margin-top: 15px;
    }
  }

  .gravatar {
    float: left;
    max-width: 50px;
    border-radius: 50%;
  }
  ```
  - 编译样式
    ```
    $ npm run dev
    ```
- 7.Git版本控制
  ```
  $ git add -A
  $ git commit -m "6.2 用户显示页面 用户局部视图include"
  ```
### 6.3 [注册表单](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.表单构建 resources/views/users/create.blade.php
  ```
  @extends('layouts.default')
  @section('title', '注册')

  @section('content')
  <div class="offset-md-2 col-md-8">
    <div class="card ">
      <div class="card-header">
        <h5>注册</h5>
      </div>
      <div class="card-body">
        <form method="POST" action="{{ route('users.store') }}">
            <div class="form-group">
              <label for="name">名称：</label>
              <input type="text" name="name" class="form-control" value="{{ old('name') }}">
            </div>

            <div class="form-group">
              <label for="email">邮箱：</label>
              <input type="text" name="email" class="form-control" value="{{ old('email') }}">
            </div>

            <div class="form-group">
              <label for="password">密码：</label>
              <input type="password" name="password" class="form-control" value="{{ old('password') }}">
            </div>

            <div class="form-group">
              <label for="password_confirmation">确认密码：</label>
              <input type="password" name="password_confirmation" class="form-control" value="{{ old('password_confirmation') }}">
            </div>

            <button type="submit" class="btn btn-primary">注册</button>
        </form>
      </div>
    </div>
  </div>
  @stop
  ```
  - 全局辅助函数 `old()` 来帮助我们在 Blade 模板中显示旧输入数据。这样当我们信息填写错误，页面进行重定向访问时，输入框将自动填写上最后一次输入过的数据。
- 2.Git版本控制
  ```
  $ git add -A
  $ git commit -m "6.3 用户注册表单"
  ```
### 6.4 [用户数据验证](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.用户数据验证 app/Http/Controllers/UsersController.php
  ```
  public function store(Request $request)
  {
      $this->validate($request, [
          'name' => 'required|unique:users|max:50',
          'email' => 'required|email|unique:users|max:255',
          'password' => 'required|confirmed|min:6'
      ], [
          'name.required' => '名字都不写，想上天吗？',
      ]);
      return;
  }
  ```
  - [表单验证请点击](https://learnku.com/docs/laravel/6.x/validation/5144)
- 2.表单提交时，增加 CSFR 验证（跨站请求伪造) resources/views/users/create.blade.php
  ```
  <form method="POST" action="{{ route('users.store') }}">
    {{ csrf_field() }}
  ```
  - 这时候如果你再次填写注册表单并进行提交，你会发现页面没什么反应，这是因为：
    - 在表单信息验证失败时，返回原页面，但在页面上没有给出错误提示；
    - 在表单信息验证通过后，页面没有重定向跳转到其它页面，并给出注册成功的提示；
- 3.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "6.4 增加 CSRF 验证"
  ```
### 6.5 [错误消息](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.错误消息局部视图 resources/views/shared/_errors.blade.php
  ```
  @if (count($errors) > 0)
    <div class="alert alert-danger">
        <ul>
            @foreach($errors->all() as $error)
            <li>{{ $error }}</li>
            @endforeach
        </ul>
    </div>
  @endif
  ```
  - Laravel 默认会将所有的验证错误信息进行闪存。当检测到错误存在时，Laravel 会自动将这些错误消息绑定到视图上，因此我们可以在所有的视图上使用 errors 变量来显示错误信息。
- 2.引用「错误消息局部视图」 resources/views/users/create.blade.php
  ```
  <div class="card-body">
    @include('shared._errors')
    <form method="POST" action="{{ route('users.store') }}">
  ```
- 3.添加语言包
  - 由于错误消息是英文的，我们添加语言包
    ```
    $ composer require "overtrue/laravel-lang:~3.0"
    ```
  - 安装成功后，在 config/app.php 文件中将以下这一行：
    ```
    Illuminate\Translation\TranslationServiceProvider::class,
    ```
    替换为
    ```
    Overtrue\LaravelLang\TranslationServiceProvider::class,
    ```
  - 在 config/app.php 中将项目设置为中文
    ```
    'locale' => 'zh-CN',
    ```
- 4.Git版本控制
  ```
  $ git add -A
  $ git commit -m "6.5 错误信息 添加语言包"
  ```
### 6.6 [注册成功](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.保存用户并重定向 app/Http/Controllers/UsersController.php
  ```
  public function store(Request $request)
  {
      $this->validate($request, [
          'name' => 'required|unique:users|max:50',
          'email' => 'required|email|unique:users|max:255',
          'password' => 'required|confirmed|min:6'
      ], [
            'name.required' => '名字都不写，想上天吗？',
      ]);

      $user = User::create([
          'name' => $request->name,
          'email' => $request->email,
          'password' => bcrypt($request->password),
      ]);

      session()->flash('success', '欢迎，您将在这里开启一段新的旅程~');
      return redirect()->route('users.show', [$user]);
  }
  ```
- 2.消息提示视图 resources/views/shared/_messages.blade.php
  ```
  @foreach (['danger', 'warning', 'success', 'info'] as $msg)
    @if(session()->has($msg))
      <div class="flash-message">
        <p class="alert alert-{{ $msg }}">
          {{ session()->get($msg) }}
        </p>
      </div>
    @endif
  @endforeach
  ```
- 3.引入消息提示视图 resources/views/layouts/default.blade.php
  ```
  <div class="container">
    <div class="offset-md-1 col-md-10">
      @include('shared._messages')
      @yield('content')
      @include('layouts._footer')
    </div>
  </div>
  ```
- 4.Git 版本控制，并合并提交
  ```
  $ git add -A
  $ git commit -m "6.6 完成用户注册功能 全局消息提示"
  $ git checkout master
  $ git merge sign-up
  $ git push
  ```
### 6.7 [在 Heroku 上使用 PostgreSQL](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.[使用多个数据库的配置](https://learnku.com/courses/laravel-essential-training/6.x/using-postgresql-on-heroku/5474)
- 2.设置环境变量 IS_IN_HEROKU
  - 如果环境为本地环境，则使用 MySQL 数据库，若为 Heroku 环境，则使用 PostgreSQL 数据库。我们可以通过为 Heroku 新增一个 IS_IN_HEROKU 配置项来判断应用是否运行在 Heroku 上。
    ```
    $ heroku config:set IS_IN_HEROKU=true
    ```
- 3.自定义辅助函数
  - 2.1 帮助为不同环境的数据库连接方式定义一个帮助方法(即辅助函数)，以便根据应用不同的运行环境来指定数据库配置信息，我们需要新建一个 `helpers.php` 
  - 2.2 新建帮助文件 app/helpers.php
    ```
    <?php

    function get_db_config()
    {
        if (getenv('IS_IN_HEROKU')) {
            $url = parse_url(getenv("DATABASE_URL"));

            return $db_config = [
                'connection' => 'pgsql',
                'host' => $url["host"],
                'database'  => substr($url["path"], 1),
                'username'  => $url["user"],
                'password'  => $url["pass"],
            ];
        } else {
            return $db_config = [
                'connection' => env('DB_CONNECTION', 'mysql'),
                'host' => env('DB_HOST', 'localhost'),
                'database'  => env('DB_DATABASE', 'forge'),
                'username'  => env('DB_USERNAME', 'forge'),
                'password'  => env('DB_PASSWORD', ''),
            ];
        }
    }
    ```
  - 2.3 自动加载帮助文件：在 composer.json 中的 autoload 中加入："files": ["app/helper.php"]
    ```
    "autoload": {
        "psr-4": {
            "App\\": "app/"
        },
        "classmap": [
            "database/seeds",
            "database/factories"
        ],
        "files": [
            "app/helpers.php"
        ]
    }
    ```
  - 2.4 运行以下命令进行重新加载文件即可
    ```
    $ composer dump-autoload
    ```
- 4.数据库配置 config/database.php
  ```
  <?php

  use Illuminate\Support\Str;

  $db_config = get_db_config();

  return [

      'default' => $db_config['connection'],

      'connections' => [

          'sqlite' => [
              'driver' => 'sqlite',
              'url' => env('DATABASE_URL'),
              'database' => env('DB_DATABASE', database_path('database.sqlite')),
              'prefix' => '',
              'foreign_key_constraints' => env('DB_FOREIGN_KEYS', true),
          ],

          'mysql' => [
              'driver' => 'mysql',
              'url' => env('DATABASE_URL'),
              'host' => env('DB_HOST', '127.0.0.1'),
              'port' => env('DB_PORT', '3306'),
              'database' => env('DB_DATABASE', 'forge'),
              'username' => env('DB_USERNAME', 'forge'),
              'password' => env('DB_PASSWORD', ''),
              'unix_socket' => env('DB_SOCKET', ''),
              'charset' => 'utf8mb4',
              'collation' => 'utf8mb4_unicode_ci',
              'prefix' => '',
              'prefix_indexes' => true,
              'strict' => true,
              'engine' => null,
              'options' => extension_loaded('pdo_mysql') ? array_filter([
                  PDO::MYSQL_ATTR_SSL_CA => env('MYSQL_ATTR_SSL_CA'),
              ]) : [],
          ],

          'pgsql' => [
              'driver'   => 'pgsql',
              'host'     => $db_config['host'],
              'port'     => env('DB_PORT', '5432'),
              'database' => $db_config['database'],
              'username' => $db_config['username'],
              'password' => $db_config['password'],
              'charset' => 'utf8',
              'prefix' => '',
              'prefix_indexes' => true,
              'schema' => 'public',
              'sslmode' => 'prefer',
          ],

          'sqlsrv' => [
              'driver' => 'sqlsrv',
              'url' => env('DATABASE_URL'),
              'host' => env('DB_HOST', 'localhost'),
              'port' => env('DB_PORT', '1433'),
              'database' => env('DB_DATABASE', 'forge'),
              'username' => env('DB_USERNAME', 'forge'),
              'password' => env('DB_PASSWORD', ''),
              'charset' => 'utf8',
              'prefix' => '',
              'prefix_indexes' => true,
          ],

      ],

      'migrations' => 'migrations',

      'redis' => [

          'client' => env('REDIS_CLIENT', 'phpredis'),

          'options' => [
              'cluster' => env('REDIS_CLUSTER', 'redis'),
              'prefix' => env('REDIS_PREFIX', Str::slug(env('APP_NAME', 'laravel'), '_').'_database_'),
          ],

          'default' => [
              'url' => env('REDIS_URL'),
              'host' => env('REDIS_HOST', '127.0.0.1'),
              'password' => env('REDIS_PASSWORD', null),
              'port' => env('REDIS_PORT', 6379),
              'database' => env('REDIS_DB', 0),
          ],

          'cache' => [
              'url' => env('REDIS_URL'),
              'host' => env('REDIS_HOST', '127.0.0.1'),
              'password' => env('REDIS_PASSWORD', null),
              'port' => env('REDIS_PORT', 6379),
              'database' => env('REDIS_CACHE_DB', 1),
          ],

      ],

  ];
  ```
- 4.Git 版本控制，并提交代码
  ```
  $ git add -A
  $ git commit -m "6.7 根据环境配置不同的数据库"
  $ git push
  ```
## 7 [会话管理](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
### 7.2 [会话](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.新建分支
  ```
  $ git checkout master
  $ git checkout -b login-logout
  ```
- 2.路由 routes/web.php
  ```
  Route::get('login', 'SessionsController@create')->name('login');
  Route::post('login', 'SessionsController@store')->name('login');
  Route::delete('logout', 'SessionsController@destroy')->name('logout');
  ```
- 3.会话控制器 app/Http/Controllers/SessionsController.php
  ```
  $ php artisan make:controller SessionsController
  ```
  app/Http/Controllers/SessionsController.php
  ```
  use Auth;
  ...
  public function create()
  {
      return view('sessions.create');
  }

  public function store(Request $request)
  {
      $credentials = $this->validate($request, [
          'email' => 'required|email|max:255',
          'password' => 'required'
      ]);

      if (Auth::attempt($credentials)) {
          session()->flash('success', '欢迎回来！');
          return redirect()->route('users.show', [Auth::user()]);
      } else {
          session()->flash('danger', '很抱歉，您的邮箱和密码不匹配');
          return redirect()->back()->withInput();
      }
  }
  ```
  - attempt() 方法会接收一个数组来作为第一个参数，该参数提供的值将用于寻找数据库中的用户数据；第二个参数为是否为用户开启『记住我』功能的布尔值。因此在上面的例子中，attempt 方法执行的代码逻辑如下：
    - 1.使用 email 字段的值在数据库中查找；
    - 2.如果用户被找到：
      - 1). 先将传参的 password 值进行哈希加密，然后与数据库中 password 字段中已加密的密码进行匹配；
      - 2). 如果匹配后两个值完全一致，会创建一个『会话』给通过认证的用户。会话在创建的同时，也会种下一个名为 laravel_session 的 HTTP Cookie，以此 Cookie 来记录用户登录状态，最终返回 true；
      - 3). 如果匹配后两个值不一致，则返回 false；
    - 3.如果用户未找到，则返回 false。
- 4.登录视图 resources/views/sessions/create.blade.php
  ```
  @extends('layouts.default')
  @section('title', '登录')

  @section('content')
  <div class="offset-md-2 col-md-8">
    <div class="card ">
      <div class="card-header">
        <h5>登录</h5>
      </div>
      <div class="card-body">
        @include('shared._errors')

        <form method="POST" action="{{ route('login') }}">
            {{ csrf_field() }}

            <div class="form-group">
              <label for="email">邮箱：</label>
              <input type="text" name="email" class="form-control" value="{{ old('email') }}">
            </div>

            <div class="form-group">
              <label for="password">密码：</label>
              <input type="password" name="password" class="form-control" value="{{ old('password') }}">
            </div>

            <button type="submit" class="btn btn-primary">登录</button>
        </form>

        <hr>

        <p>还没账号？<a href="{{ route('signup') }}">现在注册！</a></p>
      </div>
    </div>
  </div>
  @stop
  ```
- 5.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "7.2 创建会话"
  ```
### 7.3 [用户登录](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.修改导航视图 resources/views/layouts/_header.blade.php
  ```
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container ">
      <a class="navbar-brand" href="{{ route('home') }}">Weibo App</a>
      <ul class="navbar-nav justify-content-end">
        @if (Auth::check())
          <li class="nav-item"><a class="nav-link" href="#">用户列表</a></li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
              {{ Auth::user()->name }}
            </a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
              <a class="dropdown-item" href="{{ route('users.show', Auth::user()) }}">个人中心</a>
              <a class="dropdown-item" href="#">编辑资料</a>
              <div class="dropdown-divider"></div>
              <a class="dropdown-item" id="logout" href="#">
                <form action="{{ route('logout') }}" method="POST">
                  {{ csrf_field() }}
                  {{ method_field('DELETE') }}
                  <button class="btn btn-block btn-danger" type="submit" name="button">退出</button>
                </form>
              </a>
            </div>
          </li>
        @else
          <li class="nav-item"><a class="nav-link" href="{{ route('help') }}">帮助</a></li>
          <li class="nav-item" ><a class="nav-link" href="{{ route('login') }}">登录</a></li>
        @endif
      </ul>
    </div>
  </nav>
  ```
  - Auth::check() 方法用于判断当前用户是否已登录
  - 伪造 DELETE 请求：由于浏览器不支持发送 DELETE 请求，因此我们需要使用一个隐藏域来伪造 DELETE 请求。
    ```
    {{ method_field('DELETE') }}
    ```
    其等价于
    ```
    <input type="hidden" name="_method" value="DELETE">
    ```
- 2.集成 Bootstrap 的 JavaScript 库
  - 2.1 编译 resources/js/app.js 到 public/js/app.js
    - Laravel 6.x 默认已经在 resources/js/bootstrap.js 文件中为我们配置好了 jQuery 和 Bootstrap。
    - 在 resources/js/app.js 中加载 resources/js/bootstrap.js
      ```
      require('./bootstrap');
      ```
    - 执行编译任务，编译 resources/js/app.js 到 public/js/app.js
      ```
      $ npm run dev
      ```
  - 2.2 引用 public/js/app.js 文件  
    resources/views/layouts/default.blade.php
    ```
      <script src="{{ mix('js/app.js') }}"></script>
    </body>
    ```
  - 2.3 现在尝试再次点击导航栏下拉菜单，能发现它已经能够正常工作。
- 3.注册后自动登录 Auth::login($user);  
  app/Http/Controllers/UsersController.php
  ```
  use Auth;
  ...
  public function store(Request $request)
  {
      $this->validate($request, [
          'name' => 'required|max:50',
          'email' => 'required|email|unique:users|max:255',
          'password' => 'required|confirmed|min:6'
      ]);

      $user = User::create([
          'name' => $request->name,
          'email' => $request->email,
          'password' => bcrypt($request->password),
      ]);

      Auth::login($user);
      session()->flash('success', '欢迎，您将在这里开启一段新的旅程~');
      return redirect()->route('users.show', [$user]);
  }
  ```
- 4.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "7.3 登录成功后导航逻辑及自动登录"
  ```
### 7.4 [退出](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.退出 app/Http/Controllers/SessionsController.php
  ```
  public function destroy()
  {
      Auth::logout();
      session()->flash('success', '您已成功退出！');
      return redirect('login');
  }
  ```
- 2.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "7.4 用户退出登录"
  ```
### 7.5 [记住我](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.记住我
  - 使用了『记住我』功能，则登录状态会被延长到五年。
  - 没有使用『记住我』功能，则登录状态默认只会被记住两个小时。
- 2.修改登录视图，加上『记住我』复选框  
  resources/views/sessions/create.blade.php
  ```
  <div class="form-group">
    <div class="form-check">
      <input type="checkbox" class="form-check-input" name="remember" id="exampleCheck1">
      <label class="form-check-label" for="exampleCheck1">记住我</label>
    </div>
  </div>

  <button type="submit" class="btn btn-primary">登录</button>
  ```
- 3.修改会话控制器中的 store 方法  
  app/Http/Controllers/SessionsController.php
  ```
  public function store(Request $request)
  {
      $credentials = $this->validate($request, [
          'email' => 'required|email|max:255',
          'password' => 'required'
      ]);

      if (Auth::attempt($credentials, $request->has('remember'))) {
          session()->flash('success', '欢迎回来！');
          return redirect()->route('users.show', [Auth::user()]);
      } else {
          session()->flash('danger', '很抱歉，您的邮箱和密码不匹配');
          return redirect()->back()->withInput();
      }
  }
  ```
  - Auth::attempt() 方法可接收两个参数，第一个参数为需要进行用户身份认证的数组，第二个参数为是否为用户开启『记住我』功能的布尔值。
- 4.Git 版本控制 及合并提交
  ```
  $ git add -A
  $ git commit -m "7.5 登录时记住我"
  $ git checkout master
  $ git merge login-logout
  $ git push
  ```
## 8 [用户 CRUD](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
### 8.2 [更新用户](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.新建一个分支
  ```
  $ git checkout master
  $ git checkout -b user-crud
  ```
- 2.控制器 app/Http/Controllers/UsersController.php
  ```
  public function edit(User $user)
  {
      return view('users.edit', compact('user'));
  }

  public function update(User $user, Request $request)
  {
      $this->validate($request, [
          'name' => 'required|max:50',
          'password' => 'nullable|confirmed|min:6'
      ]);

      $data = [];
      $data['name'] = $request->name;
      if ($request->password) {
          $data['password'] = bcrypt($request->password);
      }
      $user->update($data);

      session()->flash('success', '个人资料更新成功！');

      return redirect()->route('users.show', $user);
  }
  ```
- 3.辩解用户的视图 resources/views/users/edit.blade.php
  ```
  @extends('layouts.default')
  @section('title', '更新个人资料')

  @section('content')
  <div class="offset-md-2 col-md-8">
    <div class="card ">
      <div class="card-header">
        <h5>更新个人资料</h5>
      </div>
        <div class="card-body">

          @include('shared._errors')

          <div class="gravatar_edit">
            <a href="http://gravatar.com/emails" target="_blank">
              <img src="{{ $user->gravatar('200') }}" alt="{{ $user->name }}" class="gravatar"/>
            </a>
          </div>

          <form method="POST" action="{{ route('users.update', $user->id )}}">
              {{ method_field('PATCH') }}
              {{ csrf_field() }}

              <div class="form-group">
                <label for="name">名称：</label>
                <input type="text" name="name" class="form-control" value="{{ $user->name }}">
              </div>

              <div class="form-group">
                <label for="email">邮箱：</label>
                <input type="text" name="email" class="form-control" value="{{ $user->email }}" disabled>
              </div>

              <div class="form-group">
                <label for="password">密码：</label>
                <input type="password" name="password" class="form-control" value="{{ old('password') }}">
              </div>

              <div class="form-group">
                <label for="password_confirmation">确认密码：</label>
                <input type="password" name="password_confirmation" class="form-control" value="{{ old('password_confirmation') }}">
              </div>

              <button type="submit" class="btn btn-primary">更新</button>
          </form>
      </div>
    </div>
  </div>
  @stop
  ```
- 3.视图样式优化 resources/sass/app.scss
  ```
  /* Users edit */

  .gravatar_edit {
    margin: 15px auto;
    text-align: center;
    .gravatar {
      float: none;
      max-width: 100px;
    }
  }
  ```
  编译样式文件
  ```
  $ npm run dev
  ```
- 4.给编辑页面加上入口 resources/views/layouts/_header.blade.php
  ```
  <a class="dropdown-item" href="{{ route('users.edit', Auth::user()) }}">编辑资料</a>
  ```
- 5.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "8.2 更改用户资料"
  ```
### 8.3 [权限系统](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.必须登录：app/Http/Controllers/UsersController.php
  ```
  public function __construct()
  {
      // except 黑名单排除不需要登录的，其余都需要登录
      $this->middleware('auth', [            
          'except' => ['show', 'create', 'store']
      ]);
  }
  ```
- 2.授权策略：只能自己编辑家自己 ()
  - 2.1 创建授权策略
    ```
    $ php artisan make:policy UserPolicy
    ```
    app/Policies/UserPolicy.php
    ```
    // update 方法接收两个参数，第一个参数默认为当前登录用户实例，第二个参数则为要进行授权的用户实例
    // 使用授权策略时，我们 不需要 传递当前登录用户至该方法内，因为框架会自动加载当前登录用户，即不用传递 $currentUser
    public function update(User $currentUser, User $user)
    {
        // 只有自己才能更新自己
        return $currentUser->id === $user->id;
    }
    ```
  - 2.2 注册授权策略 app/Providers/AuthServiceProvider.php
    ```
    public function boot()
    {
        $this->registerPolicies();
        // 修改策略自动发现的逻辑
        Gate::guessPolicyNamesUsing(function ($modelClass) {
            // 动态返回模型对应的策略名称，如：// 'App\Models\User' => 'App\Policies\UserPolicy',
            return 'App\Policies\\'.class_basename($modelClass).'Policy';
        });
    }
    ```
  - 2.3 使用授权策略 app/Http/Controllers/UsersController.php
    ```
    public function edit(User $user)
    {
        // authorize 方法接收两个参数，第一个为授权策略的名称，第二个为进行授权验证的数据。
        $this->authorize('update', $user);
        return view('users.edit', compact('user'));
    }

    public function update(User $user, Request $request)
    {
        $this->authorize('update', $user);
        $this->validate($request, [
            'name' => 'required|max:50',
            'password' => 'nullable|confirmed|min:6'
        ]);

        $data = [];
        $data['name'] = $request->name;
        if ($request->password) {
            $data['password'] = bcrypt($request->password);
        }
        $user->update($data);

        session()->flash('success', '个人资料更新成功！');

        return redirect()->route('users.show', $user->id);
    }
    ```
    - 测试：用 id 为 1 的用户登录，访问 id 为 2 的用户的编辑页面，系统将报 “403 unauthorized” 错误
- 3.友好转向 intended()  
  app/Http/Controllers/SessionsController.php
  ```
  public function store(Request $request)
  {
      $credentials = $this->validate($request, [
          'email' => 'required|email|max:255',
          'password' => 'required'
      ]);

      if (Auth::attempt($credentials, $request->has('remember'))) {
          // 登录成功
          session()->flash('success', '欢迎回来！');
          // 登录后友好转向 intended() 
          // 重定向到上一次请求尝试访问的页面上，并接收一个默认跳转地址参数，当上一次请求记录为空时，跳转到默认地址上。
          $fallback = route('users.show', Auth::user());
          return redirect()->intended($fallback);
      } else {
          // 登录失败
          session()->flash('danger', '很抱歉，您的邮箱和密码不匹配');
          return redirect()->back()->withInput();
      }
  }
  ```
  - redirect() 实例提供了一个 intended() 方法，该方法可将页面重定向到上一次请求尝试访问的页面上，并接收一个默认跳转地址参数，当上一次请求记录为空时，跳转到默认地址上。
- 4.必须为游客：「登录」、「注册」必须为访客
  - 4.1「登录」时必须是游客 app/Http/Controllers/SessionsController.php
    ```
    public function __construct()
    {
        // 「登录」时必须是游客
        $this->middleware('guest', [
            'only' => ['create']
        ]);
    }
    ```
  - 4.2 「注册」时必须是游客 app/Http/Controllers/UsersController.php
    ```
    public function __construct()
    {
        // except 黑名单排除不需要登录的，其余都需要登录
        $this->middleware('auth', [
            'except' => ['show', 'create', 'store']
        ]);

        // only 白名单设定注册必须为 游客模式（非登录）
        $this->middleware('guest', [
            'only' => ['create']
        ]);
    }
    ```
  - 4.3 guest 验证未通过的默认跳转
    - guest 验证未通过，默认跳转到页面 /home ，因我们并没有此页面，所以会报错 404 找不到页面
    - 增加提示 app/Http/Middleware/RedirectIfAuthenticated.php
      ```
      public function handle($request, Closure $next, $guard = null)
      {
          if (Auth::guard($guard)->check()) {
              session()->flash('info', '您已登录，无需再次操作。');
              return redirect(RouteServiceProvider::HOME);
          }

          return $next($request);
      }
      ```
    - 修改默认跳转 默认跳转：app/Providers/RouteServiceProvider.php
      ```
      // public const HOME = '/home';
      public const HOME = '/'; // 默认跳转由 '/home' 改为 '/'
      ```
- 5.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "8.3 权限系统 授权策略 中间件auth guest"
  ```
### 8.4 [用户列表](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.控制器(分页) app/Http/Controllers/UsersController.php
  ```
  public function __construct()
  {
      // except 黑名单排除不需要登录的，其余都需要登录
      $this->middleware('auth', [
          'except' => ['show', 'create', 'store', 'index']
      ]);
      ...
  }

  public function index()
  {
      $users = User::paginate(10); // 分页，每页10条
      return view('users.index', compact('users'));
  } 
  ```
  - paginate() 分页数据
- 2.视图(分页) resources/views/users/index.blade.php
  ```
  @extends('layouts.default')
  @section('title', '所有用户')

  @section('content')
  <div class="offset-md-2 col-md-8">
    <h2 class="mb-4 text-center">所有用户</h2>
    <div class="list-group list-group-flush">
      @foreach ($users as $user)
        @include('users._user')
      @endforeach
    </div>

    <div class="mt-3">
      {!! $users->render() !!}
    </div>
  </div>
  @stop
  ```
  - 局部视图 resources/views/users/_user.blade.php
    ```
    <div class="list-group-item">
      <img class="mr-3" src="{{ $user->gravatar() }}" alt="{{ $user->name }}" width=32>
      <a href="{{ route('users.show', $user) }}">
        {{ $user->name }}
      </a>
    </div>
    ```
  - 分页 渲染分页视图的代码必须使用 {!! !!} 语法，而不是 {{　}}，这样生成 HTML 链接才不会被转义.
    ```
    控制器中：
      $users = User::paginate(10); // 分页，每页10条
      return view('users.index', compact('users'));
    视图中：
      <div class="mt-3">
        {!! $users->render() !!}
      </div>
    ```
- 3.用户列表入口 resources/views/layouts/_header.blade.php
  ```
  <li class="nav-item"><a class="nav-link" href="{{ route('users.index') }}">用户列表</a></li>
  ```
- 4.填充用户假数据
  - 4.1 模型工厂 (模型工厂造模型) database/factories/UserFactory.php
    ```
    <?php

    use App\Models\User;
    use Illuminate\Support\Str;
    use Faker\Generator as Faker;

    $factory->define(User::class, function (Faker $faker) {
        $date_time = $faker->date . ' ' . $faker->time;
        return [
            'name' => $faker->name,
            'email' => $faker->unique()->safeEmail,
            'email_verified_at' => now(),
            'password' => '$2y$10$TKh8H1.PfQx37YgCzwiKb.KjNyWgaHb9cbcoQgdIVFlYg7B77UdFm', // secret
            'remember_token' => Str::random(10),
            'created_at' => $date_time,
            'updated_at' => $date_time,
        ];
    });
    ```
  - 4.2 数据填充
    - 生成填充文件
      ```
      $ php artisan make:seeder UsersTableSeeder
      ```
    - 编写填充文件 database/seeds/UsersTableSeeder.php
      ```
      <?php

      use Illuminate\Database\Seeder;
      use App\Models\User;

      class UsersTableSeeder extends Seeder
      {
          public function run()
          {
              $users = factory(User::class)->times(50)->make();
              User::insert($users->makeVisible(['password', 'remember_token'])->toArray());

              $user = User::find(1);
              $user->name = 'Summer';
              $user->email = 'summer@example.com';
              $user->save();
          }
      }
      ```
      - makeVisible() 方法临时显示 User 模型里指定的隐藏属性 $hidden，接着我们使用了 insert 方法来将生成假用户列表数据批量插入到数据库中
    - 调用填充文件 database/seeds/DatabaseSeeder.php
      ```
      public function run()
      {
          $this->call(UsersTableSeeder::class);
      }
      ```
  - 4.3 重置数据库
    ```
    $ php artisan migrate:refresh
    $ php artisan db:seed
    ```
    以上命令等价于
    ```
    $ php artisan migrate:refresh --seed
    ```
    - 如果如果我们要单独指定执行 UserTableSeeder 数据库填充文件，则可以这么做：
      ```
      $ php artisan migrate:refresh
      $ php artisan db:seed --class=UsersTableSeeder
      ```
- 5.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "8.4 查看用户列表 模型工厂 迁移文件 数据填充 分页"
  ```
### 8.5 [删除用户](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.加管理员字段
  - 1.1 生成迁移文件来加管理员字段
    ```
    $ php artisan make:migration add_is_admin_to_users_table --table=users
    ```
    database/migrations/[timestamp]_add_is_admin_to_users_table.php
    ```
    public function up()
    {
        Schema::table('users', function (Blueprint $table) {
            $table->boolean('is_admin')->default(false);
        });
    }

    public function down()
    {
        Schema::table('users', function (Blueprint $table) {
            $table->dropColumn('is_admin');
        });
    }
    ```
    执行迁移
    ```
    $ php artisan migrate
    ```
  - 1.2 更改填充文件，将第一个用户设置为管理员
    database/seeds/UsersTableSeeder.php
    ```
    public function run()
    {
        $users = factory(User::class)->times(50)->make();
        User::insert($users->makeVisible(['password', 'remember_token'])->toArray());

        $user = User::find(1);
        $user->name = 'Summer';
        $user->email = 'summer@example.com';
        $user->is_admin = true;
        $user->save();
    }
    ```
    执行数据库重置和填充
    ```
    $ php artisan migrate:refresh --seed
    ```
- 2.destroy 动作
  - 2.1 删除策略 app/Policies/UserPolicy.php
    ```
    public function destroy(User $currentUser, User $user)
    {
        // 管理员才能删除 且 自己不能删除自己
        return $currentUser->is_admin && $currentUser->id !== $user->id;
    }
    ```
  - 2.2 模板中用 @can 和 @endcan调用「删除策略」：resources/views/users/_user.blade.php
    ```
    <div class="list-group-item">
      <img class="mr-3" src="{{ $user->gravatar() }}" alt="{{ $user->name }}" width=32>
      <a href="{{ route('users.show', $user) }}">
        {{ $user->name }}
      </a>
      @can('destroy', $user)
        <form action="{{ route('users.destroy', $user->id) }}" method="post" class="float-right" onsubmit="return confirm('确定要删除该用户吗？')">
          {{ csrf_field() }}
          {{ method_field('DELETE') }}
          <button type="submit" class="btn btn-sm btn-danger delete-btn">删除</button>
        </form>
      @endcan
    </div>
    ```
  - 2.3 控制器中用 authorize() 调用「删除策略」，并执行删除动作：app/Http/Controllers/UsersController.php
    ```
    public function destroy(User $user)
    {
        $this->authorize('destroy', $user);
        $user->delete();
        session()->flash('success', '成功删除用户！');
        return back();
    }
    ```
- 3.Git 版本控制 及合并提交
  ```
  $ git add -A
  $ git commit -m "8.5 管理员可删除用户"
  $ git checkout master
  $ git merge user-crud
  $ git push
  ```
## 9 [邮件发送](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
### 9.2 [账户激活](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.新建分支
  ```
  $ git checkout master
  $ git checkout -b account-activation-password-resets
  ```
- 2.添加字段
  - 2.1 新建迁移文件来添加字段
    ```
    $ php artisan make:migration add_activation_to_users_table --table=users
    ```
  - 2.2 编辑迁移文件 database/migrations/[timestamp]_add_activation_to_users_table.php
    ```
    public function up()
    {
        Schema::table('users', function (Blueprint $table) {
            $table->string('activation_token')->nullable();
            $table->boolean('activated')->default(false);
        });
    }

    public function down()
    {
        Schema::table('users', function (Blueprint $table) {
            $table->dropColumn('activation_token');
            $table->dropColumn('activated');
        });
    }
    ```
  - 2.3 执行迁移
    ```
    $ php artisan migrate
    ```
- 3.生成令牌
  - 3.1 监听 Model 的 creating 事件，在用户「注册」之前生成用户的激活令牌 app/Models/User.php
    ```
    use Illuminate\Support\Str;
    ...
    public static function boot()
    {
        parent::boot();

        static::creating(function ($user) {
            $user->activation_token = Str::random(10);
        });
    }
    ```
    - boot() 方法会在用户模型类完成初始化之后进行加载，因此我们对事件的监听需要放在该方法中。
  - 3.2 在模型工厂中将假用户设为激活 database/factories/UserFactory.php
    ```
    $factory->define(User::class, function (Faker $faker) {
        $date_time = $faker->date . ' ' . $faker->time;
        return [
            'name' => $faker->name,
            'email' => $faker->unique()->safeEmail,
            'email_verified_at' => now(),
            'activated' => true,
            'password' => '$2y$10$TKh8H1.PfQx37YgCzwiKb.KjNyWgaHb9cbcoQgdIVFlYg7B77UdFm', // secret
            'remember_token' => Str::random(10),
            'created_at' => $date_time,
            'updated_at' => $date_time,
        ];
    });
    ```
  - 3.3 重置数据库 并填充
    ```
    $ php artisan migrate:refresh --seed
    ```
- 4.发送邮件
  - 4.1 在 .env 中设置邮件驱动为 log
    ```
    MAIL_DRIVER=log
    ```
  - 4.2 激活路由 (激活链接) routes/web.php
    ```
    Route::get('signup/confirm/{token}', 'UsersController@confirmEmail')->name('confirm_email');
    ```
  - 4.3 激活邮件视图 resources/views/emails/confirm.blade.php
    ```
    <!DOCTYPE html>
    <html>
    <head>
      <meta charset="UTF-8">
      <title>注册确认链接</title>
    </head>
    <body>
      <h1>感谢您在 Weibo App 网站进行注册！</h1>

      <p>
        请点击下面的链接完成注册：
        <a href="{{ route('confirm_email', $user->activation_token) }}">
          {{ route('confirm_email', $user->activation_token) }}
        </a>
      </p>

      <p>
        如果这不是您本人的操作，请忽略此邮件。
      </p>
    </body>
    </html>
    ```
  - 4.4 登录时检查是否已激活 app/Http/Controllers/SessionsController.php
    ```
    public function store(Request $request)
    {
       $credentials = $this->validate($request, [
           'email' => 'required|email|max:255',
           'password' => 'required'
       ]);

       if (Auth::attempt($credentials, $request->has('remember'))) {
            // 登录成功
            if (Auth::user()->activated) {
                // 已激活
                session()->flash('success', '欢迎回来！');    
                // 登录后友好转向 intended() 
                // 重定向到上一次请求尝试访问的页面上，并接收一个默认跳转地址参数，当上一次请求记录为空时，跳转到默认地址上。
                $default = route('users.show', Auth::user());
                return redirect()->intended($default);
            } else {
                // 未激活
                Auth::logout();
                session()->flash('warning', '您的账号未激活，请检查邮箱中的注册邮件进行激活。');
                return redirect('/');
            }
        } else {
            // 登录失败
            session()->flash('danger', '很抱歉，您的邮箱和密码不匹配');
            // 使用 withInput() 后模板里 old('email') 将能获取到上一次用户提交的内容
            return redirect()->back()->withInput();
        }
    }
    ```
  - 4.5 发送邮件/激活 app/Http/Controllers/UsersController.php
    ```
    public function __construct()
    {
        // except 黑名单排除不需要登录的，其余都需要登录
        $this->middleware('auth', [
            'except' => ['show', 'create', 'store', 'index', 'confirmEmail']
        ]);

        // only 白名单设定注册必须为 游客模式（非登录）
        $this->middleware('guest', [
            'only' => ['create']
        ]);
    }

    // 注册
    public function store(Request $request)
    {
        ...
        // Auth::login($user); // 把之前用户注册成功之后进行的登录操作 换成 以下激活邮箱发送操作
        $this->sendEmailConfirmationTo($user);
        session()->flash('success', '验证邮件已发送到你的注册邮箱上，请注意查收。');
        return redirect()->route('users.show', $user);
    }

    // 发送激活
    protected function sendEmailConfirmationTo($user)
    {
        $view = 'emails.confirm'; // 邮件用的视图
        $data = compact('user');  // 视图要的数组数据
        $from = '123@qq.com';     // 发件人邮箱
        $name = 'andy';           // 发件人姓名
        $to = $user->email;       // 收件人邮箱
        $subject = '邮件标题：感谢注册哟！请完成激活哈！'; // 邮件标题

        Mail::send($view, $data, function($message) use ($from, $name, $to, $subject) {
            $message->from($from, $name)->to($to)->subject($subject);
        });
    }

    // 激活
    public function confirmEmail($token)
    {
        // firstOrFail 方法来取出第一个用户，在查询不到指定用户时将返回一个 404 响应
        $user = User::where('activation_token', $token)->firstOrFail();

        $user->activated = true;
        $user->activation_token = null;
        $user->save();

        Auth::login($user);
        session()->flash('success', '恭喜你，激活成功');
        return redirect()->route('users.show', $user);
    }
    ```
  - 4.6 测试：注册新用户后，在 `storage/logs/laravel-{today}.log` 中查收邮件，完成激活
- 5 Git 版本控制
  ```
  $ git add -A
  $ git commit -m "9.2 用户激活 boot中做模型监听"  
  ```
### 9.3 [密码重置](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.思路说明：重置密码控制器逻辑框架已经写好，我们只需配置4个路由、1个入口、2个视图即可。
- 2.重置密码路由
  ```
  Route::get('password/reset', 'Auth\ForgotPasswordController@showLinkRequestForm')->name('password.request');
  Route::post('password/email', 'Auth\ForgotPasswordController@sendResetLinkEmail')->name('password.email');
  Route::get('password/reset/{token}', 'Auth\ResetPasswordController@showResetForm')->name('password.reset');
  Route::post('password/reset', 'Auth\ResetPasswordController@reset')->name('password.update');
  ```
- 3.登录页面中添加「忘记密码」入口 resources/views/sessions/create.blade.php
  ```
  <div class="form-group">
    <label for="password">密码（<a href="{{ route('password.request') }}">忘记密码</a>）：</label>
    <input type="password" name="password" class="form-control" value="{{ old('password') }}">
  </div>
  ```
- 4.发送「重置密码表单」的视图 resources/views/auth/passwords/email.blade.php
  ```
  @extends('layouts.default')
  @section('title', '重置密码')

  @section('content')
  <div class="col-md-8 offset-md-2">
    <div class="card ">
      <div class="card-header"><h5>重置密码</h5></div>

      <div class="card-body">
        @if (session('status'))
        <div class="alert alert-success">
          {{ session('status') }}
        </div>
        @endif

        <form class="" method="POST" action="{{ route('password.email') }}">
          {{ csrf_field() }}

          <div class="form-group{{ $errors->has('email') ? ' has-error' : '' }}">
            <label for="email" class="form-control-label">邮箱地址：</label>

            <input id="email" type="email" class="form-control" name="email" value="{{ old('email') }}" required>

            @if ($errors->has('email'))
              <span class="form-text">
                <strong>{{ $errors->first('email') }}</strong>
              </span>
            @endif
          </div>

          <div class="form-group">
            <button type="submit" class="btn btn-primary">
              发送密码重置邮件
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
  @endsection
  ```
- 5.重置密码表单视图 resources/views/auth/passwords/reset.blade.php
  ```
  @extends('layouts.default')
  @section('title', '更新密码')

  @section('content')
  <div class="offset-md-1 col-md-10">
    <div class="card">
      <div class="card-header">
          <h5>更新密码</h5>
      </div>

      <div class="card-body">
        <form method="POST" action="{{ route('password.update') }}">
          @csrf

          <input type="hidden" name="token" value="{{ $token }}">

          <div class="form-group row">
            <label for="email" class="col-md-4 col-form-label text-md-right">Email 地址</label>

            <div class="col-md-6">
              <input id="email" type="email" class="form-control{{ $errors->has('email') ? ' is-invalid' : '' }}" name="email" value="{{ $email ?? old('email') }}" required autofocus>

              @if ($errors->has('email'))
              <span class="invalid-feedback" role="alert">
                <strong>{{ $errors->first('email') }}</strong>
              </span>
              @endif
            </div>
          </div>

          <div class="form-group row">
            <label for="password" class="col-md-4 col-form-label text-md-right">密码</label>

            <div class="col-md-6">
              <input id="password" type="password" class="form-control{{ $errors->has('password') ? ' is-invalid' : '' }}" name="password" required>

              @if ($errors->has('password'))
              <span class="invalid-feedback" role="alert">
                <strong>{{ $errors->first('password') }}</strong>
              </span>
              @endif
            </div>
          </div>

          <div class="form-group row">
            <label for="password-confirm" class="col-md-4 col-form-label text-md-right">确认密码</label>

            <div class="col-md-6">
              <input id="password-confirm" type="password" class="form-control" name="password_confirmation" required>
            </div>
          </div>

          <div class="form-group row mb-0">
            <div class="col-md-6 offset-md-4">
              <button type="submit" class="btn btn-primary">
                重置密码
              </button>
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
  @endsection
  ```
- 6.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "9.3 重置密码"
  ```
### 9.4 [生产环境中发送邮件](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.开启QQ邮箱的SMTP，并复制『授权码』，授权码将作为我们的密码使用
- 2.邮箱配置
  ```
  MAIL_DRIVER=smtp
  MAIL_HOST=smtp.qq.com
  MAIL_PORT=25
  MAIL_USERNAME=844@qq.com
  MAIL_PASSWORD=etxknliajakrbced
  MAIL_ENCRYPTION=tls
  MAIL_FROM_ADDRESS=844@qq.com
  MAIL_FROM_NAME=andy
  ```
- 3.在 app/Http/Controllers/UsersController.php 中，邮件发送的 from() 可以去掉了，因为 .env 中已经配置了
  ```
  // 发送激活
  protected function sendEmailConfirmationTo($user)
  {
      $view = 'emails.confirm'; // 邮件用的视图
      $data = compact('user');  // 视图要的数组数据
      $from = '123@qq.com';     // 发件人邮箱
      $name = 'andy';           // 发件人姓名
      $to = $user->email;       // 收件人邮箱
      $subject = '邮件标题：感谢注册哟！请完成激活哈！'; // 邮件标题

      // Mail::send($view, $data, function($message) use ($from, $name, $to, $subject) {
      //     $message->from($from, $name)->to($to)->subject($subject);
      // });
      
      // 因为在 .env 中配置了 MAIL_FROM_ADDRESS MAIL_FROM_NAME，因此不再需要使用 from 方法：
      Mail::send($view, $data, function($message) use ($to, $subject) {
          $message->to($to)->subject($subject);
      });
  }
  ```
- 4.Git 版本控制，及合并提交
  ```
  $ git add -A
  $ git commit -m "9.4 移除邮件发送的 from 选项"
  $ git checkout master
  $ git merge account-activation-password-resets
  $ git push
  ```
## 10 [微博 CRUD](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
### 10.2 [微博模型](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.新建一个分支
  ```
  $ git checkout master
  $ git checkout -b user-statuses
  ```
- 2.创建模型的「迁移文件」
  ```
  $ php artisan make:migration create_statuses_table --create="statuses"
  ```
- 3.编写迁移文件(加索引) database/migrations/[timestamp]_create_statuses_table.php
  ```
  public function up()
  {
      Schema::create('statuses', function (Blueprint $table) {
          $table->increments('id');
          $table->text('content');
          $table->integer('user_id')->index();
          $table->index(['created_at']);
          $table->timestamps();
      });
  }

  public function down()
  {
      Schema::dropIfExists('statuses');
  }
  ```
  - 加索引 index()
    - user_id 会用来查找指定用户发布过的所有微博，因此为了提高查询效率，这里我们需要为该字段加上索引。
    - created_at 微博的创建时间，为其添加索引的目的是，后面我们会根据微博的创建时间进行倒序输出。
  - 对应的 sql 语句是
    ```
    CREATE TABLE `statuses` (
      `id` int(10) unsigned NOT NULL AUTO_INCREMENT,
      `content` text COLLATE utf8mb4_unicode_ci NOT NULL,
      `user_id` int(11) NOT NULL,
      `created_at` timestamp NULL DEFAULT NULL,
      `updated_at` timestamp NULL DEFAULT NULL,
      PRIMARY KEY (`id`),
      KEY `statuses_created_at_index` (`created_at`),
      KEY `statuses_user_id_index` (`user_id`)
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;
    ```
- 4.执行迁移
  ```
  $ php artisan migrate
  ```
- 5.创建微博模型
  ```
  $ php artisan make:model Models/Status
  ```
- 6.关联「微博」和「用户」（一对多）
  - app/Models/Status.php
    ```
    // 多对一 多条微博属于一个用户
    public function user()
    {
        return $this->belongsTo(User::class);
    }
    ```
  - app/Models/User.php
    ```
    // 一对多 一个用户拥有多条微博
    public function statuses()
    {
        return $this->hasMany(Status::class);
    }
    ```
  - 关联的好处
    ```
    // 关联之前创建微博
    App\Models\Status::create()
    // 关联之后创建微博，这样创建的微博会自动与用户进行关联
    $user->statuses()->create()
    ```
- 7.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "10.2 微博数据模型"
  ```
### 10.3 [显示个人微博](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.控制器 app/Http/Controllers/UsersController.php
  ```
  public function show(User $user)
  {
      $statuses = $user->statuses()
                          ->orderBy('created_at', 'desc')
                          ->paginate(10);
      return view('users.show', compact('user', 'statuses'));
  }
  ```
- 2.微博局部视图 resources/views/statuses/_status.blade.php
  ```
  <li class="media mt-4 mb-4">
    <a href="{{ route('users.show', $user->id )}}">
      <img src="{{ $user->gravatar() }}" alt="{{ $user->name }}" class="mr-3 gravatar"/>
    </a>
    <div class="media-body">
      <h5 class="mt-0 mb-1">{{ $user->name }} <small> / {{ $status->created_at->diffForHumans() }}</small></h5>
      {{ $status->content }}
    </div>
  </li>
  ```
  - diffForHumans() 该方法的作用是将日期进行友好化处理。
- 3.在个人页面 resources/views/users/show.blade.php 引用微博局部视图
  ```
  @extends('layouts.default')
  @section('title', $user->name)

  @section('content')
  <div class="row">
    <div class="offset-md-2 col-md-8">
      <section class="user_info">
        @include('shared._user_info', ['user' => $user])
      </section>
      <section class="status">
        @if ($statuses->count() > 0)
          <ul class="list-unstyled">
            @foreach ($statuses as $status)
              @include('statuses._status')
            @endforeach
          </ul>
          <div class="mt-5">
            {!! $statuses->render() !!}
          </div>
        @else
          <p>没有数据！</p>
        @endif
      </section>
    </div>
  </div>
  @stop
  ```
- 4.造微博假数据 (4.4 服务容器)
  - 4.1 生成微博模型的「模型工厂」（模型工厂造模型）
    ```
    $ php artisan make:factory StatusFactory
    ```
  - 4.2 编写微博模型的「模型工厂」 database/factories/StatusFactory.php
    ```
    <?php

    use Faker\Generator as Faker;

    $factory->define(App\Models\Status::class, function (Faker $faker) {
        $date_time = $faker->date . ' ' . $faker->time;
        return [
            'content'    => $faker->text(),
            'created_at' => $date_time,
            'updated_at' => $date_time,
        ];
    });
    ```
  - 4.3 生成填充文件
    ```
    $ php artisan make:seeder StatusesTableSeeder
    ```
  - 4.4 编写填充文件（在填充文件中 调用 「微博模型工厂」来造模型，即填充数据） 
    database/seeds/StatusesTableSeeder.php
    ```
    <?php

    use Illuminate\Database\Seeder;
    use App\Models\User;
    use App\Models\Status;

    class StatusesTableSeeder extends Seeder
    {
        public function run()
        {
            $user_ids = ['1','2','3'];
            $faker = app(Faker\Generator::class);

            $statuses = factory(Status::class)->times(100)->make()->each(function ($status) use ($faker, $user_ids) {
                $status->user_id = $faker->randomElement($user_ids);
            });

            Status::insert($statuses->toArray());
        }
    }
    ```
    - [服务容器](https://learnku.com/docs/laravel/6.x/container/5131#68be3c)
      - 上例中，通过 app() 或者 resolve() 来获取一个 Faker 容器 的实例
      - 「服务容器」：就是一个装载和解析服务的容器，服务指的是「类」或「接口」
      - 「绑定服务」：就是把服务绑定到容器中，几乎所有的服务容器绑定都会在 [服务提供者](https://learnku.com/docs/laravel/6.x/providers/5132) 中注册
        ```
        $this->app->bind('HelpSpot\API', function ($app) {
            return new HelpSpot\API($app->make('HttpClient'));
        });
        ```
      - 「解析实例」：就是通过 app() 或 resolve() 等从容器中得到「服务实例」    
    - 在 database/seeds/DatabaseSeeder.php 调用
      ```
      public function run()
      {
          $this->call(UsersTableSeeder::class);
          $this->call(StatusesTableSeeder::class);
      }
      ```
    - 对数据库进行重置和填充
      ```
      $ php artisan migrate:refresh --seed
      ```
- 5.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "10.3 用户微博列表"
  ```
### 10.4 [发布微博](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.路由 resource(,,['only'=>[]])
  ```
  Route::resource('statuses', 'StatusesController', ['only' => ['store', 'destroy']]);
  ```
- 2.控制器
  ```
  php artisan make:controller StatusesController
  ```
  app/Http/Controllers/StatusesController.php
  ```
  use Auth;
  ...
  public function __construct()
  {
      $this->middleware('auth');
  }

  public function store(Request $request)
  {
      $this->validate($request, [
          'content' => 'required|max:140'
      ]);

      Auth::user()->statuses()->create([
          'content' => $request['content']
      ]);
      session()->flash('success', '发布成功！');
      return redirect()->back();
  }
  ```
- 3.发布微博的「局部表单视图」 resources/views/shared/_status_form.blade.php
  ```
  <form action="{{ route('statuses.store') }}" method="POST">
    @include('shared._errors')
    {{ csrf_field() }}
    <textarea class="form-control" rows="3" placeholder="聊聊新鲜事儿..." name="content">{{ old('content') }}</textarea>
    <div class="text-right">
        <button type="submit" class="btn btn-primary mt-3">发布</button>
    </div>
  </form>
  ```
- 4.在首页引入局部表单视图 resources/views/static_pages/home.blade.php
  ```
  @extends('layouts.default')

  @section('content')
    @if (Auth::check())
      <div class="row">
        <div class="col-md-8">
          <section class="status_form">
            @include('shared._status_form')
          </section>
        </div>
        <aside class="col-md-4">
          <section class="user_info">
            @include('shared._user_info', ['user' => Auth::user()])
          </section>
        </aside>
      </div>
    @else
      <div class="jumbotron">
        <h1>Hello Laravel</h1>
        <p class="lead">
          你现在所看到的是 <a href="https://learnku.com/courses/laravel-essential-training">Laravel 入门教程</a> 的示例项目主页。
        </p>
        <p>
          一切，将从这里开始。
        </p>
        <p>
          <a class="btn btn-lg btn-success" href="{{ route('signup') }}" role="button">现在注册</a>
        </p>
      </div>
    @endif
  @stop
  ```
- 5.修改模型可更新字段 app/Models/Status.php
  ```
  // 允许更新微博的 content 字段
  protected $fillable = ['content'];
  ```
- 6.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "10.4 发布微博"
  ```
### 10.5 [首页微博列表](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.在用户模型中 定义「动态流」方法 app/Models/User.php
  ```
  public function feed()
  {
      return $this->statuses()
                  ->orderBy('created_at', 'desc');
  }
  ```
- 2.控制器中返回「动态流」数据 app/Http/Controllers/StaticPagesController.php
  ```
  use Auth;
  ...
  public function home()
  {
      $feed_items = [];
      if (Auth::check()) {
          $feed_items = Auth::user()->feed()->paginate(30);
      }

      return view('static_pages/home', compact('feed_items'));
  }
  ```
- 3.定义一个「动态流」局部视图 resources/views/shared/_feed.blade.php
  ```
  @if ($feed_items->count() > 0)
    <ul class="list-unstyled">
      @foreach ($feed_items as $status)
        @include('statuses._status',  ['user' => $status->user])
      @endforeach
    </ul>
    <div class="mt-5">
      {!! $feed_items->render() !!}
    </div>
  @else
    <p>没有数据！</p>
  @endif
  ```
- 4.主页中包含「动态流」局部视图 resources/views/static_pages/home.blade.php
  ```
  @if (Auth::check())
    <div class="row">
      <div class="col-md-8">
        <section class="status_form">
          @include('shared._status_form')
        </section>
        <h4>微博列表</h4>
        <hr>
        @include('shared._feed')
      </div>
      <aside class="col-md-4">
        <section class="user_info">
          @include('shared._user_info', ['user' => Auth::user()])
        </section>
      </aside>
    </div>
  @else
  ```
- 5.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "10.5 首页微博列表"
  ```
### 10.6 [删除微博](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.删除的授权策略
  ```
  $ php artisan make:policy StatusPolicy
  ```
  app/Policies/StatusPolicy.php
  ```
  use App\Models\User;
  use App\Models\Status;
  ...
  // 只有自己才能删除自己的微博
  public function destroy(User $currentUser, Status $status)
  {
      return $currentUser->id === $status->user_id;
  }
  ```
- 2.视图中的删除按钮 resources/views/statuses/_status.blade.php
  ```
  <li class="media mt-4 mb-4">
    <a href="{{ route('users.show', $user->id )}}">
      <img src="{{ $user->gravatar() }}" alt="{{ $user->name }}" class="mr-3 gravatar"/>
    </a>
    <div class="media-body">
      <h5 class="mt-0 mb-1">{{ $user->name }} <small> / {{ $status->created_at->diffForHumans() }}</small></h5>
      {{ $status->content }}
    </div>

    @can('destroy', $status)
      <form action="{{ route('statuses.destroy', $status->id) }}" method="POST" onsubmit="return confirm('您确定要删除本条微博吗？');">
        {{ csrf_field() }}
        {{ method_field('DELETE') }}
        <button type="submit" class="btn btn-sm btn-danger">删除</button>
      </form>
    @endcan
  </li>
  ```
- 3.控制器中删除动作 app/Http/Controllers/StatusesController.php
  ```
  use App\Models\Status;
  ...
  public function destroy(Status $status)
  {
      $this->authorize('destroy', $status);
      $status->delete();
      session()->flash('success', '微博已被成功删除！');
      return redirect()->back();
  }
  ```
- 4.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "10.6 删除微博"
  $ git checkout master
  $ git merge user-statuses
  $ git push
  ```
## 11 [粉丝关系](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
### 11.2 [粉丝数据表](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.新建一个分支
  ```
  $ git checkout master
  $ git checkout -b following-users
  ```
- 2.生成一个「粉丝关系数据表」(即中间表followers)
  ```
  $ php artisan make:migration create_followers_table --create="followers"
  ```
  database/migrations/[timestamp]_create_followers_table.php
  ```
  public function up()
  {
      Schema::create('followers', function (Blueprint $table) {
          $table->increments('id');
          $table->integer('user_id')->index(); // 加索引，获取「关注的人」列表要根据此字段查询
          $table->integer('follower_id')->index(); // 加索引，获取「粉丝」列表要根据此字段查询
          $table->timestamps();
      });
  }

  public function down()
  {
      Schema::dropIfExists('followers');
  }
  ```
  执行迁移，生成中间表
  ```
  $ php artisan migrate
  ```
- 3.关联博主和粉丝 (多对多) app/Models/User.php
  ```
  // 多对多关联语法：$this-> belongsToMany(关联表model，中间表表名，中间表中本model的关联ID，中间表中关联model的关联ID);
  // 本 model 为博主 （博主的粉丝列表）
  public function followers()
  {
      return $this->belongsToMany(User::class, 'followers', 'user_id', 'follower_id');
  }

  // 本 model 为粉丝 （粉丝的博主列表）
  public function followings()
  {
      return $this->belongsToMany(User::class, 'followers', 'follower_id', 'user_id');
  }

  // 关注 (所谓关注，即把粉丝的ids 加到 博主列表 中去)
  public function follow($user_ids)
  {
      if ( !is_array($user_ids) ) {
          $user_ids = compact('user_ids');
      }
      $this->followings()->sync($user_ids, false); // false 参数表示添加关注人id数组时，不删除其他关注人id
  }

  // 取关 (所谓取关，即把粉丝的ids 从 博主列表 中减去)
  public function unfollow($user_ids)
  {
      if ( !is_array($user_ids) ) {
          $user_ids = compact('user_ids');
      }
      $this->followings()->detach($user_ids);
  }

  // 是否关注
  public function isFollowing($user_id)
  {
      // $this->followings 返回的是：粉丝关注的博主列表的集合
      // $this->followings() 返回的是：数据库请求构建器（也就是数据库查询语句）
      // $this->followings == $this->followings()->get() // 等于 true
      // contains 方法是 Collection集合 的一个方法
      return $this->followings->contains($user_id);
  }
  ```
  - 「多对多」关联语法
    ```
    $this-> belongsToMany(关联表model，中间表表名，中间表中本model的关联ID，中间表中关联model的关联ID);
    ```
  - 「多对多」[关联动作](https://learnku.com/courses/laravel-essential-training/6.x/fan-data-table/5501#065818)
    - 「关注」这个动作，就是在「某粉丝id」的「博主列表」中做加法，用 attach() 和 sync() 方法
      ```
      // attach() 添加 id 时不会去重，比如多次执行时，可能会重复添加id为"2"的记录
      $user->followings()->attach([2, 3])

      // sync() 添加 id 时会去重，不会重复添加同一个id
      // sync() 的第二个参数表示添加关注人(博主)id数组时，「是否」删除其他关注人id，false 表示「否」
      $user->followings()->sync([3], false)
      ```
    - 「取关」这个动作，就是在「某粉丝id」的「博主列表」中做减法，用 detach() 方法
      ```
      $user->followings()->detach([2,3])
      ```
- 4.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "11.2 粉丝数据表"
  ```
### 11.3 [社交信息统计](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.填充「关注」的假数据
  ```
  $ php artisan make:seeder FollowersTableSeeder
  ```
  database/seeds/FollowersTableSeeder.php
  ```
  use App\Models\User;
  ...
  public function run()
  {
      // 让「第1个用户」和「其他用户」互相关注
      $users = User::all();

      $user = $users->first();
      $followers = $users->slice(1);

      $user_id = $user->id;
      $follower_ids = $followers->pluck('id')->toArray();

      // 1号 关注 其余人
      $user->follow($follower_ids);

      // 其余人 关注 1号
      foreach($followers as $follower) {
          $follower->follow($user_id);
      }
  }
  ```
  调用填充文件 database/seeds/DatabaseSeeder.php
  ```
  public function run()
    {
        $this->call(UsersTableSeeder::class);
        $this->call(StatusesTableSeeder::class);
        $this->call(FollowersTableSeeder::class);
    }
  ```
  重置数据库，并填充
  ```
  $ php artisan migrate:refresh --seed
  ```
- 2.社交统计局部视图 resources/views/shared/_stats.blade.php
  ```
  <a href="#">
    <strong id="following" class="stat">
      {{ count($user->followings) }}
    </strong>
    关注
  </a>
  <a href="#">
    <strong id="followers" class="stat">
      {{ count($user->followers) }}
    </strong>
    粉丝
  </a>
  <a href="#">
    <strong id="statuses" class="stat">
      {{ $user->statuses()->count() }}
    </strong>
    微博
  </a>
  ```
  - 知识点：计数时，尽量在「查询构建器」上count() （不过，最好的方式单独一个字段计数，这样就不用count()了）
    ```
    $user->statuses->count()   // 数据 70W 条，数据太大，内存溢出（这种是先取出集合数据，再统计，数据太大全部取出时，很耗时且占内存）
    $user->statuses()->count() // 数据 70W 条，我用这种方式是 0 秒（这种不用取出数据，直接 sql 计数）
    ```
- 3.加载子视图
  - 主页加载子视图 resources/views/static_pages/home.blade.php
    ```
    @if (Auth::check())
      <div class="row">
        <div class="col-md-8">
          <section class="status_form">
            @include('shared._status_form')
          </section>
          <h4>微博列表</h4>
          <hr>
          @include('shared._feed')
        </div>
        <aside class="col-md-4">
          <section class="user_info">
            @include('shared._user_info', ['user' => Auth::user()])
          </section>
          <section class="stats mt-2">
            @include('shared._stats', ['user' => Auth::user()])
          </section>
        </aside>
      </div>
    @else
    ```
  - 个人页面也加载子视图 resources/views/users/show.blade.php
    ```
    @extends('layouts.default')
    @section('title', $user->name)

    @section('content')
    <div class="row">
      <div class="offset-md-2 col-md-8">
        <section class="user_info">
          @include('shared._user_info', ['user' => $user])
        </section>
        <section class="stats mt-2">
          @include('shared._stats', ['user' => $user])
        </section>
        <hr>
        <section class="status">
          @if ($statuses->count() > 0)
            <ul class="list-unstyled">
              @foreach ($statuses as $status)
                @include('statuses._status')
              @endforeach
            </ul>
            <div class="mt-5">
              {!! $statuses->render() !!}
            </div>
          @else
            <p>没有数据！</p>
          @endif
        </section>
      </div>
    </div>
    @stop
    ```
- 4.css样式 resources/sass/app.scss
  ```
  .stats {
    overflow: auto;
    margin-top: 0;
    padding: 0;
    a {
      float: left;
      padding: 0 10px;
      text-align: center;
      width: 33%;
      border-left: 1px solid #eee;
      color: #33383c;
      &:first-child {
        padding-left: 0;
        border: 0;
      }
      &:hover {
        text-decoration: none;
        color: #337ab7;
      }
    }
    strong {
      display: block;
      font-size: 1.2em;
      color: black;
    }
  }
  ```
  编译样式文件
  ```
  $ npm run dev
  ```
- 5.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "11.3 社交统计信息"
  ```
### 11.4 [粉丝页面](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.路由 routes/web.php
  ```
  Route::get('/users/{user}/followings', 'UsersController@followings')->name('users.followings');
  Route::get('/users/{user}/followers', 'UsersController@followers')->name('users.followers');
  ```
- 2.入口链接 resources/views/shared/_stats.blade.php
  ```
  <a href="{{ route('users.followings', $user->id) }}">
    <strong id="following" class="stat">
      {{ count($user->followings) }}
    </strong>
    关注
  </a>
  <a href="{{ route('users.followers', $user->id) }}">
    <strong id="followers" class="stat">
      {{ count($user->followers) }}
    </strong>
    粉丝
  </a>
  <a href="{{ route('users.show', $user->id) }}">
    <strong id="statuses" class="stat">
      {{ $user->statuses()->count() }}
    </strong>
    微博
  </a>
  ```
- 3.控制器 app/Http/Controllers/UsersController.php
  ```
  public function followings(User $user)
  {
      $users = $user->followings()->paginate(30);
      $title = $user->name . '关注的人';
      return view('users.show_follow', compact('users', 'title'));
  }

  public function followers(User $user)
  {
      $users = $user->followers()->paginate(30);
      $title = $user->name . '的粉丝';
      return view('users.show_follow', compact('users', 'title'));
  }
  ```
- 4.视图（博主列表和粉丝列表共用一个视图） resources/views/users/show_follow.blade.php
  ```
  @extends('layouts.default')
  @section('title', $title)

  @section('content')
  <div class="offset-md-2 col-md-8">
    <h2 class="mb-4 text-center">{{ $title }}</h2>

    <div class="list-group list-group-flush">
      @foreach ($users as $user)
        <div class="list-group-item">
          <img class="mr-3" src="{{ $user->gravatar() }}" alt="{{ $user->name }}" width=32>
          <a href="{{ route('users.show', $user) }}">
            {{ $user->name }}
          </a>
        </div>

      @endforeach
    </div>

    <div class="mt-3">
      {!! $users->render() !!}
    </div>
  </div>
  @stop
  ```
- 5.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "11.4 关注和粉丝列表页面"
  ```
### 11.5 [关注按钮](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.路由 routes/web.php
  ```
  Route::post('/users/followers/{user}', 'FollowersController@store')->name('followers.store');
  Route::delete('/users/followers/{user}', 'FollowersController@destroy')->name('followers.destroy'); 
  ```
- 2.授权策略 app/Policies/UserPolicy.php
  ```
  public function follow(User $currentUser, User $user)
  {
      // 自己不能关注自己
      return $currentUser->id !== $user->id;
  }
  ```
- 3.关注表单的局部视图 resources/views/users/_follow_form.blade.php
  ```
  @can('follow', $user)
    <div class="text-center mt-2 mb-4">
      @if (Auth::user()->isFollowing($user->id))
        <form action="{{ route('followers.destroy', $user->id) }}" method="post">
          {{ csrf_field() }}
          {{ method_field('DELETE') }}
          <button type="submit" class="btn btn-sm btn-outline-primary">取消关注</button>
        </form>
      @else
        <form action="{{ route('followers.store', $user->id) }}" method="post">
          {{ csrf_field() }}
          <button type="submit" class="btn btn-sm btn-primary">关注</button>
        </form>
      @endif
    </div>
  @endcan
  ```
- 4.个人页面 添加「关注表单」子视图 resources/views/users/show.blade.php
  ```
  <section class="user_info">
    @include('shared._user_info', ['user' => $user])
  </section>

  @if (Auth::check())
    @include('users._follow_form')
  @endif

  <section class="stats mt-2">
    @include('shared._stats', ['user' => $user])
  </section>
  <hr>
  ```
- 5.控制器 app/Http/Controllers/FollowersController.php
  ```
  $ php artisan make:controller FollowersController
  ```
  ```
  <?php

  namespace App\Http\Controllers;

  use Illuminate\Http\Request;
  use App\Models\User;
  use Auth;

  class FollowersController extends Controller
  {
      public function __construct()
      {
          $this->middleware('auth');
      }

      public function store(User $user)
      {
          $this->authorize('follow', $user);

          if ( ! Auth::user()->isFollowing($user->id)) {
              Auth::user()->follow($user->id);
          }

          return redirect()->route('users.show', $user->id);
      }

      public function destroy(User $user)
      {
          $this->authorize('follow', $user);

          if (Auth::user()->isFollowing($user->id)) {
              Auth::user()->unfollow($user->id);
          }

          return redirect()->route('users.show', $user->id);
      }
  }
  ```
- 6.Git 版本控制
  ```
  $ git add -A
  $ git commit -m "11.5 关注按钮"
  ```
### 11.6 [动态流（显示所有关注用户的微博动态）](https://github.com/andy-love-coding/laravel1.7#%E7%9B%AE%E5%BD%95)
- 1.app/Models/User.php
  ```
  // 动态流
  public function feed()
  {
      // 自己的动态流
      // return $this->statuses()
      //                 ->orderBy('created_at', 'desc');

      // 自己和关注用户的动态流
      $user_ids = $this->followings->pluck('id')->toArray();
      array_push($user_ids, $this->id);
      return Status::whereIn('user_id', $user_ids)
                              ->with('user')
                              ->orderBy('created_at', 'desc');
  }
  ```
  - [查询构建器](https://learnku.com/docs/laravel/6.x/queries/5171) whereIn 方法取出所有用户的微博动态并进行倒序排序；
  - [预加载](https://learnku.com/docs/laravel/6.x/eloquent-relationships/5177#eager-loading) with('user') 预加载方法，提前取出所有 $statuses 里面的 $user , 避免了 N+1 查找的问题。
- 2.Git 版本控制，即合并提交
  ```
  $ git add -A
  $ git commit -m "11.6 关注用户动态流"
  $ git checkout master
  $ git merge following-users
  $ git push
  ```