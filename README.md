# Windows 向け Rails 環境構築メモ

システムチームと共同で開発する際に必要そうな、環境構築に関するメモを書いておきます。

## 環境変数の変更方法

PC を右クリック→プロパティ→システムの詳細設定→詳細設定タブ→環境変数

○○にパスを通すと書かれていたら、環境変数の Path に該当するフォルダの場所を追記する。

## 使うと良いツール

### [Chocolatey](https://chocolatey.org/)

Windows 向けパッケージ管理ツール

### [RubyInstaller](http://rubyinstaller.org/)

インストーラーから書くバージョンの Ruby をインストールすることができる。下記の uru と合わせて使うと良い。

また、gem のライブラリにはインストール時に Development Kit を要求するものがあるため、合わせてインストールすると良い。適当な場所に展開し、パスを通しておく。

### [uru](https://bitbucket.org/jonforums/uru)

Windows 向け Ruby のバージョン管理ツール。Chocolatey からインストールできる。
(pik はメンテナンスされていないので使わないほうが良い)

uru 自体は Ruby をインストールする機能を持っていないので、別途 [RubyInstaller](http://rubyinstaller.org/) でインストールを行い、uru に登録する。

```sh
# RubyInstaller で C:\Ruby223-x64 に Ruby 2.2.3 をインストール済み
$ uru admin add C:\Ruby223-x64\bin 223 # uru に 223 という名前で登録
$ uru 223 # 登録した Ruby を使用する
$ ruby -v
ruby 2.2.3p173 (2015-08-18 revision 51636) [x64-mingw32]
```
