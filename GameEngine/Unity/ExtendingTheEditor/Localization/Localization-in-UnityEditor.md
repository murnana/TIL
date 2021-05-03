# Unity エディタ拡張のローカライズ
[gettext](../../../../Localization/OSS/gettext/gettext.md)に似たシステムで、GUIの文字をローカライズ可能。

## HowTo

1. `.po` ファイルを作る (日本語なら`ja.po`とか)
2. Unityに読み込ませる
3. `.po`ファイルがあるアセンブリに`[assembly: UnityEditor.Localization.Editor.LocalizationAttribute]`を入れる ([UnityEditor.Localization.Editor.LocalizationAttribute])
4. `Localization.Tr()` でテキストを取得する ([UnityEditor.Localization.Editor.Localization.Tr(string)])


## See also...
- https://caitsithware.com/wordpress/archives/2227
- https://forum.unity.com/threads/localization-tooling-getting-locale-in-editor.852250


[UnityEditor.Localization.Editor.LocalizationAttribute]: https://docs.unity3d.com/ja/2019.4/ScriptReference/Localization.Editor.LocalizationAttribute.html
[UnityEditor.Localization.Editor.Localization.Tr(string)]: https://docs.unity3d.com/ja/2019.4/ScriptReference/Localization.Editor.Localization.html
