# `svn add`
http://jtdan.com/vcs/svn/svn-book/svn.ref.svn.c.add.html

新規ファイルをSubversionで管理するファイル/ディレクトリとして追加するためのコマンド

## About
基本的には以下のコマンドだけで済ませる
```
svn add <追加したいファイル・ディレクトリのパス>
```

やっぱまだコミットしない、という場合は `svn revert`を使う。
```
svn revert <追加をやめるファイル・ディレクトリのパス>
```
