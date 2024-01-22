# Apocalypse XAU EA ReadMe

This is the ReadMe file for the Apocalypse XAU EA code, developed by Forex Robot Easy Team. For detailed reviews and trading results of this product, please visit [here](https://forexroboteasy.com/forex-robot-review/apocalypse-xau-ea-review-unprecedented-forex-software-outperforms-all/). 

**Note:** ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

## Table of Contents

- [Includes](#includes)
- [Global Variables](#global-variables)
- [Input Parameters](#input-parameters)
- [Initializing Function](#initializing-function)
- [Deinitializing Function](#deinitializing-function)
- [Execution Function](#execution-function)
- [Open Position Function](#open-position-function)
- [Close Position Function](#close-position-function)

## Includes

The code includes the following libraries:

- Trade.mqh
- PositionInfo.mqh

## Global Variables

- `CTrade trade`: Trade class object
- `CPositionInfo positionInfo`: PositionInfo class object

## Input Parameters

- `FuHeZhi`: Opening parameter (default value: 10)

## Initializing Function

The `OnInit()` function is responsible for initializing the EA. In this function, the dynamic stop loss and take profit levels are set using the `SetDynamicStopLevel()` and `SetDynamicTakeLevel()` functions respectively.

## Deinitializing Function

The `OnDeinit(const int reason)` function is called during the deinitialization of the EA. Currently, it is empty and does not contain any specific functionality.

## Execution Function

The `OnTick()` function is executed on each tick of the symbol. It performs the following tasks:

1. Checks if the symbol is supported by the EA.
2. Checks if there is an open position.
3. Calls the appropriate function to either open or close the position.

## Open Position Function

The `OpenPosition()` function is called when there is no open position. It performs the following tasks:

1. Calculates the stop loss and take profit levels based on the `FuHeZhi` parameter and the current symbol price.
2. Opens a position using the `Buy()` function from the `trade` object.
3. Prints the opening details including the symbol, entry price, stop loss, and take profit levels.

## Close Position Function

The `ClosePosition()` function is called when there is an open position. It performs the following tasks:

1. Closes all open positions using the `PositionCloseAll()` function from the `trade` object.
2. Prints the closing details including the symbol and current price.

**Please note that this code is a sample and should be used as reference only. To find the official developer of this product, use MQL5.**

For detailed reviews and trading results of this product, please visit [here](https://forexroboteasy.com/forex-robot-review/apocalypse-xau-ea-review-unprecedented-forex-software-outperforms-all/).
