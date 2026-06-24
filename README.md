# Google Ads Account Structure Playbook 2026

Google Ads 电商账户结构：从冷启动到稳定放量的经验沉淀

做 Google Ads 账户结构时，最容易陷入的误区，是把问题理解成“到底要不要全上 Performance Max”“Search 还值不值得做”“Standard Shopping 还有没有必要”“Demand Gen 是不是一定要开”。

这些问题都重要，但如果一开始就围绕 campaign 类型讨论，很容易把账户搭成一堆互相抢量、互相归因、谁也说不清楚作用的结构。

我后来更倾向于先问另一个问题：

> 这个账户有没有把搜索意图、商品数据、转化价值和预算分配讲清楚？

Google Ads 和 Meta Ads 不一样。Meta 更像是用素材去找人，Google 则更依赖用户已经表达出来的需求、商品 Feed、搜索词、落地页和转化价值。一个 Google Ads 账户如果只开 PMax，却没有 Search 承接核心搜索词，也没有 Merchant Center Feed 优化，最后很容易变成“看起来自动化，实际上不可控”。

所以我现在看 Google Ads 结构，不会先问“哪个 campaign 类型最好”，而是先看：

- Search 有没有承接品牌词、核心品类词和高意图搜索词；
- Performance Max 有没有拿到干净的商品 Feed、足够资产和明确转化目标；
- Shopping 或 Feed 分层有没有帮助控制商品、毛利和预算；
- Demand Gen 是否真的有视觉素材和种草目标，而不是为了完整漏斗硬开；
- Smart Bidding 是否有足够转化量和正确的转化价值；
- GA4、Google Ads、Shopify / 后台 GMV 的数据口径能不能互相解释。

这套方法主要服务 DTC 独立站、Shopify 电商、跨境电商和以 Purchase / ROAS / CPA / GMV 为核心目标的 Google Ads 账户。B2B 线索、App、本地服务也能借鉴其中的判断方法，但 campaign 组合和转化口径需要重新设计。

* * *

## 核心判断

当前我更认可的 Google Ads 账户结构，不是单押某一种 campaign 类型，而是让不同 campaign 负责不同增长任务：

1. Search 负责承接明确需求；
2. Performance Max 负责跨渠道放量和商品覆盖；
3. Shopping / Feed 分层负责商品控制和利润管理；
4. Demand Gen 负责视觉种草和再激活；
5. Brand / Remarketing 负责防守和高意向承接。

落到电商账户里，成熟结构通常会变成：

| 模块 | 主要任务 | 常见预算占比 |
|---|---|---:|
| Search 非品牌词 | 承接高意图品类词、问题词、竞品词和场景词 | 20%-35% |
| Brand Search | 防守品牌词，承接已有需求，避免被竞品截流 | 5%-10% |
| Performance Max | 跨 Search、Shopping、YouTube、Discover、Gmail 等库存放量 | 35%-55% |
| Standard Shopping / Feed 分层 | 控制商品、利润、库存、爆品和长尾商品表现 | 0%-20% |
| Demand Gen | YouTube、Discover、Gmail 视觉种草和再激活 | 0%-15% |
| 大促 / Seasonal | 黑五、圣诞、清仓、上新、节点活动 | 单独预算 |

这不是一开始就要搭满的结构。

预算越小，Google Ads 结构越要先回答“哪里有确定需求”。新账户最怕的是一上来什么都开，Search 没有搜索词沉淀，PMax 没有 Feed 基础，Demand Gen 没有素材资产，最后每个 campaign 都只拿到一点点预算。

* * *

## 我会先看 8 个问题

### 1. 转化追踪有没有把真实业务价值传回去

Google Ads 现在越来越依赖 Smart Bidding。如果转化追踪不准，算法会很努力地优化一个错误目标。

冷启动前，我会先看：

| 模块 | 我主要看什么 |
|---|---|
| Google Ads Conversion | Purchase / Lead / Sign-up 是否正常触发 |
| GA4 | 关键事件、来源媒介、landing page、交易收入是否能看 |
| Enhanced Conversions | 是否开启，是否能提高转化匹配准确性 |
| Shopify / 后台 | 订单、GMV、折扣、退款、AOV 是否能和广告数据解释 |
| Conversion Value | 是否传回真实收入，是否需要按毛利或新客价值调整 |
| Attribution | 平台报告和 GA4 / 后台差异是否有解释 |

