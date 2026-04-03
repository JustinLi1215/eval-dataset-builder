# Eval Dataset Builder | 评测数据集构造器

> A QoderWork Skill for building evaluation datasets for Fliggy Search Strategy products  
> 专为飞猪搜索策略产品设计的 QoderWork 技能，用于构造评测数据集

---

## 🎯 Overview | 概述

**English:**  
Eval Dataset Builder is a specialized skill that systematically generates evaluation datasets for testing model capabilities and product features. It is designed specifically for Fliggy (Alibaba's travel platform) search strategy teams to evaluate voice search, search relevance, recommendation systems, and more.

**中文：**  
评测数据集构造器是一个专门用于系统化生成评测数据集的技能。它专为飞猪（阿里巴巴旅行平台）搜索策略团队设计，用于评测语音搜索、搜索相关性、推荐系统等产品功能。

---

## ✨ Features | 功能特性

### English

- **Dual Evaluation Types**: Supports both model capability evaluation and product feature evaluation
- **Multi-dimensional Framework**: Automatically generates scientific evaluation dimensions with appropriate weights
- **Diverse Sample Construction**: Covers core scenarios, edge cases, and user types
- **Excel Output**: Generates Excel files for easy team collaboration and annotation management
- **Travel Domain Focus**: Specialized for hotel, flight, attraction, and travel package evaluation

### 中文

- **双评测类型支持**：支持模型能力评测和产品功能评测
- **多维度评测框架**：自动生成科学的评测维度及权重分配
- **多样化样本构造**：覆盖核心场景、边界情况和用户类型
- **Excel 格式输出**：生成 Excel 文件，便于团队协作和标注管理
- **旅行业务聚焦**：专门针对酒店、机票、景点、度假套餐等场景

---

## 🚀 Supported Evaluation Types | 支持的评测类型

### Model Capability Evaluation | 模型能力评测

| Capability | Description | 描述 |
|------------|-------------|------|
| Semantic Understanding | Query understanding, intent recognition, entity extraction | Query理解、意图识别、实体抽取 |
| Reasoning Ability | Multi-turn dialogue, context understanding, logical reasoning | 多轮对话、上下文理解、逻辑推理 |
| Generation Ability | Result summarization, recommendation reasons, dialogue responses | 结果摘要、推荐理由、对话回复 |

### Product Feature Evaluation | 产品功能评测

| Feature | Description | 描述 |
|---------|-------------|------|
| Search Result Page | Relevance, ranking quality, diversity | 相关性、排序质量、多样性 |
| Voice Search | Speech recognition, semantic understanding, result matching | 语音识别、语义理解、结果匹配 |
| Recommendation System | Personalization, novelty, coverage | 个性化、新颖性、覆盖率 |
| Filter & Sort | Price sensitivity, time preference, brand preference | 价格敏感、时间偏好、品牌偏好 |

---

## 📋 Workflow | 工作流程

### Step 1: Define Evaluation Target | 第一步：明确评测目标

**English:**  
Users provide the following information:
- Evaluation object (model capability / product feature)
- Evaluation scenario (voice search / text search / recommendation, etc.)
- Evaluation dimensions (relevance / diversity / personalization, etc.)
- Data scale (number of evaluation samples)

**中文：**  
用户提供以下信息：
- 评测对象（模型能力 / 产品功能）
- 评测场景（语音搜索 / 文本搜索 / 推荐等）
- 评测维度（相关性 / 多样性 / 个性化等）
- 数据规模（评测条数）

### Step 2: Design Evaluation Dimensions | 第二步：设计评测维度

**English:**  
Automatically generate an evaluation dimension framework based on the evaluation target.

**中文：**  
根据评测目标，自动生成评测维度框架。

**Example: Voice Search Result Page Evaluation | 示例：语音搜索结果页评测**

```yaml
dimensions:
  - name: "Speech Recognition Accuracy"
    name_cn: "语音识别准确性"
    weight: 20%
    criteria: ["Perfect", "Minor Errors", "Major Errors", "Completely Wrong"]
    criteria_cn: ["完全正确", "部分错误", "大量错误", "完全错误"]
  
  - name: "Intent Understanding Accuracy"
    name_cn: "意图理解准确性"
    weight: 25%
    criteria: ["Precise Match", "Partial Match", "Deviation", "Completely Wrong"]
    criteria_cn: ["精准匹配", "部分匹配", "理解偏差", "完全错误"]
  
  - name: "Result Relevance"
    name_cn: "结果相关性"
    weight: 30%
    criteria: ["Highly Relevant", "Relevant", "Weakly Relevant", "Irrelevant"]
    criteria_cn: ["高度相关", "相关", "弱相关", "不相关"]
