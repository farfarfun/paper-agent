# 工具与技能索引

## Paperclip API（ASCII）

- `GET /api/agents/me`
- `GET /api/agents/me/inbox-lite`
- `POST /api/issues/{issueId}/checkout`
- `GET /api/issues/{issueId}/heartbeat-context`
- `PATCH /api/issues/{issueId}`（状态、评论字段视情况而定）
- `POST /api/issues/{issueId}/comments`

## 环境变量（ASCII）

- `PAPERCLIP_API_URL` `PAPERCLIP_API_KEY` `PAPERCLIP_RUN_ID` `PAPERCLIP_AGENT_ID` `PAPERCLIP_COMPANY_ID`
- 任务唤醒场景可能还有 `PAPERCLIP_TASK_ID`、`PAPERCLIP_WAKE_COMMENT_ID` 等。

## 工单交接（与人类/董事会）

阻塞在人类侧时：评论说明已完成项与所需决策 → `assigneeUserId` 指向请求方 → `assigneeAgentId` 清空 → `blocked`。



## 强制技能

- `superpowers:receiving-code-review` — 权威流程与门槛以该技能为准。
