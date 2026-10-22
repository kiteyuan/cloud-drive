# 纸鸢下载 MCP 工具参考

入口：`https://mybt.kiteyuan.info/api/v1/mcp`  
Token 管理：`https://mybt.kiteyuan.info/mcp`（需登录）

鉴权：`Authorization: Bearer <mcp_token>`

## 转存任务

### magnet_task_add

将 magnet / ed2k / 夸克·UC·迅雷·PikPak 分享链接转存到纸鸢网盘。

| 参数 | 说明 |
|------|------|
| `magnet` | 必填 |
| `drive_parent_id` | 可选，网盘父目录 |

### magnet_task_list

| 参数 | 说明 |
|------|------|
| `limit` / `offset` | 可选 |

### task_get_status

| 参数 | 说明 |
|------|------|
| `task_id` | 可选 |
| `task_ids` | 可选，批量 |

### task_delete

| 参数 | 说明 |
|------|------|
| `task_id` | 必填 |

## 任务内文件

### files_list_dir

| 参数 | 说明 |
|------|------|
| `task_id` | 必填 |
| `parent_id` / `page_token` / `limit` | 可选 |

### files_get_detail

| 参数 | 说明 |
|------|------|
| `task_id` / `file_id` | 必填 |

### files_get_play_link / files_get_download_link

| 参数 | 说明 |
|------|------|
| `task_id` / `file_id` | 必填 |

## 网盘与回收站

### drive_list

| 参数 | 说明 |
|------|------|
| `parent_id` | 可选 |
| `scope` | 可选，`"trash"` 列回收站 |
| `limit` / `offset` | 可选 |

### drive_get / drive_create_folder / drive_rename / drive_move / drive_trash / drive_restore / drive_purge

按工具名字面含义使用；`drive_create_folder` 需 `name`，其余一般需 `id`。

### drive_batch

| 参数 | 说明 |
|------|------|
| `action` | `trash` / `restore` / `purge` |
| `ids` | 字符串数组 |

### drive_empty_trash

无参数。清空回收站。

## 其他

### storage_get_status

查询网盘空间与积分。无参数。

### blindbox_get_random_magnet

随机获取一个盲盒磁力链接。无参数。