这里我会特别关注转化价值。

如果账户只告诉 Google “有转化”，但没有告诉它“哪种转化更值钱”，Smart Bidding 很容易去找便宜但低质量的订单或线索。对电商来说，最终应该尽量走向 value-based bidding，也就是让系统围绕转化价值、毛利或更接近利润的信号学习。

### 2. 出价方式是不是匹配当前阶段

Google Ads 现在的官方方向很明确：如果转化追踪可靠，系统更希望你使用 Smart Bidding，而不是长期手动调 CPC。Google 官方也建议，当不同转化有不同价值时，应该回传收入或转化价值，并使用 Maximize conversion value 或 Target ROAS。

但这不代表新账户一开始就应该直接上严格 tROAS。

我会按阶段选出价方式：

| 阶段 | 更适合的出价方式 | 我会怎么用 |
|---|---|---|
| 冷启动，几乎没有转化 | Manual CPC / Maximize Clicks / 小预算 Maximize Conversions | 先拿搜索词、点击和少量转化，不急着卡 CPA 或 ROAS |
| 有少量转化，但价值数据还不稳定 | Maximize Conversions | 适合先让系统找到能转化的人和词 |
| 电商已能回传订单金额 | Maximize Conversion Value | 比单纯追求转化数量更适合电商，因为不同订单价值不同 |
| CPA 已比较稳定 | Target CPA | 适合目标是控制获客成本，而不是追求不同订单价值 |
| ROAS 已有稳定基准 | Target ROAS | 适合成熟账户，但目标不要一开始设太高 |

我的经验是：

- Search 冷启动可以先控制词包，不要一开始全 Broad + 很激进的自动出价；
- PMax 初期更适合给系统探索空间，先不要用过高 tROAS 把量卡死；
- 电商账户只要订单金额回传可靠，最终通常应该往 Maximize Conversion Value / tROAS 走；
- tROAS 不是越高越好，目标设得太高，系统可能直接不敢花钱；
- 调整出价策略后至少观察 7-14 天，不要两三天没达到目标就来回切。

我会用一个很简单的判断：

> 数据少的时候先让系统学会“谁会买”；数据稳定后，再让系统学会“谁买得更值钱”。

### 3. Merchant Center 和商品 Feed 是否足够干净

Google Ads 电商账户里，Feed 很多时候比 campaign 设置更重要。

如果标题、图片、价格、库存、GTIN、商品类型、品牌、折扣和落地页有问题，PMax 和 Shopping 的表现都会被拖累。Google 官方 Merchant Center 也明确说明，Google 会使用产品数据把商品匹配到合适查询，准确且格式正确的商品数据对广告和免费 listing 都很重要。

我会先检查：

| Feed 项 | 判断标准 |
|---|---|
| Title | 是否包含品牌、核心品类、关键属性、使用场景 |
| Description | 是否清楚说明材质、功能、适用人群、规格 |
| Image | 主图是否清晰，是否符合政策，是否能表达产品 |
| Price / Sale price | 价格和站内一致，折扣逻辑清楚 |
| Availability | 库存状态准确，缺货商品不要继续浪费预算 |
| GTIN / Brand / MPN | 能补尽量补，提升商品识别和匹配 |
| Product type / Custom label | 是否支持按毛利、价格带、库存、爆品、季节拆分 |

如果 Feed 没整理好，我不会急着讨论 PMax 要不要拆 5 个 campaign。Feed 是 Google 电商投放的底座。

### 4. Search 是否承接了真正明确的需求

Search 的价值，不只是“抢关键词”，而是承接用户已经表达出来的购买意图。

我会把 Search 分成几类看：

| 类型 | 作用 |
|---|---|
| Brand Search | 防守品牌词、官网词、产品名词 |
| Category Search | 承接核心品类词，如 running shoes、standing desk |
| Problem / Use Case Search | 承接问题和场景词，如 shoes for flat feet |
| Competitor Search | 谨慎测试竞品词，注意 CPA、政策和落地页承接 |
| High-intent Long-tail | 承接高意图长尾，通常 CPA 更稳但量有限 |

Google 官方现在更推荐 Broad Match + Smart Bidding + Responsive Search Ads 的组合，也明确说不需要为了优化而按匹配类型过度拆分，因为出价系统会按 query 和 auction-time 信号判断。

