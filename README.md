# Backtesting-a-KD-RSI-MACD-trading-strategy-using-Python

## Basic Setup(基本設置)  
1. Target Selection: From the component stocks of Taiwan 50 index, select the following 15 industry's stocks with the highest percentage of shares.    

* Semiconductor Industry: Taiwan Semiconductor Manufacturing Co., Ltd. 2330
* Electronics Industry: Hon Hai Precision Industry Co., Ltd. 2317
* Communication Network Industry: MediaTek Inc. 2409
* Plastic Industry: Formosa Plastics Corporation 1301
* Financial Insurance Industry: Cathay Financial Holding Co., Ltd. 2883
* Iron and Steel Industry: China Steel Corporation 2002
* Optoelectronics Industry: Chi Mei Optoelectronics Corporation 2337
* Electronic Components Industry: Delta Electronics, Inc. 2308
* Computer and Peripheral Equipment Industry: Acer Inc. 2353
* Oil, Electric, Gas Industry: Formosa Petrochemical Corporation 1314
* Food Industry: Uni-President Enterprises Corp. 1216
* Textile and Fiber Industry: Far Eastern New Century Corporation 1326
* Cement Industry: Taiwan Cement Corporation 1101
* Electronics Retail Industry: Largan Precision Co., Ltd. 2337
* Trading and Department Stores: Uni-President Enterprises Corp. 1229
2. Data Frequency and Period: Daily Data, from January 1st, 2013 to January 1st, 2023.

3. Data Source: Yahoo Finance, retrieved through the yfinance package.

4. Transaction Costs: 0.1425% of the transaction amount will be charged as transaction fees when buying or selling stocks.

5. Operating Strategy- KD, RSI, MACD

* KD value can be used to not only determine buy and sell signals, but also objectively indicate market overbought or oversold conditions. When using KD data, D value should be used.
* When D value < 20, it represents bearish strength and market oversold conditions, indicating possible rebound or rise in the near future => buy signal
* When D value > 80, it represents bullish strength and market overbought conditions, indicating possible pullback or decline in the near future => sell signal
* If RSI > 50, we assume that the price is rising => buy signal
* If RSI < 50, we assume that the price is falling => sell signal.
* MACD is a trend-following momentum indicator that is calculated by subtracting the 26-day exponential moving average (EMA) from the 12-day EMA. It is typically displayed as a histogram and a signal line.
* When the MACD line (the blue line) crosses above the signal line (the red line), it is a bullish signal, indicating that it is a good time to buy.
* When the MACD line crosses below the signal line, it is a bearish signal, indicating that it is a good time to sell.

6. In summary, the basic setup for this strategy includes selecting 15 stocks from the Taiwan 50 index, using daily data from January 1st, 2013 to January 1st, 2023, and sourcing data from Yahoo Finance through the yfinance package. The strategy also includes using KD, RSI, and MACD indicators to determine buy and sell signals, as well as taking into account transaction costs of 0.1425% of the transaction amount.
### 中文說明
1. 標的選擇：從台灣50指數當中的成分股，挑選出以下15個產業中，各個持股比例最大的上市股票標的。  

* 半導體業：台積電 2330  
* 電子業：鴻海 2317  
* 通信網路業：宏達電 2409  
* 塑膠工業：台塑 1301  
* 金融保險業：國泰金 2883  
* 鋼鐵工業：中鋼 2002  
* 光電業：奇美電子 2337   
* 電子零組件業：台達電 2308  
* 電腦及週邊設備業：宏碁 2353   
* 油電燃氣業：台塑石化 1314  
* 食品工業：統一 1216  
* 紡織纖維：遠東新 1326  
* 水泥工業：台泥 1101  
* 電子通路業：聯強國際 2337   
* 貿易百貨：統一超 1229  
2. 資料頻率與期間：日資料，自2013年01月01日 至2023年01月01日。
3. 資料來源：Yahoo Finance，透過yfinance套件抓取。
4. 手續費成本：買賣股票時，手續費依成交金額的0.1425％計收。

5. 操作策略- KD, RSI, MACD
* KD 值除了可以判斷買賣訊號，還可以客觀的表現市場過熱或過冷，判斷市場行情時要使用 D 值的數據。  
* 當 D 值 < 20，代表空頭強勢，市場過冷，隨時可能反彈或回升 => 為買入信號  
* 當 D 值 > 80，代表多頭強勢，市場過熱，隨時可能回檔或下跌回升 => 為賣出信號  
* 如果 RSI  > 50 ，我們就假設價格正在上升 =>  為買入信號   
* 如果 RSI < 50，我們就假設價格正在下降 => 為賣出信號  
* MACD指標(柱狀圖、DIF-MACD) > 0 => 為買入信號   
* MACD指標(柱狀圖、DIF-MACD) < 0 =>為賣出信號  
