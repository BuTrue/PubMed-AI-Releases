# Third-Party Notices（公开构建）

PubMed AI 本体以 MIT License 发布。

## 图标

- Lucide Icons（ISC）：https://github.com/lucide-icons/lucide
- 使用方式：内联 SVG 路径数据

## 图形界面

- PySide6 / Qt（LGPL-3.0 或商业授权）：https://www.qt.io/qt-for-python
- 使用方式：运行时动态链接

## 中文分词与导出（GUI 可选依赖）

| 组件 | 许可证 | 用途 |
|---|---|---|
| jieba | MIT | 中文关键词提取 |
| openpyxl | MIT | Excel 导出/导入 |
| python-docx | MIT | Word 导出 |
| reportlab | BSD-3-Clause | PDF 导出 |
| lxml | BSD-3-Clause | python-docx 的 XML 依赖 |
| Pillow | HPND | reportlab 图像支持 |
| charset-normalizer | MIT | 依赖链 |

各组件版权归其作者所有；完整许可证文本可在对应项目的发布页/仓库中查看。

## 期刊指标数据

公开构建**不包含**中科院分区表、SCI 影响因子/JCI 数据或由其生成的预构建库。
相关数据版权分别归中国科学院文献情报中心和 Clarivate 所有，不属于本项目
MIT 许可证覆盖范围。程序仍可正常运行；如你拥有授权数据，可在软件设置中
自行导入影响因子 CSV。
