# KPI_setting

## ▍功能說明
這個功能主要是為了讓電商業者快速了解整體賣場銷售以及影響銷售的關鍵成效<br>
<img decoding="async" src="https://i.imgur.com/cJv77Yi.png" width="50%"><br>

## ▍程式說明
一、ETL 資料獲取、匯入資料庫<br>
shopee_pyetl_pshop_update_by_day.ipynb<br>
auto_update.py<br>
使用 LSTM model 預測未來銷售金額，訓練數據包含每日賣場數據，如來客數、頁面停留時間、頁面瀏覽數、賣場跳出率…等數據，並以每日銷售金額作為預測目標進行模型訓練，透過可視化圖表挑整參數，最終以最貼合真實數值的預測做為 KPI 設定。<br>

二、KPI 設定、繪製比照圖表<br>
kpi_setting.py<br>
goal.py<br>
使用 LSTM model 預測未來銷售金額，訓練數據包含每日賣場數據，如來客數、頁面停留時間、頁面瀏覽數、賣場跳出率…等數據，並以每日銷售金額作為預測目標進行模型訓練，透過可視化圖表挑整參數，最終以最貼合真實數值的預測做為 KPI 設定。<br>
<img decoding="async" src="https://i.imgur.com/LitdMgh.png" width="50%"><br>
這張圖是預測銷售與實際銷售的比對圖，可以看到預測值有貼合實際趨勢變化<br>
<img decoding="async" src="https://i.imgur.com/fOxL6yN.png" width="50%"><br>
【調參過程】<br>
<img decoding="async" src="https://i.imgur.com/aSZ2Yqy.png" width="50%"><br>
【最終結果以及神經層】<br>
<img decoding="async" src="https://i.imgur.com/s4Yxphf.png" width="50%"><br>

三、當日賣場分數、成效差距比較<br>
store_overview.py<br>
【賣場分數】<br>
<img decoding="async" src="https://i.imgur.com/ddSbEHi.png" width="50%"><br>
使用可處理不同資料類型、高維度資料的決策樹(Decision Tree)作為最終使用的分類模型<br>
數據來源以每日賣場數據為主，如來客數、頁面停留時間、頁面瀏覽數、賣場跳出率…等數據，並以每日銷售金額作為分類依據<br>

【成效差距比較】<br>
<img decoding="async" src="https://i.imgur.com/b0A6fug.png" width="50%"><br>
以決策樹模型計算出的權重，以權重大至小排序，成為上至下排版依據，<br>
並將所有個別數據平均，作為警告提醒，以此重點呈現出應努力目標<br>








