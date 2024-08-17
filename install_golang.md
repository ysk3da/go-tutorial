# Go言語の開発環境を構築する ~ Macbook Pro M2編

Go言語の開発環境が必要になったので、構築する。

## バージョン管理ツールの選定

`asdf`を使っていく。

anyenv も定番だが、新しいもの好きなので、試したい気持ち。

- [asdfで各言語のバージョン管理をしようぜ！](./install_asdf.md)

`asdf`は複数の言語をバージョン管理できるツールです。
各言語のpluginをinstallする必要があります。

今回はgo言語なので、

~~~sh
# asdf の golang プラグインをインストールする
asdf plugin add golang
~~~

## 利用可能なバージョンの確認

~~~sh
asdf list all golang
~~~

いっぱいありますね。
公式に行ってstableのナンバーを見てきましょう。
latestはv1.23.0ですね。
一旦これをインストールしましょう。

~~~sh
asdf install golang latest
~~~

バージョン確認してみましょう。

~~~sh
go version

# あれ？
Consider adding one of the following versions in your config file at 
golang 1.23.0
~~~

あ、global 指定忘れてますね

~~~sh
asdf global golang latest
~~~

これでどうかな？

~~~sh
go version

# お、来ましたね
go version go1.23.0 darwin/arm64
~~~

一応 rootも確認してみよう。

~~~sh
go env GOROOT

## おおー ばっちり
/Users/｛お名前｝/.asdf/installs/golang/1.23.0/go
~~~

## Hello,world してみよう！

- [Tutorial: Get started with Go](https://go.dev/doc/tutorial/getting-started)

## まとめ

Goをインストールしてみました。

思ってるより時間かかるので、時間あるときこまめにやろう。