但我不会在新账户一开始就盲目全 Broad。

如果转化量不够、否词体系没有搭好、落地页承接不清楚，Broad 很可能先带来一批不相关搜索。我的做法通常是：先用 Phrase / Exact 和少量 Broad 控制冷启动，再随着转化量、搜索词和否词沉淀，逐步扩大 Broad 和 AI Max for Search 的测试范围。

### 5. 素材资源有没有按 campaign 类型搭好

Google Ads 的素材资源不是只给 Demand Gen 用。Search、PMax、Demand Gen 都需要素材，只是素材形式不同。

我会分三层搭：

| Campaign 类型 | 需要的素材资源 | 核心要求 |
|---|---|---|
| Search / AI Max | RSA 标题、描述、落地页文案、附加资产 | 覆盖搜索意图，广告承诺和落地页一致 |
| Performance Max | 标题、长标题、描述、图片、Logo、视频、商品 Feed | 每个 Asset group 要有足够文字、图片和视频，不只依赖 Feed |
| Demand Gen | 横版/竖版视频、方图/横图、产品场景图、短文案 | 更像视觉种草，需要高质量图片和视频组合 |

Search 素材我会这样搭：

- 每个 ad group 围绕一个清晰主题，不把太多意图混在一起；
- RSA 标题覆盖核心关键词、利益点、价格/折扣、信任背书、CTA；
- 描述里写清楚产品差异、配送、退换、保障和促销；
- 补齐 sitelink、callout、structured snippet、price、promotion、image asset；
- 如果使用 AI Max，要检查 Text customization 和 Final URL expansion，不要让流量跑到无关页面。

PMax 素材我会这样搭：

- Asset group 按产品线、场景、人群或页面意图组织；
- 不只上传最低数量素材，而是让每个 Asset group 至少有完整文字、图片和视频；
- 视频尽量自己上传，不完全依赖 Google 自动生成；
- 图片要覆盖产品白底图、场景图、卖点图、评论/信任背书图；
- Feed 要和 Asset group 对上，不要一个组里混太多不相关商品。

Demand Gen 素材我会这样搭：

- 先复用 Meta / TikTok 里已经验证过的高质量素材，但要改成适合 YouTube、Discover、Gmail 的版式；
- 视频要有明确前 3 秒 hook，适合竖版和横版场景；
- 图片不要只放产品图，要有场景、人群、使用结果和品牌质感；
- 同一轮测试要按角度分组，例如痛点、场景、社会证明、Offer、产品演示；
- 评估时不要只看 last-click ROAS，还要看新用户、辅助转化、观看质量和再营销表现。

我的判断是：

> Google Ads 的素材搭建，不是“补齐系统要求”，而是让 Google 能用不同素材理解不同意图、商品和场景。

### 6. PMax 是在放量，还是在抢已有流量

Performance Max 是当前 Google Ads 电商账户里非常重要的 campaign 类型。官方说明里，PMax 会结合 Smart Bidding 和归因技术，在多个 Google 库存中实时选择更可能达到目标的广告机会；Google AI 会根据预算、业务目标、转化、受众信号和资产去寻找潜在客户。

但 PMax 的问题也很明显：它很强，但不够透明。

我会重点看：

- PMax 是否主要吃品牌词和再营销流量；
- 是否和 Search 抢同一批高意图 query；
- 是否有新客增长，还是只是在吃已有需求；
- 商品 Feed 是否有足够分层；
- Asset group 是否围绕产品线、场景或人群组织；
- Final URL expansion 是否把流量送到了不该去的页面；
- ROAS 是否被老客、品牌词或低毛利商品拉高。

PMax 不是不能做主力。对很多电商账户，它确实会是主力。

但我不会让 PMax 成为账户里唯一能解释增长的 campaign。如果 Search、Feed、商品分层、GA4 和后台数据都解释不了 PMax 的增长，那这个结构还不够健康。

### 7. Demand Gen 是否真的有上层漏斗任务

Demand Gen 适合做视觉种草、场景教育、再激活和扩展需求，尤其是在 YouTube、Shorts、Discover、Gmail 等视觉场景里。

