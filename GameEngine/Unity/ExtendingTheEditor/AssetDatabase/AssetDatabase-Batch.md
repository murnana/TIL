# AssetDataaseのバッチ処理
https://docs.unity3d.com/ja/current/Manual/AssetDatabaseBatching.html

[AssetDatabase.StartAssetEditing()]と[AssetDatabase.StopAssetEditing()] で囲む処理のこと。

## About
`AssetDatabase` 関連の処理は1つ1つを実行すると時間がかかる。そのため、大量のアセットデータを扱う時はバッチ処理を行うことで高速化を図る。

[AssetDatabase.StartAssetEditing()]と[AssetDatabase.StopAssetEditing()]の中にある処理は、[AssetDatabase.StopAssetEditing()]でまとめて処理が行われる。使い方は以下の通り:

```cs
AssetDatabase.StartAssetEditing();
try {
  // AssetDatabase関連の処理
} finally {
  AssetDatabase.StopAssetEditing();
}
```

[AssetDatabase.StartAssetEditing()]の後で例外が発生しても、必ず[AssetDatabase.StopAssetEditing()]が呼ばれる形にする。そうでないと
Unityソフトウェアが固まったままになる。


[AssetDatabase.StartAssetEditing()]: https://docs.unity3d.com/ja/current/ScriptReference/AssetDatabase.StartAssetEditing.html
[AssetDatabase.StopAssetEditing()]: https://docs.unity3d.com/ja/current/ScriptReference/AssetDatabase.StopAssetEditing.html
