# 史莱姆的大野望 1 代 · 史莱姆大修
# Ambition of the SLIMES (1) · Slime Rework Collection
# スライムの大野望 1 · スライムリワーク集

> **AI 声明**：本项目的**全部代码由 AI 编写**。人类作者只负责**设计、平衡数值与审核**结果。
>
> **AI Disclosure**: **All code in this project was written by AI.** The human author only handled design, balance values and review.
>
> **AI 開示**：**本プロジェクトのコードはすべて AI が作成しました。** 人間の作者は設計・数値バランス・レビューのみを担当しています。

---

## ⚠️ 运行环境（必读）/ Requirements / 動作環境

| | 要求 |
|---|---|
| **BepInEx** | **5.4.x 系列的 x86（32 位）版本** —— 本作是 32 位 Unity 游戏，**x64 版无法加载**；**BepInEx 6 不支持** |
| 游戏 | 《史莱姆的大野望》**1 代**（Steam 版）|
| 可选 | [BepInEx.ConfigurationManager](https://github.com/BepInEx/BepInEx.ConfigurationManager/releases) —— 装后可**按 F2** 在游戏内调所有数值 |

- **BepInEx 5.4.x, x86 (32-bit)** — this is a 32-bit Unity game; the x64 build will not load, and **BepInEx 6 is not supported**.
- **BepInEx 5.4.x、x86（32 ビット）版**が必要です。本作は 32 ビット Unity ゲームのため、x64 版は読み込まれません。**BepInEx 6 は非対応**です。

---

## 功能介绍

### 一、四只老史莱姆重做

原作里这四只能力单薄，重做后各自有了明确的定位：

- **甜心史莱姆**（原冲锋）→ **奶妈**。给队友回复 30% 最大生命，**对史莱姆翻倍**；被夺取的身体每回合自动回血 15%。
- **韧性史莱姆**（原守卫）→ **护盾手**。给队友套 40% 减伤盾（对自己 30%）；夺来的身体**血上限翻倍**，并获得一层**永久的 20% 护盾**。
- **共振史莱姆**（原魔力）→ **法术溅射**。夺取敌人后，**那具身体的法术作用半径 +1**。溅射范围会以橙色格子直接画在战场上，一眼可见。（只对自己夺取的身体生效，不能给队友）
- **远视史莱姆**（原伸缩）→ **双向间合操控**。给队友 **+1 攻击距离**，同时给敌人 **−1 攻击距离**（持续 3 回合，**只对远程单位**，不叠加、重复攻击只刷新回合）；它自己还能**隔一格夺取敌人**，无视地形高差。

### 二、弃船（脱壳）

任何被夺取的身体都能**主动脱壳**：付出的史莱姆以 1 点血逃出，留在原地的**空壳会变成敌人**（免疫贿赂与色诱、可被 100% 夺取、眩晕 3 回合）。

次数按稀有度分配，**越朴素的史莱姆越能周旋**：

| 稀有度 | 脱壳次数 |
|---|---|
| C | 2（升过级 3）|
| B | 1（升过级 2）|
| A / S | 1 |

琥珀可以再买 1 次。**换身体本身就成了玩法** —— 想要哪只史莱姆的能力，就去夺一具身体。

### 三、宝石与琥珀

宝石系统提供 **12 项琥珀强化**可选（速度、攻防、射程、魔抗、夺取、再动、分裂、重生、继承……以及**脱壳次数**），随琥珀等级开放更多点数；另有隐藏的**越狱**功能。

### 四、夺取相关

- **残血好夺**：敌人**每损失 2% 生命，夺取概率 +1%**。打到残血再夺，是最划算的抓法。
- **夺取保底**：连续失败会累积成功概率。
- **属性继承**：夺取时继承目标属性。

### 五、分裂与继承

- **分裂 +1**：分裂史莱姆能多分裂一代。
- **无限分裂**（特殊版，独立插件）。
- **999 继承**：两种继承史莱姆能长期持有身体。
- **全继承**：所有史莱姆都能保留夺取的身体（重生型除外）。

### 六、便利与扩展

- **库存 30 → 48**：**兼容只有 30 格的老存档**。
- **花名册编辑器（F7）**：直接编辑队伍。
- **出击位堆叠**、**抽奖保底**。

### 七、技能调整

- **幽灵**：技能射程与作用范围各可 +1，可对队友使用。
- **超级传送**：允许对自己使用。

---

## Features (English)

**Four slimes reworked.** **Sweetheart** is now a healer: 30% of max health to an ally, doubled on slimes, and the body it claims regenerates 15% each turn. **Tenacity** is a shield support: 40% damage reduction for an ally (30% for itself), and the claimed body gets double max HP plus a permanent 20% shield. **Resonance** makes the claimed body's spells cover one tile wider, drawn on the field as orange tiles so you can see it. **Farsighted** stretches an ally's attack distance by one and shortens an enemy's by one for three turns (ranged units only, never stacking, a second hit only refreshes it) — and it can take a body from one tile away, ignoring height.

**Abandon ship.** Any slime can leave the body it took, escaping at 1 HP while the shell left behind turns hostile — immune to bribery and seduction, 100% possessable, dazed for three turns. Sheds are handed out by rarity, so the plainer the slime the more it can afford to move around: a C gets two (three after its level-up mark), a B one (two after), an A or S one. Amber can buy one more. Changing bodies becomes a real choice: want a different ability, go take a different body.

**Gems and amber.** Twelve amber upgrades to pick from — speed, attack and defence, reach, magic resistance, possession, extra turns, splitting, revival, inheritance, and one more shed — unlocking more points as the amber levels. A hidden jailbreak feature is included as well.

**Taking bodies.** A weakened foe is easier to take: every 2% of health it has lost adds 1% to the possession chance. Failed attempts build up pity, and attributes carry over.

**Splitting and inheriting.** Dividing slimes get one extra generation, an endless-splitting special build ships separately, both inheriting slimes hold a body for 999 turns, and one plugin lets every slime keep what it takes (revive breeds excluded).

**Convenience.** Unit box raised from 30 to 48 while still loading 30-entry saves, a roster editor on F7, stacking deploy slots, and pity for the prize draw.

**Ability tweaks.** The ghost's ability reaches one tile further and covers one tile more, and may be used on allies; the super teleport may target yourself.

---

## 機能紹介（日本語）

**4 体のスライムを再設計。** **スイートハート**はヒーラーになり、味方の最大 HP の 30%（スライムには倍）を回復、奪った体は毎ターン 15% 自然回復します。**テナシティ**はシールド役になり、味方に 40%（自分は 30%）の軽減を張り、奪った体は最大 HP が倍になり 20% の永続シールドを得ます。**レゾナンス**は奪った体の魔法範囲を 1 マス広げ、その範囲はオレンジのマスで戦場に描かれるので一目で分かります。**遠視**は味方の攻撃距離を +1、敵の攻撃距離を −1（3 ターン、遠距離のみ、重複せず再攻撃はターン更新のみ）し、本体は高低差を無視して 1 マス先からでも奪えます。

**脱皮。** のっとった体からいつでも抜け出せます。スライムは HP 1 で脱出し、残った抜け殻は敵になります（賄賂・誘惑無効、奪取率 100%、3 ターン行動不能）。回数はレア度で決まり、**地味なスライムほど何度も動けます**：C は 2 回（レベルアップ後 3 回）、B は 1 回（同 2 回）、A / S は 1 回。琥珀でさらに 1 回買えます。**体を乗り換えること自体が戦術**になります。

**宝石と琥珀。** 12 種類の琥珀強化（速度・攻防・射程・魔法耐性・奪取・再行動・分裂・復活・継承、そして脱皮回数）から選べ、琥珀のレベルに応じてポイントが増えます。隠しの脱獄機能も含まれます。

**奪取まわり。** 敵の HP が 2% 減るごとに奪取率が +1%。失敗が続くと天井が上がり、属性も継承されます。

**分裂と継承。** 分裂スライムがもう一代分裂でき、無限分裂は別ビルドとして同梱。2 種類の継承スライムは 999 ターン体を保持し、別プラグインで全スライムが体を保持できます（復活型を除く）。

**利便性。** ユニット枠を 30 → 48 に拡張（30 枠の旧セーブも読み込み可）、F7 の名簿エディタ、出撃枠の重複、抽選の天井。

**アビリティ調整。** ゴーストのアビリティは射程と範囲が 1 マスずつ伸び、味方にも使えます。スーパーテレポートは自分を対象にできます。

---

## 插件清单 / Plugin list / プラグイン一覧

每个功能都是**独立 DLL**，只装你想要的。 / Every feature is a **separate DLL** — install only what you want. / 機能ごとに**独立した DLL** です。

| DLL | 中文 | English | 日本語 |
|---|---|---|---|
| **Slime1AbilityTweaks** | 四只史莱姆重做 + 幽灵 + 传送 | Four slime reworks, ghost, teleport | 4 体の再設計、ゴースト、テレポート |
| **Slime1AbandonShip** | 弃船（脱壳）| Abandon ship | 脱皮 |
| **Slime1Gem** | 宝石系统 + 琥珀 12 项 | Gem system, 12 amber upgrades | 宝石システム、琥珀 12 項目 |
| **Slime1WeakOccupy** | 残血好夺 | Weakened foes easier to take | 弱った敵ほど奪いやすい |
| **Slime1DividePlus1** | 分裂多一代 | One extra split | 分裂がもう一代 |
| **Slime1DivideInf** | 无限分裂（特殊版）| Endless splitting (special) | 無限分裂（特殊版）|
| **Slime1Inherit999** | 999 次继承 | 999-turn inheritance | 999 ターン継承 |
| **Slime1InheritInf** | 所有史莱姆可继承 | All slimes inherit | 全スライムが継承 |
| **Slime1Box48** | 库存 30 → 48 | Unit box 30 → 48 | ユニット枠 30 → 48 |
| **Slime1BoxEditor** | 花名册编辑器（F7）| Roster editor (F7) | 名簿エディタ（F7）|
| **Slime1DeployStack** | 出击位堆叠 | Stacking deploy slots | 出撃枠の重複 |
| **Slime1OccupyPity** | 夺取保底 | Possession pity | 奪取の天井 |
| **Slime1PrizePity** | 抽奖保底 | Prize draw pity | 抽選の天井 |
| **Slime1SunAttr** | 夺取继承属性 | Inherit attributes | 属性の継承 |

---

## 安装 / Installation / 導入

1. 安装 **BepInEx 5.4.x x86**
2. 把 `Slime1*.dll` 放进 `BepInEx/plugins/`
3. 启动游戏

1. Install **BepInEx 5.4.x x86**
2. Drop the `Slime1*.dll` files into `BepInEx/plugins/`
3. Start the game

1. **BepInEx 5.4.x x86** を導入
2. `Slime1*.dll` を `BepInEx/plugins/` に入れる
3. ゲームを起動

装 [ConfigurationManager](https://github.com/BepInEx/BepInEx.ConfigurationManager/releases) 后**按 F2** 可调所有数值。 / With [ConfigurationManager](https://github.com/BepInEx/BepInEx.ConfigurationManager/releases) installed, **press F2** to tune every value. / [ConfigurationManager](https://github.com/BepInEx/BepInEx.ConfigurationManager/releases) 導入後、**F2** で全数値を調整できます。

## 注意 / Notes / 注意

- 所有数值都能在配置里改，默认值是调整过的平衡值。
- `Slime1Box48` 兼容只有 30 格库存的老存档。
- **建议先备份存档。**

- Every value is configurable; the defaults are the balance that was settled on.
- `Slime1Box48` still loads saves that only carry 30 roster entries.
- **Back up your save file first.**

- すべての数値は設定で変更できます。既定値は調整済みのバランス値です。
- `Slime1Box48` は 30 枠しかない旧セーブも読み込めます。
- **セーブデータは事前にバックアップしてください。**
