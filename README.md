# Investment Risk Analysis using Multi Agents

## Overview

The project is a multi-agent system designed to monitor, analyze, and optimize trading strategies in real-time. Leveraging advanced statistical modeling, machine learning techniques, and risk assessment. This system aims to provide actionable insights and enhance trading decisions for various stocks.

## Features

- **Data Analysis**: Continuously monitor and analyze market data to identify trends and predict market movements.
- **Trading Strategy Development**: Create and refine trading strategies based on market insights and user-defined risk tolerance.
- **Trade Execution Planning**: Recommend optimal trade execution strategies considering current market conditions.
- **Risk Assessment**: Evaluate potential risks associated with trading activities and provide mitigation recommendations.

## Agents

1. **Data Analyst**: Specializes in analyzing financial markets to provide critical insights.
2. **Trading Strategy Developer**: Formulates and optimizes trading strategies based on data analysis.
3. **Trade Advisor**: Recommends optimal execution strategies for trades.
4. **Risk Advisor**: Evaluates risks associated with trading strategies and suggests safeguards.

## Installation

You can set up the environment by running the following command in a Google Colab cell:

  ```python
  !pip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.29 -q
  ```

### Setup API Keys
Make sure to set your API keys for Serper and OpenAI:

  ```python
  import os
  from google.colab import userdata
  
  os.environ["SERPER_API_KEY"] = userdata.get('SERPER_API_KEY')
  os.environ["OPENAI_API_KEY"] = userdata.get('OPENAI_API_KEY')
  ```

### Running the Assistant
1. **Define Your Agents and Tasks**: Create instances of agents and tasks to suit your trading needs.
2. **Initialize the Crew**: Combine agents and tasks into a crew for orchestration.
3. **Kickoff the Process**: Start the financial trading analysis with your desired parameters.

```python
# Example inputs for initiating the process
financial_trading_inputs = {
    'stock_selection': 'AAPL',
    'initial_capital': '100000',
    'risk_tolerance': 'Medium',
    'trading_strategy_preference': 'Day Trading',
    'news_impact_consideration': True
}

result = financial_trading_crew.kickoff(inputs=financial_trading_inputs)
```

## Example Output
The output will provide insights on trading opportunities, strategy recommendations, execution plans, and risk assessments tailored to your selected stock.

## Contributing
Contributions are welcome! If you have suggestions for improvements or new features, feel free to create an issue or submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE.txt) file for details.
