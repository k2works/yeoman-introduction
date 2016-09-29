YEOMAN入門
===
# 目的
YEOMANを使えるようになる

# 前提
| ソフトウェア     | バージョン    | 備考         |
|:---------------|:-------------|:------------|
| Vagrant        |1.8.4        |             |


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
$ npm install -g yo gulp
$ npm install -g generator-webapp
```
### 基本スキャフォルド
```
$ mkdir my-yo-project
$ cd my-yo-project
$ yo webapp
$ gulp
```
インストールに失敗したら再度インストールする
```
$ yo webapp
```

#### テストサーバを起動する
```
$ gulp serve
```

![](https://farm9.staticflickr.com/8671/16455529438_1660bf411b_z.jpg)

## <a name="3">チュートリアル</a>

# 参照
+ [YEOMAN](http://yeoman.io/)
+ [YEOMAN開発環境をVagrant Ubuntu 14.04にセットアップ](http://blog.hrendoh.com/setup-yeoman-dev-environments-on-vagrant-ubuntu-14-04/#.VOr4JVOsWKs)
+ [yeoman angular generator wont start on grunt serve](http://stackoverflow.com/questions/24639586/yeoman-angular-generator-wont-start-on-grunt-serve)
