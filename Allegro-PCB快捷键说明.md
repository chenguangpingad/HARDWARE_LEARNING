# Allegro PCB 快捷键说明

> 适用：Cadence Allegro PCB Editor 17.4（Windows）
> 配置文件：`%HOME%\pcbenv\env`（本机：`C:\Users\gpchen\AppData\Roaming\SPB_Data\pcbenv\env`）

## 一、快捷键原理

Allegro 的快捷键由 `env` 文件里的两类命令定义：

| 命令 | 用途 | 例子 |
| --- | --- | --- |
| `alias` | Ctrl 组合键 / 字母键 / 特殊键 | `alias ~R 'add connect'` |
| `funckey` | F1~F12 / 方向键 / 单字符键 | `funckey F2 'add connect'` |

- `~` 表示 **Ctrl**（如 `~R` = Ctrl+R）
- 命令含空格时用**单引号**括起
- 修改后**重启 Allegro** 生效

## 二、文件位置

| 系统 | 路径 |
| --- | --- |
| Windows | `%HOME%\pcbenv\env` |
| Linux | `$HOME/pcbenv/env` |

确认 `HOME`：Windows 命令行 `echo %HOME%`。

> **注意**：env 里 `### User Preferences section` 之后是 Allegro 自动生成区（库路径等），**自定义快捷键要写在它之前**。

## 三、完整快捷键表

### 1. 单键（最常用）

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `0` | 取消元件飞线 | unrats component |
| `1` | 删除 | delete |
| `3` | 旋转 | rotate |
| `4` | 自旋 | spin |
| `6` | 取消网络飞线 | unrats net |
| `7` | 显示属性 | show element |
| `8` | 交换元件 | swap components |
| `9` | 状态 | status |
| `A` | 画线（切割线）| add line |
| `B` | DB Doctor | dbdoctor |
| `C` | 铜皮挖空复制 | shape void copy |
| `D` | 差分对设置 | diff pairs |
| `E` | 约束管理器 | cmgr |
| `F` | 创建 Fanout | create fanout |
| `+` / `-` | 切换 subclass | subclass -+ / -- |
| `,` / `.` | 下一层 / 上一层 | layer down / layer up |

### 2. F 功能键

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `Esc` | 取消当前命令 | cancel |
| `F1` | 帮助 | help |
| `F2` | 移动 | move |
| `F4` | 网络排程 | net schedule |
| `F5` | 重绘 | redraw |
| `F6` | 完成 | done |
| `F7` | 下一个 | next |
| `F8` | 撤销上一步 | oops |
| `F9` | 取消 | cancel |
| `F10` | 网格开关 | grid toggle |
| `F11` | 放大 | zoom in |
| `F12` | 切换铜皮显示 + 重绘 | settoggle no_etch_shape_display;redraw |

### 3. Ctrl 组合

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `Ctrl+↑` | 按格点上移 | ipick_to_gridunit 0 +1 |
| `Ctrl+↓` | 按格点下移 | ipick_to_gridunit 0 -1 |
| `Ctrl+←` | 按格点左移 | ipick_to_gridunit -1 |
| `Ctrl+→` | 按格点右移 | ipick_to_gridunit +1 |
| `Ctrl+F2` | 下一个 | next |
| `Ctrl+F5` | 颜色 | color192 |
| `Ctrl+F6` | 层优先级 | layer priority |
| `Ctrl+Shift+F5` | 状态 | status |
| `Ctrl+B` | 切换推挤模式 | bubset |
| `Ctrl+D` | 删除 | delete |
| `Ctrl+Shift+B` | 切换平滑模式 | smoothset |
| `Ctrl+Y` | 重做 | redo |

### 4. Shift 组合

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `Shift+↑/↓/←/→` | 移动 + 按格点微调 | move; ipick_to_gridunit |
| `Shift+F2` | 属性编辑 | property edit |
| `Shift+F3` | 推挤 | slide |
| `Shift+F4` | 测量 | show measure |
| `Shift+F5` | 复制 | copy |
| `Shift+F6` | 移动 | move |
| `Shift+F7` | 取消高亮 | dehilight |
| `Shift+F8` | 高亮 | hilight pick |
| `Shift+F9` | 顶点编辑 | vertex |
| `Shift+F10` | 另存为 | save_as temp |
| `Shift+F11` | 上一次视图 | zoom previous |
| `Shift+F12` | 全图 | zoom world |

