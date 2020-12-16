# `AssetDatabase` でのリネーム
https://docs.unity3d.com/ja/current/ScriptReference/AssetDatabase.RenameAsset.html  
ファイル名の変更だけなら `AssetDatabase.RenameAsset(string, string)` が便利。

## Example
`Assets/SomeFolder/Foo.png` を `Assets/SomeFolder/Bar.png` に変更

```cs
using UnityEditor;
// ...

AssetDatabase.RenameAsset(pathName: "Assets/SomeFolder/Foo.png", newName: "Bar");
```

## See also...
- https://baba-s.hatenablog.com/entry/2019/02/11/193000
  