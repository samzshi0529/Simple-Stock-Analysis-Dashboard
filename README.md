# 股票分析看板使用说明

## 简介
本看板提供了一个交互式工具，用于下载、分析和预测股票数据。它包括了数据下载、技术指标计算、股票数据绘图、财务分析以及股票价格预测等功能。

## 安装依赖
在开始之前，请确保安装了以下Python库：
- `cmdstanpy`
- `yfinance`
- `plotly`
- `pandas`
- `numpy`
- `technical_analysis` (假设为技术指标分析库)

## 日志配置
```python
import logging
cmdstanpy_logger = logging.getLogger("cmdstanpy")
cmdstanpy_logger.disabled = True
