# Allegro PCB 快捷键说明

> 适用：Cadence Allegro PCB Editor 17.4（Windows）
> 配置文件：`%HOME%\pcbenv\env`（本机：`C:\Users\gpchen\AppData\Roaming\SPB_Data\pcbenv\env`）
> 本配置**不依赖任何第三方 Skill 包**，全部为标准 Allegro 命令。

## 一、快捷键原理

Allegro 的快捷键由 `env` 文件里的两类命令定义：

| 命令 | 用途 | 例子 |
| --- | --- | --- |
| `alias` | Ctrl 组合键 / 字母键 / 特殊键 | `alias ~R 'add connect'` |
| `funckey` | F1~F12 / 方向键 / 单字符键 | `funckey F2 'add connect'` |

- `~` 表示 **Ctrl**（如 `~R` = Ctrl+R）
- 命令含空格时用**单引号**括起
- **空格键**写成 `funckey " "`（Cadence 官方示例写法）
- 修改后**重启 Allegro** 生效

## 二、文件位置

| 系统 | 路径 |
| --- | --- |
| Windows | `%HOME%\pcbenv\env` |
| Linux | `$HOME/pcbenv/env` |

确认 `HOME`：Windows 命令行 `echo %HOME%`。

> **注意**：env 里 `### User Preferences section` 之后是 Allegro 自动生成区（库路径等），**自定义快捷键要写在它之前**。

## 三、完整快捷键表

### 1. 高频操作（重点）

| 键 | 功能 | 命令 |
| --- | --- | --- |
| **空格** | **旋转** | rotate |
| **Ctrl+W** | **布线** | add connect |
| **Ctrl+E** | **铺铜** | shape add |
| **N** | **打过孔** | add via |
| **V** | **选择铜皮/挖空** | shape select |
| **Delete** | **删除** | delete |
| **F2** | 全图 | zoom fit |
| **F3** | 布线（备用）| add connect |

### 2. 功能键（F2~F12）

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `Esc` | 取消当前命令 | cancel |
| `F1` | 帮助 | help |
| `F2` | 全图显示 | zoom fit |
| `F3` | 布线 | add connect |
| `F4` | 显示属性 | show element |
| `F5` | 重绘 | redraw |
| `F6` | 完成 | done |
| `F7` | 下一个 | next |
| `F8` | 撤销上一步 | oops |
| `F9` | 取消 | cancel |
| `F10` | 网格开关 | grid toggle |
| `F11` | 放大 | zoom in |
| `F12` | 缩小 | zoom out |

### 3. Ctrl 组合

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `Ctrl+↑` | 按格点上移 | ipick_to_gridunit 0 +1 |
| `Ctrl+↓` | 按格点下移 | ipick_to_gridunit 0 -1 |
| `Ctrl+←` | 按格点左移 | ipick_to_gridunit -1 |
| `Ctrl+→` | 按格点右移 | ipick_to_gridunit +1 |
| `Ctrl+W` | **布线** | add connect |
| `Ctrl+E` | **铺铜** | shape add |
| `Ctrl+D` | 删除 | delete |
| `Ctrl+N` | 新建 | new |
| `Ctrl+O` | 打开 | open |
| `Ctrl+B` | 切换推挤模式 | bubset |
| `Ctrl+Shift+B` | 切换平滑模式 | smoothset |
| `Ctrl+F2` | 下一个 | next |
| `Ctrl+F5` | 颜色 | color192 |
| `Ctrl+F6` | 层优先级 | layer priority |
| `Ctrl+Shift+F5` | 状态 | status |
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

### 5. 方向键 / 翻页 / 符号

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `↑ / ↓ / ← / →` | 视图漫游 | roam x/y $roamInc |
| `PageUp` | 上一层 | layer up |
| `PageDown` | 下一层 | layer down |
| `+` | 切换 subclass（-+）| subclass -+ |
| `−` | 切换 subclass（--）| subclass -- |

### 6. 字母别名（命令窗口直接输入）

| 别名 | 功能 |
| --- | --- |
| `N` | **打过孔（add via）** |
| `V` | **选择铜皮/挖空（shape select）** |
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
| `reopen` / `revert` | ~~重新打开设计~~（已注释：`$module` 启动时未定义会报错）|
| `cdnshelp` | Cadence 帮助 |

## 四、只读内置项（无法覆盖）

以下快捷键由 Allegro 内置且**只读**，env 中无法修改：

| 键 | 功能 |
| --- | --- |
| `Ctrl+S` | 保存（save）|
| `Ctrl+Z` | 撤销（undo）|
| `Tab` | 切换（tab）|
| `C` | ctab |
| `C+S` | sctab |
| `S` | stab |

> 这些在 env 中以注释形式保留，仅作说明。

## 五、修改方法

1. **备份**：`copy env env.bak`
2. 用**记事本**打开 `%HOME%\pcbenv\env`
3. 在 `### User Preferences section` **之前**追加，例如：
   ```
   funckey " " rotate
   alias ~W    add connect
   alias ~E    shape add
   alias N     add via
   alias V     shape select
   funckey Delete delete
   ```
4. 保存，**重启 Allegro**
5. 在命令窗口输入 `alias` 验证是否加载

## 六、常见问题

| 问题 | 原因 | 解决 |
| --- | --- | --- |
| 按键无反应 | env 未加载 | 重启 Allegro；检查 `HOME` 路径 |
| 提示 command not found | 命令名拼错 | 核对命令名 |
| 启动异常 | env 语法错误 | 用备份还原，逐行排查 |
| 启动报 `Parse error ... Variable not defined` | env 里有**未定义变量**（如 `$module`）| 注释掉该行（如 `reopen`/`revert`），或把变量换成固定值 |
| 中文注释乱码 | env 编码问题 | 注释用**英文**（纯 ASCII）|
| 快捷键冲突 | 与内置只读项冲突 | 只读项无法覆盖（见第四节）|
| 空格键无效 | 写法不对 | 必须写成 `funckey " " ...`（引号内一个空格）|

## 七、关键命令速查（env 用）

| 功能 | 命令 |
| --- | --- |
| 布线 | `add connect` |
| 推挤 | `slide` |
| 蛇形/等长 | `delay tune` |
| 过孔 | `add via` |
| 旋转 | `rotate` |
| 铺铜 | `shape add` |
| 选择铜皮 | `shape select` |
| 删除 | `delete` |
| 自动布线 | `auto_route` |
| 自动连接 | `auto_connect` |
| 移动/复制 | `move` / `copy` |
| 换层 | `layer up` / `layer down` |
| 差分对设置 | `diff pairs` |
| Fanout | `create fanout` |
| 约束管理器 | `cmgr` |
| DRC | `check` |
| 全图 | `zoom fit` |
| 框选 | `zoom window` |

## 八、本版重点改动

| 操作 | 旧 | 新 |
| --- | --- | --- |
| 旋转 | 无 | **空格** |
| 布线 | F3 | **Ctrl+W**（F3 保留）|
| 铺铜 | 无 | **Ctrl+E** |
| 过孔 | 无 | **N** |
| 选择铜皮 | 无 | **V**（shape select）|
| 删除 | Ctrl+D | **Delete**（Ctrl+D 保留）|

---

*本文件对应 env 版本：2026-11-25（纯标准命令版 + 6 项自定义快捷键）*
