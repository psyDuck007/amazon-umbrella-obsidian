# AMC营销云搜索词分析

## 适用场景

用于记录 Amazon Marketing Cloud 中 Sponsored Ads keyword / search term 查询结果，并把 AMC 的曝光、点击、购买路径数据转成广告动作。

## 数据来源

| 日期 | 来源文件 | 查询类型 | 状态 |
|---|---|---|---|
| 2026-06-13 | `/Users/kedaya007/Documents/Codex/project/New project/outputs/lingxing_reports/part-00000-cd51c19e-4978-482a-97b4-f11e52f35053-c000.csv` | Traffic by keyword and search term | 已分析 |
| 2026-06-13 | `/Users/kedaya007/Documents/Codex/project/New project/outputs/lingxing_reports/part-00000-45650fdd-922f-46cf-be72-a8236e78a7f0-c000.csv` | Attributed conversions by keyword and search term | 已分析 |
| 2026-06-13 | `/Users/kedaya007/Documents/Codex/project/New project/outputs/lingxing_reports/part-00000-cd53b6e9-0c56-41c4-aa38-2adc0413918e-c000.csv` | First vs attributed search terms | 已分析 |
| 2026-06-13 | `/Users/kedaya007/Documents/Codex/project/New project/outputs/lingxing_reports/amc_keyword_traffic_conversion_path_analysis_2026-06-12.xlsx` | 合并分析工作簿 | 已生成 |

## 已观察结果

当前 AMC 可见搜索词中，有 attributed purchases 的主要搜索词：

| 搜索词 | 购买数 | 判断 |
|---|---:|---|
| `cantilever umbrella with base included` | 10 | 核心成交词，建议单独精准/词组承接 |
| `cantilever umbrella` | 7 | 核心大词，需用预算和竞价控制 |
| `deck umbrella with base` | 7 | 高价值场景词，适合重点拓展 |
| `cantilever patio umbrellas` | 3 | 可保留并观察 |
| `large patio umbrella with lights` | 2 | 灯款机会词，需继续验证 |

路径查询中可见路径主要为同词成交，暂未发现明显的“先搜 A、后搜 B 成交”的辅助路径。该结论可能受样本量和 AMC 隐私阈值影响。

## 操作规则

- 有购买的可见搜索词优先进入精准匹配或词组匹配候选。
- `deck umbrella with base` 应单独关注，因为同时具备较好点击意愿和购买归因。
- `cantilever umbrella with base included` 不应只依赖 broad 扩词，需要独立精准承接。
- 大词如 `cantilever umbrella` 不能只因 CTR 较低就否定，需结合购买、ACOS、广告位和预算消耗判断。
- 空白或隐藏维度不能用于加词或否词，只能作为 AMC 隐私阈值下的整体贡献参考。
- 如果 `total_dpv` 全部为 0，只能分析购买归因，不能分析详情页浏览漏斗。

## 风险边界

- AMC 数据可能因隐私阈值隐藏部分搜索词或路径。
- 当前分析缺少 spend、sales、ACOS、CPC，因此不能直接决定最终否词和降价。
- 否定词必须结合广告后台 7 天或 14 天花费、点击、订单、ACOS 再确认。

## 下一步

- 将有购买词与广告后台搜索词报表交叉验证。
- 对 `deck umbrella with base`、`cantilever umbrella with base included` 单独建组或加精准后，观察 7 天点击、花费、订单和 ACOS。
- 对点击多但无购买的相关词，先进入观察表，不立即机械否定。

