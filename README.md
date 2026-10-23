# PubMed AI · 官方发布与文档

PubMed AI 是一款 Windows 桌面文献工具：PubMed 检索、中文翻译、AI 相关性筛选、收藏/标注、检索历史、关键词图谱与多种格式导出。

**本仓库只存放发布包、使用文档和第三方声明，不包含源代码。**

## 下载

前往 **[Releases](https://github.com/BuTrue/PubMed-AI-Releases/releases/latest)** 下载最新版本：

| 文件 | 适合场景 | 说明 |
|---|---|---|
| `PubMedAI-Setup-v*.exe` | 推荐 | 安装包，按用户安装，无需管理员权限；支持覆盖升级 |
| `PubMedAI-Portable-v*.exe` | 免安装 | 单个 exe，双击运行；首次启动会释放运行文件 |
| `SHA256SUMS.txt` | 校验 | 下载后核对文件完整性 |

## 功能

- PubMed 检索、排序、继续检索与本地结果缓存
- 中文标题/摘要翻译；支持 SenseNova、NVIDIA NIM、小绿鲸备用翻译
- AI 相关性筛选与 AI 智能检索
- 收藏、标注、彩色下划线、背景高亮、撤销/重做
- 检索历史、关键词图谱、期刊信息
- Word / PDF / Excel / Markdown / CSV / JSON / RIS / BibTeX 导出
- 启动时检查新版本，下载安装包后覆盖安装；收藏、标注、历史保留

## 安装与运行

### 安装包（推荐）

1. 下载 `PubMedAI-Setup-v*.exe` 并双击。
2. 安装到 `%LOCALAPPDATA%\Programs\PubMedAI`，不需要管理员权限。
3. 从开始菜单或桌面快捷方式启动。
4. 新版本安装包会沿用原安装目录，自动关闭旧程序并覆盖安装。

### 便携版

1. 下载 `PubMedAI-Portable-v*.exe`，放到任意可写目录。
2. 双击运行。首次启动会释放运行文件到 `%LOCALAPPDATA%\PubMedAI\<版本>`，后续启动更快。
3. 便携版同样支持在软件内检查更新；更新会下载官方安装包。

## 系统要求

| 项目 | 要求 |
|---|---|
| 系统 | Windows 10 / 11，64 位 |
| 内存 | 建议 4 GB 以上 |
| 网络 | 检索 PubMed、AI 翻译/筛选、检查更新需要联网 |
| 运行环境 | 无需安装 Python；安装包已包含运行库 |

## 版本更新

- 软件启动后会自动检查 GitHub Releases（约每 24 小时一次）。
- 也可在菜单「帮助 → 检查更新」手动检查。
- 发现新版本后可下载安装包；确认后软件会关闭并启动安装程序，覆盖旧版本。
- 用户数据保存在 `%APPDATA%\pubmed_ai`，覆盖安装和卸载默认都不会删除。

## 数据与隐私

- API Key、Token 只保存在本机 `%APPDATA%\pubmed_ai\config.json`，不会上传到本项目仓库。
- 软件不包含遥测；检查更新只请求 GitHub 公开 Releases API。
- 公开版本**不包含**中科院分区表、SCI 影响因子/JCI 数据；详见 [数据说明](docs/DATA_NOTICE.md)。
- 详细隐私说明见 [PRIVACY.md](docs/PRIVACY.md)。

## 文件校验

下载后可在 PowerShell 中校验：

```powershell
Get-FileHash .\PubMedAI-Setup-v0.5.0.exe -Algorithm SHA256
```

将结果与 Release 中的 `SHA256SUMS.txt` 对照。

## 常见问题

**Windows 提示“已保护你的电脑”？**
发布包暂未做代码签名，可能出现 SmartScreen 提示。请确认文件来自本仓库 Releases，并核对 SHA256 后再运行。

**安装后期刊分区/影响因子为空？**
公开版本不附带受版权限制的期刊数据。如你拥有授权数据，可在「设置 → 导入影响因子 CSV」中导入。

**便携版第一次启动较慢？**
单文件版首次运行需要释放 Qt 运行文件；后续会复用缓存，速度恢复正常。追求启动速度建议使用安装包。

**如何卸载？**
Windows 设置 → 应用 → PubMed AI → 卸载。用户数据仍保留在 `%APPDATA%\pubmed_ai`。

## 许可证

软件本体采用 MIT License，见 [LICENSE](LICENSE)。第三方组件与数据说明见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) 和 [docs/DATA_NOTICE.md](docs/DATA_NOTICE.md)。
