# svn checkout
http://jtdan.com/vcs/svn/svn-book/svn.ref.svn.c.checkout.html
Subversionのリポジトリをローカルからダウンロードするためのコマンド

## About
基本的には
```bash
svn checkout <リポジトリのURL>
```
で全部落ちてくる。

が、特定のリポジトリを落としたい場合はいくつか方法がある。

### 特定のリポジトリを落とす

<リポジトリのURL> の中の、<フォルダパス>だけを落としたい場合。
```
svn checkout <リポジトリのURL>/<フォルダパス>
```
とやると、<フォルダパス> をルートディレクトリとして落ちてくる。

```
svn checkout --depth empty <リポジトリのURL>
cd <落ちてきた場所>
svn update --set-depth infinity ./＜ファイルパス＞
```
とやると、どのリポジトリを参照するのかだけが落ちてきて、実際のファイルは落ちてこない。
