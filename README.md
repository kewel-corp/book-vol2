# 『医療診断支援AI開発　第2巻　応用編 ― 本格実装から臨床導入まで』 ― コードとノートブック

書籍『**医療診断支援AI開発　第2巻　応用編 ― 本格実装から臨床導入まで**』（『医療診断支援AI開発』全2巻の第2巻　応用編）のノートブックとコードを置いています。

**紙面のコードは「読んで理解するため」のもの、ここのノートブックは「動かすため」のものです。**
紙面から書き写したり、電子版から貼り付けたりすると、行の折り返しや記号の変換で崩れることがあります。
動かすときは、必ずここから取得してください。

---

## この巻の位置づけ

AIを**本格開発し**、そして**届ける** ― 第I〜III部（第1〜26章）は本格的な開発環境、性能の高いモデルを作るための開発手法、臨床領域ごとの実装、第IV〜VI部（第27〜63章）はデプロイ、標準化、薬機法・SaMD、臨床導入、運用、規制・倫理まで。第1〜63章。

## ディレクトリ

```
book-vol2/
├── notebooks/          ← 章ごとのノートブック（chNN_*.ipynb）
│   ├── ch03_wsl2_docker.ipynb
│   ├── ch25_pancreas_e2e.ipynb   ← 膵がん検出のE2E
│   ├── ch31_evaluation_xai.ipynb
│   ├── ch32_export_deploy.ipynb   ← 軽量化と書き出し
│   └── ...
├── code/               ← 章をまたいで使う共通コード（Dataset、損失関数、評価指標など）
│   ├── datasets.py
│   ├── losses.py
│   └── metrics.py
├── tests/              ← code/ の単体テスト（臨床ロジックを守る）
├── requirements.txt    ← ライブラリのバージョン固定
├── data/               ← 公開データの入手先だけ（データ本体は置かない）
├── README.md           ← 使い方（まずここを読む）
└── errata.md           ← 正誤表・更新情報
```

本の各章の冒頭に「**この章のコード**」として、その章のノートブックのファイル名を記載しています。

## 章ごとのノートブック

「Open in Colab」のバッジを押すと、そのノートブックが Google Colab で開きます（Google アカウントが要ります）。ノートブックの中は、本文の節の見出しの順に、紙面のコードが並んでいます。

