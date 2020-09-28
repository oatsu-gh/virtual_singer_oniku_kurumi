# 更新履歴 / Change Log

## v0.0.1

-  2020-09-29
- 初配布

### 仕様

- world による合成
- jp_qst001_nnsvs_simple_4-2.hed を使用
  - NNSVS (Sinsy) の jp_qst001_nnsvs.hed を改変
  - 母音や子音の分類を削減
- テーブルは sinsy のデフォルトを改変したものを使用
  - フォルダは dic/sinsy
  - 「を」のローマ字表記をすべて「o」に統一
- 環境構築は [setup-nnsvs-on-wsl](https://github.com/oatsu-gh/setup-nnsvs-on-wsl) v0.0.2 を想定

### 学習方法

- 御丹宮くるみ歌声データベース を使用

- 2020年9月27日 時点での NNSVS を使用して学習

- jp_qst001_nnsvs_simple_4-2.hed（282次元）