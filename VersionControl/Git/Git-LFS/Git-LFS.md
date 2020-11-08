# Git LFS (Git Large File Storage)
https://git-lfs.github.com/
[Git](./Git.md)で、大きなサイズのファイル (たとえば画像、サウンド、ビデオ)を管理するのに向いているツール

## About
[Git](./Git.md)はテキストベースのファイルをバージョン管理するには向いているが、バイナリファイルは差分を保存することがほぼ不可能です。

そのため、差分だけとっておこうと思っても、結局ファイルをフルで持つのと同義になってしまい、結果Gitリポジトリの容量がかなり膨らんでしまいます。

Git LFS では、指定したファイルを別のサーバーに上げて管理するようにします。

リモートリポジトリ側は、代わりに別のサーバーから持ってくるためのポインターとして、テキストベースのデータを入れます。

## How to Use

### Commandline

## コミット
1. `git lfs version` でGit LFSのバージョンを表示します。git lfsが見つからない場合はパスが通っていないか、インストールされていませんのでインストールをします。
2. ローカルに落としてきたリポジトリ上で `git lfs install` で初期化します。
3. git lfsで管理するファイルを `.gitattributes` に追加します
   1. コマンドで `git lfs track "*.psd"`
   2. `.gitattributes` に `*.psd filter=lfs diff=lfs merge=lfs -text` と書かれる
4. 対象ファイルと`.gitattributes` をコミットします