Google 在 2025 的 Marketing Live 里把 Performance Max、AI Max for Search 和 Demand Gen 放进 Power Pack，说明 Google 对这三个 AI-powered campaign 的方向很明确：Search 捕捉需求，PMax 放大跨渠道转化，Demand Gen 扩展视觉需求。

但 Demand Gen 不应该为了“漏斗完整”硬开。

我会先看：

- 有没有足够好的视频、图片和短文案资产；
- 产品是不是需要教育、场景展示或信任建立；
- 是否有再营销或类似受众基础；
- 是否能接受更长转化周期；
- 是否用 GA4 和后台看辅助转化、路径和新客质量。

如果素材很弱、预算很小、产品需求又很明确，我会优先把钱放在 Search、Shopping / PMax，而不是先开 Demand Gen。

### 8. 预算和学习量能不能支撑拆分

Google Ads 也有一个常见问题：账户结构看起来很完整，但每个 campaign 都吃不饱。

拆 campaign 之前，我会先问：

> 这个拆分会让预算和学习信号更清楚，还是更分散？

可以考虑拆的情况：

| 拆分方式 | 适合情况 |
|---|---|
| 按品牌 / 非品牌拆 | 品牌词 ROI 很高，需要单独看防守价值 |
| 按产品线拆 | AOV、毛利、库存、落地页和搜索意图差异明显 |
| 按利润 / 价格带拆 | 需要把预算优先给高毛利或高 AOV 商品 |
| 按国家 / 语言拆 | 市场价格、语言、履约、竞争环境明显不同 |
| 按大促拆 | 大促预算、素材、折扣和节奏会影响常规 campaign |

不建议拆的情况：

| 拆分原因 | 为什么不建议 |
|---|---|
| 只是为了看起来结构完整 | 每个 campaign 学习量不足 |
| 按 Match Type 拆太细 | Smart Bidding 学习被切碎，管理复杂 |
| PMax 按太多产品小组拆 | 商品数据和转化不足，难以学习 |
| Demand Gen 没有素材也硬开 | 上层流量多，但转化解释困难 |

* * *

## 从零冷启动，我会怎么搭

### 阶段 0：先把数据和商品基础检查完

Google Ads 冷启动不是从创建 PMax 开始，而是从确认“系统能不能看到正确的商品和收入”开始。

我会先完成这些检查：

| 检查项 | 判断标准 |
|---|---|
| Google Ads 转化 | Purchase / Revenue 正常回传 |
| GA4 | 交易、来源媒介、landing page、事件路径能看 |
| Enhanced Conversions | 已开启或确认可开启 |
| Merchant Center | 商品无大面积拒登，Feed 字段完整 |
| 商品分层 | 至少能按品类、毛利、价格带、库存或爆品打 custom label |
| 站点承接 | 移动端速度、商品页、结账、支付、运费、退换政策清楚 |
| UTM | Google Ads、GA4、Shopify 能对上 campaign 和 ad group |

如果这一步没过，我不会急着加预算。因为后面的 tROAS、CPA、Search terms、PMax insights 都可能误导判断。

### 阶段 1：先用 Search / Shopping 拿可解释的第一批信号

如果是新账户、新站点或历史数据很少，我通常不会第一天就把大部分预算丢给 PMax。

更稳的方式是先拿到可解释的搜索词、商品和转化信号：

| Campaign | 作用 | 设置思路 |
|---|---|---|
| Brand Search | 防守品牌需求 | Exact / Phrase，低预算，单独看品牌词 |
| Non-brand Search | 测高意图需求 | 核心品类词、场景词、问题词，先控制范围 |
| Standard Shopping 或小预算 PMax | 测商品和 Feed | 从主推商品、爆品或高毛利商品开始 |

这个阶段的目标不是马上规模化，而是回答：

- 哪些搜索词真的有购买意图；
- 哪些商品有点击和转化潜力；
- 哪些页面承接不住；
- 哪些价格带、品类、offer 更容易成交；
- 转化价值是否正常回传。

### 阶段 2：有转化后，逐步引入 Smart Bidding 和 Broad

当账户开始有稳定转化后，我会逐步把结构从“控制型测试”转向“智能出价扩量”。

动作通常包括：

- Search 从 Phrase / Exact 扩展到部分 Broad；
- 使用 Smart Bidding，例如 Maximize Conversions、Maximize Conversion Value、tCPA 或 tROAS；
- RSA 补齐标题、描述、USP、价格、保障和 CTA；
- 搜索词报告持续加否词；
- 观察 Broad 是否带来增量，而不是只带来无关流量。

