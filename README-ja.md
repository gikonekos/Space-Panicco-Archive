# Space Panicco Archive

PC-98用アクションゲーム  
**Space Panicco（すぺーす ぱにっ娘）** の歴史的アーカイブです。

初公開は **1994年** です。

このリポジトリは、**オリジナル作者の一人** によって作成されました。

このリポジトリは、当時の配布ファイル、ドキュメント、ディスクイメージ、
および関連する実行環境を、歴史保存およびアーカイブ目的で保管しています。

---

## スクリーンショット

| Round 1 | Round 2 |
|--------|--------|
| ![Round 1](screenshots/panicco_round01.png) | ![Round 2](screenshots/panicco_round02.png) |
| Neko Project II x64<br>MS-DOS 3.30 | Neko Project 21/W x64<br>MS-DOS 6.20 |

異なる2種類の PC-98 エミュレータ環境上で動作している本作のスクリーンショットです。

## 実プレイ動画

YouTube:  
https://youtu.be/8eCXOkeMTiQ?si=NoKIfhCUnl9IO7mv

私による検証動画です。

Part 1:  
https://youtu.be/C4Pq5myM1MM?si=iI2zo26VY3TZ-VxH

Part 2:  
https://youtu.be/358hQeHvXBA?si=HKnguAuyYuJ1Zfxx

Part 2 には、DEFファイル編集、20面からの続きプレイ、および 32 面が最終面であることの確認が含まれています。

## Space Panicco マップエディタ / ステージデータ作業ログ

ブラウザベースのマップエディタと、ステージデータ編集作業を紹介するライブ作業ログです。

https://www.youtube.com/live/grgZ0_BMUdI?si=731Cmi7v9VpSJQHv

---

## ツール

