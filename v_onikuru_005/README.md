# v_onikuru_005

御丹宮くるみ歌声データベースから学習したNNSVS用モデルのひとつ。

## 音声ファイル前処理

- まず、ERA 4 DE-CLIPPER (Accusonus) でクリッピング修復
  - Mode: **2**
  - Quality: HIGH
  - Output: -6dB
- 次に、tranQuilizr G2 (A.O.M.) でローカット
- 最後に、[えこでこツール](https://ja.osdn.net/projects/ecodecotool/) で音圧一括調整
  - 設定音圧: 89dB

## 学習方法

- jp_qst001_nnsvs_simple_4-3.hed を使用
  - トライフォン
  - n_is_N **あり**
  - N を子音から除外
- **stage 0 での 音量ノーマライズ（最大化）を無効化**
- **stage 0 での offset collection を無効化**
- Sinsyのほぼデフォルトの日本語→ローマ字変換テーブルを使用
  - 「を」が必ず「o」に変換されるように改変
- 200 epochs で学習し、best_loss を使用するように変更。

## 歌声の特徴

- 非常に安定したピッチで歌ってくれるが単調で機械っぽい。