# ファイル構造解析: Space Panicco (PC-98, 1994)

本ドキュメントは、オリジナル配布物の解析に基づき、
Space Panicco のファイル構成を記述する。

---

## 概要

[Confirmed]

本プログラムは、実行ファイルと複数の外部データファイルで構成される。

確認されたファイル：

- PANIC.EXE
- PANIC.BGM
- PANIC.EFS
- PANIC.D32
- PANIC.DEF

---

## 実行ファイル

### PANIC.EXE

[Confirmed]

メイン実行ファイル。

内容：

- ゲームロジック
- 外部ファイル参照
- 著作権文字列

確認された文字列：

- "panic.bgm"
- "panic.efs"
- "panic.d32"
- "panic.def"

---

## 楽曲データ

### PANIC.BGM

[Confirmed]

テキスト形式の楽曲データ。

特徴：

- MML風記法
- 複数パート
- "*" による曲区切り
- ";" によるコメント

---

## 効果音データ

### PANIC.EFS

[Confirmed]

テキスト形式の効果音データ。

特徴：

- 数値列
- 各効果音は0で終端
- "effect 1"～"effect 5" のラベル

---

## グラフィックデータ

### PANIC.D32

[Confirmed]

実行ファイルから参照されている。

[Unknown]

- 内部フォーマット
- エンコード方式
- 解像度や構造

---

## 設定データ

### PANIC.DEF

[Confirmed]

実行ファイルから参照されている。

[Unknown]

- 内容詳細
- 設定・テーブル・メタデータのいずれか

---

## ファイルロードモデル

[Confirmed]

実行ファイルは以下のファイルを名前指定で参照する：

- panic.bgm
- panic.efs
- panic.d32
- panic.def

これはリソースが実行時に外部ファイルとして読み込まれる構造を示す。

---

## エラーハンドリング

[Confirmed]

実行ファイルには以下のエラーメッセージが存在する：

- "not open = panic.D32 !!"
- "not open = panic.def !!"

これは：

- 実行時にファイル存在チェックが行われる
- 欠損時に明示的エラーが出る

ことを示す。

---

## 機能分離

[Confirmed]

本プログラムは機能ごとにファイルが分離されている：

| 機能 | ファイル |
|------|----------|
| プログラム本体 | PANIC.EXE |
| 音楽 | PANIC.BGM |
| 効果音 | PANIC.EFS |
| グラフィック | PANIC.D32 |
| 設定 | PANIC.DEF |

---

## 結論

[Confirmed]

Space Panicco は以下の特徴を持つ構造である：

- 実行ファイルが制御を担当
- 各種リソースは外部ファイルとして分離
- 実行時にファイルロードを行うモジュラー構造
