---
name: drive-mcp
description: >-
  Connects an AI agent to 纸鸢下载 / 纸鸢网盘 via MCP to add magnet/ed2k/share transfer
  tasks, browse drive files, play/download links, and manage trash. Use when the
  user wants agent-driven cloud-drive ops through mybt.kiteyuan.info MCP.
---

# 纸鸢下载 · MCP 网盘操作

通过纸鸢下载官方 **MCP**，让 Agent 代为提交转存任务、浏览网盘、取播放/下载链接、管理回收站等。

## 前置条件（必须先做）

1. 打开 [纸鸢下载 MCP 页](https://mybt.kiteyuan.info/mcp) 并**登录账号**。
2. 在页面上**生成 / 重置 MCP Token**（明文仅当次可见；丢失需重新生成）。
3. 将 Token 配进 Agent 的 MCP 客户端。未登录或 Token 无效会 401。

## MCP 连接

- Token 管理页：`https://mybt.kiteyuan.info/mcp`
- Streamable HTTP 入口：`https://mybt.kiteyuan.info/api/v1/mcp`
- 鉴权：`Authorization: Bearer <mcp_token>`（不要放进 URL query）

```json
{
  "mcpServers": {
    "kiteyuan-drive": {
      "url": "https://mybt.kiteyuan.info/api/v1/mcp",
      "headers": {
        "Authorization": "Bearer <mcp_token>"
      }
    }
  }
}
```

工具名与参数见 [reference.md](./reference.md)。

## 何时使用

- 用户要用 Agent **转存** magnet / ed2k / 夸克·UC·迅雷·PikPak 分享链
- 用户要 **列目录、重命名、移动、回收站**
- 用户要取 **在线播放 / 下载** 直链，或查 **积分与空间**

## Agent 工作流

1. 确认 MCP 已连接；401 则让用户回 MCP 页检查登录与 Token。
2. 转存：`magnet_task_add` → `magnet_task_list` / `task_get_status` 跟进度。
3. 任务内文件：`files_list_dir` → `files_get_play_link` / `files_get_download_link`。
4. 网盘文件树：`drive_list` / `drive_get` / `drive_create_folder` / `drive_rename` / `drive_move`。
5. 回收站：`drive_trash` / `drive_restore` / `drive_purge` / `drive_batch` / `drive_empty_trash`。
6. 空间与积分：`storage_get_status`。

## 注意

- Token 等同账号凭证，勿提交公开仓库或发给不可信方。
- 下载请优先提示用户用 HTTP 直链；多线程下载器有时会触发风控。
- 不要编造未通过 MCP 返回的任务、文件或链接。
