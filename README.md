<div align="center">

<img src="./favicon.ico" width="72" height="72" alt="纸鸢下载" />

# 纸鸢下载

**磁力转存 · 网盘文件 · 在线播放 · Agent / MCP 可接入**

[![Website](https://img.shields.io/badge/Website-kiteyuan.info-0ea5e9?style=flat-square)](https://kiteyuan.info/)
[![Web](https://img.shields.io/badge/Web-mybt.kiteyuan.info-22c55e?style=flat-square)](https://mybt.kiteyuan.info/)
[![Client](https://img.shields.io/badge/Client-drive.kiteyuan.info-f59e0b?style=flat-square)](https://drive.kiteyuan.info/)
[![MCP](https://img.shields.io/badge/MCP-接入文档页-a855f7?style=flat-square)](https://mybt.kiteyuan.info/mcp)
[![Stars](https://img.shields.io/github/stars/kiteyuan/cloud-drive?style=flat-square)](https://github.com/kiteyuan/cloud-drive)

</div>

纸鸢下载（磁力转存）为永久免费公益服务：可通过签到获取积分，兑换空间与会员权益。支持磁力、电驴及第三方分享链接转存；网盘内可新建文件夹、迁移、重命名等；在线播放直链延迟通常低于直接下载（画质可能略有压缩）。延迟取决于网络环境。下载建议优先使用 HTTP 直链，多线程下载器有时会触发风控。

## MCP 网盘操作 Skill

路径：[`skills/drive-mcp`](./skills/drive-mcp)

给希望用 Agent（Claude Code、Codex、Cursor 等）操作纸鸢网盘的用户。能力通过官网 MCP 提供，不经过本仓库。

**使用方法：**

1. 打开 [纸鸢下载 MCP 页](https://mybt.kiteyuan.info/mcp) 并登录，生成 MCP Token。
2. 将 `skills/drive-mcp` 交给 Agent，并按 Skill 把 Token 配进 MCP 客户端（入口 `https://mybt.kiteyuan.info/api/v1/mcp`）。
3. 即可让 Agent 转存链接、浏览网盘、取播放/下载链接、管理回收站等。

---

#### 1. 转存

网盘内支持磁力、电驴（成熟）以及第三方分享链接转存；第三方转存仍在完善中。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/4378e2ed-08b7-49bf-9ae9-39575b410165" />

#### 2. 网盘基础操作

支持新建文件夹、迁移和重命名等文件操作。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/edf9f9ca-fd0c-486d-9c54-8807982a6eb1" />

#### 3. 任务与文件交互

任务列表在小浮窗内；成功转存的文件支持一系列操作。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/72b61c1f-ca08-4b7f-806b-e2475b227a3f" />
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/82761f30-392c-41e4-9e13-4c2426994c4a" />

#### 4. 在线播放

播放链路优化，大陆用户延迟更低；交互贴近常见视频播放器。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/eca20a55-1b4c-4a8e-ad06-2574266cd98e" />

#### 5. 回收站

误删文件可在回收站恢复；回收站内文件仍占空间，彻底清除后才释放。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/aab15b38-bd5b-4e2d-9bd1-239557d2e8b4" />

#### 6. 头像与昵称

支持上传头像与修改昵称。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/58734a04-34fb-47a2-9e1a-f2b2184859d5" />

#### 7. 积分

【我的积分】可签到兑换会员权益。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/02f9ed33-9cd0-4ad2-a243-9c4c7ebde3c6" />

#### 8. MCP

网盘能力同步至 MCP，接入后可用 AI Agent 操作纸鸢网盘。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/9bde71e9-4f85-4324-bb55-f053ac273f03" />
