# Package内にあるテストを実行するには
`manifest.json` に ` "testables": ["com.unity.some-package"]`を追加するだけ

## About
パッケージ内のテストスクリプトは、通常Unity Runnerで実行することができません。
そのため、`manifest.json`に`testables`を追加する必要があります。

```json
{
  "dependencies": {
    "com.unity.some-package": "1.0.0",
    "com.unity.other-package": "2.0.0",
    "com.unity.yet-another-package": "3.0.0",
  },
  "testables": ["com.unity.some-package", "com.unity.other-package"]
}
```

## Seealso
https://docs.unity3d.com/Manual/cus-tests.html#tests
https://docs.unity3d.com/Manual/upm-manifestPrj.html#testables
