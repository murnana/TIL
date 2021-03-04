# XCode Command line toolsがOS更新後に消える

## About
OSアップデート後にgitが行方不明になったときとかに怪しい。

```bash
xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing xcrun at: /Library/Developer/CommandLineTools/usr/bin/xcrun
```

Terminalから `xcode-select --install` をすると解決する。


## See also

https://stackoverflow.com/questions/52522565/git-is-not-working-after-macos-update-xcrun-error-invalid-active-developer-pa
