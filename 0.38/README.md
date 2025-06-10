# Pose Analysis 0.38 更新予定情報

2025年6月13日に当該バージョンをリリース予定です。<br>
以下の通り、破壊的変更が含まれていますので、注意してください。<br>

## CSV フォーマット(raw.csv)の変更（破壊的変更）

このバージョンでは、CSV フォーマット（主に raw.csv）が大幅に変更されました。<br>
version 0.38 の iOS アプリと Web ダッシュボードは、この新しいフォーマットに対応しています。<br>
一方、今回のアップデートにより、過去のバージョンで生成された CSV ファイルは読み込むことができなくなります。<br>
Web ダッシュボードについても同様です。<br>
過去のバージョンで生成された CSV ファイルを読み込むことはできません。<br>
<br>
以下では、その新しいフォーマットの詳細を説明します。

---

### Sample

[ここからダウンロード](./sample_v0.38.csv)

### 基本カラム

| カラム名 | 内容 |
|----------|------|
| `elapsed` | 開始からの経過秒数（ミリ秒） |
| `frame` | フレーム番号 |
| `score` | 姿勢推定全体の信頼度スコア（0.0〜1.0） |

---

### 各関節データ構成

各関節ごとに以下の7つのフィールドが存在します：

| サフィックス名 | 意味 |
|----------------|------|
| `Score` | 姿勢推定スコア（0.0〜1.0） |
| `X`, `Y`, `Z` | 3次元空間上の座標（単位はモデル依存、通常は正規化済み） |
| `OneEuroX`, `OneEuroY`, `OneEuroZ` | OneEuroFilter によって平滑化された座標 |

<br>
ワンユーロフィルタとは、ローパスフィルタの一種で、ノイズを除去し、より滑らかな動きを実現するために使用されます。<br>

---

### 記録される関節一覧

以下の関節について、上記7つのカラムが記録されます：

- rShldrBend
- rForearmBend
- rHand
- rThumb2
- rMid1
- lShldrBend
- lForearmBend
- lHand
- lThumb2
- lMid1
- lEar
- lEye
- rEar
- rEye
- Nose
- rThighBend
- rShin
- rFoot
- rToe
- lThighBend
- lShin
- lFoot
- lToe
- abdomenUpper
- hip
- head
- neck
- spine

---

### データ型

| フィールド | 型 | 備考 |
|------------|----|------|
| `elapsed` | int | 秒単位の浮動小数点数 |
| `frame` | int | フレーム番号（整数） |
| `score`, `Score` | float | 0.0〜1.0 の信頼度 |
| `X`, `Y`, `Z`, `OneEuroX`, `OneEuroY`, `OneEuroZ` | float | 空間座標（単位はモデル依存） |

---

### 注意事項

- 各行は1フレームに対応しています。
- 項目の順序は固定です。ヘッダーとデータの整合性が取れていることを確認してください。


### その他の csv

#### angles.csv

変更無し。<br>
raw.csv の x, y, z の値を角度に変換したものです。<br>

#### one_euro_angles.csv

raw.csv の OneEuroX, OneEuroY, OneEuroZ の値を角度に変換したものです。<br>

### 撤去されたCSV

- kalman.csv
- lowpass.csv
- kalman_angles.csv
- lowpass_angles.csv

## 課金体制の変更

Pose Analysis の課金体制が変更されました。<br>
新しい課金体制では、以下のような変更が行われています：
<br>
- 10回測定チケット
  - 更新後価格：100円
    - 修正前：1,000円
- 50回測定チケット
  - 更新後価格：500円
    - 修正前：5,000円
- 500回測定チケット
  - 更新後価格：5,000円
    - 修正前：50,000円
- 1000回測定チケット
  - 更新後価格：10,000円
    - 修正前：100,000円

# 以上
