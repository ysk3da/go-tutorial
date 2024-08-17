# Go言語でHello,world

ISUCONでベンチマーカーを動かすためにGoをインストールした。

そこでHello,worldもしておこう。

- [Go言語の開発環境を構築する ~ Macbook Pro M2編](./install_golang.md)

手引はここ

- [Tutorial: Get started with Go](https://go.dev/doc/tutorial/getting-started)

手順は下記

~~~sh
mkdir hello

cd hello

go mod init example/hello
~~~

ここまで来たら、`hello`ディレクトリの中に`hello.go`ファイルを作成する

~~~go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
~~~

そして、このファイルをrunする！

~~~sh
go run .

# おおー！ 無事に出力されました！
Hello, World!
~~~
