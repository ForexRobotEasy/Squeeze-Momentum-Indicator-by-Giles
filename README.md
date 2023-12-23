# Squeeze Momentum Indicator

This is a custom indicator called Squeeze Momentum Indicator developed by Forex Robot Easy Team. You can find more detailed reviews and trading results of this product at [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/squeeze-momentum-indicator-review-master-volatility-trading/).

## Indicator Parameters

The indicator has the following input parameters that can be modified:

- Period: The period used for calculating Bollinger Bands and Keltner Channel. The default value is 20.
- Deviation: The deviation used for calculating Bollinger Bands. The default value is 2.0.
- Smooth: The smoothing period used for calculating Keltner Channel. The default value is 20.
- MomentumPeriod: The period used for calculating momentum direction. The default value is 10.

## Indicator Buffers

The indicator uses the following buffers:

- ExtSqueezeBuffer: Stores the value of the squeeze period. If the squeeze period is true, it stores the closing price; otherwise, it stores 0.0.
- ExtMomentumBuffer: Stores the value of the momentum direction. If the squeeze period is true, it stores the calculated momentum; otherwise, it stores 0.0.
- ExtSqueezeReleaseBuffer: Stores the value of the squeeze release. If the squeeze period is true and followed by a blue dot, it stores the closing price; otherwise, it stores 0.0.

## Indicator Initialization

During initialization, the indicator sets up the buffers and their styles.

## Indicator Deinitialization

During deinitialization, the indicator removes the indicator buffers.

## Indicator Calculation

The indicator calculation function is called for each new bar. It calculates the squeeze period, squeeze release, and momentum direction for each bar.

The squeeze period is calculated by checking if the Bollinger Bands are within the Keltner Channel. If the closing price is above the upper channel or below the lower channel, the squeeze period is set to false.

The squeeze release is determined by checking if the squeeze period is followed by a blue dot in the buffer.

The momentum direction is calculated by summing the differences between the closing prices of the current bar and the previous bar for the specified momentum period and dividing it by the momentum period.

The calculated values are then stored in the respective indicator buffers.

## Note

Please note that Forex Robot Easy Team is not the official developer of this product. The provided code is a sample that can work as described in the product. To find the official developer of this product, please use MQL5.
