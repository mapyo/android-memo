# android-memo

## adb

### dumpsys

現在のActivity取得
```
adb shell dumpsys activity | grep -B 1 "Run #[0-9]*:"
```

### input

メールアドレス入力→エンター→パスワード
```
adb shell input text example@example.com; adb shell input keyevent 66; adb shell input text examplepass
```


## Coding Style
- https://github.com/cookpad/styleguide/blob/master/java.ja.md
- https://github.com/cookpad/android-code-style

