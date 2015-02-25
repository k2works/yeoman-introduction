YEOMAN入門
===
# 目的
YEOMANを使えるようになる

# 前提
| ソフトウェア     | バージョン    | 備考         |
|:---------------|:-------------|:------------|
| ChefDK    　　　|0.3.5        |             |
| Vagrant        |1.6.5        |             |
| vagrant-berkshelf　　|        |             |
| vagrant-omnibus　　|        |             |


# 構成
+ [セットアップ](#1)
+ [はじめに](#2)
+ [チュートリアル](#3)

# 詳細
## <a name="1">セットアップ</a>
```bash
$ vagrant up
$ vagrant ssh
$ cd /vagrant
```
## <a name="2">はじめに</a>
### yoとジェネレーターをインストールする
```
$ sudo chown -R vagrant:vagrant ~/.npm
$ sudo npm install -g yo bower grunt-cli gulp
```
### 基本スキャフォルド
```
$ mkdir my-yo-project
$ cd my-yo-project
$ sudo npm install -g generator-webapp
$ yo webapp
```
インストールに失敗したら再度インストールする
```
$ npm install
```

#### ホストマシンから見れるようにする
_Gruntfile.js_
```
    // The actual grunt server settings
    connect: {
      options: {
        port: 9000,
        open: true,
        livereload: 35729,
        // Change this to '0.0.0.0' to access the server from outside
        hostname: '0.0.0.0'
      },
```

#### テストサーバを起動する
```
$ grunt server
```

![](https://farm9.staticflickr.com/8671/16455529438_1660bf411b_z.jpg)

## <a name="3">チュートリアル</a>

# 参照
+ [YEOMAN](http://yeoman.io/)
+ [YEOMAN開発環境をVagrant Ubuntu 14.04にセットアップ](http://blog.hrendoh.com/setup-yeoman-dev-environments-on-vagrant-ubuntu-14-04/#.VOr4JVOsWKs)
+ [yeoman angular generator wont start on grunt serve](http://stackoverflow.com/questions/24639586/yeoman-angular-generator-wont-start-on-grunt-serve)