如果是电商账户，我会更倾向最终走向 Maximize Conversion Value / tROAS，因为它比单纯追求 Purchase 数量更接近业务结果。

但 tROAS 不应该过早卡得太死。冷启动阶段如果目标 ROAS 设置过高，系统可能拿不到足够探索空间，反而跑不出量。

### 阶段 3：PMax 成为主力，但不能失控

当 Search 和 Feed 已经有一定信号，PMax 可以开始承担主力放量。

我会这样搭：

| 层级 | 设置思路 |
|---|---|
| Campaign | 先 1 个 PMax 主 campaign，不要一开始拆太多 |
| Feed | 优先放主推品、爆品、高毛利或库存稳定商品 |
| Asset group | 按产品线、场景、人群或页面意图组织 |
| Audience signal | 用购买用户、加购用户、站内访客、搜索主题、竞品/兴趣作为信号 |
| Bidding | 初期给系统探索空间，稳定后再逐步使用 tROAS |
| URL control | 审核 Final URL expansion，排除博客、政策页、无关页面 |

我会特别关注 PMax 是否吃掉 Brand Search 或低质量再营销。如果 PMax ROAS 很高，但整体账户 GMV 没涨，或者 Search 非品牌词下滑，就要检查是否存在抢量和归因重叠。

### 阶段 4：成熟结构形成

当账户有稳定转化量、Feed 分层、Search 词包和 PMax 学习后，可以进入成熟结构。

成熟结构可以这样看：

| Campaign | 角色 | 预算 |
|---|---|---:|
| Brand Search | 防守品牌和官网词 | 5%-10% |
| Non-brand Search | 承接明确高意图需求 | 20%-35% |
| Performance Max | 商品放量和跨渠道转化 | 35%-55% |
| Standard Shopping / Feed Split | 控制商品、毛利、长尾和库存 | 0%-20% |
| Demand Gen | 视觉种草、再激活和新客扩展 | 0%-15% |
| Seasonal / Promo | 大促、清仓、上新 | 单独预算 |

这里最重要的是：不要让每个 campaign 都想完成所有事情。

Search 要解释搜索意图，PMax 要解释商品和跨渠道增长，Demand Gen 要解释视觉种草和增量，再营销要解释高意向承接。每个 campaign 都要有一句话说清楚它存在的理由。

### 阶段 5：放量和维护

Google Ads 放量时，我会比 Meta 更关注“搜索词、商品、毛利和增量”。

常见动作：

- Search：扩关键词、扩 Broad、加 AI Max、优化 RSA、加否词；
- PMax：补资产、优化 Feed、拆高毛利商品、排除无关 URL；
- Shopping：按 custom label 管理爆品、长尾、低毛利、缺货风险；
- Demand Gen：按素材角度、视频开头、受众信号和再营销层级测试；
- Bidding：从 Maximize Conversion Value 逐步走向 tROAS；
- 数据复盘：用 GA4、Shopify 和 Google Ads 对齐 GMV、AOV、ROAS、退款和新客。

暂停或调整规则：

| 情况 | 动作 |
|---|---|
| Search 花费高但搜索词明显不相关 | 加否词，收紧词包或降低 Broad 占比 |
| Search CTR 高但 CVR 低 | 检查落地页、价格、offer、配送和广告承诺 |
| PMax ROAS 高但整体 GMV 没涨 | 查品牌词、再营销、归因重叠和是否抢 Search |
| PMax 某些商品高花费无转化 | 用 listing group / custom label 做控制 |
| Demand Gen 点击多但转化弱 | 看辅助转化、新客、观看质量和素材承接，不只看 last-click |
| tROAS 设置后量大幅下降 | 目标可能过紧，放宽 tROAS 或回到 Maximize Conversion Value 观察 |

* * *

## 常见错误

### 1. 新账户一上来全靠 PMax

PMax 很强，但新账户如果没有 Search、Feed 和转化价值基础，很容易跑出一个看起来自动化、实际不可解释的结构。

### 2. 忽视 Merchant Center Feed

Google 电商投放里，Feed 不是后台资料，而是广告匹配系统的一部分。标题、图片、价格、库存、GTIN 和 custom label 都会影响表现。

