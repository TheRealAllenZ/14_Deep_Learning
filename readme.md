# Completed Work sit in [https://github.com/TheRealAllenZ/14_Deep_Learning/tree/master/Instructions/Starter_Code] Starter Code Directory

# Conclusions


### CLOSING PRICE 

A few observations:

1. The Predicted vs. Real appears to be a decent model by way of (a) trend, as well as (b) amplitude 
2. white LSTM - or STM - seem to weigh more heavily or more prominently the most recent data, the purpose of using Long - STM model would be to minimize this recent-weighting effect.   

An additional observation is that the Real price vs Predicted price curves exhibit a 'lag'.  With time-series data as it pertains to price, it makes perfect sense that following the rolling window, the Predicted curve will be exhibit a delay following the Real/Actual curve. 

Finally, an effective model will exhibit capable predictive capabilities. Within time-series data, the trend and amplitude can be easily modeled and predicted. However, seeing as how the amplitude toward the July timeframe supports large price swings.  In that context, the LSTM does not do a good enough job:  

we can observe that at the beginning of July, there are 3 price spikes with 3 concurrent dips. Yet, reviewing the Predicted curve ('the model'), there is only 1 price swing (rise and fall), over the course of ***3 actual*** price swing.  
    
Following the first 3 price swings in July, the next 3 price swings, also similarly yield only 1 spike on the Predicted Curve.  
    
Taken together, both price spike groupings debase the value of any predictive capabilities that this model might have provided, at least in current form. 

In fact, most regression models may do a better job. 

More tweaking or updating of neurons and layers might yield better results.  As applied, this model is not good. 






### FNG vs. Closing Prices

### I have tried several different parameters for rolling windows randing from ***5 to 90 and 180 days***, as well a different unit numbers from ***5 to 10, through to 90 and 180*** units. Same result. 

#### The ***Delta*** between 'predicted' vs. 'actual' is always very far apart. 

If I use longer rolling windows or higher UNIT numbers, the delta between "predicted" vs. "actual" is in fact smaller; but not for a better result.  Quite the contrary, the predictibility of the 'predicted' curve effectively disappears because the over-fitting is so extreme that the FNG "Predicted" curve is effectively horizontal.  

Second, and last, taken all of the foregoing together, what we can infer is that market sentiment or "FNG" is a poor predictor of price and trajectory. From March to May 2019, the consumer sentiment rails between highs and lows almost in a bi-polar or neurotic fashion.  During that same period, the actual Price stays pretty much flat and static.  

Reviewing May to June, the consumer sentiment not only stays relatively stable, a huge dive of sentiment (near all-time-low) FNG during this 2 - month period, does not affect price whatsoever.  In fact, bitcoin Price ventures into a meotoric rise in spite of that negative sentiment to reach its all-time-high of $12,000; again, in spite of the negative FNG.  

In closing, FNG, or consumer sentiment is truly a poor predictor for closing price having no relationship, and in some cases even an inverse relationship to asset performance.  

