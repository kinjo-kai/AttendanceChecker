AttendanceChecker
概要

AttendanceCheckerは、勤怠CSVファイルを読み込み、勤怠データのチェックを行うJava製デスクトップアプリケーションです。

出勤時刻の遅刻判定や入力不備の検出を行い、結果を画面表示およびCSVファイルとして出力できます。

未経験から開発エンジニアを目指す中で、Javaの基礎文法だけでなく、オブジェクト指向設計、ファイル入出力、GUI開発を学ぶことを目的として作成しました。

システム構成
パッケージ構成
App
├─ GuiMain.java
├─ Main.java

model
├─ Attendance.java
└─ CheckResult.java

service
├─ AttendanceCheckService.java
└─ SummaryService.java

util
├─ CsvUtil.java
├─ ConfigUtil.java
├─ EncodingUtil.java
├─ LoggerUtil.java
└─ PropertyUtil.java

view
├─ MainFrame.java
└─ ResultTableCellRenderer.java
主な機能
勤怠CSV読込
UTF-8対応
Shift-JIS対応
ヘッダー行スキップ
空行スキップ
列数チェック
勤怠チェック
社員ID未入力チェック
退勤時刻未入力チェック
出勤時刻フォーマットチェック
遅刻判定
結果表示
Swing GUI
JTableによる一覧表示
CSV出力
結果CSV出力
エラーCSV出力
集計CSV出力
集計機能

社員ごとに以下を集計します。

出勤日数
遅刻回数
エラー回数
ログ出力

java.util.loggingを利用してログを出力しています。

使用技術
Java
Swing
JTable
CSVファイル操作
Java Logging API
Git / GitHub
工夫した点
責務を分離した設計

以下のように役割ごとにクラスを分割しました。

model：データ保持
service：業務ロジック
util：共通処理
view：画面表示

保守性や拡張性を意識して設計しています。

設定ファイル化

遅刻判定時刻をconfig.propertiesで管理し、ソースコードを変更せず設定変更できるようにしました。

文字コード対応

実務ではUTF-8だけでなくShift-JISのCSVも扱うことがあるため、両方の文字コードに対応しました。

GUI化

当初はコマンドラインアプリとして作成しましたが、利用しやすさ向上のためSwingを利用してGUI化しました。

また、判定結果に応じて色分け表示を行い、視認性を向上させています。

今後の改善予定
JUnitによる単体テスト追加
ファイル保存先選択機能
月次勤怠集計機能
データベース連携
Spring Boot版への移行
実行画面

※ GUI画面のスクリーンショットを掲載予定

作者

Java開発エンジニアを目指して学習中。
実務では運用保守業務に従事しながら、Javaを中心に開発スキルを習得しています。
