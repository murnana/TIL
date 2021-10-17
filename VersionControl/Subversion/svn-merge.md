# Subversionでのマージ


## Step

1. 現在のリビジョンを取得 `svn log --stop-on-copy`
2. マージ `svn merge -r <作業コピーのリビジョン>:HEAD <マージ元パス>`
3. 競合内容がなければコミット `svn commit`

## See also
- http://cockatiel-cage.hateblo.jp/entry/2012/12/14/122449
- http://jtdan.com/vcs/subversion.bluegate.org/doc/re17.html
