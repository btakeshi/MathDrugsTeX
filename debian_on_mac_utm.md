# UTM で Debian on Mac

## ネットワークインストールISOイメージを取得

[arm64](https://www.debian.org/CD/netinst/)
右側のISOイメージを取得

## UTMにて

新規仮想マシンを作成
仮想化
Linux
続ける
起動ISOイメージ▶先程ダウンロードしたファイル
どこかでappleなちゃらにチェック

UTMスタート
あとは画面の指示に従うだけ。
```
# apt install sudo
# visudo
```
viが立ち上がるので、
```
btakesh ALL=(ALL:ALL) ALL
```
と打ち込んで、Ctrl-O ENTER Ctrl-X
```
ip a
```
でIPアドレスを確認し、あとはMacターミナルから接続する。


## Terminal

```
% ssh IPアドレス
$ sudo apt update
$ sudo apt upgrade
# apt install sudo
```

sudo apt install ruby-full build-essential

## Git

$ sudo apt install git
$ git config --global user.name "BUTO Takeshi"
$ git config --global user.email "mail"

## Jekyll

gem install --user-install jekyll bundle
.bashrcに
export GEM_HOME="$HOME/gems"
export PATH="$HOME/.local/share/gem/ruby/3.3.0/bin:$PATH"
を追加した。
