# 01 证据台账（CEO大模型 · AI 产品经理优化版）

## 0. 文件清单与 AI PM 能力标签

| 文件ID | 文件名 | AI PM 能力标签 | 贡献类型 |
|---|---|---|---|
| F001 | CEO大模型_项目总览.md | 全局 | 项目背景/架构/成果/复盘 |
| F002 | 销售agent-商机+日报+聊天分析交接文档.md | ETL/工作流/数据表 | 数据源/字段/定时任务/API |
| F003 | CEO大模型项目分析报告.md | 全局 | 竞品/定位/风险 |
| F004 | CEO大模型产品经理工作流程与接手指南.md | 方法论 | 角色/流程/工具 |
| F005 | 优化方案_Fix_Manager_Issues.md | Prompt Engineering | 防幻觉/代码清洗/溯源 |
| F006 | 管家Agent项目深度分析与SOP方案.md | Agent 架构 | 架构重构/SOP |
| F007 | 管家部agent需求.md（15,911字） | Agent 架构 | PRD/需求设计 |
| F008 | 管家部agent需求—AI回访+话术.md（11,269字） | RAG/Prompt | AI功能PRD |
| F009 | 12月复盘-CEO大模型.md | 方法论 | 里程碑/复盘 |
| F010 | 各 PRD 文档（×15+） | 工作流/Agent/数据 | 需求输出物 |

## 1. 证据声明表（Claim Schema）

### 核心指标类

| claim_id | claim_text | AI PM 能力维度 | metric_level | evidence_strength | source | defense_speech |
|---|---|---|---|---|---|---|
| C001 | 项目为 CRM 型 AI 效能平台，后续规划 SaaS to-B | 项目定性 | factual | 🟢 strong | F001 L7-14 | 基于项目总览文档和团队沟通确认 |
| C002 | 覆盖管家 Agent + 销售 Agent 双 Agent 架构 | Agent 架构 | factual | 🟢 strong | F001 L128-129 | 已上线两大 Agent 工作台 |
| C003 | 接入 5 大数据源（CRM/KICP/在线客服/企微/见鱼） | ETL 数据治理 | factual | 🟢 strong | F002 全文 | 交接文档有完整 API 和字段定义 |
| C004 | 8+ 功能模块持续上线 | Agent 架构 | factual | 🟢 strong | F001 L71-93 | PRD 清单可一一对应 |
| C005 | 33 份 PRD/需求/交接文档 | 产出密度 | factual | 🟢 strong | 文件系统 | 可逐一打开验证 |

### AI 工作流类

| claim_id | claim_text | AI PM 能力维度 | metric_level | evidence_strength | source | defense_speech |
|---|---|---|---|---|---|---|
| C006 | 4 条 Dify 工作流（出题/日报/KP/话术） | Dify 工作流 | factual | 🟢 strong | F001 L83-87, F002 L472-576 | 有 API Key 和工作流配置可追溯 |
| C007 | 考试 4h→10min（95.8%） | Dify 工作流 | derived | 🟢 derived | F001 L155 | 前后时长对比，可按公式复算 |
| C008 | 日报 2h→30min（83.3%） | Dify 工作流 | derived | 🟢 derived | F001 L156 | 调研报告确认的口径 |
| C009 | 工资 30min→秒级（99%+） | 数据产品 | derived | 🟢 derived | F001 L158 | "秒级"为区间口径 |
| C010 | 播报 1-2h/次→0 耗时 | 定时任务 | derived | 🟢 derived | F001 L159 | 人工环节被自动化替代 |
| C011 | 管家查数 3min→10s（~94%） | ETL 数据治理 | estimated | 🟠 estimated | F001 L157 | 按步骤时长估算，非埋点 |

### Prompt Engineering 类

| claim_id | claim_text | AI PM 能力维度 | metric_level | evidence_strength | source | defense_speech |
|---|---|---|---|---|---|---|
| C012 | 出题格式错误率 15%-20%（优化前） | Dify 工作流 | estimated | 🟠 estimated | F001 L225 | 历史反馈区间，非当前生产值 |
| C013 | 生成→校验→修正三步链路设计 | Dify 工作流 | factual | 🟢 strong | F001 L86, F005 | 已上线运行 |
| C014 | ETL 聚合替代实时 API 方案决策 | ETL 数据治理 | factual | 🟢 strong | F001 L136 | 已实施 |
| C015 | Token 成本 3000→600（月，~80%） | Prompt Engineering | estimated | 🟠 estimated | F001 L151 | 按团队规模估算 |

