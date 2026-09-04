# NFC 写卡台 · macOS 安装包

这是 NFC 写卡台的公开发行仓库，仅提供安装包、签名更新清单和版本说明，**不包含应用源码**。

## 下载

- [下载最新版 DMG](https://github.com/17qiche-com/nfc-write-station-releases/releases/latest/download/NFC-Write-Station-macOS-arm64.dmg)
- [查看所有版本及更新说明](https://github.com/17qiche-com/nfc-write-station-releases/releases)

系统要求：Apple Silicon Mac（M 系列芯片），macOS 13 或更高版本。

打开 DMG，将“NFC 写卡台”拖入“应用程序”。旧版用户应先退出应用，再替换同名应用；不要删除应用数据目录或钥匙串中的卡片密码。

## 应用内更新

v0.10.1 及后续版本可在左下角或应用菜单中点击“应用更新”，无需 GitHub 账号或访问令牌。确认新版本后，应用会下载、校验签名、安装并重新启动。

写卡或任务检查进行中请先暂停，等待当前卡片操作结束。更新不清除任务数据、历史记录及已保存卡片密码。

v0.10.0 及更早版本请从本仓库手动下载安装一次，之后使用新的公开更新源。

## 文件与安全

- `.dmg`：用于手动安装。
- `.zip`：供应用内自动更新使用。
- `appcast.xml`：经过 Ed25519 签名的版本清单，包含更新包签名。
- `SHA256SUMS`：安装包完整性校验值。

更新包使用 Sparkle 的 Ed25519 签名校验。当前版本未做 Apple Developer ID 公证；该更新签名不等同 Apple 公证，首次安装仍可能出现系统安全提示。

本仓库不收集或存放用户的 NFC 卡片数据、任务文件、密码和访问令牌。GitHub 自动提供的“Source code”压缩包仅包含此发行仓库的说明文件，不是应用源码。
