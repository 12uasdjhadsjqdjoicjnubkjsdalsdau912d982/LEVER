# An Online Adaptive Sequence Learning Framework for High-Frequency Trading

<p align="center">
<img src=".\image\example.png" height = "360" alt="" align=center />
<br><br>
<b>Figure 1.</b> Case study of LEVER.
</p>

Figure \ref{case} visualizes the details of inverse attention correlations and the corresponding trading time in the time index chart of one randomly-chosen stock, stock A, on Dec 21, 2019.

As can be seen, two 30-minute moving time windows in the red dash box separately record the tradable moments captured by LEVER.
We use a softmax function based on the dot products of any two column vectors in the learned outlier patterns $CshAttn(\cdot)$, and obtain the inverse attention correlations for both short-scope reader and long-scope reader, which are recorded by the strings of heatmap. 
Note that darker color indicates stronger correlation. 

Here, we draw two different types of arrow lines to represent those short-scope and long-scope readers with the highest weights, which precisely include the desired pivot points that expert traders use to determine the corresponding SRLs.

We discover that the predicted momentum trading signals in the last minute are primarily triggered by two co-existing conditions: 
(i) Price trend is prone to break out the current balance held by support and resistance levels. 
(ii) The corresponding trading volume has witnessed dramatic variations compared to the previous ones.  
These two conditions have been validated by existing momentum-based trading strategies.
Finally, the average return of these two predicted trading signals is 0.48\%, slightly higher than the one of traditional momentum-based HFT (i.e., 0.45\%) in real-life trading scenario, demonstrating the predictive power of our proposed LEVER.
