# 万象拼音 - Rime输入方案

[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/amzxyz/rime_wanxiang)
[![GitHub Stars](https://img.shields.io/github/stars/amzxyz/rime_wanxiang?style=social)](https://github.com/amzxyz/rime_wanxiang/stargazers)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> 🚀 基于深度优化的词库和语法模型的智能拼音输入方案 | 让中文输入行云流水

---

## ✨ 核心亮点

### 🎯 为什么选择万象？

- ⚡ **智能整句输入** - AI筛选的大基数词库 + 语言模型，更精准的整句联想
- 🎵 **全声调标注** - 唯一支持整句拼音串上屏的方案，可显示/输入音调
- 🔧 **6种辅助码** - 墨奇/鹤形/自然码/虎码/五笔/汉心码，拼音+辅助码任意组合
- 🔍 **强大反查系统** - 支持两分/多分/笔画三种打法，U+Unicode完整覆盖
- 🎨 **丰富Lua扩展** - 成对符号、tips提示、手动排序、无感造词等创新功能

### 📸 效果预览

![效果展示](https://storage.deepin.org/thread/202502200358104987_效果.png)

---

## 🚀 快速开始（30秒上手）

### 方式一：快速部署 ⚡

1. 将方案文件置于Rime用户目录
2. 输入以下指令切换双拼/全拼类型
3. 重新部署，完成！

```bash
/flypy    → 小鹤双拼
/mspy     → 微软双拼
/zrm      → 自然码
/sogou    → 搜狗双拼
/pinyin   → 全拼
/wxsp     → 万象双拼
# ... 更多指令见下方
```

> 💡 **提示**：这些指令能一次性完成4个补丁文件的输入类型修改，无需手动配置！

### 方式二：Plum一键安装 🛠️

#### 基础版（完整）
```bash
bash rime-install amzxyz/rime_wanxiang@wanxiang-base:plum/full
```

#### 自然码辅助版（完整）
```bash
bash rime-install amzxyz/rime_wanxiang@wanxiang-zrm-fuzhu:plum/full
```

<details>
<summary>📦 查看全部Plum安装命令</summary>

**基础版**
```bash
# 完整版
bash rime-install amzxyz/rime_wanxiang@wanxiang-base:plum/full

# 仅词库
bash rime-install amzxyz/rime_wanxiang@wanxiang-base:plum/dicts
```

**辅助码版本**
```bash
# 自然码辅助
bash rime-install amzxyz/rime_wanxiang@wanxiang-zrm-fuzhu:plum/full
bash rime-install amzxyz/rime_wanxiang@wanxiang-zrm-fuzhu:plum/dicts

# 墨奇辅助
bash rime-install amzxyz/rime_wanxiang@wanxiang-moqi-fuzhu:plum/full
bash rime-install amzxyz/rime_wanxiang@wanxiang-moqi-fuzhu:plum/dicts

# 小鹤辅助
bash rime-install amzxyz/rime_wanxiang@wanxiang-flypy-fuzhu:plum/full
bash rime-install amzxyz/rime_wanxiang@wanxiang-flypy-fuzhu:plum/dicts

# 虎码辅助
bash rime-install amzxyz/rime_wanxiang@wanxiang-tiger-fuzhu:plum/full
bash rime-install amzxyz/rime_wanxiang@wanxiang-tiger-fuzhu:plum/dicts

# 五笔辅助
bash rime-install amzxyz/rime_wanxiang@wanxiang-wubi-fuzhu:plum/full
bash rime-install amzxyz/rime_wanxiang@wanxiang-wubi-fuzhu:plum/dicts

# 汉心辅助
bash rime-install amzxyz/rime_wanxiang@wanxiang-hanxin-fuzhu:plum/full
bash rime-install amzxyz/rime_wanxiang@wanxiang-hanxin-fuzhu:plum/dicts

# 首右辅助
bash rime-install amzxyz/rime_wanxiang@wanxiang-shouyou-fuzhu:plum/full
bash rime-install amzxyz/rime_wanxiang@wanxiang-shouyou-fuzhu:plum/dicts
```

</details>

### 方式三：更新工具 📲

- **Windows**：[wanxiang-tools.exe](https://github.com/amzxyz/RIME-LMDG/releases/tag/tool) - 内置在线更新器
- **跨平台脚本**：[rime-wanxiang-update-tools](https://github.com/rimeinn/rime-wanxiang-update-tools)

---

## 📦 安装方式对比

| 安装方式 | 适合人群 | 难度 | 更新便利性 | 推荐指数 |
|---------|---------|------|-----------|---------|
| 快速部署 | 新手体验 | ⭐ | 手动更新 | ⭐⭐⭐ |
| Plum脚本 | 命令行用户 | ⭐⭐ | 一键更新 | ⭐⭐⭐⭐⭐ |
| 更新工具 | Windows用户 | ⭐ | 自动更新 | ⭐⭐⭐⭐⭐ |
| Custom Patch | 长期使用者 | ⭐⭐⭐ | 手动更新 | ⭐⭐⭐⭐ |

---

## ⚙️ 版本选择

| 特性 | 标准版 | 增强版PRO |
|-----|-------|----------|
| **方案文件** | `wanxiang.schema.yaml` | `wanxiang_pro.schema.yaml` |
| **支持类型** | 全拼、任何双拼 | 只支持双拼 |
| **自动调频** | ✅ 默认开启 | ❌ 默认关闭 |
| **用户词记录** | 无差别自动记录 | 需手动造词（`·`引导） |
| **用户词位置** | `wanxiang.userdb` | `zc.userdb` |
| **辅助码** | 基于声调的辅助 | 7种辅助码可选，兼容声调 |
| **推荐场景** | 日常使用 | 专业用户/追求精准控制 |

---

## 🎯 核心功能详解

### 1️⃣ 辅助码系统

万象拼音支持多种辅助码，让你在拼音基础上快速定位目标字。

<details>
<summary>📖 直接辅助码（仅PRO）</summary>

**使用场景**：想要"镇"字显示在前面

输入 `vf`（镇）+ `j`（金字旁声母）→ 快速出现"镇"字

如果继续输入其他主体字的声母，可以进一步缩小范围。

![直接辅助码示例](https://storage.deepin.org/thread/202407041147131421_截图_选择区域_20240704121809.png)
</details>

<details>
<summary>📖 间接辅助码（仅PRO）</summary>
**使用场景**：避免辅助码干扰双拼词语

输入 `ni/re` - 通过 `/` 引导辅助码
- 不加 `/` 时，与普通双拼无异，如 `vsg` 可以输出"中国"
- 加 `/` 后，进入辅助码筛选模式

**聚拢功能**：输入 `nire/` 让系统侧重于单字匹配
</details>

<details>
<summary>📖 声调辅助筛选</summary>

**7890** 代表 **1234** 声（轻声归并到4声）

输入示例：
- `ni9` → 你（三声）
- `niRE` → 大写字母代表辅助码
- `niR9E` → 混合使用声调和辅助码

![声调辅助示例](https://storage.deepin.org/thread/202505120222182012_截图_选择区域_20250512101814.png)
</details>

<details>
<summary>📖 输入后反查筛选</summary>

**使用场景**：通过反查字库定位词组或单字

输入主要拼音后，通过 `` ` `` 引导进入反查状态：

- `lkuiuo`jd`` → 筛选包含"老"字底的词
- `lkuiuo`gt`` → 筛选包含"实"字的词
- 支持 `.*t.*b.*g.*` 的正则匹配逻辑

**注意**：词组匹配不支持笔画，单字支持两分、多分、笔画
</details>

---

### 2️⃣ 输入前反查

<details>
<summary>📖 拆字模式</summary>

**使用场景**：不认识的字用部件组合输入

示例：输入"震"字
- 输入 `yu` `if`（雨 辰）+ `` ` `` → 出现"震"字
- 同时给出辅助码提示：`y`（雨声母）+ `i`（辰声母）

![拆字模式示例](https://storage.deepin.org/thread/202409280324599355_截图_选择区域_20240928112256.png)
</details>

<details>
<summary>📖 笔画模式</summary>

使用 `hspnz` 代表横竖撇捺折五笔画

示例：
- 两分：`ni`re``、`ni`rfer``
- 多分：`mu`ckrida``
- 笔画：`ni`pspzhpd``
</details>

---

### 3️⃣ 混合编码

所有混合编码功能统一在 `wanxiang_mixedcode.schema.yaml` 方案中，无需引导，直接输入。

| 功能 | 输入示例 | 输出 |
|-----|---------|------|
| 中英混合 | `1000wclips` | 1000wclips |
| 混合编码 | `AD钙奶` | AD钙奶 |
| 技术词汇 | `PN结`、`Type-C` | PN结、Type-C |
| 纯英文 | `hello` | hello |
| 金额大写 | `R1234` | 一千二百三十四、壹仟贰佰叁拾肆元整 |
| Unicode | `U62fc` | 拼 |

![混合编码示例](https://storage.deepin.org/thread/202509260105536966_混合编码.jpg)

---

### 4️⃣ Lua扩展功能

万象拼音提供丰富的Lua扩展功能，让输入更高效。

<details>
<summary>🔧 日期时间快捷输入</summary>

**引导键**：`/` 或 `o`

| 编码 | 功能 | 说明 |
|-----|------|------|
| `/sj` 或 `osj` | 时间 | 显示当前时间 |
| `/rq` 或 `orq` | 日期 | 显示当前日期 |
| `/rc` 或 `orc` | 日期差 | `/rc26p`（加26天）、`/rc26-`（减26天） |
| `/nl` 或 `onl` | 农历 | 显示农历日期 |
| `/xq` 或 `oxq` | 星期 | 显示星期几 |
| `/ww` 或 `oww` | 周数 | 今年第几周 |
| `/jq` 或 `ojq` | 节气 | 显示节气信息 |
| `/dt` 或 `odt` | 日期+时间 | 显示完整日期时间 |
| `/tt` 或 `ott` | 时间戳 | Unix时间戳 |
| `/jr` 或 `ojr` | 节日 | 显示节日信息 |
| `/day` 或 `oday` | 问候模板 | 显示问候语 |

**N模式**：`N0101`（月日）或 `N20250315`（完整年月日）

> 💡 支持自定义格式和顺序，详见方案配置
</details>

<details>
<summary>🔧 计算器模式</summary>

**引导键**：`V`

输入示例：
- `V3+5` → `8` 和 `3+5=8`
- 支持 `+ - * / % ^`
- 支持 `sin(x)` `cos(x)` 等函数
- 详见 `super_calculator.lua`

![计算器示例](https://storage.deepin.org/thread/202509260127113759_计算器1.png)
</details>

<details>
<summary>🔧 超级Tips提示</summary>

**触发键**：逗号 `,`（默认）

支持类型：
- 表情
- 化学式
- 翻译
- 符号
- 货币
- 车牌
- 偏旁部首

**快捷键**：
- `Ctrl+T` - 开关Tips
- `,` - 上屏Tips内容

⚠️ **注意**：仓输入法、超越输入法需交由rime处理，设置中关闭前端接管

![Tips示例](https://storage.deepin.org/thread/202509260128462735_tips化学式.jpg)
</details>

<details>
<summary>🔧 辅助码提示（仅PRO）</summary>

**快捷键**：
- `Ctrl+A` - 循环切换：辅助码提示 → 声调全拼提示 → 关闭注释
- `Ctrl+C` - 开启拆分辅助提示（优先级更高）

默认显示1个字的辅助码，可在方案文件中自定义长度。

![辅助码提示示例](https://storage.deepin.org/thread/202509260134283927_辅助码提示.jpg)
</details>

<details>
<summary>🔧 快速符号（快符）</summary>

输入 `a/` 快速上屏"！"符号

可自定义26个字母的映射关系：
- `repeat` - 重复上一次上屏的内容
- 修改正则表达式可改变引导策略

配置位置：`quick_symbol_text` 段落
</details>

<details>
<summary>🔧 输入码音调显示</summary>

**快捷键**：`Ctrl+S`

实时动态显示全拼并加音调（万象特色功能）

`Shift+Enter` - 上屏当前显示的编码字符串
</details>

<details>
<summary>🔧 用户按需造词（仅PRO）</summary>

**引导键**：`` ` ``

三种造词方式：
1. `` ` `` 起始的主动造词
2. 编码后双击 `` ` `` 的主动造词（后触发）
3. 次选造词 - 次选是词库组合成的，上屏即记录

> 💡 PRO版讲究自主可控，避免异常词汇污染词库
</details>

<details>
<summary>🔧 手动排序</summary>

**快捷键**：
- `Ctrl+J` - 向左一步
- `Ctrl+K` - 向右一步
- `Ctrl+L`（零）- 移除排序信息
- `Ctrl+P` - 置顶选中候选

支持：
- 词典候选排序
- 动态Lua候选排序（日期/时间等格式）

数据存储：`lua/sequence.userdb`
</details>

<details>
<summary>🔧 更多Lua功能</summary>

| 功能 | 触发方式 | 说明 |
|-----|---------|------|
| 输入统计 | `/rtj` `/ztj` `/ytj` `/ntj` `/tj` | 日/周/月/年/生涯统计 |
| 翻译模式 | `Ctrl+E` | opencc中英文互译 |
| 字符集过滤 | `Ctrl+G` | 小字集/大字集切换 |
| 输入模式切换 | `Ctrl+Q` | 中文/英文/混合编码切换 |
| 声调辅助回退 | 直接输入7890 | 在声调间快速切换 |
| 候选切割机 | `Ctrl+1~0` | 上屏首选前N个字 |
| Tab循环切换 | `Tab` | 循环切换音节 |
| Unicode | `U` + 编码 | `U62fc` → 拼 |
| 符号输入 | `/sx` `/yd` 等 | 特殊符号快捷输入 |
| 错音错字提示 | 自动触发 | `gei yu` → `jǐ yǔ`提示 |

![错音提示示例](https://storage.deepin.org/thread/202509260127525844_错音给予.jpg)
</details>

---

## 🎓 进阶配置

### Custom Patch 个性化

⚠️ **重要**：
- Custom文件生效位置：**用户目录根目录**（与schema同级）
- custom目录仅用于携带和更新不覆盖
- 根目录的 `wanxiang.custom.yaml` 才是你的配置文件

```yaml
# wanxiang.custom.yaml
patch:
  # 方案列表
  schema_list:
    - schema: wanxiang

  # 简繁切换
  switches/@0/reset: 1

  # Tips快捷键（comma/period等）
  key_binder/tips_key: comma

  # 自定义短语文件名称
  translator/translation_file: custom_phrase.txt

  # 关闭自动调频（仅PRO）
  # engine/translators/@7/enable_user_dict: false
```

> 💡 详细配置方法见方案文件 `custom/` 目录下的教程

### 辅助码切换指令

所有指令格式：`/` + 代码

```
/flypy    → 小鹤双拼
/mspy     → 微软双拼
/zrm      → 自然码
/sogou    → 搜狗双拼
/znabc    → 智能ABC
/ziguang  → 紫光双拼
/pyjj     → 拼音加加
/gbpy     → 国标双拼
/lxsq     → 乱序17
/pinyin   → 全拼
/wxsp     → 万象双拼
/zrlong   → 自然龙（反查全拼）
/hxlong   → 汉心龙（反查全拼）
/jjf      → 间接辅助
/zjf      → 直接辅助
```

### 反查配置

在你的 `wanxiang.custom.yaml` 中配置：

```yaml
wanxiang_lookup:
  tags: [abc]              # 生效的tag
  key: "`"                 # 反查引导符
  lookup: [wanxiang_reverse]  # 反查数据库
  data_source: [comment, db]  # 数据源优先级
  # comment: 从词库注释(辅助码)提取
  # db: 从反查数据库提取
```

---

## 🌟 平台特殊说明

### iOS 仓输入法

1. 方案下载：仓设置 → 输入方案 → "+" → 万象拼音
2. 切换方案：长按 `/` + 方案代码（如 `/flypy`）
3. **关键步骤**：文件管理 → 拷贝键盘词库至应用
4. 重新部署

### iOS 元书输入法

1. 从 `RimeSharedSupport` 复制 `include_keyboard_rime_files.txt`
2. 修改文件底部新增：```^.*[.]custom.*$```
3. 重新部署

### Android

⚠️ **注意权限问题**：
- 小企鹅等前端数据位于 `data` 目录
- 需通过系统文件管理器迁移（不是MT文件管理）
- 或通过root修改权限保持一致

---

## 🔗 常见问题

<details>
<summary>❓ PRO版为什么默认关闭调频？</summary>

**原因**：
- 保持词库纯净可控
- 避免异常词汇和生僻字自动记录
- 用户通过 `·` 引导手动造词，更具可控性
- 适合追求精准的专业用户

**开启方法**：
```yaml
# wanxiang_pro.custom.yaml
patch:
  engine/translators/@7/enable_user_dict: true
```
</details>

<details>
<summary>❓ 如何更新词库和方案？</summary>

**推荐方式**：
1. **Plum用户**：重新运行安装命令即可自动更新
2. **工具用户**：使用wanxiang-tools内置更新器
3. **手动更新**：下载Release包，保留 `*.custom.yaml` 后覆盖

**白名单保护**：wanxiang-tools支持白名单，保护自定义文件不被覆盖
</details>

<details>
<summary>❓ 自定义词库如何添加？</summary>

**步骤**：
1. 使用工具将词库刷成万象格式（声调+辅助码）
2. 固定词库（推荐）：
   ```yaml
   patch:
     translator/packs/+:
       - userxx  # 你的词库名
   ```
3. 或重命名 `wanxiang.dict.yaml` 为 `wanxianguser.dict.yaml`

> 💡 [词库工具下载](https://github.com/amzxyz/RIME-LMDG/releases/tag/tools)
</details>

<details>
<summary>❓ 如何同步多设备用户词？</summary>

**方法**：
1. 设置同步目录（默认 `用户目录/sync`）
2. 修改 `installation_id` 为设备名称
3. 创建设备清单 `sequence_device_list.txt`
4. 点击"同步用户数据"
5. 通过云同步同步 `sync` 目录

⚠️ **不要**将整个rime文件夹放入同步软件，会导致数据库锁定
</details>

<details>
<summary>❓ 模型文件很大，影响性能吗？</summary>

**回答**：不会！

- 模型是固定的二进制数据，**不会增大**
- 只占用少量CPU算力，内存占用极少
- 不同于热加载数据，应视为优秀的算法模块
- 非常值得投入，大幅提升整句准确度
</details>

---

## 📚 相关资源

### 官方文档
- [🚀 新手安装配置指南](https://docs.qq.com/doc/DQ0FqSXBmYVpWVFpy?rtkey=)
- [词库问题收集反馈表](https://docs.qq.com/smartsheet/DWHZsdnZZaGh5bWJI?viewId=vUQPXH&tab=BB08J2)
- [RIME-LMDG 词库与语言模型仓库](https://github.com/amzxyz/RIME-LMDG)

### 友情链接
- [Oh My Rime](https://www.mintimate.cc/zh/guide/installRime.html) - Rime基础入门
- [Rime参数配置](https://xishansnow.github.io/posts/41ac964d.html) - 详细配置说明

### 工具下载
- [Windows词库工具](https://github.com/amzxyz/RIME-LMDG/releases/download/tools/wanxiang-tools.exe)
- [Linux/Mac词库工具](https://github.com/amzxyz/RIME-LMDG/releases/download/tools/wanxiang-dicts-tools-linux-mac)
- [更新脚本](https://github.com/rimeinn/rime-wanxiang-update-tools)

### 自定义数据
在线获取（不随方案包提供）：
- `jm_flypy.txt` - 小鹤简码
- `jm_zrm.txt` - 自然码简码
- `tips_user.txt` - Tips翻译数据

---

## 🎁 万象特色总结

### 🏆 独家功能

1. **唯一支持整句拼音串上屏** - 词库全部带声调标注
2. **错位构词法** - 长期死磕权重最优解、分词片段最优解
3. **最全面的反查数据库** - 支持到U+，两分/多分/笔画
4. **有趣且实用** - 成对符号、Tips提示、手动排序、无感造词
5. **6种辅助码兼容** - 头部全拼编码，可转化为任何双拼
6. **精益求精** - 从里到外追求最优、最精

### 💡 核心理念

> **万象词库中的带声调拼音标注+词组构成+词频是整个万象项目的核心，是使用体验的基石。方案的其它功能皆可自定义，我希望使用者可以基于词库+转写的方式获得输入体验。**

---

## 💬 反馈与贡献

- **问题反馈**：[GitHub Issues](https://github.com/amzxyz/rime_wanxiang/issues)
- **深度讨论**：[Ask DeepWiki](https://deepwiki.com/amzxyz/rime_wanxiang)
- **词库反馈**：[在线表单](https://docs.qq.com/smartsheet/DWHZsdnZZaGh5bWJI?viewId=vUQPXH&tab=BB08J2)

---

## ❤️鸣谢

- 感谢网友的热情提报问题，使得模型和词库体验进一步提升。
---

## ☕ 赞赏支持

如果觉得项目好用，可以请AMZ喝咖啡

<img alt="pay" src="./custom/赞赏.jpg" height="312" width="446">

---

<div align="center">

**⭐ 如果这个项目对你有帮助，请给一个Star支持一下！**

**感谢网友的热情提报问题，使得模型和词库体验进一步提升**

Made with ❤️ by [AMZ](https://github.com/amzxyz)

</div>
