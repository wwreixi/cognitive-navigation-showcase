# 🧭 认知导航 · 标杆案例库

## 单点诊断 → 会话级导航 → 群体协同：三层能力闭环验证

---

### 能力矩阵总览

| 层级 | 能力 | 标志性验证 | 核心数据 | 完整报告 |
|:---|:---|:---|:---|:---|
| **Loop1 单点诊断** | 逐轮推理健康度实时量化（S/T/C/D） | 12道逻辑/数学题全类型诊断 | S均值 0.415，12/12公式验证，3/3 trigger覆盖 | — |
| **Loop2 会话级导航** | 长会话耗散监控 + RESET_CONTEXT纠偏 | 8轮商业选址对照测试 | 终态S提升 **18.4%**，陷阱冲击检测 **5.7x** | [📊 查看报告](./reports/loop2-session-navigation-report.html) |
| **Loop3 群体协同** | 多Agent群协作合规验证 | 阿里Qoder CN三Agent金融尽调 | S提升 **17.5%**，三Agent诊断一致性 **100%** | [📋 完整尽调报告](./examples/final-report.md) |

---

### Loop1：单点诊断（已验证）

对每一次推理输出 S（健康度）、T（转化力）、C（约束力）、D（内耗）四项量化指标，核心公式 **S = T - C - D** 在全部测试用例中 100% 成立。

| 验证场景 | 规模 | S均值 | 公式验证 | trigger覆盖 |
|:---|:---|:---|:---|:---|
| 12道逻辑/数学/主观题诊断 | 12题 | 0.415 | 12/12 ✅ | high_dissipation / low_constraint / S_continuous_decline |
| 三Agent金融尽调逐轮诊断 | 15用例 | 0.40→0.47 | 15/15 ✅ | 覆盖全警戒区（GREEN/YELLOW/ORANGE/RED） |

> 详见 [理论框架简介](./docs/theory-framework.md) 和 [商业价值简报](./docs/business-brief.md)

---

### Loop2：会话级导航（新增 ✨）

**长会话持续监控 + 智能纠偏干预**，以「餐饮门店选址连续商业推演」为统一主线，通过8轮对照实验验证：

#### 核心结论

| 指标 | 对照组（无导航） | 实验组（有导航） | 差异 |
|:---|:---|:---|:---|
| 终态S值 | 0.385 | **0.456** | **+18.4%** |
| 最终决策 | 基于错误参数推荐选址 | 基于正确参数理性决策 | 业务价值显著 |
| 参数错误识别 | 复盘未发现任何错误 | 完整识别陷阱+纠正过程 | 自省能力质的差距 |

#### 三项关键发现

| 发现 | 数据 | 含义 |
|:---|:---|:---|
| **干扰分层效应** | 陷阱冲击是噪音的 **5.7倍** | 错误前提植入比冗余信息干扰破坏性强一个数量级 |
| **纠偏延迟恢复** | RESET_CONTEXT后需 **2轮固化期** | 纠偏需配合跟踪确认机制，非即时生效 |
| **S值盲区** | 内部一致的错误推理可产出高S值 | 健康度指标需"前提校验"机制补充 |

[📊 查看完整报告](./reports/loop2-session-navigation-report.html)

---

### Loop3：群体协同

**阿里 Qoder CN 三Agent金融尽调合规验证**，展示多Agent群协作场景下认知导航的合规质量保障能力。

#### 三 Agent 诊断一致性

| Agent | S | T | C | D | zone |
|-------|---|---|---|---|------|
| 法规研究员 | 0.65 | 0.95 | 0.20 | 0.10 | YELLOW |
| 合规分析师 | 0.65 | 0.95 | 0.20 | 0.10 | YELLOW |
| 报告撰写官 | 0.65 | 0.95 | 0.20 | 0.10 | YELLOW |

三个独立 Agent 调用同一诊断引擎，输出完全一致，证明引擎稳定可靠。

#### 最终报告结构

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

#### 跨平台验证矩阵（铁三角）

| 平台 | 场景 | S值 | 验证状态 |
|:---|:---|:---|:---:|
| 阿里 Qoder CN | 三Agent金融尽调 | 0.65 | ✅ |
| 智谱 Z Code | 三Agent合规分析 | 0.08 | ✅ |
| WorkBuddy | 双组对照（Agent群） | 0.40→0.47 | ✅ |

---

### 标杆意义总结

| 维度 | Loop1 单点诊断 | Loop2 会话级导航 | Loop3 群体协同 |
|:---|:---|:---|:---|
| 协作流程 | 单轮检测 | 长会话全链路 | 多Agent接力 |
| 诊断一致性 | 全轮次S=T-C-D成立 | 16/16会话级验证 | 三Agent完全一致 |
| 纠偏能力 | — | ✅ RESET_CONTEXT | — |
| 平台验证 | Qoder CN + WorkBuddy | WorkBuddy | Qoder CN + Z Code + WorkBuddy |
| 业务价值 | 逐轮质量保障 | 长会话可信度提升18.4% | 群协作合规一致性100% |

---

### 产品矩阵

认知导航产品体系由三个公开仓库组成，覆盖**引擎 → 协作 → 落地**完整链路：

| 仓库 | 定位 | 角色 |
|------|------|------|
| [agent-trace-diagnostics](https://github.com/wwreixi/agent-trace-diagnostics) | Agent 运行时认知安全诊断工具（基于动力学系统理论） | 🔧 核心引擎 |
| [multi-agent-collaboration-navigation](https://github.com/wwreixi/multi-agent-collaboration-navigation) | 多 Agent 群协作合规质量验证与实时干预 | 🔗 协作框架 |
| [cognitive-navigation-showcase](https://github.com/wwreixi/cognitive-navigation-showcase) | 标杆案例库：单点→会话→群体三层验证（本仓库） | 📋 落地验证 |

```
agent-trace-diagnostics          multi-agent-collaboration-navigation
    (核心诊断引擎)                        (群协作导航框架)
         │                                    │
         └──────────────┬─────────────────────┘
                        ▼
          cognitive-navigation-showcase
        (标杆案例库 · 三层能力闭环验证)
```

---

### 相关文档

**三层能力报告**

| 层级 | 文档 | 说明 |
|:---|:---|:---|
| 总览 | [商业价值简报](./docs/business-brief.md) | 三层能力矩阵 + 竞品对比 + 目标客户 |
| Loop2 | [Loop2 会话级导航验证报告](./reports/loop2-session-navigation-report.html) | 8轮对照测试完整数据与可视化 |
| Loop3 | [完整尽调报告](./examples/final-report.md) | 三Agent金融尽调8章节报告 |
| 基础 | [理论框架简介](./docs/theory-framework.md) | 易用学·认知导航理论基础 |
| 配置 | [Agent 配置参考](./agents/agent-config.md) | 三Agent配置参数 |

**平台复现测试（双组对比）**

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

# 3. 按三层能力逐级验证
#    Loop1：单题诊断 → S/T/C/D 公式验证
#    Loop2：长会话对照测试 → 8轮推理 + RESET_CONTEXT
#    Loop3：多Agent群协作 → 三Agent合规尽调

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

**案例状态**：✅ 三层能力闭环已完成 | **最后更新**：2026 年 7 月
