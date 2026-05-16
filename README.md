# AttendanceChecker

## 概要
勤怠CSVファイルを読み込み、
出勤・遅刻・エラーチェックを行い、
結果CSV・エラーCSVを出力するJavaアプリケーションです。

## 使用技術
- Java
- Eclipse
- Git / GitHub
- CSVファイル処理
- Logger
- Properties設定ファイル

## 主な機能
- 勤怠CSV読込
- 出勤判定
- 遅刻判定
- エラーチェック
- 結果CSV出力
- エラーCSV出力
- ログ出力

## 実行方法

```bash
java -jar attendance.jar attendance.csv error.csv
```

## 入力CSV例

```csv
社員ID,日付,出勤時刻,備考
1001,2025-01-01,08:55,
1002,2025-01-01,09:10,
```

## 出力ファイル
- result_attendance.csv
- error_attendance.csv
- application.log

## ディレクトリ構成

```text
src/
 ┣ App/
 ┣ model/
 ┣ service/
 ┗ util/
```

## 工夫した点
- クラス分割による保守性向上
- Loggerによるログ管理
- CSV入出力の共通化
- エラー時終了コード対応

## 今後の改善点
- JUnitテスト追加
- GUI化
- リファクタリング
- 集計機能改善