### Prompt 防幻觉类

| claim_id | claim_text | AI PM 能力维度 | metric_level | evidence_strength | source | defense_speech |
|---|---|---|---|---|---|---|
| C016 | 经理日报幻觉问题（Compliance Bias） | Prompt Engineering | factual | 🟢 strong | F005 L5-30 | 有问题描述和根因分析文档 |
| C017 | 归属错配问题（Context Bleeding） | Prompt Engineering | factual | 🟢 strong | F005 L31-50 | 有具体案例和修复方案 |
| C018 | 防幻觉熔断协议设计 | Prompt Engineering | factual | 🟢 strong | F005 L60-90 | 有完整 Prompt 设计文档 |
| C019 | 溯源锚定机制设计 | Prompt Engineering | factual | 🟢 strong | F005 L91-120 | 有完整 Prompt 设计文档 |
| C020 | 前置 Python 代码节点设计 | Prompt Engineering | factual | 🟢 strong | F005 L121-165 | 有完整代码和逻辑说明 |

### RAG 知识库类

| claim_id | claim_text | AI PM 能力维度 | metric_level | evidence_strength | source | defense_speech |
|---|---|---|---|---|---|---|
| C021 | RAG 知识库 + 6 大回访场景 | RAG 知识库 | factual | 🟢 strong | F008 全文 | 有完整 PRD（11,269 字） |

### 数据架构类

| claim_id | claim_text | AI PM 能力维度 | metric_level | evidence_strength | source | defense_speech |
|---|---|---|---|---|---|---|
| C022 | 8 张核心数据表字段设计参与 | ETL 数据治理 | factual | 🟢 strong | F002 L108-458 | 交接文档有完整字段清单 |
| C023 | 15+ APScheduler 定时任务 | ETL 数据治理 | factual | 🟢 strong | F002 L439-457 | 交接文档有完整任务列表 |
| C024 | 数据匹配规则（三重匹配） | ETL 数据治理 | factual | 🟢 strong | F002 L459-471 | 有详细匹配逻辑说明 |

### 数据口径治理类

| claim_id | claim_text | AI PM 能力维度 | metric_level | evidence_strength | source | defense_speech |
|---|---|---|---|---|---|---|
| C025 | 百度渠道口径冲突发现与治理 | 数据产品 | factual | 🟢 strong | F001 L211-217 | 有问题描述和处置方案 |
| C026 | "先定义口径再展示数据"规范 | 数据产品 | factual | 🟢 strong | F001 L211-217 | 已落地到 PRD 规范 |

### 角色边界与方法论类

| claim_id | claim_text | AI PM 能力维度 | metric_level | evidence_strength | source | defense_speech |
|---|---|---|---|---|---|---|
| C027 | 角色边界：产品侧 Owner | 角色 | factual | 🟢 strong | F004 L14-18 | 工作流程文档明确分工 |
| C028 | 4 轮一线用户调研 | 方法论 | factual | 🟢 strong | F001 L119-124 | 有调研对象和反馈 |
| C029 | 竞品分析（管家+销售双方向） | 方法论 | factual | 🟢 strong | F003 | 有完整竞品分析报告 |

### 估算/成本类

| claim_id | claim_text | AI PM 能力维度 | metric_level | evidence_strength | source | defense_speech |
|---|---|---|---|---|---|---|
| C030 | 年化节省 3-5 万（estimated） | 商业价值 | estimated | 🟠 estimated | F001 L152 | 区间估算，不替代财务审计 |

## 2. 数据差距问卷

| 差距项 | 当前状态 | 理想状态 | 风险等级 | 面试应对 |
|---|---|---|---|---|
| 管家查数精确效率 | 流程测算（94%） | 系统埋点 | 🟠 中 | 标注为估算，先讲口径再讲结论 |
| Token 成本精确值 | 团队规模估算 | 调用日志/账单 | 🟠 中 | 讲假设条件和计算方法 |
| 年化节省精确值 | 区间估算 | 财务凭证 | 🟠 中 | 给区间，不做硬承诺 |
| 出题格式错误率 | 历史反馈区间 | A/B 测试数据 | 🟡 低 | 用于解释改造必要性，非质量承诺 |

## 3. 冲突处理规则

1. 以主证据文档（F001/F002/F005）为准
2. 历史包装文案降权处理
3. 估算值显式标注，不与精确值混讲
4. 角色边界严格遵循 F004 定义

来源: 2026-02-19 | 全量源文件交叉校验
