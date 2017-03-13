# android-memo

## adb

### am

特定のアプリを強制終了させる

```
adb shell am force-stop com.android.chrome
```

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

### pm

インストールされているパッケージ一覧
```
adb shell pm list package
```

### run-as
アプリ内のデータを見る

```
adb shell
adb run-as com.hoge # パッケージ名
```

### kill-server start-server
```
adb kill-server; adb start-server
```

## 便利ツール

- Vysor
 - https://chrome.google.com/webstore/detail/vysor/gidgenkbbabolejbgbpnhbimgjbffefm
 - http://hack-it-iron.hatenablog.com/entry/2015/09/25/164444

## Coding Style
- https://github.com/cookpad/styleguide/blob/master/java.ja.md
- https://github.com/cookpad/android-code-style

## tips

### 端末の横幅・高さを取得する

```
getResources().getDisplayMetrics().widthPixels
getResources().getDisplayMetrics().heightPixels
```

## gradle

### 署名情報の確認

```
./gradlew signingReport
```
