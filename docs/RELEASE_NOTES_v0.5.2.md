# PubMed AI v0.5.2

修复 PubMed 检索 429 限流处理。

## 修复

- 未配置 NCBI API Key 时，抓取并发自动限制为 3；配置 Key 后最多 10，避免高并发触发 429。
- NCBI 返回 429 时尊重 `Retry-After`，至少退避 3 秒，最长等待 20 秒后重试。
- 429 持续时继续自动切换 Europe PMC 备用源，并在界面提示来源。
- 检测到 429 不再直接把原始网络错误抛给用户。

## 建议

NCBI 高峰期建议在「设置 → 检索与网络」配置 NCBI API Key；无 Key 时每秒最多约 3 次请求是上游硬限制。

## 下载

- `PubMedAI-Setup-v0.5.2.exe`：推荐，覆盖安装旧版本，用户数据保留。
- `PubMedAI-Portable-v0.5.2.exe`：单文件免安装版。
- `SHA256SUMS.txt`：校验文件。
