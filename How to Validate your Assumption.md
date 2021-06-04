# How to validate assumption for data research ?

https://realpython.com/numpy-scipy-pandas-correlation-python/?fbclid=IwAR0nXm8vMiNUCTxQXgfECjE0tEIQw6d9OaamvIl7ZgUjkncWRcLElXJ-9Wo  
  
http://webftp.nkut.edu.tw/~092544/SPSS/25%E7%A8%AE%E7%B5%B1%E8%A8%88%E6%96%B9%E6%B3%95%E7%A7%98%E6%8A%80.pdf



## First Action (Scatter Plot)

在進行相關分析之前，建議研究者先進行散佈圖的繪製，可以確認兩變數之間是否有線性以外的關係。  

### 解釋與範例( [ref](https://dasanlin888.pixnet.net/blog/post/406709977) )
依變項是受訪者「有無受到運動傷害」（有=1、無=0），自變項則有「性別」、「運動前有無暖身」、「年齡」、「運動年數」

**自變數 (Independent Variable)**: 又稱獨立變數，通常表示想要推測的原因。  自變項只分連續與類別兩種解釋。  
- 連續變項: 即數字越大越會怎麼樣
- 類別變項: 必須做虛擬編碼（Dummy Code），此時類別變項裡會指定某一類為參照組（又稱被比較組，可由研究者自行決定），參照組一旦決定，所有的類別都會被解釋成與參照組做比較。  
ex. 指定性別部分以女性為參照組，運動前暖身以無暖身為參照組，所以解釋即為男性相較女性還要怎麼樣、有暖身相較沒暖身還要怎麼樣。  
  
**依變項 (Dependent Variable)**: 稱解釋變數，通常表示所要推測的結果。  

### 其他變數
**干擾變數（Moderating Variables)**: 介於自變數與應變數之間具調節作用，亦稱或者調節、情境變數。  
  
**控制變數（Control Variable）**: 是自變數的特殊類型，它會潛在地影響應變數。控制變數通常是人口統計或個人的變數，必須要被「控制」，才能確定自變數對應變數真正的影響。  
  
**中介變數（Intervening Variable）**: 影響應變數的隱性因素。  

### 甚麼叫做 "有關係" ?
如果自變數對應的依變數的機率分布會因為自變數取不同的值而機率分布不同, 說明兩者有關

