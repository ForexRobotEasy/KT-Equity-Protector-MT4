# KT Equity Protector MT4

## Overview
This code is a sample implementation of the KT Equity Protector MT4, a tool designed to monitor the account equity in MetaTrader 4 and take action based on predefined stop loss and profit target levels. It is developed by the Forex Robot Easy Team and more information about this product can be found on their website [here](https://forexroboteasy.com/forex-robot-review/kt-equity-protector-mt4-review-secure-forex-trading/).

## Functionality
The code includes necessary libraries and defines variables for stop loss and profit target levels. It also includes flags to track if the stop loss or profit target is triggered. The code utilizes the Trade and PositionInfo classes to manage trades and positions.

The code provides the following functions:

### CloseAllOrders()
This function is responsible for closing all market and pending orders. It uses the PositionInfo class to get the total number of open positions and iterates through them to close each position using the trade.PositionClose() function.

### ShutOpenCharts()
This function is responsible for closing all open charts. It uses the ChartGetInteger() function to get the total number of open charts and iterates through them to close each chart using the ChartClose() function.

### MonitorAccountEquity()
This function is responsible for monitoring the current account equity and taking action based on predefined stop loss and profit target levels. It uses the AccountInfoDouble() function to get the current account equity. If the account equity reaches the stop loss level, it sets the stop loss flag, closes all orders, and shuts all open charts. If the account equity reaches the profit target level, it sets the profit target flag, closes all orders, and shuts all open charts.

### OnTick()
This is the event handler for the OnTick event. It checks if the stop loss or profit target is triggered and if not, calls the MonitorAccountEquity() function.

### OnInit()
This is the event handler for the OnInit event. It initializes the trade class by setting the expert magic number and trade parameters such as deviation in points, order filling type, order type, order time type, and maximum allowed slippage.

### OnDeinit()
This is the event handler for the OnDeinit event. It prints a message when the program is stopped, indicating the reason.

### OnStart()
This is the event handler for the OnStart event. It runs the program indefinitely by calling the OnTick() event handler and delaying for 1 second using the Sleep() function.

## Product Description
The KT Equity Protector MT4 is a powerful tool developed by the Forex Robot Easy Team that helps traders monitor their account equity and automatically take action based on predefined stop loss and profit target levels. By using this tool, traders can secure their forex trading by ensuring that they exit trades when their account equity reaches certain thresholds.

The KT Equity Protector MT4 provides the following features:

- Stop Loss and Profit Target: Traders can define their desired stop loss and profit target levels based on their risk tolerance and trading strategy.

- Automatic Order Closure: When the account equity reaches the stop loss or profit target level, the tool automatically closes all market and pending orders.

- Chart Closure: In addition to closing orders, the tool also shuts all open charts to ensure that no further trading activity takes place.

Please note that ForexRobotEasy is not the official developer of this product. We are showcasing a sample code that demonstrates the functionality of the KT Equity Protector MT4. To find the official developer of this product, please refer to the MQL5 website. For detailed reviews and trading results of this product, please visit the official developer's website [here](https://forexroboteasy.com/forex-robot-review/kt-equity-protector-mt4-review-secure-forex-trading/).
