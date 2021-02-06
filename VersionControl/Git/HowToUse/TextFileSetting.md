# テキストファイルの属性
.gitattributes で、コミット時にチェックを走らせたりとか



### About
テキストファイルのエンコードや改行コードをそろえたい場合、一般的には「Linter(リンター)」と呼ばれるツールを使うことが多い。

Linterはエンコードや改行コードだけはなく、フォーマットまで揃えられるが、Gitでバージョン管理しているものに対し、コミット時にチェックを走らせたり、強制的に変換したい場合は、属性をつけると良い。

----

例えばこのリポジトリの場合、マークダウンファイルのエンコードはすべて「UTF-8」、改行コードは「LF」でそろえている。
属性は
```
*.md text working-tree-encoding=UTF-8 eol=lf
```
で設定している。


- `text` はテキストファイルであることを示す
- `working-tree-encoding=UTF-8` はエンコードが「UTF-8」であることを表してる
- `eol=lf` は改行コードが「LF」であることを表している



## See Also...
- [Existing Git repository with files in mixed encodings - Stack Overflow](https://stackoverflow.com/questions/59434963/existing-git-repository-with-files-in-mixed-encodings)
