---
license: Apache License 2.0
tags:
- 医学指南
- 循证医学
- Cochrane
- 专家共识
- 医药数据
- PDF
- OCR
- 信息抽取
- medical-guidelines
- evidence-based-medicine
- document-ai
configs:
- config_name: default
  data_files:
  - split: train
    path: metadata/documents_manifest.jsonl
---

# 中外医学指南和询证文献样本20份

本数据集是「中外医学指南和询证文献」开源样本，包含中国医学指南/专家共识 PDF 与 Cochrane 系统评价（循证文献）PDF 原件，以及对应 JSON 元数据。样本覆盖国内指南与国际循证文献两类医学文本，便于文档解析、检索增强、知识库构建和模型训练评测。

本次发布保留 PDF 原件，并提供面向数据预览、检索和程序加载的 JSONL 清单。中国指南位于 `data/guidelines/`，Cochrane 文献位于 `data/cochrane/`，结构化元数据位于 `metadata/`。

如需了解更多中外医学指南、循证文献、临床共识、医学知识库建设、OCR 解析或批量授权合作，可联系 18996195218，或发送邮件至 zhouhaoran@shujuyoupu.com。

## 数据集简介

- 数据类型：中国医学指南/专家共识 PDF、Cochrane 系统评价 PDF、文档级元数据与文件校验信息。
- 样本数量：20 份 PDF（中国医学指南 10 份、Cochrane循证文献 10 份）。
- PDF 总大小：约 35.13 MB。
- PDF 总页数：1215 页。
- 样本组成：20 份 PDF 原件、1 个文档清单、1 个文件清单、1 个数据集摘要。
- 覆盖范围：神经病学/周围神经、肾脏病/慢性肾脏病、消化系统/胃炎、皮肤病/玫瑰痤疮、脑血管病、急危重症/中毒、产科/围产、感染病/疟疾、血管外科/间歇性跛行、运动医学/踝关节、感染病/呼吸道。
- 适用任务：医学指南 OCR、版面解析、章节/推荐意见抽取、循证文献结构化、医学实体识别、临床知识库构建、医学文档问答和检索增强评测。

## 数据结构

```text
open_data/modelscope/medical-guidelines-evidence-literature-sample-20/
  README.md
  data/
    guidelines/
      中国慢性胃炎诊治指南.pdf
      ...
    cochrane/
      CD000014_Amnioinfusion for meconium-stained liquor in labour.pdf
      ...
  metadata/
    documents_manifest.jsonl
    files_manifest.jsonl
    dataset_summary.json
```

## 样本清单

| document_id | 分类 | 题名 | 主题 | 年份 | PDF 页数 | PDF 大小 |
|---|---|---|---|---:|---:|---:|
| doc-001 | 中国医学指南 | 中国慢性炎性脱髓鞘性多发性神经根神经病诊治指南 | 神经病学/周围神经 | - | 6 | 0.993 MB |
| doc-002 | 中国医学指南 | 中国慢性肾脏病患者血钾管理实践专家共识（2020年） | 肾脏病/慢性肾脏病 | 2020 | 12 | 1.316 MB |
| doc-003 | 中国医学指南 | 中国慢性肾脏病患者高血压管理指南（2023年版） | 肾脏病/慢性肾脏病 | 2023 | 33 | 1.166 MB |
| doc-004 | 中国医学指南 | 中国慢性肾脏病营养治疗临床实践指南（2021版） | 肾脏病/慢性肾脏病 | 2021 | 21 | 1.120 MB |
| doc-005 | 中国医学指南 | 中国慢性胃炎诊治指南 | 消化系统/胃炎 | - | 31 | 4.415 MB |
| doc-006 | 中国医学指南 | 中国玫瑰痤疮诊疗指南（2021版） | 皮肤病/玫瑰痤疮 | 2021 | 10 | 0.870 MB |
| doc-007 | 中国医学指南 | 中国脑出血诊治指南（2019） | 脑血管病 | 2019 | 12 | 1.006 MB |
| doc-008 | 中国医学指南 | 中国脑卒中防治指导规范（2021年版） | 脑血管病 | 2021 | 618 | 5.502 MB |
| doc-009 | 中国医学指南 | 中国脑小血管病诊治专家共识2021 | 脑血管病 | 2021 | 11 | 2.247 MB |
| doc-010 | 中国医学指南 | 中国蘑菇中毒诊治临床专家共识（2019） | 急危重症/中毒 | 2019 | 16 | 12.355 MB |
| doc-011 | Cochrane循证文献 | Amnioinfusion for meconium-stained liquor in ... | 产科/围产 | - | 52 | 0.509 MB |
| doc-012 | Cochrane循证文献 | Amniotomy for shortening spontaneous labour | 产科/围产 | - | 4 | 0.045 MB |
| doc-013 | Cochrane循证文献 | Amodiaquine for treating malaria | 感染病/疟疾 | - | 67 | 0.472 MB |
| doc-014 | Cochrane循证文献 | Angioplasty (versus non surgical management) ... | 血管外科/间歇性跛行 | - | 5 | 0.053 MB |
| doc-015 | Cochrane循证文献 | Interventions for preventing ankle ligament i... | 运动医学/踝关节 | - | 4 | 0.045 MB |
| doc-016 | Cochrane循证文献 | Thyrotropin-releasing hormone added to cortic... | 产科/围产 | - | 72 | 0.779 MB |
| doc-017 | Cochrane循证文献 | Anti-D administration in pregnancy for preven... | 产科/围产 | - | 28 | 0.321 MB |
| doc-018 | Cochrane循证文献 | Anti-D administration after childbirth for pr... | 产科/围产 | - | 22 | 0.236 MB |
| doc-019 | Cochrane循证文献 | Topical antibiotic prophylaxis to reduce resp... | 感染病/呼吸道 | - | 111 | 0.947 MB |
| doc-020 | Cochrane循证文献 | Antibiotics for treatment of sore throat in c... | 感染病/呼吸道 | - | 80 | 0.732 MB |

