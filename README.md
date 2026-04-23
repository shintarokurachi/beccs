# beccs-3d-model

**バイオマスCCSの工程可視化：熱電併給と地中貯留のインタラクティブ3Dモデル**

*An Interactive 3D Model of BECCS: Combined Heat & Power and Geological Storage*

## Demo

https://shintarokurachi.github.io/beccs-3d-model/

## 概要 / Overview

バイオマスCCS（BECCS: Bioenergy with Carbon Capture and Storage）の四工程を、熱電併給（CHP）・地域熱供給を含む形で可視化したWebGLベースの3Dモデル。Three.js による単一HTMLファイルで構成され、ビルド不要で動作する。

A WebGL-based 3D visualization of BECCS (Bioenergy with Carbon Capture and Storage), incorporating combined heat & power (CHP) and district heating. Built as a single HTML file with Three.js; no build step required.

## 工程 / Stages

画面下のボタンで四工程を切り替えると、カメラがその地点にズームし、CO₂・バイオマス炭素・熱・電力の流れが段階に応じて切り替わる。

1. **① 大気CO₂の吸収 / Atmospheric CO₂ uptake** — 森林・エネルギー作物による光合成
2. **② 熱電併給 / Combined Heat & Power（CHP）** — バイオマスの燃焼による発電と、地域熱供給網を介した住宅への熱・電力の同時供給
3. **③ アミン法によるCO₂分離 / Amine-based CO₂ separation** — 吸収塔でCO₂とオフガス（N₂・O₂）を分離、再生塔で高純度CO₂を回収
4. **④ 地中貯留 / Geological storage** — 帯水層への圧入、帽岩による長期固定（負の排出）

## 先行事例との関係 / Relation to Prior Work

BECCSやCCS工程の可視化は、産業界（ExxonMobil、Rockwell Automation等のWebGL/ARコンテンツ）、NGO・研究機関（Carbon Visuals、British Geological Survey、ORNLのTableau可視化、Climate InteractiveのEn-ROADS政策シミュレーター等）により既に多数行われている。これらの多くは英語中心であり、また個別工程の物理的メカニズムよりも全体像や政策的インパクトの可視化を目的としている。

本モデルは、(1) 熱電併給・地域熱供給と統合されたバイオマス利用形態を組み込み、(2) アミン吸収法によるCO₂とオフガスの分離メカニズムを粒子フローで可視化し、(3) 日本語UIで参照可能な教材として公開する点を特徴とする。

BECCS and CCS visualizations already exist from both industrial (e.g., ExxonMobil, Rockwell Automation) and educational (e.g., Carbon Visuals, ORNL, Climate Interactive's En-ROADS) sources. This model is characterized by: (1) incorporating biomass utilization integrated with CHP and district heating, (2) visualizing amine-based CO₂/off-gas separation via animated particle flows, and (3) providing a Japanese-language UI.

## 使い方 / Usage

`index.html` をブラウザで開くだけで動作する。

- ドラッグ：視点回転
- ピンチ / ホイール：ズーム
- 下部ボタン：工程切替

Open `index.html` in any modern browser.

## ローカル起動 / Run locally

```bash
git clone https://github.com/shintarokurachi/beccs-3d-model.git
cd beccs-3d-model
python3 -m http.server 8000
```

## 技術 / Stack

- Three.js (r128, CDN)
- Pure HTML / CSS / Vanilla JS
- 外部ビルドツール・パッケージマネージャ不使用

## 作成上の注記 / Development Note

本モデルの実装にあたっては、Anthropic社のClaude（Claude Opus 4.7）を共同作業者として用いた。モデルの構成、各段階の教育的内容、視覚化すべき物質フロー、アミン分離の可視化方針等の設計判断は著者が行い、Three.jsによる実装はClaudeが反復的に生成・改善した。

This visualization was developed in collaboration with Anthropic's Claude (Claude Opus 4.7). The author determined the conceptual design, pedagogical structure, and domain-specific content; Claude generated and iteratively refined the Three.js implementation.

## ライセンス / License

MIT License. 詳細は [LICENSE](./LICENSE) を参照。

## 引用 / Citation

```
倉地真太郎（2026）「バイオマスCCSの工程可視化：熱電併給と地中貯留のインタラクティブ3Dモデル」
Kurachi, S. (2026). An Interactive 3D Model of BECCS:
Combined Heat & Power and Geological Storage.
https://github.com/shintarokurachi/beccs-3d-model
```

## 作成 / Author

倉地真太郎（Shintaro Kurachi） — 明治大学政治経済学部  
Meiji University, School of Political Science and Economics

研究・教育用途での利用を歓迎する。改変・再配布はMITライセンスに従う。
