# 演播室2 插件：player_database

选手 / 队伍 / 解说 SQLite 数据库 + 二级管理面板 + CSV 导入导出。
安装：把本仓库内容放到 `{exe}/mods/player_database/`。

- 原生库：`native/libgdsqlite.windows.template_{debug,release}.x86_64.dll`（Windows x64）；
- 依赖：`control_panel_base`（`dependencies`）；
- API 契约：`api_version: >=2.0.0 <3.0.0`。

## CI

`smoke.yml` 在 **windows-latest** 上跑（原生库仅 Windows），对 core `main` 与
`core-v2.0.0` 各冒烟一次：显式检出 `control_panel_base@v1.0.0`，复制进 core 的
`plugins/`，无头启动并断言 `插件已加载并启用: player_database`。
