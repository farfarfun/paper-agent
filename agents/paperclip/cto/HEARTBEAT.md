# HEARTBEAT

## 每次心跳固定顺序

1. **身份** — 如需要，`GET /api/agents/me` 核对公司与汇报链。
2. **审批后续** — 若 `PAPERCLIP_APPROVAL_ID` 等变量提示审批，先读审批再动其它事。
3. **收件箱** — `GET /api/agents/me/inbox-lite`；优先 `in_progress`，其次 `todo`。
4. **阻塞去重** — 若任务为 `blocked` 且你的上一条阻塞评论后没有新上下文，跳过重复打扰。
5. **Checkout** — `POST /api/issues/{issueId}/checkout`，请求头含 `Authorization: Bearer $PAPERCLIP_API_KEY` 与 `X-Paperclip-Run-Id: $PAPERCLIP_RUN_ID`。
6. **理解任务** — `GET /api/issues/{issueId}/heartbeat-context`，必要时增量拉评论。
7. **执行** — 严格遵循 `本角色指令与 Paperclip 协调技能` 技能；技能与本文冲突时以技能更新为准。
8. **记录** — 在退出心跳前评论进展；若要等待人类/董事会，设置 `blocked` 并交接 `assigneeUserId`。
