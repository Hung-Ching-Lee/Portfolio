# 影像分類

### 觀察樣本,每個類別樣本數不盡相同,因此先簡單訓練模型,觀察樣本較少的類別是否分錯比較多,視情況做數據增強


![image](https://github.com/Hung-Ching-Lee/Portfolio/blob/master/%E5%BD%B1%E5%83%8F%E8%BE%A8%E8%AD%98/%E8%9D%A6%E7%9A%AE%E6%AF%94%E8%B3%BD_%E5%88%86%E9%A1%9E/%E6%A8%A3%E6%9C%AC%E8%A7%80%E5%AF%9F.png)

 
  
  
  
  
### 看來並沒有此現象,倒是相似的類別機器較容易分錯,例如:窄褲與牛仔褲

![image](https://github.com/Hung-Ching-Lee/Portfolio/blob/master/%E5%BD%B1%E5%83%8F%E8%BE%A8%E8%AD%98/%E8%9D%A6%E7%9A%AE%E6%AF%94%E8%B3%BD_%E5%88%86%E9%A1%9E/confusion_matrix-Copy1.png)
  
  
  
  
  
  
  
### 因此嘗試簡單的模型共識算法,將各個模型對於各類別給出的機率值給予相等權重的平均,看能不能得到比單一模型更高的準確度

![image](https://github.com/Hung-Ching-Lee/Portfolio/blob/master/%E5%BD%B1%E5%83%8F%E8%BE%A8%E8%AD%98/%E8%9D%A6%E7%9A%AE%E6%AF%94%E8%B3%BD_%E5%88%86%E9%A1%9E/4%E6%A8%A1%E5%9E%8B.png)
  
  
  
  
  
  
### 可以看到,能夠得到較為穩定的結果
![image](https://github.com/Hung-Ching-Lee/Portfolio/blob/master/%E5%BD%B1%E5%83%8F%E8%BE%A8%E8%AD%98/%E8%9D%A6%E7%9A%AE%E6%AF%94%E8%B3%BD_%E5%88%86%E9%A1%9E/%E8%A7%80%E5%AF%9F%E4%B8%8D%E5%90%8C%E6%A8%A1%E5%9E%8B%E9%A0%90%E6%B8%AC%E7%B5%90%E6%9E%9C.png)