# ライセンス調査: Space Panicco (PC-98, 1994)

本ドキュメントは、*Space Panicco* に使用されているサードパーティ製ライブラリの調査および、
ライセンス表記の明確化についてまとめたものである。

---

## 背景

本アーカイブプロジェクトの公開にあたり、ドキュメント内のライセンス表記が不十分であるとの指摘があった。

この指摘は、master.lib の作者の一人である以下の人物によってなされた：

- Akihiko Koizuka (戀塚昭彦)

このフィードバックを契機として、オリジナル実行ファイルに含まれるコンポーネントの詳細調査を実施した。

---

## きっかけ

[Testimony]

Akihiko Koizuka による公開コメント：

> 「ライセンス表記が不十分」

この発言は、当時のライブラリエコシステムに直接関与した人物による一次的証言として扱う。

---

## 調査方法

[Confirmed]

以下の資料を使用した：

- 実行ファイル: `PANIC.EXE`
- データファイル: `PANIC.BGM`, `PANIC.EFS`
- ドキュメント: `master.man`, `BGM / EFS マニュアル`
- 関連ライブラリ資料（master.lib, bgmlib）

実施した解析：

- バイナリからの文字列抽出
- データ形式と仕様書の照合
- マニュアルに基づくAPI構造の確認

---

## 調査結果

### 1. コンパイラ

[Confirmed]

実行ファイルから確認された文字列：

- "Turbo-C - Copyright (c) 1988 Borland Intl."
- "Copyright (c) 1987,1988 Borland International"

結論：

- 本プログラムは **Borland Turbo C** によりビルドされている

---

### 2. BGMライブラリ

[Confirmed]

実行ファイルから確認された文字列：

- "BGM Library ver1.12 use TIMER interrupt"
- "Copyright(C)1989-93 Fumitake Yodo and studiofemy"

結論：

- 本プログラムは **BGM Library ver1.12** を使用している
- 作者: Fumitake Yodo / STUDIO FEMY

---

### 3. master.lib

[Confirmed]

実行ファイルから確認された文字列：

- "MASTERM.LIB Version 0.21"
- "Copyright (c)1993 A.Koizuka,Kazumi"

ドキュメントより：

- master.lib 0.21（統合前バージョン）
- bgmlib は version 0.22 以降で統合

結論：

- Space Panicco は **master.lib 0.21（統合前）** を使用している

---

### 4. BGM / EFS システム

[Confirmed]

- `PANIC.BGM` は bgmlib の MML サブセット仕様と一致
- `PANIC.EFS` は bgmlib の EFS仕様（4ms単位の周波数列）と一致

ドキュメント対応：

- 「BGM / EFS マニュアル（bgmlib.man ベース）」

結論：

- サウンドシステムは **bgmlib仕様と整合する**

---

## ライセンス表記の問題

[Confirmed]

- 実行ファイル内には著作権表記が存在する
- しかし現代のドキュメントには十分に反映されていなかった

[Testimony]

- ライセンス表記の不足は、Akihiko Koizuka により明示的に指摘された

---

## 対応

[Confirmed]

本調査に基づき：

- 使用されているサードパーティコンポーネントを特定
- README において適切なクレジットを追加

現在、以下のコンポーネントが明示的に記載されている：

- Borland Turbo C
- BGM Library ver1.12 (Fumitake Yodo / STUDIO FEMY)
- master.lib 0.21 (Akihiko Koizuka, Kazumi)

---

## 確実性について

- 技術的な結論はすべてバイナリおよびドキュメントに基づく
- 証言は明確に区別し、単独の根拠とはしていない
- 検証可能な情報以外の推定は行っていない

---

## 結論

本調査により、Space Panicco が複数のサードパーティコンポーネントに依存していること、
および適切なライセンス表記が必要であることが確認された。

また、Akihiko Koizuka による指摘は、ライセンス表記の不備を是正する直接の契機となった。
