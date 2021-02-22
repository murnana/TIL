# `svn:needs-lock'
編集時にロックを強制します


## About
プロパティの設定:
```
svn propset svn:needs-lock true <ファイルパス>
```

プロパティの削除:
```
svn propdel svn:needs-lock -R -q <ファイルパス>
```


## See also...
- [ロック](https://tortoisesvn.net/docs/release/TortoiseSVN_ja/tsvn-dug-locking.html) - TotoiseSVN
- [Locking](http://svnbook.red-bean.com/en/1.8/svn.advanced.locking.html) - Svnbook
- [Subversionの属性の使い方～基本的な操作・ファイルの無視・ロック～ | バージョン管理システム入門(初心者向け)](https://tracpath.com/bootcamp/learning_subversion_tutorial2.html)

