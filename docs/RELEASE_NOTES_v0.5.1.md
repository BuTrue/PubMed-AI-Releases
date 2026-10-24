# PubMed AI v0.5.1

修复打包版关键词图与导出依赖问题。

## 修复

- 打包版内置 `jieba` 及词典数据，关键词图恢复正常中文分词，不再退化成 6 字碎片。
- 打包版内置 `openpyxl`、`python-docx`、`reportlab`，Excel / Word / PDF 导出可用。
- 关键词图在打包版启动时序下重新计算视图变换，避免空白。
- 便携版解压缓存按版本号隔离；升级到 0.5.1 不会复用旧版本缓存。
- 更新检查支持配置代理，并在 Python TLS 握手被代理拒绝时回退到系统 curl。

## 安装

- `PubMedAI-Setup-v0.5.1.exe`：推荐，覆盖安装旧版本，用户数据保留。
- `PubMedAI-Portable-v0.5.1.exe`：单文件免安装版。
- `SHA256SUMS.txt`：校验文件。
