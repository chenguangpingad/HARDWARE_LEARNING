# Allegro PCB 快捷键说明

> 适用：Cadence Allegro PCB Editor 17.4（Windows）
> 配置文件：`%HOME%\pcbenv\env`（本机：`C:\Users\gpchen\AppData\Roaming\SPB_Data\pcbenv\env`）

## 一、快捷键原理

| 命令 | 用途 | 例子 |
| --- | --- | --- |
| `alias` | Ctrl 组合键 / 功能键 / 特殊键 | `alias ~D delete` |
| `funckey` | 单字符键 / 功能键 / 方向键 | `funckey r add connect` |

- `~` 表示 **Ctrl**（如 `~D` = Ctrl+D）
- 命令含空格时用**单引号**括起
- 修改后**必须完全退出 Allegro 再重开**才生效

## 二、文件路径

```
C:\Users\gpchen\AppData\Roaming\SPB_Data\pcbenv\env
```

快速打开：`Win+R` → `notepad %HOME%\pcbenv\env`

> 自定义内容必须写在 `### User Preferences section` **之前**。

## 三、快捷键总表

### 1. 功能键 alias（F2~F12）

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `F2` | 全图 | zoom fit |
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

### 2. Shift + 功能键

| 键 | 功能 | 命令 |
| --- | --- | --- |
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

### 3. Ctrl 组合

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `Ctrl+N` | 新建 | new |
| `Ctrl+O` | 打开 | open |
| `Ctrl+S` | 保存 | save |
| `Ctrl+D` | 删除 | delete |
| `Ctrl+Z` | 撤销 | undo |
| `Ctrl+Y` | 重做 | redo |
| `Ctrl+F2` | 下一个 | next |
| `Ctrl+F5` | 颜色 | color192 |
| `Ctrl+F6` | 层优先级 | layer priority |
| `Ctrl+Shift+F5` | 状态 | status |

### 4. 单字符键（funckey）

| 键 | 功能 | 命令 | 备注 |
| --- | --- | --- | --- |
| `a` | 推挤 | slide | |
| `A` | 切割线 | fp_cutcline | ⚠ 依赖 Skill |
| `b` | 平滑 | custom smooth | 覆盖了前面的 `b opps` |
| `B` | DB Doctor | dbdoctor | |
| `c` | 复制 | copy | |
| `C` | 铜皮挖空复制 | shape void copy | |
| `d` | 完成 | done | |
| `D` | 差分对设置 | diff pairs | |
| `e` | 移动 | move | |
| `E` | 约束管理器 | cmgr | |
| `f` | 铺铜 | shape add | |
| `F` | 创建 Fanout | create fanout | |
| `g` | 编辑铜皮边界 | shape edit boundary | |
| `h` | 分配颜色 | assign color | |
| `H` | 过孔中心等长 | x_eq_cline | ⚠ 可能依赖 Skill |
| `I` | 删除孤岛 | island_delete | ⚠ 可能依赖 Skill |
| `j` | 取消高亮 | dehilight | |
| `k` | 颜色 | color | |
| `m` | 测量 | show measure | |
| `M` | 铜皮合并 | shape merge shapes | |
| `N` | 下一个 | next | |
| `n` | 角度 45° | angle 45 | |
| `o` | 删除铜皮 | shap delete（笔误）| ⚠ 应为 `shape delete` |
| `p` | 交换引脚 | swap pins | |
| `q` | 切换 | toggle | |
| `r` | 布线 | add connect | |
| `R` | 画线 | add line | |
| `s` | 网络飞线 | rats net | |
| `S` | （空）| — | ⚠ 未定义命令 |
| `t` | 蛇形/等长 | delay tune | |
| `T` | 加文字 | add text | |
| `u` | 镜像 | mirror | |
| `v` | 选铜片 | shape select | |
| `w` | 元件飞线 | rats component | |
| `y` | 相位调谐 | phase tune | 覆盖了前面的 `y shape void polygon` |
| `Y` | 层优先级 | layer priority | |
| `z` | 更改 | change | |
| `Z` | 铜皮类型转换 | shape change type | |
| `home` | 图纸信息 | summary drawing report | |

