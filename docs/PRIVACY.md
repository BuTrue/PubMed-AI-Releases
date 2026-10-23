# 隐私说明

PubMed AI 是本地桌面软件，不提供账号系统，也不收集遥测数据。

## 本地保存的数据

以下数据只保存在本机 `%APPDATA%\pubmed_ai`：

- 检索历史、收藏、标注、阅读状态
- 中文翻译缓存、检索结果缓存
- 模型/翻译服务的 API Key、Token、代理设置
- 期刊指标数据（如用户自行导入）
- 更新检查时间

## 联网行为

软件只会在以下场景发起网络请求：

1. 检索/抓取 PubMed、Europe PMC 文献（NCBI E-utilities / Europe PMC）
2. 调用用户配置的 AI 翻译或筛选服务
3. 小绿鲸备用翻译（仅在用户配置并启用时）
4. 检查 GitHub Releases 版本更新
5. 打开 DOI、PMC、PDF 等外部链接（由用户点击触发）

不会把本地收藏、标注、检索历史上传到本项目仓库。API Key/Token 不会写入日志或发布包。

## 更新检查

更新检查请求：

`https://api.github.com/repos/BuTrue/PubMed-AI-Releases/releases/latest`

该请求不包含任何用户标识或本地文献数据。安装包下载地址来自 GitHub Releases。

## 删除数据

退出软件后删除 `%APPDATA%\pubmed_ai` 即可清除本地数据。卸载程序默认不删除该目录。