## JSON 元数据

`metadata/documents_manifest.jsonl` 每行对应一份文档：

```json
{
  "document_id": "doc-001",
  "category": "guideline",
  "category_zh": "中国医学指南",
  "title": "中国慢性炎性脱髓鞘性多发性神经根神经病诊治指南",
  "title_en": null,
  "source": "中国医学指南/专家共识",
  "language": "zh",
  "topic": "神经病学/周围神经",
  "year": null,
  "cochrane_id": null,
  "pdf_path": "data/guidelines/中国慢性炎性脱髓鞘性多发性神经根神经病诊治指南.pdf",
  "pdf_file_name": "中国慢性炎性脱髓鞘性多发性神经根神经病诊治指南.pdf",
  "pdf_size_bytes": 1041132,
  "pdf_size_mb": 0.993,
  "pdf_pages": 6,
  "pdf_sha256": "...",
  "text_extractable_by_pypdf": true
}
```

`metadata/files_manifest.jsonl` 每行对应一个文件，包含 `document_id`、`category`、`title`、`file_path`、`file_type`、`size_bytes`、`size_mb`、`sha256`。

`metadata/dataset_summary.json` 保存本次样本的文件数量、PDF 总大小、总页数、分类分布、主题分布和元数据文件列表。

## 加载方式

通过 ModelScope SDK 加载结构化清单：

```python
from modelscope import MsDataset

ds = MsDataset.load(
    "medical-guidelines-evidence-literature-sample-20",
    namespace="SHPDataGR",
    subset_name="default",
    split="train",
    version="master",
)

print(ds[0]["title"])
print(ds[0]["category_zh"])
print(ds[0]["pdf_path"])
```

如需读取 PDF，请根据 `pdf_path` 定位到 `data/guidelines/` 或 `data/cochrane/` 下的对应文件。

## 数据质量和限制

- 本数据集是 20 份 PDF 样本，不代表完整的中外医学指南库或 Cochrane 文献库。
- PDF 原件可能存在扫描质量、文本层、字体嵌入、表格排版和换行差异。
- `text_sample` 由程序从 PDF 前两页尝试抽取，仅用于快速判断文本层可读性，不应替代 PDF 原文。
- 中国指南部分题名、年份以文件名及正文可识别信息为准；同一主题可能存在不同版本或修订稿。
- Cochrane 文献文件名中的 `CD` 编号为 Cochrane 文档编号，题名来自文件名解析。
- 医学指南与循证结论可能随研究进展和指南更新而变化，请以最新官方版本为准。

## 合规和使用说明

本数据集仅用于医学文档解析、信息抽取、检索、知识库建设、模型训练与评测等合规研究用途，不构成诊疗建议、用药建议或临床决策依据。使用者如基于本数据进行研究、训练、产品开发或再发布，应遵守数据集许可证、平台规则以及相关医学信息与版权合规要求。

## 合作与联系

本数据集为中外医学指南与循证文献样本。若需要更大规模的指南 PDF、专家共识、Cochrane/系统评价语料、结构化字段、OCR 解析结果、私有化语料建设或模型训练数据合作，请联系 18996195218，或发送邮件至 zhouhaoran@shujuyoupu.com。

## 引用方式

暂无固定论文引用格式。使用时建议注明数据集名称、版本、访问平台和数据批次。
