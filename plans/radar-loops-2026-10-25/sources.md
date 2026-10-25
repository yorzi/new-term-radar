# 来源与证据账本

核查日期：2026-10-25。来源证明其明确陈述的事实，不能自动证明某个 Radar 有商业价值。网址可能更新；实际执行前重新核对日期、版本和条款。未保留整站副本，不复制第三方评论库。

## 本地直接观察

| ID | 来源 | 本轮观察 | 边界 |
|---|---|---|---|
| L1 | [原 Atlas](../radar_opportunity_atlas_2026.html) | 32 个构想、五类焦点、编辑评分 | 2026-10-14 的假设性报告，不是市场数据 |
| L2 | [store.py](../../radar/store.py)、[review.py](../../radar/review.py) | term 主键和 Trends 回测 | 不具备完整客户/行动/结果账本 |
| L3 | [asks.py](../../radar/asks.py)、[pains.py](../../radar/pains.py)、[opportunity.py](../../radar/opportunity.py) | 求助筛选、痛点分组、教程规则；asks 也保留低搜索量候选 | 不能只取有搜索量的表；one_click 是启发式标签，不是需求验证 |
| L4 | [seller_history.py](../../radar/seller_history.py)、[sellers.py](../../radar/sellers.py) | 上游已有支付链接历史；代码说明活链接幸存偏差和数据再发布限制 | 未运行付费 history，不验证源码标价是否仍有效 |
| L5 | `/Users/andy/Workspace/OpenSource/radar-integration-gap/AGENTS.md` 和 `./radar status --json` | 已有独立 Radar，陈旧候选 102、labels/actions/outcomes 0 | 未刷新；只证明本地记录，不能否定仓库外实际行动 |
| L6 | Git origin/fork 元数据、fetch、HEAD 与 upstream/main 比较 | 真正上游及同步提交可确定 | 只同步本地，origin 未推送 |

上述代码核查基线为 `143fc76ac284d0f292d817eb6dcfba12ea8bd01b`。L5 为另一个仓库的只读观察，不是本仓库功能。

## 官方与一手资料

