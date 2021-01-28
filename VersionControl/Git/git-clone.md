# git-clone
リポジトリのコピー

## About
リモートリポジトリから自分の手元にコピーしたいときに使うコマンド。
`git clone <url>` が基本だが、それ以外にもオプションをつけられる。

> - `git clone --filter=blob:none <url>` は ブロブレスクローン を作成します。このクローンは、到達可能なすべてのコミットとツリーをダウンロードする一方、ブロブは必要に応じて取得します。このクローンは、開発者や複数回ビルドを実行するようなビルド環境に最適です。
> 
> - `git clone --filter=tree:0 <url>` は ツリーレスクローン を作成します。このクローンは、到達可能なすべてのコミットをダウンロードする一方、ツリーとブロブは必要に応じて取得します。このクローンは、一度ビルドを実行した後に削除される予定で、コミット履歴にはアクセスしたいというビルド環境に最適です。
> 
> - `git clone --depth=1 <url>` は シャロークローン を作成します。このクローンはコミット履歴を切り捨ててクローンのサイズを小さくします。これによって、想定外の問題を引き起こしたり、利用可能な Git コマンドが制限されます。また、このクローンは後からのフェッチに過度のストレスを与えることになるので、開発者が使用することは強くお勧めしません。一度ビルドした後にリポジトリを削除するビルド環境では便利です。
> 
> [パーシャルクローンとシャロークローンを活用しよう - GitHubブログ](https://github.blog/jp/2021-01-13-get-up-to-speed-with-partial-clone-and-shallow-clone/)



### ブランチを指定してクローン

```bash
git clone --branch <branch> <repo>
```
`<branch>` はリモートブランチ名 (originは要らない).
`<repo>` はリモートリポジトリへのURL.




## See also..
- [パーシャルクローンとシャロークローンを活用しよう - GitHubブログ](https://github.blog/jp/2021-01-13-get-up-to-speed-with-partial-clone-and-shallow-clone/)
- [Get up to speed with partial clone and shallow clone - The GitHub Blog](https://github.blog/2020-12-21-get-up-to-speed-with-partial-clone-and-shallow-clone/)
- [Git clone: a data-driven study on cloning behaviors - The GitHub Blog](https://github.blog/2020-12-22-git-clone-a-data-driven-study-on-cloning-behaviors/)
- [リモートから特定のブランチを指定してcloneする - Qiita](https://qiita.com/icoxfog417/items/5776e0f0f758f0f0e48a)
