# 水豚噜噜桌面宠物

> 嗨，我是噜噜。今天也可以慢慢过，不用太着急。🍊

一只温和、慢悠悠的小水豚，住进你的电脑桌面，陪你度过工作与生活里的小小日常。

噜噜喜欢吃水果、泡澡、晒太阳，偶尔也会打个盹。你可以喂它一点好吃的，和它聊聊天，看它学习、打工、攒一点金币，再一起去便利店逛逛。忙起来的时候，噜噜也会轻轻提醒你：喝口水，休息一下吧。

## 认识噜噜

水豚噜噜是一个源自中国动画《平头哥》的原创角色，2024 年 3 月首次亮相。官方设定里，它是“平行宇宙里一只头顶橘子的小水豚”，情绪稳定、热爱泡澡和放假，梦想是吃到美味的冰淇淋。因为圆滚滚的外形和松弛的性格，它慢慢从动画配角变成了很多人喜欢的表情包和陪伴角色。

在桌面上，噜噜也是这样一只“慢慢来”的小水豚。它不会催你，也不会打扰你。你忙的时候，它就在屏幕一角安安静静地待着；你想休息的时候，摸摸它的头，它会很开心。

参考资料：

- [水豚噜噜 - 维基百科](https://zh.wikipedia.org/zh-hans/%E6%B0%B4%E8%B1%9A%E5%99%9C%E5%99%9C)
- [水豚噜噜 - CLE 中国授权展](https://www.chinalicensingexpo.com/cn/product/Cartoon-Animation-1849)

## 它能做什么

- **陪你待一会儿**：拖动噜噜到屏幕任意角落，摸摸它的头和肚子，它会有自己的小反应。
- **养成**：生命值、饱食度、心情、精力会随时间变化，学习、打工、吃东西都会影响它的状态。
- **聊天**：支持本地 Mock 对话，也可以接入你自己的 OpenAI 兼容服务；噜噜会记得你的称呼和约定。
- **提醒你照顾自己**：喝水提醒、休息提示、睡觉动画，都是希望你慢一点。
- **一起过日子**：商城、背包、装饰、每日任务、金币和等级，让噜噜的日常更完整。
- **四套形象**：噜噜、干饭、恐龙、睡衣，四种 3D 形象可以随时切换。

## 安装

请前往 [最新正式版本](https://github.com/caibenhao/capybara-lulu/releases/latest) 选择适合你电脑的安装包。安装包类型如下：

| 电脑类型 | 安装包文件名后缀 |
| --- | --- |
| Apple Silicon Mac（M 系列芯片） | `_aarch64.dmg` |
| Intel Mac | `_x64.dmg` |
| Windows x64（Intel / AMD 64 位） | `_windows_x64-setup.exe` |

当前正式版为 [`1.0.0`](https://github.com/caibenhao/capybara-lulu/releases/tag/app-v1.0.0)，已提供 Apple Silicon Mac、Intel Mac 和 Windows x64 安装包，可从上述入口下载。具体提供的平台以公开 Release 的资产列表为准。`.sig`、`.app.tar.gz` 和 JSON 文件用于应用更新与验证，首次安装请选择 DMG 或 Windows setup EXE。

### macOS

1. 从本仓库 [最新正式版本](https://github.com/caibenhao/capybara-lulu/releases/latest) 下载 DMG 安装包。
   - Apple Silicon（M 系列芯片）请选择名称以 `_aarch64.dmg` 结尾的文件。
   - Intel Mac 请选择名称以 `_x64.dmg` 结尾的文件。
2. 打开 DMG，将“水豚噜噜”拖入“应用程序”，然后弹出磁盘镜像。
3. 在“应用程序”中打开“水豚噜噜”。若提示无法验证开发者或 Apple 无法检查恶意软件，先关闭提示，再进入“系统设置 → 隐私与安全性”，找到本次拦截记录，点击“仍要打开”，按提示确认。
4. 若没有“仍要打开”入口，并提示应用“已损坏”，请先确认文件来自本仓库的正式 Release。仅对这份可信应用，在终端执行以下命令后重新打开：

```bash
xattr -dr com.apple.quarantine "/Applications/水豚噜噜.app"
```

此命令只移除噜噜的下载隔离标记，不需要关闭系统 Gatekeeper。如果 macOS 明确提示检测到恶意软件，请停止安装，不要用此命令绕过提示。

安装后可在应用设置中检查并安装更新。更新包会经过独立的 Tauri 更新签名校验；该校验不等同于 Apple 公证。

### Windows x64

Windows x64 安装包已随 `0.1.7` 正式发布。目前未使用代码签名证书签名，首次运行安装程序时可能出现 SmartScreen 提示。

1. 从 [最新正式版本](https://github.com/caibenhao/capybara-lulu/releases/latest) 下载名称以 `_windows_x64-setup.exe` 结尾的 NSIS 安装包，例如 `capybara-lulu_1.0.0_windows_x64-setup.exe`。选择 EXE 文件，不要下载同名的 `.sig`；当前不提供 MSI 安装包。
2. 双击安装。如果 Windows SmartScreen 提示未知发布者，请先确认文件来自本仓库的正式 Release，再选择「更多信息 → 仍要运行」。若 Windows 安全中心明确检测到恶意软件，请停止安装，不要关闭防护或绕过拦截。
3. 应用依赖 Microsoft Edge WebView2 Runtime。若系统尚未安装，安装程序会尝试下载并安装，请保持联网；如果自动安装失败，可从 [Microsoft 官方页面](https://developer.microsoft.com/microsoft-edge/webview2/#download-section) 安装 Evergreen WebView2 Runtime 的 x64 版本，再重新运行噜噜安装包。
4. 安装完成后，从开始菜单启动「水豚噜噜」。首次启动只显示桌面宠物，可通过宠物右键菜单或托盘图标打开设置等面板。

后续可在应用设置中检查并安装更新。更新包使用独立的 Tauri 更新签名校验，这不等同于 Windows 代码签名。

## 日常陪伴

- 左键拖动噜噜，可以把它放到屏幕任意位置。
- 单击噜噜的身体部位，它会做出对应反应；摸摸头会加心情。
- 右键噜噜，可以快速喂食、休息、学习、打工、聊天，或打开商城、背包和设置。
- 托盘图标可以显示/隐藏噜噜、重置位置、打开面板和退出应用。
- 在设置里可以开启喝水提醒，选择 15、30、45 或 60 分钟的间隔。
- 开启“安静陪伴”后，噜噜会减少主动动作，不主动提醒，更像一个安静的小陪伴。

## AI 对话

如果你想让噜噜更像“会回应你的小水豚”，可以在设置里接入任何 OpenAI 兼容接口。

你需要填写：

- **API Base URL**
- **模型名称**
- **API Key**

也可以按服务商支持情况，选择是否开启“思考模式”和流式输出。配置完成后，噜噜会用更自然的语气回应你，并给出一些简单的建议动作，但不会直接执行。

如果暂时不想配置，也可以使用内置的 Mock 对话模式，先体验和噜噜聊天的感觉。

## 开源项目

这个仓库只分发应用安装包和更新文件，不包含项目源码。应用本身使用了以下开源项目，感谢它们让噜噜能站到桌面上。

### UI 库：Animal Island UI

[Animal Island UI](https://github.com/guokaigdg/animal-island-ui) 是本项目的核心 UI 组件库，整体岛屿风格和自然系配色都来自它。应用里的按钮、卡片、输入框、下拉框、开关、标签、提示和物品图标，很多都由它提供，让噜噜的界面看起来像一座温暖的小岛。

它采用 `CC BY-NC 4.0` 许可证，允许个人学习和非商业使用，禁止商业用途。因此这个应用也保持非商业的个人陪伴用途。

### 其他主要项目

| 项目 | 用途 |
| --- | --- |
| [React](https://github.com/facebook/react) | 界面框架 |
| [Three.js](https://github.com/mrdoob/three.js) | 3D 模型渲染 |
| [Tauri](https://github.com/tauri-apps/tauri) | 桌面应用壳与系统窗口能力 |
| [Zustand](https://github.com/pmndrs/zustand) | 状态管理 |
| [SQLx](https://github.com/launchbadge/sqlx) | 本地数据存储 |
| [Tokio](https://github.com/tokio-rs/tokio) | Rust 异步运行时 |
| [aes-gcm](https://github.com/RustCrypto/AEADs) | 模型加密 |

## 素材与权利说明

这里的 3D 模型、动画和素材不包含在开源代码里，也不允许提取或再分发。水豚噜噜的名称和形象版权归官方权利人所有，本项目只是把它做成个人陪伴应用，不作商业用途。

如果你希望在其他场景使用角色或素材，请先联系官方授权。

## 这个仓库是什么

这里用于分发水豚噜噜桌面宠物的安装包、版本说明和应用更新文件，不包含项目源码。

Release 中自动生成的 `Source code (zip)` 和 `Source code (tar.gz)` 只是本仓库说明文件的归档，不是桌面应用安装包。

> 你今天也辛苦啦。噜噜在呢，要不要一起休息一小会儿？
