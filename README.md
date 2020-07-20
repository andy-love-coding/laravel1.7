## 3 构建页面
### 3.2 创建应用
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
### 3.3 静态页面
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
### 3.4 Artisan 命令
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
## 4 优化页面
### 4.2 样式美化
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
### 4.3 前端工作流
- [Laravel 前端工作流](https://learnku.com/courses/laravel-essential-training/6.x/laravel-front-end-workflow/5454)
  - SASS 语法基础
  - NPM, Yarn, Laravel Mix
### 4.4 浏览器缓存问题
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
### 4.5 局部视图
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
### 4.6 布局中的链接(命名路由)
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
### 4.7 用户注册页面
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
## 5 用户模型
- 1.准备好舞台
  ```
  $ git checkout master
  $ git checkout -b modeling-users
  ```
### 5.2 数据库迁移
- 1.[数据库迁移](https://learnku.com/courses/laravel-essential-training/6.x/database-migration/5461)
  - [可用的字段类型](https://learnku.com/docs/laravel/6.x/migrations/5173#b419dd)
### 5.3 查看数据库表
- 1.[数据库工具 SequelPro](https://learnku.com/courses/laravel-essential-training/6.x/check-the-database-table/5462#679a96)
- 2.执行迁移（生成表）
  ```
  $ php artisan migrate
  ```
### 5.4 模型文件
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
### 5.5 创建用户对象(Tinker)
- 1.进入 Tinker 环境
  ```
  $ php artisan tinker
  ```
- 2 创建一个用户对象
  ```
  >>> App\Models\User::create(['name'=> 'Summer', 'email'=>'summer@example.com','password'=>bcrypt('password')])
  ```
### 5.6 查找用户对象(测试)
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
### 5.7 更新用户对象(测试)
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
### 5.8 小结
- 1.将代码切回到主分支中进行合并，并提交
  ```
  $ git checkout master
  $ git merge modeling-users
  $ git push
  ```