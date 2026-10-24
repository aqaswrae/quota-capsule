# 额度胶囊 · Codex + Claude

Windows 托盘额度工具：桌面胶囊显示 Codex 5 小时剩余额度，点击可查看 Codex 与 Claude 的额度详情。支持靠边自动收起、开机自启动和自选安装目录。

## 下载

前往 [v0.8.8 下载页面](https://github.com/aqaswrae/quota-capsule/releases/tag/v0.8.8)，在 **Assets** 中选择一个文件：

- `QuotaCapsule-Setup-0.8.8.exe`：直接双击安装。
- `QuotaCapsule-0.8.8.zip`：包含同一个安装程序和安装说明。解压后运行 EXE。

两个文件不必都下载。适用系统为 **Windows x64**，需要 **.NET Framework 4.8**。安装时可选择当前用户有写入权限的目录，默认是 `%LOCALAPPDATA%\QuotaCapsule`。

## 使用

1. 启动后点击桌面胶囊，在详情中选择 **网页登录 Codex**，使用系统浏览器登录自己的 ChatGPT/Codex 账号。安装包已附带读取额度所需的 Codex CLI 组件。
2. 如需显示 Claude 个人订阅额度，在 Chrome 或 Edge 的扩展管理页开启开发者模式，选择 **加载已解压的扩展程序**，指向安装目录内的 `extension` 文件夹；然后在同一浏览器打开 [Claude 用量页](https://claude.ai/settings/usage)。
3. 胶囊靠边收起后会露出 32 像素；找不到时左键单击托盘图标即可展开。点击任务栏右下角“显示桌面”时，胶囊会自动恢复；从菜单主动隐藏则保持隐藏。托盘菜单会根据当前状态显示“显示胶囊”或“隐藏胶囊”。

额度详情中的“网页登录”“刷新”和“打开 Claude 用量页”现在会在鼠标经过、按下与点击后显示反馈。Free 账号会显示服务返回的本月额度；订阅账号通常显示 5 小时和每周额度。

本工具不要求你输入密码或 API Key。Claude 扩展读取用量页上显示的百分比，经本机回环地址传给桌面胶囊。该页面结构变动时，自动读取可能暂时失效。

**注意：**这是第三方工具，与 OpenAI、Anthropic 无官方关联。当前安装包未经代码签名，Windows 可能提示“未知发布者”。Claude 实际登录账号的页面读取仍待更多用户验证。
