# BGMシステム解析: Space Panicco (PC-98, 1994)

本ドキュメントは、バイナリ解析およびドキュメント照合に基づき、
*Space Panicco* におけるサウンドシステムを記述する。

---

## 概要

[Confirmed]

本作のサウンドシステムは、PCスピーカを用いたソフトウェア音源である。

実行ファイルには以下の文字列が確認されている：

- "BGM Library ver1.12 use TIMER interrupt"

これはタイマ割り込み駆動のBGMシステムであることを示す。

---

## 構成要素

[Confirmed]

以下のコンポーネントが関与している：

- BGM Library ver1.12
- master.lib Version 0.21

ドキュメントより、bgmlib は version 0.22 以降で master.lib に統合されている。
したがって、version 0.21 は統合前の状態である。

---

## BGMデータ形式

[Confirmed]

`PANIC.BGM` はテキスト形式の楽曲データである。

内容は bgmlib の MMLサブセット仕様と一致する。

確認された特徴：

- 音階：A～G
- 音長指定：数値（例：4, 8, 16）
- テンポ指定：T
- オクターブ：O, <, >
- 休符：R
- パート区切り：","
- 最大3パート構成
- 曲区切り："*"

---

## 効果音データ形式

[Confirmed]

`PANIC.EFS` はテキスト形式の効果音データである。

確認された特徴：

- 数値列
- 0で終端
- "effect 1"～"effect 5" のラベル

ドキュメントより：

- 各値は出力周波数を表す
- 4ms単位で処理される

---

## 再生モデル

[Confirmed]

ドキュメントおよびバイナリ文字列より：

- 再生はタイマ割り込みで駆動される
- BGMと効果音は同一の出力（PCスピーカ）を共有する
- BGMはMML形式で定義される
- 効果音は周波数列で定義される

---

## API構造

[Confirmed]

master.man に以下のAPIが記載されている：

- bgm_init
- bgm_read_data
- bgm_read_sdata
- bgm_start_play
- bgm_select_music
- bgm_sound
- bgm_stop_play
- bgm_finish

---

## データロード

[Confirmed]

実行ファイルには以下の参照が存在する：

- "panic.bgm"
- "panic.efs"

これは外部ファイルとしてBGMおよび効果音が読み込まれることを示す。

---

## 結論

[Confirmed]

Space Panicco のサウンドシステムは：

- BGM Library ver1.12 を使用
- master.lib 0.21 と組み合わせて動作
- 楽曲はテキスト形式MMLで定義
- 効果音は周波数列で定義
- PCスピーカをタイマ割り込みで駆動する
