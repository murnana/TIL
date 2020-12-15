# `SerializedProperty.isExpanded`
https://docs.unity3d.com/ja/current/ScriptReference/SerializedProperty-isExpanded.html

## About

`PropertyDrawer`を作るときにお世話になる。

プロパティの表示を展開する場合は`true`、畳む場合は`false`となる。

```cs
// property = SerializedProperty
property.isExpanded = EditorGUI.Foldout(
    position: , // ラベルの範囲
    foldout: property.isExpanded,
    content: // ラベル
);
if (property.isExpanded) {
    // 展開後の描画処理
}
```
