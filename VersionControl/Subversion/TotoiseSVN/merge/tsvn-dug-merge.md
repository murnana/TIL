# コンフリクトの解決

TotoiseSVNでマージ作業をすると、たまにコンフリクトを解決しなければならないことがある。

https://tortoisesvn.net/docs/release/TortoiseSVN_en/tsvn-dug-merge.html


TotoiseSVNで用意されている、コンフリクト解消手段はこれらになる。


### Postpone
今は競合を解決しない。

### Accept base
ローカルの状態を正とする

### Accept incoming
ローカルを破棄し、マージソースのファイルを使う

### Reject incoming
ローカルの変更を正とする

### Accept incoming for conflicts
マージソースとローカルの変更が競合した場合、
マージソースと競合するローカルの変更だけ破棄->マージソース適用
競合しなかったローカルの変更は適用

### Reject conflicts
マージソースとローカルの変更が競合した場合、
マージソースからの変更が破棄 -> ローカルの変更を適用
競合しなかったマージソースとローカルの変更はすべて保持される

### Mark as resolved
競合を解決済みとしてマークする

### Edit
マージエディタを開いて編集する