### 5. 数字键

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `0` | 取消元件飞线 | unrats component |
| `1` | 删除 | delete |
| `2` | 元件飞线 | rats component |
| `3` | 旋转（文字）| rotate |
| `4` | 旋转（元件）| spin |
| `5` | 网络飞线 | rats net |
| `6` | 取消网络飞线 | unrats net |
| `7` | 显示属性 | show element |
| `8` | 交换元件 | swap components |
| `9` | 状态 | status |

### 6. 其它

| 键 | 功能 | 命令 |
| --- | --- | --- |
| `+` / `-` | 切换 subclass | subclass -+ / -- |
| `F12` | 切换铜皮显示 + 重绘 | settoggle no_etch_shape_display;redraw |

## 四、⚠ 配置里的冲突与笔误

当前 env 有下面这些问题，会让某些键**互相覆盖**或**失效**，建议修正：

| 问题 | 位置 | 说明 | 建议 |
| --- | --- | --- | --- |
| **F3 冲突** | `alias F3 add connect` + `funckey F3 fp_aligntest` | F3 定义了两次 | 删掉其中一条 |
| **F4 冲突** | `alias F4 show element` + `funckey F4 net schedule` | F4 定义了两次 | 删掉其中一条 |
| **F12 冲突** | `alias F12 zoom out` + `funckey F12 settoggle...` | F12 定义了两次 | 保留一个 |
| **b 冲突** | `funckey b opps` + `funckey b custom smooth` | 后者覆盖前者 | 删掉 `b opps` |
| **y 冲突** | `funckey y shape void polygon` + `funckey y phase tune` | 后者覆盖前者 | 删掉前者 |
| **笔误 1** | `funckey b opps` | 应为 `oops` | 改成 `oops` |
| **笔误 2** | `funckey o shap delete` | 应为 `shape delete` | 加个 e |
| **空命令** | `funckey S` | 没有命令，无效 | 删掉或补命令 |
| **重复行** | `funckey + subclass -+` / `- subclass --` | 各出现两次 | 删掉重复 |
| **只读项** | `alias ~S save` / `alias ~Z undo` | 内置只读，重定义无效 | 可保留（无害）|
| **Skill 依赖** | `A`、`F3`(funckey)、`H`、`I` | 可能依赖第三方 Skill | 装了才有用 |

## 五、修改方法

1. **备份**：`copy env env.bak`
2. `Win+R` → `notepad %HOME%\pcbenv\env`
3. 在 `### User Preferences section` **之前**修改
4. 保存，**完全退出 Allegro 再重开**
5. 命令窗口输入 `alias` 验证

## 六、常见问题

| 问题 | 原因 | 解决 |
| --- | --- | --- |
| 按键无反应 | env 未加载 / 未重启 | 完全退出再重开 Allegro |
| 启动报 `Parse error ... Variable not defined` | 有未定义变量（如 `$module`）| 注释掉该行 |
| 提示 command not found | 命令名拼错或缺 Skill | 核对命令；装 Skill 或注释 |
| 单字符键无效 | 光标在命令窗口/Find 面板 | 点一下画布再按 |
| 功能键冲突 | 同一键被 alias 和 funckey 各定义一次 | 见第四节 |

## 七、常用命令速查

| 功能 | 命令 |
| --- | --- |
| 布线 | `add connect` |
| 推挤 | `slide` |
| 蛇形/等长 | `delay tune` |
| 过孔 | `add via` |
| 旋转（元件）| `spin` |
| 旋转（文字）| `rotate` |
| 铺铜 | `shape add` |
| 选铜皮 | `shape select` |
| 删除 | `delete` |
| 换层 | `layer up` / `layer down` |
| 差分对设置 | `diff pairs` |
| Fanout | `create fanout` |
| 约束管理器 | `cmgr` |
| DRC | `check` |
| 全图 | `zoom fit` |

---

*本文件对应当前 env（132 行，2026-11-25）*
