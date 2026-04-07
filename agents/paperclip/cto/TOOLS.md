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



## 角色补充

- 代码与仓库：以 `git`、测试与 CI 输出为准，不凭印象断言。
- 与 CEO：战略冲突或资源缺口及时升级；与董事会交互遵循工单交接政策。
