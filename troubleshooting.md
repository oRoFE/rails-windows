# トラブルシューティング

- gem install berkshelf で `make: *** [installlib] Error 2` が発生する。
  - Windows で Berkshelf を使う場合は chef-dk が必要。
    - 参考: http://qa.atmarkit.co.jp/q/4004
  - [Tar for Windows](http://gnuwin32.sourceforge.net/packages/gtar.htm) からBinaries(Zip) と Dependencies(Zip) をダウンロードし、展開して得られるファイルをDevKitのディレクトリに上書きする。
    - 参考: http://qiita.com/takeyuweb/items/ec4c28f6bca08bce0bda
- berks コマンドで `certificate verify failed` エラーが出る。
  - 証明書をダウンロードし、環境変数を設定する。
  - 参照: http://qiita.com/bibio/items/8c766be648fdd4f4e2fb