## 簡單的分類
![image](https://user-images.githubusercontent.com/3915612/120610684-04cae680-c486-11eb-9419-914d63308c34.png)



----

## 方法分類  
![image](https://user-images.githubusercontent.com/3915612/118391765-9ce46580-b668-11eb-93fb-60b1dc3c8779.png)  
  
  
![image](https://user-images.githubusercontent.com/3915612/118391806-c7362300-b668-11eb-9ee4-4413c68e5711.png)


----

## 皮爾森積差相關分析(Pearson Correlation)
https://www.yongxi-stat.com/pearson-correlation/

### 功能
皮爾森相關分析用於探討兩連續變數之間的線性關係，若兩變數之間的相關係數絕對值較大，則表示彼此相互共變的程度較大。

![image](https://user-images.githubusercontent.com/3915612/118388072-d3b08080-b654-11eb-9242-f1f2b3111056.png)

Excel教學: https://support.microsoft.com/zh-tw/office/pearson-%E5%87%BD%E6%95%B8-0c3e30fc-e5af-49c4-808a-3ef66e034c18
```
PEARSON(array1, array2)
PEARSON 函數語法具有下列引數：
Array1    必要。 這是一組自變數。
Array2    必要。 這是一組因變數。
```

YT教學  
[![](http://img.youtube.com/vi/sUD27eKd-KE/0.jpg)](http://www.youtube.com/watch?v=sUD27eKd-KE "")  
(Tools is here: http://embedyoutube.org/)

### 注意
1、皮爾森相關分析並無法確切偵測到非線性的相關，例如指數或對數的相關，此時要先將變數進行轉換，再進行相關分析。  
2、相關分析並無法直接做出因果推論，因果推論必須要符合變數的獨立性、時序性及相關性，通常也需要參考文獻的邏輯推導過程，單純由相關分析是不足以直接斷定變數之間的因果關係的。  

---

## 二元羅吉斯迴歸
https://www.yongxi-stat.com/logistic-regression/

二元羅吉斯迴歸與線性迴歸的差別，僅在於依變項/Outcome尺度的不同  
當依變項為二類的類別變項（通常Coding 1 & 0）時，會採用二元羅吉斯迴歸進行分析；而當依變項為連續尺度的變項時，則是使用線性迴歸。  
（當依變項的水準為三類以上，則採用多項式羅吉斯迴歸）。  
  
自變數對依變數的影響是以*指數*的方式做變動，因此不需要常態分配的假設。  
![image](https://user-images.githubusercontent.com/3915612/118390193-63a7f780-b660-11eb-8212-1cb300ff9b8b.png)

### 公式
令依變數Y為二元反應的變數(成功或失敗)，p為其成功的機率，受自變數ｘ所影響，則p與ｘ之關係如下  
  
Y事件成功的機率 ![image](https://user-images.githubusercontent.com/3915612/118390210-79b5b800-b660-11eb-85d8-39f4d28a79f6.png)  
  
Y事件失敗的機率 ![image](https://user-images.githubusercontent.com/3915612/118390211-7b7f7b80-b660-11eb-9cf0-e0fb1095b1de.png)  
  
勝算(Odds) 即事件成功機率與失敗機率的比值 ![image](https://user-images.githubusercontent.com/3915612/118390240-994ce080-b660-11eb-964f-825e49ea92e0.png)
  
  
### 使用範例
【例題1】某公司欲根據過去「溫度」與「零件測試成功與否」的資料，建立以 溫度預測零件測試成功機率之迴歸模式。  
> 一個連續型的自變數(溫度)去預測y(零件測試成功與否)。其中，y=1表示零件測試成功，y=0表示零件測試失敗。
> 

【例題2】某醫療單位欲根據過去肺部疾病就診病患的基本資料，建立以有無「吸菸」、有無「家族病史」預測「罹患肺癌」機率之迴歸模式。  
> 兩個類別型的自變數(吸菸、家族病史)去預測y(罹患肺癌與否)。其中，y=1表示罹患肺癌，y=0表示沒有罹患肺癌。  
> 

---

## 卡方檢定-獨立性檢定(The Chi-Squared Test of Independence)

卡方獨立性檢定適用於**分析**兩組類別變數的關聯性。  
  
根據$/X^2/分佈及自由度可以確定在H0假設成立的情況下獲得當前統計量及更極端情況的概率P。  

同一樣本中，兩個變項的關聯性檢定，也就是探討兩個類別變項(例如：性別和結婚狀態)之間，是否為相互獨立，或者是有相依的關係存在，若是達到顯著，則需查看兩個變項的關連性強度。  
  
### 資料條件
1. 所有的變項為類別變項(categorical variable)
2. 樣本須為獨立變項(Independent variable)→第一組的樣本不影響第二組的樣本；第二組的樣本也不影響第一組。
3. 每一檢定細格(cell)內的數據應該設為頻率或計數數目，而不是百分比或是經過轉換之數據。
4. 至少有80%以上的類別，其樣本數大於5，亦即樣本數目至少要為類別數目的五倍。

### 可檢測項目
- 獨立性考驗(the test for independence)
> 獨立性的意義是指變項間的關係，而非樣本。當兩個變項間的關係為獨立時，則一個案分類到第一個變項中某一類別的機率，是和此個案出現在另一個變項之某一類別的機
率無關。  
> ex. 性別 和他或她是否會結婚（婚姻狀況）無關。  
> 公式 X^2 = SUM( (f_observed - f_expected)^2 / f_expected )

- 適合度考驗(the test of goodness of fit)
http://www3.nccu.edu.tw/~soci1005/Ch12.pdf  

- 同質性考驗

### 自由度df(抽樣數)與建立臨界區
卡方機率分配的圖形依照自由度的不同畫出  
![image](https://user-images.githubusercontent.com/3915612/118392165-b686ac80-b66a-11eb-984d-ffa629722078.png)  
    
df = ( num(列)-1 ) * ( num(行)-1 )  
依照需求決定自由度與對應的臨界區 (可能df=4, 信賴臨界值97.5%; df=5, 臨界值95%)  
![image](https://user-images.githubusercontent.com/3915612/118392269-580dfe00-b66b-11eb-87b8-22f603ca041d.png)  

此時會獲得對照用的X^2_critical (=曲線下面積)  

### 假說檢定(Hypothesis Testing)
建立假說H_0(兩變相獨立)與反向假說H_1(兩變相非獨立)  
會造就下面結果表格  
![image](https://user-images.githubusercontent.com/3915612/118392028-f1d4ab80-b669-11eb-82ee-521a95c8b0b7.png)
  
### EX. 如何驗證性別與教育程度有無關係?  

1. 雙變項交叉表
交叉表同時呈現出兩個不同變項間次數分配的情況。因此，雙變項交叉表可用來探索這兩個變項間是否有明顯的關係存在。  
![image](https://user-images.githubusercontent.com/3915612/118390630-aff43700-b662-11eb-9255-d8efc6a13c8a.png)  
如果性別和教育程度並無關係，即兩變項為獨立時，則 50 位男性有大專學歷及大專以下程度的機率應相當接近。  

2. 檢定值計算  
假設觀測值為  
![image](https://user-images.githubusercontent.com/3915612/118391398-a5d43780-b666-11eb-9c61-4267bdea48e8.png)  
  
- H_0: 如果性別和教育程度無關，則男性（或女性）上大專或大專以下的比例就會和大專或大專以下之**邊緣總數的比例**相同。
> 22/55(man) = 18/45(woman) = 40/100(all) = 40%  
> 此時男性的期待數字f_e = 55 * 40% = 22  
> 計算出表格中每區的期待值  
> ![image](https://user-images.githubusercontent.com/3915612/118390990-9eac2a00-b664-11eb-8bfc-bf9e228393b6.png)  
 
- H_0: 當性別與教育程度無關時，大專程度的 40 人中，男生的比例會是 55%，而女生的比例就是 45%。
> 依照公式 X^2 = SUM( (f_observed - f_expected)^2 / f_expected )  
> X^2_obtain = (30-22)^2/22 + (10-18)^2/18 + (25-33)^2/33 + (35-27)^2/27 = 10.78  
  
將獲得的X^2_obtain比較X^2_critical,  X^2_obtain > X^2_critical  
表示兩者非獨立, 在你設定的df, 準確度條件下, 成立H_1
  
### 更多的卡方範例
https://yashi4sale.pixnet.net/blog/post/45635923

-----

# How to do correlation in Excel?
https://www.statisticshowto.com/probability-and-statistics/excel-statistics/excel-regression-analysis-output-explained/
