# AGENTS.md · 〔机构名〕 企业 AI 知识库 · Agent 总入口

> 这不是文件地图，而是可执行指令。
> 任何 agent 接到任务，先读这一页，再按指引去对应工作流。

## 一、这个库是什么

〔机构名〕 的组织上下文基础设施。它是给 agent 用的执行底座，不是普通文档中心，也不是要求每个人手动翻文件的网盘。

衡量标准：agent 能不能带着正确上下文，把一件真实业务做对。

组织主轴 = 工作流，不是部门。见 `10-workflows/`。

## 二、人和 agent 怎么分工

- 人负责提出目标、补充事实、提供素材、授权和审核。
- agent 负责读取上下文、判断工作流、执行任务、生成结果和自检。
- DRI/部门主管负责维护自己工作流的业务资产和定版判断。
- 知识库负责人负责治理、权限、索引、同步和全局一致性。

普通员工不需要手动跑完整工作流。普通员工只需要描述具体任务、已知事实和限制条件；agent 负责判断该读哪些文件、走哪条工作流。

## 三、首次上手协议

当用户说：

```text
帮我开始使用这个知识库。
```

agent 应先读取：

1. `START-HERE.md`
2. `AGENTS.md`
3. `INDEX.md`

然后询问用户角色和本次目标：

```text
你现在使用这个知识库的角色是什么？

1. 老板/负责人
2. DRI/部门主管
3. 普通员工
4. 知识库维护者
5. agent

你这次想完成什么事？
```

根据用户角色决定下一步：

- 老板/负责人：优先做全库体检、缺口盘点、边界确认、定版审核。
- DRI/部门主管：进入其负责的工作流，读取任务卡和 context，辅助补资产和审核输出。
- 普通员工：根据其描述判断工作流，读取必要上下文后执行，不要求用户自己找文件。
- 知识库维护者：检查占位符、草稿、权限风险、索引、同步和进化日志。
- agent：按本文件的工作协议执行。

## 四、Agent 工作协议

1. 判断任务属于哪条工作流（对照下表）。
2. 打开那条工作流的 `_task-card.md`（目标/上下文/指令/工具/权限/验收）。
3. 按任务卡 Context 清单读全 `context/`，再动手。
4. 动手前检查权限（`90-governance/permissions.md`）和定版状态（只用 `status: 定版`，见 `90-governance/lifecycle.md`）。
5. 完成后对照 `evals.md` 自检。
6. 新经验按 `90-governance/intake-rules.md` 回流入库。
7. 踩坑、被红线拦、客户反馈、遇到库没覆盖的新情况，记一行进 `90-governance/进化日志.md`，定期按 `进化复盘SOP.md` 复盘回流。

## 五、任务路由表

| 你接到的任务长这样 | 去这条工作流 | 先读这张卡 |
|---|---|---|
| 〔获客引流 相关任务〕 | `traffic-acquisition` | `10-workflows/traffic-acquisition/_task-card.md` |
| 〔销售转化 相关任务〕 | `sales-conversion` | `10-workflows/sales-conversion/_task-card.md` |
| 〔课程研发 相关任务〕 | `course-development` | `10-workflows/course-development/_task-card.md` |
| 〔教学交付 相关任务〕 | `teaching-delivery` | `10-workflows/teaching-delivery/_task-card.md` |
| 〔续费复购转介绍 相关任务〕 | `renewal-referral` | `10-workflows/renewal-referral/_task-card.md` |
| 跨工作流的方法论/实体 | 共享知识，非工作流 | `20-knowledge/` |

## 六、目录主轴

```text
00-org/         DRI 责任地图 + 黑话词典
10-workflows/   主轴：工作流（每条 = 任务卡 + context + sop + evals）
20-knowledge/   跨工作流复用的方法论/实体
30-raw/         原始大文件索引（不复制）
90-governance/  准入/定版/权限/同步/进化
```

## 七、工具约定

- 本地库 = 知识生产车间；协作平台（飞书等）= 前台，定版后单向同步（见 `90-governance/feishu-sync.md`）。
- 原始大文件（PPT/视频/图片）留原地，`30-raw/` 仅索引引用。
- 用户没有明确要 agent 改库时，先产出建议或草稿；涉及定版、权限、同步时要提示人工审核。

## 八、一句话总纲

> 不要让用户翻箱倒柜。判断任务属于哪条工作流 -> 读任务卡 -> 带全上下文 -> 执行 -> 按 evals 验收。
> 目标不是找到文件，是带着正确上下文把事做对。
