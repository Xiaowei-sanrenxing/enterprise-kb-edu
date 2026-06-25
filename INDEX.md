# INDEX · 〔机构名〕 全库索引

> 给 agent 的快速地图。新用户先看 [`START-HERE.md`](./START-HERE.md)，agent 先用 [`AGENTS.md`](./AGENTS.md) 路由，再用本页定位具体资产。

## 使用入口

- `START-HERE.md` — 新用户的一句话启动入口：先问角色，再进入对应路径
- `AGENTS.md` — agent 执行协议：判断工作流、读取任务卡、带上下文执行、自检
- `CLAUDE.md` — Claude Code 使用本库时的行为约定
- `客户使用手册.md` — 面向客户/团队的完整白话说明
- `话术速查卡.md` — 不知道怎么跟 AI 开口时可直接复制的提示词
- `谁读库指引.md` — 谁负责读库、谁负责补事实、谁负责审核的说明
- `待填清单.md` — 初始化知识库时需要补齐的占位符清单

## 角色路径

- 老板/负责人 — 让 agent 做全库体检、缺口盘点、边界确认和定版审核
- DRI/部门主管 — 让 agent 进入负责的工作流，补资产、产草稿、做复盘
- 普通员工 — 描述具体任务和已知事实，由 agent 判断工作流并执行
- 知识库维护者 — 检查草稿、权限、索引、同步、进化日志和待定版资产
- agent — 按 `AGENTS.md -> _task-card.md -> context -> permissions/lifecycle -> evals` 执行

## 工作流资产清单

- **获客引流** `10-workflows/traffic-acquisition/` — 把潜在家长/学员从公域引到私域或到店
- **销售转化** `10-workflows/sales-conversion/` — 把线索从首触推进到报名成交或明确流失
- **课程研发** `10-workflows/course-development/` — 课程设计、课件讲义、迭代更新
- **教学交付** `10-workflows/teaching-delivery/` — 排课上课、作业答疑、学员陪跑
- **续费复购转介绍** `10-workflows/renewal-referral/` — 续班、口碑裂变、老带新

## 共享知识 20-knowledge/

跨工作流复用的方法论、实体、品牌、产品、案例和标准表达，按需补充。

## 组织上下文 00-org/

- `dri-map.md` — 每条工作流的负责人
- `glossary.md` — 公司术语、行业黑话和关键实体
- `roles-and-agent-usage.md` — 老板、DRI、普通员工、知识库维护者和 agent 的使用边界

## 原始源 30-raw/

- `原始素材索引.md` — 指向原始大文件（录音/PPT/客户对话），不复制

## 治理 90-governance/

- `intake-rules.md` — 新材料怎么入库
- `lifecycle.md` — 草稿、审核、定版、废弃的生命周期
- `permissions.md` — 权限、隐私、对外使用边界
- `feishu-sync.md` — 定版内容如何同步到协作平台
- `进化日志.md` — 记录踩坑、客户反馈、红线拦截和未覆盖的新情况
- `进化复盘SOP.md` — 定期把进化日志复盘回流为稳定资产

---

> 建库日期：2026-06-25 ｜ 维护：〔知识库负责人〕