| ID | 已访问来源 | 支持的判断 | 不支持的判断 |
|---|---|---|---|
| S01 | [RubyLLM 官网](https://rubyllm.com/) | 存在统一 Ruby API、provider 扩展路线，应先查官方能力 | 某条本地候选仍缺支持、某公司愿付费 |
| S02 | [GitHub API rate limits](https://docs.github.com/en/rest/using-the-rest-api/rate-limits-for-the-rest-api) | 限额依认证与端点变化；搜索更严格，须处理限流 | 所有扫描均可无限免费使用 |
| S03 | [RubyGems API](https://guides.rubygems.org/rubygems-org-api/) | 可查版本/包元数据和依赖相关信息 | 下载量是活跃用户，或反向依赖覆盖私人应用 |
| S04 | [Dependabot version updates](https://docs.github.com/en/code-security/concepts/supply-chain-security/dependabot-version-updates) | 自动版本更新已是成熟替代；纯版本 bump 差异小 | 行为迁移和业务回归均已自动解决 |
| S05 | [OpenAI deprecations](https://developers.openai.com/api/docs/deprecations) 与 [Assistants migration](https://developers.openai.com/api/docs/assistants/migration) | 官方迁移页说明 Assistants API 已于 2026-08-26 停用；应作为已过期案例 | 现在还有停服前的窗口、未知客户正在受影响 |
| S06 | [Claude model deprecations](https://platform.claude.com/docs/en/about-claude/model-deprecations) | active/deprecated/retired 不同；不同承载平台可能有不同时间表 | 名称相同的跨平台模型会同日停止 |
| S07 | [Glitch 官方变化公告](https://blog.glitch.com/post/changes-are-coming-to-glitch/) | 2025-05-22 公告称 hosting/profile 于 2025-07-08 关闭，仪表盘导出可到 2025 年底 | 当前仍能导出、整个公司失败、公告中的解释是唯一原因 |
| S08 | [W3C：选择无障碍评估工具](https://www.w3.org/WAI/test-evaluate/tools/selecting/) | 自动检查不能完成全部无障碍评估 | 扫描通过等于完整合规或真实 AT 验收 |
| S09 | [W3C WCAG-EM overview](https://www.w3.org/WAI/test-evaluate/conformance/wcag-em/) | 评估需界定范围和方法 | 对本轮未评估站点的任何合规结论 |
| S10 | [PageSpeed Insights 方法](https://developers.google.com/speed/docs/insights/v5/about) | 区分实验室/现场数据；页面样本不足可能退到 origin 或无现场数据 | 某次低分必然导致收入损失、无数据等于表现好 |
| S11 | [Zapier integrations](https://zapier.com/apps) | 广泛原生连接/自动化能力，是工作流方案的现实替代 | 任意具体流程无需开发就能满足全部约束 |
| S12 | [n8n 部署选择](https://docs.n8n.io/choose-how-to-use-n8n/) 与 [OEM 文档](https://docs.n8n.io/deploy/host-n8n/deploy-as-an-oem-integration.md) | 自托管/云及嵌入界面是不同交付；OEM 需商业协议 | 所有咨询或后端用法都需要 OEM；也不能反推任何使用都免费 |
| S13 | [Hacker News 官方 API](https://github.com/HackerNews/API) | 可读取公开故事和评论 | 有官方全文关键词搜索接口、完整代表市场需求 |
| S14 | [SAM.gov opportunities API](https://open.gsa.gov/api/get-opportunities-public-api/) | API key/分页和版本边界需处理；API 提供机会当前 active 版本 | 有 API 权限就有投标资格 |
| S15 | [TED Search API](https://docs.ted.europa.eu/api/latest/search.html) | 可公开搜索采购公告；无须认证的读取入口 | 非本地供应商自动有资格 |
| S16 | [WordPress plugins_api](https://developer.wordpress.org/reference/functions/plugins_api/) | 可获取插件信息与查询插件 | 是跨市场通用评论采集接口、安装数代表付费 |
| S17 | [YouTube commentThreads.list](https://developers.google.com/youtube/data/reference/rest/v3/commentThreads/list) | 官方评论线程读取入口及配额；每次调用消耗配额 | 视频有评论就能无条件读取全部回复、无任何配额成本 |
| S18 | [Reddit 开发者数据访问说明](https://support.reddithelp.com/hc/en-us/articles/14945211791892-Developer-Platform-Accessing-Reddit-Data) | 不同用途与访问路径有不同条件，商业采集需单独核实 | 第三方转售接口自动赋予再发布或任意商业使用权 |

## 竞争与排除证据

| ID | 来源 | 观察与处理 |
|---|---|---|
| C01 | [Failory](https://www.failory.com/) | 已提供失败案例内容和免费 newsletter；这是直接替代，不采用其“失败率”标题作为统计证据，也未核实自报订阅人数 |
| C02 | [Sunset](https://sunsethq.com/) | 其业务是公司关停服务；与软件迁移同含 sunset 一词，但不是本报告迁移服务的同类证据 |

检索失败/改址：n8n 旧 `sustainable-use-license/` 路径返回 Page Not Found，改用实际可访问部署和 OEM 文档；Groove 某 startup-failure 路径不可访问，未据此提炼案例。未以工具提示文本代替源正文，未把不可访问链接列为已验证来源。

## 本轮没有证明的事项

1. 五类闭环的市场规模、客户支付意愿、获客成本和行业成功率。
2. 本地 102 条机会的当前真实性、维护者意愿、最新 PR 状态。
3. 任一真实第三方网站存在缺陷；未执行站点批量审计。
4. 任一 workflow 已有三个真实使用者，或新方案优于 Zapier/n8n。
5. 任一案例当事人的主观动机、未披露财务数据或因果归因。

这些未知应由后续小实验回答，不能靠增加报告篇幅解决。
