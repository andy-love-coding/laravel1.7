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
### 5.1 章节说明
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
## 6 用户注册
### 6.2 显示用户信息
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
### 6.3 注册表单
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
### 6.4 用户数据验证
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
### 6.5 错误消息
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
### 6.6 注册成功
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
### 6.7 在 Heroku 上使用 PostgreSQL
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
## 7 会话管理
### 7.2 会话
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
### 7.3 用户登录
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
### 7.4 退出
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
### 7.5 记住我
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
## 8 用户 CRUD
### 8.2 更新用户
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
### 8.3 权限系统
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
### 8.4 用户列表
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