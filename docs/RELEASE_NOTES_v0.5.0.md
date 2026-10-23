# PubMed AI v0.5.0

首个公开 Windows 发布版本。

## 下载

- `PubMedAI-Setup-v0.5.0.exe`：推荐，按用户安装，无需管理员权限
- `PubMedAI-Portable-v0.5.0.exe`：单文件免安装版
- `SHA256SUMS.txt`：文件校验

## 主要功能

- PubMed 检索、排序、继续检索、本地结果缓存
- 中文标题/摘要翻译，支持多引擎故障转移
- AI 相关性筛选、AI 智能检索
- 收藏、标注、彩色下划线、背景高亮、撤销/重做
- 检索历史、关键词图谱、期刊信息
- Word / PDF / Excel / Markdown / CSV / JSON / RIS / BibTeX 导出
- 内置版本检查与覆盖安装

## 安装说明

### 安装包

安装到 `%LOCALAPPDATA%\Programs\PubMedAI`，不需要管理员权限。新版本安装包会沿用同一目录并覆盖旧版本。

### 便携版

单文件，双击运行。首次启动会释放运行文件到 `%LOCALAPPDATA%\PubMedAI\0.5.0`，后续启动复用缓存。

## 数据说明

公开版本不包含中科院分区表、SCI 影响因子/JCI 数据。PubMed 检索、翻译、收藏、标注等功能不受影响；如拥有授权数据，可在设置中导入影响因子 CSV。

## 校验

下载后请对照 Release 中的 `SHA256SUMS.txt` 校验文件。发布包暂未做代码签名，Windows SmartScreen 可能提示；请确认来源为本仓库后再运行。

## 已知限制

- 仅支持 Windows 10/11 64 位
- 便携版首次启动比安装版慢
- 公开版本不预置受版权限制的期刊指标数据
