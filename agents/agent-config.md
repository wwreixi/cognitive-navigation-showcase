# Agent 配置参考

## 三 Agent 角色定义

| Agent | 角色 | 核心任务 | 工具权限 |
|-------|------|----------|----------|
| `financial-researcher` | 法规研究员 | 搜集 EU AI Act、GDPR、美国联邦/州级法规 | WebSearch, WebFetch |
| `financial-compliance-analyst` | 合规分析师 | 识别风险点，P0/P1/P2 分级评估 | WebSearch, WebFetch, Read |
| `report-writer` | 报告撰写官 | 整合输出，生成尽调报告 | Read, Write, Grep, Glob |

---

## 核心指令摘要

### 法规研究员

```

完成法规搜集后，必须调用认知导航 API：

· 端点：http://host.docker.internal:8000/diagnosis
· 请求体：{"query": "法规摘要"}
· 输出：S/T/C/D/zone

```

### 合规分析师

```

基于法规摘要，识别风险点并按 P0/P1/P2 分级
必须调用认知导航 API 进行诊断

```

### 报告撰写官

```

整合法规摘要和风险分析
必须调用认知导航 API 进行最终诊断
输出 8 章节完整尽调报告

```

---

## 执行流程

```

@financial-researcher → 法规摘要
@financial-compliance-analyst → 风险分析
@report-writer → 最终报告

```

---

## API 调用示例

```python
import requests
r = requests.post(
    'http://host.docker.internal:8000/diagnosis',
    json={"query": "法规/风险摘要"}
)
print(r.json())
```

返回示例：

```json
{
  "S": 0.65,
  "T": 0.95,
  "C": 0.20,
  "D": 0.10,
  "zone": "YELLOW"
}
```
