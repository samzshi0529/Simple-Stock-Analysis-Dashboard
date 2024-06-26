# 股票分析看板使用说明

# Disclaimer

This Stock Analysis Dashboard is provided for educational and entertainment purposes only. It is not intended for real-world investment or financial advice. Users should conduct their own due diligence and consult with professional financial advisors before making any investment decisions. The creators of this dashboard make no representations or warranties regarding the accuracy, completeness, or reliability of any information provided. Use of the dashboard is at the user's own risk.

By using this dashboard, you acknowledge and agree that you have read and understood this disclaimer.

# 免责声明

本股票分析看板仅供教育和娱乐目的使用，并不意味着用于实际投资或提供财务咨询。用户应进行自己的尽职调查，并在作出任何投资决策前咨询专业财务顾问。本看板的创建者不对提供的任何信息的准确性、完整性或可靠性作出任何表示或保证。使用该看板风险由用户自担。

通过使用本看板，您确认并同意您已阅读并理解此免责声明。

## 简介
制作了一个供自己娱乐使用的简单股票分析看板。

## 使用方法
在开始使用前，请确保你已经根据安装说明配置好了环境和所需的依赖库。在安装好所需的库后，只需使用支持Jupyter Notebook的编译器（Anaconda或Google Colab）运行该repository中的Dashboard Code.ipynb即可。
![替代文本](/Instruction.gif)
### 安装依赖
在使用看板之前，请确保已经安装了以下Python库：
- `cmdstanpy`: 用于统计建模和贝叶斯分析。
- `yfinance`: 提供下载历史市场数据的功能。
- `plotly`: 一个强大的绘图库，支持多种图表类型。
- `pandas`: 提供高性能、易用的数据结构和数据分析工具。
- `numpy`: 基础科学计算库，支持多维数组和矩阵运算。
- `technical_analysis`: 这是一个假设的库名，假设用于计算股票的技术指标。

可以使用pip命令来安装这些依赖：
```shell
pip install cmdstanpy yfinance plotly pandas numpy technical_analysis
```

### 选择分析模式
1. **单股票分析（Single Stock）**：选择此模式以分析一支单一证券，并查看其技术指标和预测。
2. **多股票分析（Multiple Stock）**：选择此模式以比较两支股票的价格走势和技术指标。
<img width="297" alt="Screenshot 2024-03-17 at 12 01 50 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/f4039b21-5a7c-4ff7-a7e7-85404e248104">

### 如何查询股票代码
- **看板使用Yahoo Finance的代码**：前往Yahoo Finance查询你感兴趣的证券，证券的代码便会出现在名字上；例如沪深300指数CSI300的代码就是如图的000300.SS。
<img width="295" alt="Screenshot 2024-03-17 at 11 57 43 AM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/d2d9e357-1b33-471e-b81c-08219e5a4b1b">

### 输入股票代码
- **股票代码 1（Ticker 1）**：输入你想分析的第一支股票的代码。
<img width="288" alt="Screenshot 2024-03-17 at 12 00 23 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/2e866ddc-9e9a-4ca9-a188-9709b598dca8">

- **股票代码 2（Ticker 2）**：在多股票分析模式下，输入第二支想要比较的股票代码。
<img width="591" alt="Screenshot 2024-03-17 at 12 00 41 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/c675d4aa-3b43-493b-ae8b-ebe7a72f276d">

### 选择日期范围
- **开始日期（Start Date）**：选择你想开始分析的日期。
- **结束日期（End Date）**：选择你想结束分析的日期。
<img width="621" alt="Screenshot 2024-03-17 at 12 02 34 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/dca7cec2-861d-42f6-80de-dfce36314ef2">

### 技术指标选择
在单股票分析模式下，你可以勾选以下技术指标来进行详细分析：
- **MA50**：50天移动平均线
- **MA200**：200天移动平均线
- **RSI**：相对强弱指标
- **Bollinger Bands**：布林带
- **MACD**：移动平均收敛发散指标
<img width="626" alt="Screenshot 2024-03-17 at 12 02 54 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/40ee0e5a-ad4a-457a-95f5-775f74b9a4b0">

### 按钮功能
- **价格图表（Price Chart）**：点击此按钮，根据所选股票代码、日期范围和技术指标，生成和展示股票的价格图表。（*注意*你每次调整技术指标、日期等参数后都需要重新点击Price Chart按钮）
- **时间序列分析（Time Series Analysis）**：在单股票分析模式下可用。点击此按钮，将使用Meta开发的Prophet模型进行股价时间序列分析并展示结果。
<img width="241" alt="Screenshot 2024-03-17 at 12 03 14 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/fc8b2e50-9f05-4564-9154-01f1bdd4e261">

### 查看结果
- **分析结果**：点击相应的按钮后，结果会显示在界面下方的输出区域。包括股价图表、技术指标图表和预测结果。
<img width="956" alt="Screenshot 2024-03-17 at 12 04 30 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/a063d1be-a0c4-4907-a662-9afe7ae29baa">
<img width="430" alt="Screenshot 2024-03-17 at 12 04 43 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/87705099-2985-4728-9e28-e85260dad859">
<img width="947" alt="Screenshot 2024-03-17 at 12 05 11 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/a601ca8a-8e03-4982-bda5-cfaac3016771">
<img width="843" alt="Screenshot 2024-03-17 at 12 05 27 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/731f1a24-584c-4cf7-98f0-81ab0c91fb69">
<img width="843" alt="Screenshot 2024-03-17 at 12 06 31 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/5b9cb75d-9ad0-408f-9c18-c9c62c108c3a">
<img width="509" alt="Screenshot 2024-03-17 at 12 06 48 PM" src="https://github.com/samzshi0529/Simple-Stock-Analysis-Dashboard/assets/60007017/556bf832-02c8-4cc3-98d2-4b9957ba26cb">

## 注意事项
- 选择的日期范围应该在股票的交易历史之内。
- 技术指标的选择会影响图表的绘制，合理选择以获得最有用的分析结果。
- 股价预测基于历史数据进行，任何分析结果仅供参考，投资决策需要谨慎。

## 使用限制
- 您被明确禁止将本看板用于实际投资或财务咨询。
- 本看板按“现状”提供，不附带任何形式的明示或暗示保证。使用本看板的风险由您自己承担。
- 您不得以任何可能损害作者或任何第三方的方式使用本看板。
- 未经作者书面明确授权，严禁将本看板用于商业用途。
