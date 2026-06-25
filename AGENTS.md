# AGENTS.md · 〔机构名〕 企业 AI 知识库 · Agent 总入口

> ⚠️ 这不是"文件地图",这是"可执行指令"。
> 任何 agent 接到任务,**先读这一页**,再按指引去对应工作流。

## 一、这个库是什么
〔机构名〕 的组织上下文基础设施——给一群 agent 用的执行底座,不是文档中心。
衡量标准:agent 能不能带着正确上下文,把一件真实业务做对。
**组织主轴 = 工作流,不是部门。** 见 `10-workflows/`。

## 二、Agent 工作协议
1. 判断任务属于哪条工作流(对照下表)。
2. 打开那条工作流的 `_task-card.md`(目标/上下文/指令/工具/权限/验收)。
3. 按任务卡 Context 清单读全 `context/`,再动手。
4. 动手前检查权限(`90-governance/permissions.md`)和定版(只用 `status: 定版`,见 `90-governance/lifecycle.md`)。
5. 完成后对照 `evals.md` 自检。
6. 新经验按 `90-governance/intake-rules.md` 回流入库。
7. 踩坑/被红线拦/客户反馈/遇到库没覆盖的新情况 → 记一行进 `90-governance/进化日志.md`（库靠它越用越聪明，定期按 `进化复盘SOP.md` 复盘回流）。

## 三、任务路由表
| 你接到的任务长这样 | 去这条工作流 | 先读这张卡 |
|---|---|---|
| 〔获客引流 相关任务〕 | `traffic-acquisition` | `10-workflows/traffic-acquisition/_task-card.md` |
| 〔销售转化 相关任务〕 | `sales-conversion` | `10-workflows/sales-conversion/_task-card.md` |
| 〔课程研发 相关任务〕 | `course-development` | `10-workflows/course-development/_task-card.md` |
| 〔教学交付 相关任务〕 | `teaching-delivery` | `10-workflows/teaching-delivery/_task-card.md` |
| 〔续费复购转介绍 相关任务〕 | `renewal-referral` | `10-workflows/renewal-referral/_task-card.md` |
| 跨工作流的方法论/实体 | (共享知识,非工作流) | `20-knowledge/` |

## 四、目录主轴
```
00-org/         DRI 责任地图 + 黑话词典
10-workflows/   ★主轴:工作流(每条=任务卡+context+sop+evals)
20-knowledge/   跨工作流复用的方法论/实体
30-raw/         原始大文件索引(不复制)
90-governance/  准入/定版/权限/同步
```

## 五、工具约定
- 本地库 = 知识生产车间;协作平台(飞书等) = 前台,定版后单向同步(见 `90-governance/feishu-sync.md`)。
- 原始大文件(PPT/视频/图片)留原地,`30-raw/` 仅索引引用。

## 六、一句话总纲
> 不要翻箱倒柜。判断任务属于哪条工作流 → 读那张任务卡 → 带全上下文 → 按 evals 验收。
> 目标不是"找到文件",是"带着正确上下文把事做对"。
