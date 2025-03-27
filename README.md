# はじめに

PowershellとBoxCLIを用いた検証用リポジトリ。

# フォルダ構成

以下の構成で作成する

```
ルートディレクトリ
└メイン1（エントリーポイント）.ps1　 ：　実際にコマンドラインから直接実行する関数
└メイン2（エントリーポイント）.ps1　 ：　　　　　　　　　〃
...
functions
  └関数1.ps1　：　共通処理をまとめた関数がまとめられたファイル
  └関数2.ps1
...

└Config.ps1　　：設定値がまとめられたファイル（DB接続情報など）
```

# 命名規則

- ファイル名はキャメルケースとする
  例：
  ◯`Get-Folder.ps1`
  ✗`get_older.ps1`

- 「メイン（エントリーポイント）」のファイル名は、`Main-XXX.ps1`とすること
  例：`Main-CreateFolder`

- 関数のファイル名は`XXXUtils.ps1`とすること
  例：
  `FileUtils.ps1`
  `UserUtils.ps1`

- 関数名（ファイル名ではなく）は`動詞+名詞`を用いること
  例：

  ```powershell
  functions Get-CommonFolder {
    〜
  }
  ```

  ```powershell
  functions Get-AdministratorFolder {
    〜
  }
  ```
