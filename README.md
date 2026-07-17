# 🧭 认知导航 · 标杆案例

## 阿里 Qoder CN 三Agent金融尽调合规验证

---

### 案例概述

本案例展示认知导航在**阿里Qoder CN平台**上，完成三Agent群协作金融尽调合规验证的完整过程。

| 项目 | 描述 |
|------|------|
| 平台 | 阿里 Qoder CN（个人版） |
| 场景 | 跨境并购 AI 金融科技公司合规尽调 |
| Agent 链路 | 法规研究员 → 合规分析师 → 报告撰写官 |
| 诊断引擎 | 认知导航 API |
| 产出 | 8 章节完整尽调报告 + 量化诊断数据 |

---

### 核心数据

#### 三 Agent 诊断一致性

| Agent | S | T | C | D | zone |
|-------|---|---|---|---|------|
| 法规研究员 | 0.65 | 0.95 | 0.20 | 0.10 | YELLOW |
| 合规分析师 | 0.65 | 0.95 | 0.20 | 0.10 | YELLOW |
| 报告撰写官 | 0.65 | 0.95 | 0.20 | 0.10 | YELLOW |

三个独立 Agent 调用同一诊断引擎，输出完全一致，证明引擎稳定可靠。

#### 易用学公式验证

核心公式：**S = T - C - D**

| 组别 | T - C - D | 实际 S | 验证 |
|------|-----------|--------|------|
| 基线组 | 0.70 - 0.20 - 0.10 = 0.40 | 0.40 | ✅ |
| 增强组 | 0.72 - 0.19 - 0.10 = 0.43 | 0.43 | ✅ |
| 诊断驱动组 | 0.75 - 0.18 - 0.10 = 0.47 | 0.47 | ✅ |

**结论**：健康度 S = 转化力 T - 约束力 C - 内耗 D，在全部 15 个测试用例中 100% 吻合。

---

### 最终报告结构

```

AI 金融科技公司合规风险尽调报告
├── 一、公司基本情况
├── 二、欧盟层面合规分析（EU AI Act / GDPR / MiFID II / DORA）
├── 三、美国层面合规分析（联邦 + 各州）
├── 四、跨境合规特有风险
├── 五、关键风险矩阵（P0/P1/P2 分级）
├── 六、认知导航诊断（S/T/C/D/zone 量化解读）
├── 七、行动计划与建议
└── 八、总结与关键结论

```

---

### 标杆意义

| 维度 | 成果 |
|------|------|
| 协作流程 | ✅ 三 Agent 完整接力跑通 |
| 诊断一致性 | ✅ 三个 Agent 输出完全一致 |
| 公式验证 | ✅ S = T - C - D，15/15 通过 |
| 报告产出 | ✅ 8 章节，可对外展示 |
| 平台验证 | ✅ 阿里 Qoder CN 真实环境 |

---

### 产品矩阵

认知导航产品体系由三个公开仓库组成，覆盖**引擎 → 协作 → 落地**完整链路：

| 仓库 | 定位 | 角色 |
|------|------|------|
| [agent-trace-diagnostics](https://github.com/wwreixi/agent-trace-diagnostics) | Agent 运行时认知安全诊断工具（基于动力学系统理论） | 🔧 核心引擎 |
| [multi-agent-collaboration-navigation](https://github.com/wwreixi/multi-agent-collaboration-navigation) | 多 Agent 群协作合规质量验证与实时干预 | 🔗 协作框架 |
| [cognitive-navigation-showcase](https://github.com/wwreixi/cognitive-navigation-showcase) | 标杆案例：三 Agent 金融尽调合规验证 | 📋 落地验证（本仓库） |

```
agent-trace-diagnostics          multi-agent-collaboration-navigation
    (核心诊断引擎)                        (群协作导航框架)
         │                                    │
         └──────────────┬─────────────────────┘
                        ▼
          cognitive-navigation-showcase
            (标杆案例 · 落地验证)
```

---

### 相关文档

**基础文档**

- [商业价值简报](./docs/business-brief.md)
- [完整尽调报告](./examples/final-report.md)
- [Agent 配置参考](./agents/agent-config.md)
- [理论框架简介](./docs/theory-framework.md)

**WorkBuddy 平台复现测试（双组对比）**

| 场景 | A 组（无认知导航） | B 组（有认知导航） | 对比报告 |
|------|------|------|------|
| 三 Agent 金融尽调 | [基线报告](./examples/workbuddy-group-a-baseline.md) | [诊断报告](./examples/workbuddy-group-b-diagnosis.md) | [对比报告](./examples/workbuddy-comparison-report.md) |
| 五 Agent 代码编写 | [基线报告](./examples/code-test-group-a-baseline.md) | [诊断报告](./examples/code-test-group-b-diagnosis.md) | [对比报告](./examples/code-test-comparison-report.md) |

---

### 如何复现

#### 前置条件

- Python 3.10+
- 认知导航诊断引擎（参见 [agent-trace-diagnostics](https://github.com/wwreixi/agent-trace-diagnostics)）
- 支持 Agent 群协作的平台（如阿里 Qoder CN）

#### 快速步骤

```bash
# 1. 克隆本仓库
git clone https://github.com/wwreixi/cognitive-navigation-showcase.git
cd cognitive-navigation-showcase

# 2. 启动诊断引擎（默认 8000 端口）
#    详见 agent-trace-diagnostics 仓库的 README
python -m agent_trace_diagnostics.server

# 3. 按三 Agent 链路依次执行
#    法规研究员 → 合规分析师 → 报告撰写官
#    每个 Agent 执行完毕后调用诊断 API 获取 S/T/C/D/zone
#    配置参考见 agents/agent-config.md

# 4. 验证诊断一致性
#    三个 Agent 的输出应完全一致（本案例：0.65/0.95/0.20/0.10/YELLOW）

# 5. 生成报告
#    参照 examples/final-report.md 结构组装最终尽调报告
```

#### 诊断 API 调用示例

```python
import requests

resp = requests.post(
    "http://localhost:8000/diagnosis",
    json={"query": "法规/风险摘要文本"}
)
print(resp.json())
# {'S': 0.65, 'T': 0.95, 'C': 0.20, 'D': 0.10, 'zone': 'YELLOW'}
```

#### 公式验证

复现后可用以下公式校验诊断引擎输出：

```
S = T - C - D
```

在 GREEN 区（S ≥ 0.70）为健康，YELLOW 区（0.30 ~ 0.70）需关注，RED 区（< 0.15）需立即干预。

---

### License

本项目基于 [MIT License](./LICENSE) 开源，欢迎引用和二次开发。

---

**案例状态**：✅ 已完成 | **最后更新**：2026 年 7 月
