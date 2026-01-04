# Alexis Eyewear Intelligence System

Alexis眼镜智能系统 - 基于AI的眼镜品牌数据管理和分析系统

## 项目简介

这是一个为Alexis眼镜打造的智能数据管理系统，通过AI技术实现眼镜商品数据的自动清洗、品牌识别、型号提取和质量评审。

## 核心特性

- **智能品牌识别**：自动识别国际奢侈品、日本设计师品牌、日本眼镜品牌等多种品牌类型
- **型号自动提取**：基于品牌特定规则提取商品型号
- **Persona评审机制**：通过6个专业Persona进行多角度质量评审
- **数据治理体系**：建立品牌字典、数据标准和质量检查机制

## 项目结构

```
alexis-eyewear-intelligence/
├── personas/              # Persona定义和评审标准
│   ├── 01_甲方_60岁买手美术教授.md
│   ├── 02_五个行业专家Personas.md
│   └── README.md
├── docs/                  # 文档和设计
│   ├── architecture.md    # 系统架构设计
│   ├── agent-loop.md      # Agent Loop设计
│   └── data-model.md      # 数据模型设计
├── data/                  # 数据文件
│   ├── brand-dictionary.csv    # 品牌字典
│   ├── raw/                    # 原始数据
│   └── cleaned/                # 清洗后数据
└── README.md
```

## Persona体系

### 甲方Persona
- **角色**：60岁奢侈品眼镜买手 + 美术教授
- **职责**：定义数据质量标准，评审品牌识别准确性
- **核心关注**：品牌的准确性、数据的商业价值

### 五个行业专家Personas
1. **奢侈品采购顾问**：评审品牌识别和品牌字典
2. **电商数据分析师**：评审数据完整性和商业价值
3. **眼镜行业品牌经理**：评审品牌分类和品牌管理
4. **零售运营经理**：评审运营指标和决策支持
5. **数据治理专家**：评审数据标准化和治理体系

## Agent Loop架构（设计中）

### 单个Persona的Agent Loop
每个Persona作为一个独立的Agent Node，具有：
- **输入**：清洗后的数据、品牌字典、质量报告
- **处理**：基于自己的专业角度进行评审
- **输出**：评审报告、评分、改进建议
- **反馈**：根据改进建议优化数据

### Personas组合的Agent Loop
多个Persona协作形成智能团队：
- **并行评审**：多个Persona同时评审数据
- **综合评分**：汇总各Persona的评分
- **优先级排序**：根据影响程度对改进建议排序
- **迭代优化**：根据综合建议优化数据，重新评审

## 技术栈

- **数据处理**：Python + Pandas
- **品牌识别**：正则表达式 + 品牌字典
- **AI评审**：基于Persona的多角度评审机制
- **版本控制**：Git + GitHub

## 当前进展

- ✅ 完成4个店铺（3,604件商品）的数据清洗
- ✅ 建立36个品牌的品牌字典
- ✅ 实现品牌识别率57.9%、型号识别率23.9%
- ✅ 通过销售团队的真人验证
- 🚧 正在设计Persona Agent Loop架构
- 🚧 正在建立数据治理体系

## 下一步计划

1. 完善Persona Agent Loop架构设计
2. 实现Personas协作机制
3. 优化品牌识别算法，提升识别率到95%+
4. 建立自动化的数据质量检查机制
5. 扩展到更多店铺和品牌

## 贡献指南

欢迎提出Issue和Pull Request。在贡献之前，请先阅读[贡献指南](docs/CONTRIBUTING.md)。

## 许可证

MIT License

## 联系方式

- 项目维护者：Alexis眼镜团队
- GitHub: https://github.com/sbm111111/alexis-eyewear-intelligence
