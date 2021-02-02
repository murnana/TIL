# PresetにしたくないMonoBehaviourやScriptableObjectの設定
`UnityEngine.ExcludeFromPresetAttribute` を使います

## About
`UnityEngine.Timeline.TimelineAsset` のように、Presetにならないアセットがたまにある。
あるいは、Presetにしたくないもの (プロジェクトの設定ファイルとか) がある場合、クラスに属性である　`UnityEngine.ExcludeFromPresetAttribute` をつけてあげると良い。


## See also...
- [Unity - Scripting API: ExcludeFromPresetAttribute](https://docs.unity3d.com/ScriptReference/ExcludeFromPresetAttribute.html)