### 3. 品牌词和非品牌词混在一起看

Brand Search 通常 ROAS 很高，但它不代表新增需求。一定要分开看品牌防守和非品牌增长。

### 4. 太早上严格 tROAS

冷启动时目标 ROAS 卡得太高，系统可能不敢探索，最后量跑不出来。

### 5. Broad Match 没有否词和转化基础

Broad + Smart Bidding 是官方方向，但前提是转化追踪、落地页、否词和预算能支撑探索。

### 6. Demand Gen 没有好素材也硬开

Demand Gen 是视觉场景，不是 Search 的替代品。没有视频、图片、场景内容和较长判断周期时，容易被误判。

* * *

## 这个方法论最后会落成什么

我会把 Google Ads 账户看成一个“需求承接 + 商品放量 + 价值出价”的系统。

这个系统里有四件事必须同时成立：

1. Search 承接真实搜索需求；
2. Feed 让 Google 正确理解商品；
3. PMax 用干净数据和资产做跨渠道放量；
4. Smart Bidding 学到的是收入、毛利或更接近利润的转化价值。

如果只开 PMax，但 Feed 很弱，账户会失控。

如果 Search 做得很细，但转化价值没传准，系统会优化错目标。

如果 Demand Gen 看起来带来了很多点击，但没有新客、路径和辅助转化解释，就不能证明它在创造增量。

所以这套经验的核心不是照抄一个结构，而是建立一套判断方法：

> 什么时候先控制，什么时候交给自动化，什么时候拆商品，什么时候扩 Broad，什么时候该停下来先修 Feed、追踪、页面或 offer。

* * *

## 仓库里的模板

- `templates/cold-start-checklist.md`：Google Ads 冷启动检查清单；
- `templates/account-structure-canvas.md`：账户结构梳理画布；
- `templates/bidding-and-assets-checklist.md`：出价方式与素材资源检查清单；
- `templates/search-query-review.csv`：搜索词复盘模板；
- `templates/product-feed-segmentation.csv`：商品 Feed 分层模板；
- `docs/sources.md`：参考来源。

* * *

## 参考来源

- Google Ads Help：Google Ads Best Practices。https://support.google.com/google-ads/answer/6154846
- Google Ads Help：About Performance Max campaigns。https://support.google.com/google-ads/answer/10724817
- Google Ads Help：About Smart Bidding。https://support.google.com/google-ads/answer/7065882
- Google Ads Help：Pick the right bid strategy。https://support.google.com/google-ads/answer/6167148
- Google Ads Help：About Target ROAS bidding。https://support.google.com/google-ads/answer/6268637
- Google Ads：How to use broad match and AI-powered Search advertising。https://business.google.com/us/resources/articles/reaching-the-right-customers-on-search/
- Google Ads Blog：AI Max for Search campaigns。https://blog.google/products/ads-commerce/google-ai-max-for-search-campaigns/
- Google Ads Help：Set up AI Max in Google Ads。https://support.google.com/google-ads/answer/15909989
- Google Ads Help：Best practices for asset groups in Performance Max campaigns。https://support.google.com/google-ads/answer/14528220
- Google Ads Help：Demand Gen campaign creative asset specifications。https://support.google.com/google-ads/answer/13704860
- Google Marketing Live 2025：Power Pack。https://business.google.com/us/accelerate/gml-announcements/
- Google Merchant Center Help：Product data specification。https://support.google.com/merchants/answer/7052112
- Google Ads：Enhanced conversions best practices。https://business.google.com/us/accelerate/resources/articles/conversions-best-practices/
- Google Ads Help：Creative Excellence Guide for Demand Gen campaigns。https://support.google.com/google-ads/answer/14733311
- Google Ads Developers：Performance Max for online sales with a product feed。https://developers.google.com/google-ads/api/performance-max/retail
- Store Growers：Performance Max Campaigns: The Ultimate Ecommerce Guide 2026。https://www.storegrowers.com/performance-max-campaigns/
- Store Growers：The Ultimate Guide To Google Ads For Ecommerce 2026。https://www.storegrowers.com/google-ads-ecommerce/
- Smarter Ecommerce：How to run Google Shopping alongside Performance Max in 2026。https://smarter-ecommerce.com/blog/en/google-shopping/how-to-run-google-shopping-alongside-performance-max-in-2026/
