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
  