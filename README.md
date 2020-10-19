# ひとこと掲示板

研修でPython3を用いて、ひとこと掲示板を作成しました。

# デモ

![画像の説明](hitokoto.png "ひとこと掲示板イメージ")

「名前」と「本文」を入力し、投稿することできます。

# 環境

Ubuntu 20.04.1 LTS

Python 3.8

MySQL Ver 8.0.21

# 事前準備

pip3コマンドをインストールします。

```bash
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
$ sudo python3 get-pip.py
```

pip3コマンドでmysqlclientをインストールします。

```bash
$ pip3 install mysqlclient
```

userdir.confのOptionsにExecCGIを追加します。

```bash
Options ExecCGI MultiViews Indexes
```

CGIモジュールを有効にします。

```bash
$ sudo a2enmod cgi
$ sudo systemctl restart apache2
```

~/public_html/.htaccessを以下の内容で作成します。

```bash
AddHandler cgi-script .cgi
```

# 使用方法

ブラウザで以下のアドレスを入力します。

```bash
http://[IPアドレス]/~[ユーザ名]/bbs.py
```

# 注意

Macではテストを行っていません

# 作成者

後藤
