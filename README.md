# HUMANS OF EARTH

An interactive 3D globe visualizing the history and future of human population, from 10,000 BC to 2100 AD.

Each dot of light represents 50,000 people. Watch civilizations rise as flickering firelight in the ancient world, transition to electric glow in the modern era, and explore possible futures under different fertility scenarios.

## Features

- **12,000-year timeline** — Slide from 10,000 BC to 2100 AD
- **Story mode** — a guided fable from the first fires to 2100, with camera flights to each chapter's stage (✦ button or `S` key). Chapter 8 changes with the scenario you choose; the epilogue "The Frozen Light" switches on the Ageless scenario and the machine light
- **4 future scenarios** — Linear TFR decline / Stable TFR / Soft landing (floor at 0.8) / Ageless (after 2030 death fades toward accidents-only — and births, tied to deaths in this model, fade with it; the lights stop flickering and freeze)
- **Machine light layer** — a speculative second layer of cold cyan dots (1 dot = 1 GW) growing where energy and cooling are cheap — Iceland, the Sahara, the Gobi, Atacama — instead of along the rivers and coasts that human light has followed for millennia
- **Age structure coloring** — Toggle to see aging populations shift from orange to blue-purple
- **Migration flow arcs** — Gravity model with GDP attraction and language bonuses (2024+)
- **Bilingual** — English / Japanese (auto-detected, switchable)

## Live Demo

*(URL TBD — Cloudflare Pages)*

## Running Locally

```bash
npx serve .
# Open http://localhost:3000
```

Requires a local HTTP server (`<script type="module">` does not work over `file://`).

## Data Sources

| Data | Source | License |
|------|--------|---------|
| Earth texture | NASA Blue Marble Next Generation | Public domain |
| City light positions | NASA VIIRS Black Marble | Public domain |
| Historical population | Our World in Data (HYDE 3.2) | CC-BY 4.0 |
| Fertility rate (TFR) | UN World Population Prospects 2024 via OWID | CC-BY 4.0 |
| Life expectancy | UN World Population Prospects 2024 via OWID | CC-BY 4.0 |
| Infant mortality | UN IGME 2024 via OWID | CC-BY 4.0 |
| Age structure | World Bank Development Indicators | CC-BY 4.0 |
| Country boundaries | Natural Earth | Public domain |
| Historical cities | Reba et al. (2016) — Chandler + Modelski | CC-BY 4.0 |
| GDP projections (SSP) | For migration model | CC-BY 4.0 |
| Language groups | For migration language bonus | — |

Full references: [`docs/methodology/data-sources.md`](docs/methodology/data-sources.md)

## Known Limitations

- Future projections are thought experiments, not predictions
- Life expectancy and infant mortality are fixed at 2023 values
- Ancient population data relies on HYDE 3.2 model estimates (not measurements)
- Pre-Columbian Americas population is particularly uncertain ([details](docs/methodology/data-sources.md#10-hyde-32-owid-歴史人口の背後のモデル))

## Tech Stack

- [Globe.GL](https://globe.gl/) — WebGL globe rendering
- [Three.js](https://threejs.org/) — 3D graphics
- Vanilla JavaScript — No build tools, no framework

## License

[MIT](LICENSE)

---

# HUMANS OF EARTH

紀元前1万年から西暦2100年まで、人類の人口の歴史と未来をインタラクティブな3D地球儀で可視化するプロジェクト。

光の1ドットが5万人を表す。古代世界の揺らめく焚き火から、近現代の電気の光への移行、そして出生率シナリオに基づく未来の可能性を探索できる。

## 機能

- **1万2千年のタイムライン** — 紀元前1万年〜西暦2100年をスライダーで操作
- **物語モード** — 最初の焚き火から2100年までのガイド付き寓話。各章の舞台へカメラが移動（✦ボタン / `S`キー）。第8章は選択中のシナリオで結末が変わり、終章「凍った光」では不老シナリオと機械の光が灯る
- **4つの未来シナリオ** — 出生率の線形低下 / 固定 / 緩やかな着地（下限0.8）/ 不老（2030年以降、死が事故のみに近づく。このモデルでは出生は死亡に比例するため、出生もともに薄れ、光は揺らぎを止めて凍る）
- **機械の光レイヤー** — 冷たいシアンの第2レイヤー（1ドット = 1GW・想像）。人類の光が数千年寄り添ってきた川と海岸ではなく、エネルギーと冷却の安い場所——アイスランド、サハラ、ゴビ、アタカマ——に育つ
- **年齢構成の色分け** — 高齢化する社会がオレンジ→青紫に変化
- **移民フロー** — GDP引力+言語ボーナスの重力モデル（2024年以降）
- **日英対応** — ブラウザ言語で自動切替、手動切替も可能

## ローカル実行

```bash
npx serve .
# http://localhost:3000 を開く
```

`<script type="module">` を使用しているため、`file://` では動作しません。ローカルHTTPサーバーが必要です。

## データソース

| データ | 出典 | ライセンス |
|--------|------|-----------|
| 地球テクスチャ | NASA Blue Marble Next Generation | パブリックドメイン |
| 都市光の位置 | NASA VIIRS Black Marble | パブリックドメイン |
| 歴史人口 | Our World in Data (HYDE 3.2) | CC-BY 4.0 |
| 合計特殊出生率 | 国連世界人口推計2024 via OWID | CC-BY 4.0 |
| 平均寿命 | 国連世界人口推計2024 via OWID | CC-BY 4.0 |
| 乳幼児死亡率 | UN IGME 2024 via OWID | CC-BY 4.0 |
| 年齢構成 | 世界銀行 開発指標 | CC-BY 4.0 |
| 国境データ | Natural Earth | パブリックドメイン |
| 歴史都市 | Reba et al. (2016) — Chandler + Modelski | CC-BY 4.0 |
| GDP予測 (SSP) | 移民モデル用 | CC-BY 4.0 |
| 言語グループ | 移民の言語ボーナス用 | — |

詳細な参考文献: [`docs/methodology/data-sources.md`](docs/methodology/data-sources.md)

## 既知の限界

- 未来予測は思考実験であり、予測ではない
- 平均寿命・乳幼児死亡率は2023年値で固定
- 古代の人口データは HYDE 3.2 のモデル推計値（実測ではない）
- 先コロンブス期アメリカの人口推計は特に不確実（[詳細](docs/methodology/data-sources.md#10-hyde-32-owid-歴史人口の背後のモデル)）

## ライセンス

[MIT](LICENSE)