### 5. 方向键 / 翻页

| 键 | 功能 |
| --- | --- |
| `↑ / ↓ / ← / →` | 视图漫游（roam）|
| `PageUp` | 上一层（layer up）|
| `PageDown` | 下一层（layer down）|

### 6. 字母别名（直接输入）

| 别名 | 功能 |
| --- | --- |
| `x` / `y` | pick 选取 |
| `window` | 框选缩放 |
| `zc` | 中心缩放 |
| `ix` / `iy` | ipick 按格点选取 |
| `pickx` / `picky` | pick |
| `hilite` / `dehilite` | 高亮 / 取消高亮 |
| `bubset` | 推挤模式循环 |
| `smoothset` | 平滑模式循环 |
| `edps` | 焊盘编辑（padedit）|
| `rps` | 替换焊盘（replace padstack）|
| `sar` / `uar` | 设置 / 取消自动漫游 |
| `unplrp` | 报告未放置元件 |
| `reopen` / `revert` | 重新打开设计 |
| `cdnshelp` | Cadence 帮助 |

## 四、Skill 依赖项（已注释）

以下快捷键来自第三方 Skill 包（Jun 工具包 / FP 工具包），本机**未安装**，已在 env 中注释，替换为等价的 Allegro 标准命令：

| 键 | 原 Skill 命令 | 已替换为 |
| --- | --- | --- |
| `Esc` | FP_QuickView_AutoHide | `cancel` |
| `,` | Jun_LayerEtch Down | `layer down` |
| `.` | Jun_LayerEtch Up | `layer up` |
| `A` | fp_cutcline | `add line` |
| `F2` | Jun_movecomps | `move` |
| `G` | skill Jun_GridTool | 注释（无等价）|
| `2` / `5` | skill Jun_GridTool | 注释 |
| `G25` / `G40` / `G50` | skill Jun_GridTool | 注释 |
| `F3` | fp_aligntest | 注释 |
| `Ctrl+F` | FP_RUN | 注释 |
| `Ctrl+N` / `new` | FP_New | 注释 |
| `Ctrl+O` / `open` | FP_Open | 注释 |

**启用方法**：装好 Skill 包后，把 env 里 `# ---------- SKILL-dependent entries` 下面的注释去掉即可。

## 五、修改方法

1. **备份**：`copy env env.bak`
2. 用**记事本**打开 `%HOME%\pcbenv\env`
3. 在 `### User Preferences section` **之前**追加：
   ```
   alias ~R 'add connect'
   funckey F2 'move'
   ```
4. 保存，**重启 Allegro**
5. 在命令窗口输入 `alias` 验证是否加载

## 六、常见问题

| 问题 | 原因 | 解决 |
| --- | --- | --- |
| 按键无反应 | env 未加载 | 重启 Allegro；检查 `HOME` 路径 |
| 提示 command not found | 命令名拼错或 Skill 未装 | 核对命令；安装 Skill 或注释该行 |
| 启动异常 | env 语法错误 | 用备份还原，逐行排查 |
| 中文注释乱码 | env 编码问题 | 注释用**英文**（纯 ASCII）|
| 快捷键冲突 | 与内置只读项冲突 | 只读项（`~S`、`~Z`、`\t`、`C`、`CS`、`S`）无法覆盖 |

## 七、关键命令速查（env 用）

| 功能 | 命令 |
| --- | --- |
| 布线 | `add connect` |
| 推挤 | `slide` |
| 蛇形/等长 | `delay tune` |
| 过孔 | `add via` |
| 自动布线 | `auto_route` |
| 自动连接 | `auto_connect` |
| 铺铜 | `shape add` |
| 移动/复制/删除 | `move` / `copy` / `delete` |
| 换层 | `layer up` / `layer down` |
| 差分对设置 | `diff pairs` |
| Fanout | `create fanout` |
| 约束管理器 | `cmgr` |
| DRC | `check` |
| 全图 | `zoom fit` |
| 框选 | `zoom window` |

---

*本文件对应 env 版本：2026-11-25（方案 A：Skill 项已注释替换）*