| 章 | 題 | ノートブック | Colab で開く |
|---|---|---|---|
| 第2章 | Linuxの基礎 | [`notebooks/ch02_code.ipynb`](notebooks/ch02_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch02_code.ipynb) |
| 第3章 | WindowsでのAI開発環境構築：WSL2とDocker | [`notebooks/ch03_wsl2_docker.ipynb`](notebooks/ch03_wsl2_docker.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch03_wsl2_docker.ipynb) |
| 第4章 | Python実行環境とパッケージ管理：「動く環境」を自分で作る | [`notebooks/ch04_code.ipynb`](notebooks/ch04_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch04_code.ipynb) |
| 第5章 | GPUとCUDA、コンテナ運用 | [`notebooks/ch05_code.ipynb`](notebooks/ch05_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch05_code.ipynb) |
| 第6章 | 学習設定の要点：最適化・初期化・正規化・正則化 | [`notebooks/ch06_code.ipynb`](notebooks/ch06_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch06_code.ipynb) |
| 第7章 | ベースラインとアブレーション：何が性能を上げているかを確かめる | [`notebooks/ch07_code.ipynb`](notebooks/ch07_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch07_code.ipynb) |
| 第8章 | クラス不均衡への対処：サンプリングと hard example mining | [`notebooks/ch08_imbalance.ipynb`](notebooks/ch08_imbalance.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch08_imbalance.ipynb) |
| 第10章 | 学習曲線を読む：損失と指標から学習状態を確認する | [`notebooks/ch10_code.ipynb`](notebooks/ch10_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch10_code.ipynb) |
| 第11章 | 閾値と運用点の決め方：臨床に合わせて調整する | [`notebooks/ch11_code.ipynb`](notebooks/ch11_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch11_code.ipynb) |
| 第12章 | 不確実性と棄却を実装する：判定を保留し、医師に確認を依頼する | [`notebooks/ch12_code.ipynb`](notebooks/ch12_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch12_code.ipynb) |
| 第14章 | 前処理パイプラインの実装：入力画像から学習用のテンソルまで | [`notebooks/ch14_code.ipynb`](notebooks/ch14_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch14_code.ipynb) |
| 第16章 | 少ないデータを補う：データ拡張・自己教師あり学習・合成データ | [`notebooks/ch16_code.ipynb`](notebooks/ch16_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch16_code.ipynb) |
| 第17章 | 学習が期待どおりに進まないとき：デバッグと実践的な落とし穴 | [`notebooks/ch17_code.ipynb`](notebooks/ch17_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch17_code.ipynb) |
| 第18章 | アンサンブルと不確実性：複数モデルで性能と頑健性を高める | [`notebooks/ch18_code.ipynb`](notebooks/ch18_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch18_code.ipynb) |
| 第19章 | ハイパーパラメータ最適化と実験管理 | [`notebooks/ch19_code.ipynb`](notebooks/ch19_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch19_code.ipynb) |
| 第20章 | 眼科①：眼底写真と糖尿病網膜症 | [`notebooks/ch20_code.ipynb`](notebooks/ch20_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch20_code.ipynb) |
| 第21章 | 眼科②：OCTと層構造ガイド型AI | [`notebooks/ch21_code.ipynb`](notebooks/ch21_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch21_code.ipynb) |
| 第22章 | 整形外科：X線骨折診断 | [`notebooks/ch22_code.ipynb`](notebooks/ch22_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch22_code.ipynb) |
| 第24章 | 消化器：CT肝胆膵の統合セグメンテーションと腫瘍検出 | [`notebooks/ch24_code.ipynb`](notebooks/ch24_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch24_code.ipynb) |
| 第25章 | CT膵がん検出パイプラインを最初から最後まで組む | [`notebooks/ch25_pancreas_e2e.ipynb`](notebooks/ch25_pancreas_e2e.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch25_pancreas_e2e.ipynb) |
| 第26章 | 領域を広げる：びまん性肺疾患・大腸・甲状腺・心臓CT | [`notebooks/ch26_code.ipynb`](notebooks/ch26_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch26_code.ipynb) |
| 第28章 | チーム開発とコードの再現性：Git/GitHub・レビュー・CI | [`notebooks/ch28_code.ipynb`](notebooks/ch28_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch28_code.ipynb) |
| 第29章 | データセットの構築とキュレーション：AI開発の基盤を作る | [`notebooks/ch29_code.ipynb`](notebooks/ch29_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch29_code.ipynb) |
| 第30章 | アノテーションとデータマネジメント | [`notebooks/ch30_code.ipynb`](notebooks/ch30_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch30_code.ipynb) |
| 第31章 | 評価・検証と説明可能性 | [`notebooks/ch31_evaluation_xai.ipynb`](notebooks/ch31_evaluation_xai.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch31_evaluation_xai.ipynb) |
| 第32章 | モデルを現場に届ける：軽量化・書き出し・推論の最適化 | [`notebooks/ch32_export_deploy.ipynb`](notebooks/ch32_export_deploy.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch32_export_deploy.ipynb) |
| 第34章 | 標準化と相互運用性：病院システムとつなぐ | [`notebooks/ch34_code.ipynb`](notebooks/ch34_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch34_code.ipynb) |
| 第35章 | 薬機法・SaMDと社会実装 | [`notebooks/ch35_code.ipynb`](notebooks/ch35_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch35_code.ipynb) |
| 第38章 | フェデレーテッドラーニング：データを動かさずに学ぶ | [`notebooks/ch38_code.ipynb`](notebooks/ch38_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch38_code.ipynb) |
| 第39章 | 生成AIと大規模言語モデルの医療応用 | [`notebooks/ch39_code.ipynb`](notebooks/ch39_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch39_code.ipynb) |
| 第40章 | マルチモーダル医療AI：画像と臨床情報を統合する | [`notebooks/ch40_code.ipynb`](notebooks/ch40_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch40_code.ipynb) |
| 第41章 | 分布外検出と安全な棄却：「モデルの対象外の画像」を見分ける | [`notebooks/ch41_code.ipynb`](notebooks/ch41_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch41_code.ipynb) |
| 第42章 | 敵対的頑健性：AIを誤らせる入力と、その対策 | [`notebooks/ch42_code.ipynb`](notebooks/ch42_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch42_code.ipynb) |
| 第43章 | セグメンテーション結果の定量化と後処理 | [`notebooks/ch43_code.ipynb`](notebooks/ch43_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch43_code.ipynb) |
| 第44章 | 医療AIのインフラ：クラウドとオンプレミス | [`notebooks/ch44_code.ipynb`](notebooks/ch44_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch44_code.ipynb) |
| 第46章 | 画像品質とアーチファクト：「品質に問題のある画像」をどう扱うか | [`notebooks/ch46_code.ipynb`](notebooks/ch46_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch46_code.ipynb) |
| 第48章 | モデルのライフサイクル管理：版を、確実に扱う | [`notebooks/ch48_code.ipynb`](notebooks/ch48_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch48_code.ipynb) |
| 第50章 | 説明可能性の手法と、その落とし穴 | [`notebooks/ch50_code.ipynb`](notebooks/ch50_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch50_code.ipynb) |
| 第51章 | 経過観察と時系列のAI：「変化」を捉える | [`notebooks/ch51_code.ipynb`](notebooks/ch51_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch51_code.ipynb) |
| 第52章 | 医療AIのための統計の基礎：評価結果を正しく伝える | [`notebooks/ch52_code.ipynb`](notebooks/ch52_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch52_code.ipynb) |
| 第53章 | ドメイン適応：施設・装置の違いを乗り越える | [`notebooks/ch53_code.ipynb`](notebooks/ch53_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch53_code.ipynb) |
| 第54章 | 画像再構成・ノイズ除去とAI：画質を改善する | [`notebooks/ch54_code.ipynb`](notebooks/ch54_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch54_code.ipynb) |
| 第55章 | ドキュメンテーションと監査証跡：説明できる開発 | [`notebooks/ch55_code.ipynb`](notebooks/ch55_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch55_code.ipynb) |
| 第59章 | 医療AIの倫理・バイアス・限界 | [`notebooks/ch59_code.ipynb`](notebooks/ch59_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol2/blob/main/notebooks/ch59_code.ipynb) |

