# 贡献指南（Agent-Security）

本仓库用于沉淀智能体安全相关知识与复现过程。为了让内容 **可检索、可复现、可协作**，请遵循以下约定。

## 新增内容放哪里
- 论文阅读：`papers/`
- 复现记录：`reproductions/`
- 实验/评测：`experiments/`
- 公开事件复盘：`incidents/`
- 工具与脚本使用说明：`tooling/`
- 资料与链接汇总：`resources/`

各目录下的 `README.md` 会说明更细的放置规则。

## 文件命名约定
建议使用：
- 论文笔记：`YYYY-paper-short-title.md` 或 `YYYY-venue-short-title.md`
- 复现/实验：`YYYY-MM-DD-short-title.md`
- 会议纪要：`YYYY-MM-DD-topic.md`

标题尽量短，包含关键词，避免“notes/记录”这类信息密度低的词。

## 统一元数据（推荐）
建议在 Markdown 顶部加入 YAML Front Matter，便于后续搜索与自动化：
```yaml
---
title: ...
date: 2026-03-12
owners: [team-or-person]
status: draft|active|done|blocked
tags: [prompt-injection, tool-use, rce]
sources:
  - type: paper|blog|repo|talk
    ref: ...
---
```

## 可复现与可验证
- 写清：环境（OS/依赖/模型/版本）、步骤、输入输出、结论与局限
- 结果尽量有截图/日志片段/统计表（注意脱敏）
- 如果结论依赖某个代码版本，请引用 commit hash 或 release tag

## 安全与合规（必须）
- 不要提交任何密钥、token、内部 URL、客户数据、受限数据、未公开漏洞细节
- 涉及红队/漏洞利用内容时：确保只引用公开信息，并写明适用范围与风险提示
- 如需放置敏感材料：请改用内部受控系统并在此处仅保留索引（不含敏感内容）

## PR/提交建议
- 一个 PR 聚焦一个主题（一个论文/一次复现/一个方法总结）
- PR 描述里写明：动机、主要新增、验证方式（复现结果/对照实验）
- 使用 `.github/PULL_REQUEST_TEMPLATE.md`（如存在）

## 模板
模板集中在 `resources/templates/`，建议复制后再填写：
- `resources/templates/paper-note-template.md`
- `resources/templates/reproduction-template.md`
- `resources/templates/experiment-template.md`
