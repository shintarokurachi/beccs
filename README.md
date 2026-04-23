# beccs-3d-model

バイオマスCCS（BECCS: Bioenergy with Carbon Capture and Storage）の4工程をインタラクティブに表示する3Dモデル。Three.js を用いた単一HTMLファイル。

An interactive 3D visualization of the BECCS (Bioenergy with Carbon Capture and Storage) process. Single HTML file, built with Three.js.

## Demo

https://shintarokurachi.github.io/beccs-3d-model/

## 概要 / Overview

画面下のボタンで4つの段階を切り替えると、カメラが該当地点にズームし、CO₂の流れ（赤）とバイオマス由来の炭素の流れ（緑）のアニメーションが段階に応じて切り替わる。

Clicking the step buttons moves the camera to each stage and updates the particle flows accordingly.

1. **① 大気CO₂の吸収 / Atmospheric CO₂ uptake** — 森林・エネルギー作物による光合成
2. **② バイオマスの燃焼・発電 / Combustion & power generation** — 発電所での熱・電力生成
3. **③ CO₂の回収 / CO₂ capture** — 排ガスからの分離・回収
4. **④ 地中貯留 / Geological storage** — 帯水層への圧入（負の排出）

## 使い方 / Usage

`index.html` をブラウザで開くだけで動作する。ビルド不要。

- ドラッグ：視点回転
- ピンチ / ホイール：ズーム
- 下部ボタン：工程切替

Open `index.html` in any modern browser. No build step required.

## ローカル起動 / Run locally

```bash
git clone https://github.com/shintarokurachi/beccs-3d-model.git
cd beccs-3d-model
# そのまま index.html を開く、または簡易サーバで:
python3 -m http.server 8000
```

## 技術 / Stack

- Three.js (r128, CDN)
- Pure HTML / CSS / Vanilla JS
- 外部ビルドツール・パッケージマネージャ不使用

## ライセンス / License

MIT License. 詳細は [LICENSE](./LICENSE) を参照。

## 作成 / Author

倉地真太郎（Shintaro Kurachi） — 明治大学政治経済学部

研究・教育用途での利用を歓迎する。改変・再配布はMITライセンスに従う。
