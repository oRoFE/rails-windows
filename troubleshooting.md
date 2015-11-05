# トラブルシューティング

- gem install berkshelf で `make: *** [installlib] Error 2` が発生する。
  - Windows で Berkshelf を使う場合は chef-dk が必要。
    - 参考: http://qa.atmarkit.co.jp/q/4004
  - [Tar for Windows](http://gnuwin32.sourceforge.net/packages/gtar.htm) からBinaries(Zip) と Dependencies(Zip) をダウンロードし、展開して得られるファイルをDevKitのディレクトリに上書きする。
    - 参考: http://qiita.com/takeyuweb/items/ec4c28f6bca08bce0bda
- [dep-selector-libgecode](https://github.com/chef/dep-selector-libgecode) (Berkshelf の依存ライブラリ) のインストール (ビルド) に失敗する。
  - ビルド中、メモリを 2 GB くらい使用するため、メモリ割り当てが足りない可能性も。割り当て量を増やすと解決する可能性が高い。
- berks コマンドで `certificate verify failed` エラーが出る。
  - 証明書をダウンロードし、環境変数を設定する。
  - 参照: http://qiita.com/bibio/items/8c766be648fdd4f4e2fb
- vagrant がフォルダのマウントに失敗する。`Failed to mount folders in Linux guest. ...`
  - [vbox をリビルドする](http://qiita.com/osamu1203/items/10e19c74c912d303ca0b)
  - 上記でもダメなら、`$ vagrant plugin install vagrant-vbguest` する。
- vagrant まわりがなんかおかしい。
  - `$ vagrant destroy` すれば直る時もある。
- 仮想マシン内で `bundle install` に失敗する。
  - インストール先を共有フォルダ (Vagrant なら `/vagrant`) 外にすることで解決する場合がある。
