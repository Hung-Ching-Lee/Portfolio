# Portfolio
#### <a href="https://www.kaggle.com/tristan581/17k-apple-app-store-strategy-games" target="_blank" style="text-decoration:none;color:red;">資料來源:Kaggle 17K Mobile Strategy Games</a>

因為沒有下載數量,但用戶討論數量應可以代表下載量(有下載才會討論)  
可以看到此為五個變數之相關矩陣  
主要要探討Size(APP大小)對於User Rating Count(下載量)之影響
![image](https://github.com/Hung-Ching-Lee/Portfolio/blob/master/%E6%95%B8%E6%93%9A%E5%88%86%E6%9E%90/%E5%BD%B1%E9%9F%BFAPP%E4%B8%8B%E8%BC%89%E9%87%8F%E5%9B%A0%E7%B4%A0/%E7%9B%B8%E9%97%9C%E4%BF%82%E6%95%B8%E7%9F%A9%E9%99%A3.png)
  
  
  
  
  
  
從迴歸結果可以看到:Size(APP大小)與UserRatingCount(下載量) 為顯著正相關  
然而這不能代表:提升APP大小可以增加下載次數  
因:APP大小並非"隨機"被決定,兩者間也未必有因果關係  
因此下邊使用Propensity Score Matching(PSM)藉由配對的方式控制其他變數,盡量使Size effect呈現一個隨機的狀態,再來觀測Size對於下載量的影響 迴歸顯示檔案大小與下載次數呈現正相關,由於可能內生性與選擇性偏誤,並不能說明兩者間有因果關係,在此例子中,下載量應該難以反向影響APP大小,然而APP大小非"隨機被決定"因此可能有選擇性偏誤之問題
![image](https://github.com/Hung-Ching-Lee/Portfolio/blob/master/%E6%95%B8%E6%93%9A%E5%88%86%E6%9E%90/%E5%BD%B1%E9%9F%BFAPP%E4%B8%8B%E8%BC%89%E9%87%8F%E5%9B%A0%E7%B4%A0/%E8%BF%B4%E6%AD%B8%20-%20%E8%A4%87%E8%A3%BD.png)
  
  
  
  
  
  
可以看到,在配對之前,大容量的APP平均下載量為7045,高於小容量的4158  
在配對之後,大容量的APP平均下載量為7045,低於小容量的176667  
這說明在其他條件不變下,APP大小愈小愈能得到高的下載次數
![image](https://github.com/Hung-Ching-Lee/Portfolio/blob/master/%E6%95%B8%E6%93%9A%E5%88%86%E6%9E%90/%E5%BD%B1%E9%9F%BFAPP%E4%B8%8B%E8%BC%89%E9%87%8F%E5%9B%A0%E7%B4%A0/%E8%BF%B4%E6%AD%B8%20-%20%E8%A4%87%E8%A3%BD.png)
  
  
  
  
  
  
均衡項檢測中  
U:Umatch  
M:Match  
可以看到在配對之後實驗組與控制組之變數值無顯著差異  
圖表也可看到配對大致均衡
![image](https://github.com/Hung-Ching-Lee/Portfolio/blob/master/%E6%95%B8%E6%93%9A%E5%88%86%E6%9E%90/%E5%BD%B1%E9%9F%BFAPP%E4%B8%8B%E8%BC%89%E9%87%8F%E5%9B%A0%E7%B4%A0/%E5%9D%87%E8%A1%A1%E6%80%A7%E6%AA%A2%E6%B8%AC.png)
![image](https://github.com/Hung-Ching-Lee/Portfolio/blob/master/%E6%95%B8%E6%93%9A%E5%88%86%E6%9E%90/%E5%BD%B1%E9%9F%BFAPP%E4%B8%8B%E8%BC%89%E9%87%8F%E5%9B%A0%E7%B4%A0/%E5%9C%96.png)
