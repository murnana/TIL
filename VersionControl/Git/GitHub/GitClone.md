# git clone
リポジトリをローカルにコピーすること。  
ここでは、GitHubからのcloneについて説明する。

- https://docs.github.com/ja/free-pro-team@latest/github/using-git/which-remote-url-should-i-use


## HTTPS vs SSH
GitHubでは、HTTPSとPersonal access token (PAT)でのクローンを推奨している。

- https://docs.github.com/ja/free-pro-team@latest/github/getting-started-with-github/set-up-git

## HTTPSでのクローン

### from Private repository
古いのかな・・・？
```bash
git clone https://<ユーザ名>@github.com/foo/bar.git
```

- [https時代のgitアカウントを使い分ける方法 - Qiita](https://qiita.com/1natsu172/items/a4a3357a0481440ec6a5)

