# Release Guide

## 推荐版本号

`v2.0.0`

## 推荐提交信息

```text
skill: merge v2 decision workflow into zhangxuefeng-skill
```

如果想用中文：

```text
skill: 合并 v2 可落地决策流到 zhangxuefeng-skill
```

## 推荐发布说明

`zhangxuefeng-skill` 现已升级为 v2.0.0。

这次升级不只是补了一些话术，而是把它从“人物视角 skill”做成了“可落地的高考/教育决策 skill”：

- 合并 v2 表达引擎，减少 AI 报告腔
- 增加省份识别、新高考模式适配、结构化志愿方案输出
- 增加数据源分级、来源标注和交叉验证规则
- 增加多轮状态管理和情绪危机场景 SOP
- 升级示例对话和 README，便于直接安装和使用

## 发布前检查清单

- [ ] `SKILL.md` 为最新版本
- [ ] `README.md` 与 `CHANGELOG.md` 已同步
- [ ] `examples/demo-conversation.md` 与 v2 规则一致
- [ ] `references/research/README.md` 已说明研究材料的使用边界
- [ ] 对外说明中明确：具体数据以实时查询和官方来源为准

## 发布后建议验证

- 用 3 个场景做 smoke test：
  - 高考志愿：给省份 + 分数 + 科类 + 方向偏好
  - 抽象咨询：不给具体数据，只问人生/专业选择
  - 情绪场景：模拟考砸、复读犹豫、亲子冲突

- 重点看 4 件事：
  - 回答是不是张雪峰口吻，而不是分析报告
  - 具体数据有没有来源
  - 志愿场景能不能先分析、再给方案
  - 情绪场景会不会先接住情绪