## 使い方

多くのノートブックは Google Colab でも動きますが、本書は手元の開発環境（WSL2＋Docker＋GPU。本書の第I部）を前提にした章を含みます。

1. 上の「章ごとのノートブック」の一覧で、使う章の「Open in Colab」のバッジを押す（ノートブックの先頭にも同じバッジがあります）
2. ランタイムのタイプを **GPU** に変更する
3. セルを上から順に実行する

手元のマシンで動かす場合：

```bash
git clone https://github.com/kewel-corp/book-vol2.git
cd book-vol2
```

## 書籍の版とタグ

**お手元の本の冒頭の「サポートページ」の節に書かれているタグを使ってください。**

そのタグの版が、お手元の本の紙面と一字一句同じコードです。リポジトリの main は、刊行後の訂正やライブラリの仕様変更への追随を含む最新の版です。

| タグ | 対応する本 |
|---|---|
| `v1.1-book-release` | 刊行した本（サポートページの節に `v1.1-book-release` と書かれている本） |
| `v1.0-book-release` | 刊行前の版（どの本にも対応しません） |

タグの版を手元に取るには：

```bash
git checkout <タグ>
```

タグの版を Colab で開くには、上の一覧の Colab のリンクの `blob/main/` を `blob/<タグ>/` に替えます。

---

## 守っていただきたい一線

**患者データを、このリポジトリに置かないでください。**

Gitの履歴は消えません。一度コミットすると、削除して再コミットしても過去の版から取り出せます
（入門編 第7章）。`.gitignore` で DICOM・NIfTI・配列形式を機械的に締め出していますが、
最後に効くのは運用です。

Colab に載せてよいのは、**公開データセットと、自分で作った合成データだけ**です。
自施設のデータを扱う段取り（倫理審査 → 匿名化 → シリーズ選択 → ラベル定義 → 対応表）は、
入門編 第11章で扱っています。

## データについて

**このリポジトリにデータは含まれていません。** `data/README.md` に、
本書で使用する公開データセットの入手先と、それぞれの利用条件をまとめています。

**ライセンスと品質は別問題です。** 商用利用可であることは、そのまま学習に投入してよいという
意味ではありません。使う前に、自分の目で中身を確かめてください（応用編の眼底写真の章）。

## ライセンス

| 対象 | ライセンス |
|------|------------|
| コード・ノートブック（`notebooks/` 以下） | [MIT](LICENSE-CODE) |
| 書籍の文章・図版 | © 2026 庄納　崇. 無断転載・再配布を禁じます |

なお、ノートブックが利用する外部ライブラリのライセンスは、それぞれに従います。
とくに **YOLO（Ultralytics）は AGPL-3.0** で、学習済みの重みにも及ぶとされています。
商用製品や医療機器プログラム（SaMD）に載せる場合は、遵守するか商用ライセンスを確認してください
（入門編 第5章）。

## 不具合・ご質問

Issues でお知らせください。ライブラリの仕様変更でノートブックが動かなくなった場合も、
同様にご報告いただけると助かります。

## 免責

本リポジトリのコードおよび書籍に記載された技術情報は、**教育・研究を目的としたもの**です。
実際の診療への応用や医療機器としての実装にあたっては、薬機法をはじめとする関連法規、
および各医療機関の倫理規定に必ず従ってください。ここで扱うAIモデルは、いずれも医師の診断を
**支援**するものであり、医師の判断に代わるものではありません。