- [VMAP Editor](https://gikonekos.github.io/Space-Panicco-Archive/tools/map-editor/)  
  Space Panicco の VMAP ファイル用ブラウザベースエディタ

- [How to use the VMAP Editor](https://github.com/gikonekos/Space-Panicco-Archive/blob/main/docs/tools/map-editor/README.md)  
  使用方法とファイル形式の概要

---

## ゲームについて

Space Panicco は、**Space Panic に着想を得たプラットフォームアクションゲーム** です。

プレイヤーは穴を掘り、敵を落とし、攻撃を避けながら各ラウンドを攻略していきます。

本作は **NEC PC-9801 シリーズ** 向けに開発され、**MS-DOS** 上で動作します。

---

## ゲームクレジット

- 企画・グラフィック・音楽: **基 建吉**
- プログラム: **芸夢 職人**

---

## サードパーティコンポーネント

本プログラムは、以下のサードパーティ製ソフトウェアを使用している、またはこれらを用いて構築されています。

### コンパイラ

- **Borland Turbo C**  
  Copyright (c) 1987–1988 Borland International

### BGM ライブラリ

- **BGM Library ver1.12**  
  Copyright (c) 1989–1993 Fumitake Yodo / STUDIO FEMY

### ユーティリティライブラリ

- **master.lib Version 0.21**  
  Copyright (c) 1993 Akihiko Koizuka, Kazumi

### 同梱 DOS 環境

- **FreeDOS(98) ベースの DOS 環境**  
  PC-98 での実行およびテスト用として、起動可能な DOS 環境が同梱されています。

同梱の起動環境では、以下のようなコンポーネントに関する表示が行われます。

- **FreeDOS(98) kernel**
  - Copyright 1995–2022 Pasquale J. Villani and The FreeDOS Project
  - Copyright 2001–2022 FreeDOS(98) porting project
  - GNU General Public License, version 2 or later
  - Absolutely no warranty

- **FreeDOS XMS-Driver for 80286**
  - Copyright 1995 Till Gerken
  - Copyright 2001–2005 Martin Stromberg
  - Copyright 2016 sava

- **FreeCOM ver 0.85a_DBCS (PC-98)**

サードパーティコンポーネントに関するすべての権利は、それぞれの著作権者に帰属します。

詳細は以下を参照してください。

- [RIGHTS.md](RIGHTS.md)
- [RIGHTS_ja.md](RIGHTS_ja.md)
- [docs/FREEDOS98-LICENSE-NOTES.md](docs/FREEDOS98-LICENSE-NOTES.md)

---

## 配布履歴

本作は **1994年** に、日本語フリーソフトとして PC-9801 DOS 向けに公開されました。

このリポジトリに収録されている資料は、その歴史的配布物と関連文書を保存するものです。

---

## Internet Archive

保存されたコピーは、以下でも公開しています。

- [Internet Archive](https://archive.org/details/space-panicco)

---

## リポジトリ構成

- `original/` — 当時の配布アーカイブファイルおよびディスクイメージ
- `extracted/` — 元アーカイブから展開した内容
- `docs/` — ドキュメント、マニュアル、ライセンス注記、関連メモ
- `screenshots/` — ゲームのスクリーンショット
- `environment/` — エミュレータおよび実行環境関連ファイルとメモ
- `analysis/` — 保存・解析・リバースエンジニアリング関連メモ

---

## オリジナル配布物

`original/` ディレクトリには、**Space Panicco** の当時の配布ファイルを保存しています。

これらのファイルは、歴史保存およびアーカイブ目的で保管されています。

内容には以下が含まれます。

- 当時のアーカイブパッケージ
- ディスクイメージ

展開済みファイルは `extracted/` ディレクトリに分けて保存しています。

解析、改変、再整理した資料は、`original/` の外側に置くべきものとしています。

---

## 動作要件

- NEC PC-9801 シリーズ互換環境
- MS-DOS または互換性のある PC-98 DOS 環境
- フロッピーディスクイメージ、または元パッケージから展開したファイル群

---

## エミュレータ

本作は、以下のような PC-98 エミュレータで動作します。

- Neko Project II
- Neko Project 21/W

---

## 動作確認済み環境

以下の環境で動作確認を行っています。

- **Neko Project II x64** + **MS-DOS 3.30**
- **Neko Project 21/W x64** + **MS-DOS 6.20**
- **Neko Project II x64** + 同梱の **FreeDOS(98) ベース起動ディスク**

---

## 実行方法

1. PC-98 エミュレータ環境を用意する  
2. 保存済み DOS イメージ、または同梱の FreeDOS(98) ベース起動ディスクを起動する  
3. ディスクイメージをマウントするか、展開済みゲームファイルを開く  
4. メイン実行ファイルを起動する  

詳細は以下を参照してください。

- [Running the Game](docs/Running-the-Game.md)
- [Running the Game (Japanese)](docs/Running-the-Game_ja.md)

---

## ディスクイメージ形式

収録されているフロッピーディスクイメージは、歴史資料として元の形式のまま保存しています。

現代のエミュレータ環境で実行しやすくするため、補助的な便宜用イメージが追加されている場合があります。

---

## 音響システム

本作は通常プレイ中のサウンドに、PC-98 本体内蔵スピーカー（BEEP）を使用します。

音楽関連機能には、当時のソフトウェア環境におけるサードパーティ製ライブラリが利用されています。

---

## ステージデータ

ステージグラフィックおよびゲームプレイ用データは、オリジナルのゲームリソースの一部として保存されています。

### 追加ステージファイル

ブラウザベースの **VMAP エディタ** を用いて、追加のステージデータセット（**VMAP033.DAT–VMAP064.DAT**）を構成しました。  
一部のステージは、エミュレータ上でも検証を行い、テスト後に手動で調整しています。

- [VMAP Editor](https://gikonekos.github.io/Space-Panicco-Archive/tools/map-editor/)
- [Guide](docs/tools/map-editor/README.md)
- [VMAP033–VMAP064](analysis/work/maps/panicco-33-64.zip)

---

## ドキュメント

追加ドキュメントは `docs/` ディレクトリに収録されています。

内容には以下が含まれます。

- オリジナルマニュアル本文
- 日本語メモ
- 英語メモ
- 実行手順
- FreeDOS(98) ライセンス注記

---

## 権利について

このリポジトリは、1994年公開のフリーソフトゲーム *Space Panicco* の歴史的アーカイブです。

オリジナルゲーム本体および当時の配布資料の著作権は、引き続き元の権利者に帰属します。

GitHub 上で公開されていることは、オリジナルゲームがオープンソース化されたことを意味しません。

個人利用、プレイ、保存、共有、非商用利用は歓迎します。

営利目的での再配布や再パッケージ化は、本アーカイブの趣旨ではありません。

また、このリポジトリには、保存・研究目的の解析およびリバースエンジニアリング資料が含まれる場合がありますが、それらはオリジナルゲームの著作権状態を変更するものではありません。

詳細は以下を参照してください。

- [RIGHTS.md](RIGHTS.md)
- [RIGHTS_ja.md](RIGHTS_ja.md)

---

## 連絡先

このアーカイブに関する歴史的情報については、リポジトリ所有者のプロフィールおよび関連アーカイブノートを参照してください。

---

## 免責事項

このリポジトリは、歴史保存およびアーカイブ目的で提供されています。

現代のシステム、エミュレータ、DOS 環境、あるいは同梱の便宜用起動イメージに対する互換性は保証されません。

---

## 謝辞

歴史的な日本製 PC ソフトウェアの保存と記録に協力してくださった皆様に感謝します。
