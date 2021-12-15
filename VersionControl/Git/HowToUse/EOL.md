## Gitで、ファイル毎に改行コードを指定する
改行コードを指定する場合は、_.gitattributes_ ファイルに `eol=lf` を入れる。

### 例
C#のソースコード(_.cs_) の改行コードをlfにする
```
*.cs text eol=lf
```

その後、以下コマンドですべてのファイルを _.gitattributes_ の設定どおりにする
```sh
git add --renormalize .
```

### See also
- [Configuring Git to handle line endings - GitHub Docs](https://docs.github.com/ja/get-started/getting-started-with-git/configuring-git-to-handle-line-endings)
- [.gitattributesで改行コードの扱いを制御する - Qiita](https://qiita.com/nacam403/items/23511637335fc221bba2)
