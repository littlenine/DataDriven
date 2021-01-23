# Product Engagement Score (PES)

The product engagement score (PES) 是一種觀察使用者與你的產品互動的指標.  
公式: [Feature adoption + App retention + Stickiness] / 3

- *Feature adoption*: The percentage of features that generate 80% of click volume
- *App retention*: The percentage of users retained in the first three months of usage
- *Stickiness*: The percentage of monthly active users who return daily (DAU/MAU)

![](https://www.pendo.io/wp-content/uploads/2020/10/Product_engagement_score_PES_example.jpg)

## Core-elements of PES
好的使用量測指標必須包含下面三種特型
- 能測量: 容易取得, 不用花費大量力氣來取得資料
- 好讀: 容易理解,不用上下文來解釋
- 切題: 符合商業目標

## Stickiness
使用者黏著度意味著產品價值與客戶感受價值的吻合程度,是簡單且好解讀的指標  

常見指標：日活躍使用者(daily active user), 週活躍使用者(weekly active user), 月活躍使用者(monthly active user)  
可用比例來觀測,如 DAU/MAU 或 WAU/MAU  
> 25%黏著度: 在每個月只少使用一次產品的使用者中,有1/4每天都至少使用一次
![](https://www.pendo.io/wp-content/uploads/2019/07/Pendo_eBook_10KPIs_Image_DAUMAU.png)  

當然不同的產品會有不一樣的使用情境, 不是每天都上來看就代表有用, 要找到自己產品的頻率, 可思考下面兩題  
> 哪些使用者黏著度最高, 為何？
> 有沒有什麼可採用的手段增加黏著度？ 
  
Ref：[use-stickiness-ratio-measure-product-health](https://www.pendo.io/pendo-blog/use-stickiness-ratio-measure-product-health/)  
Ref：[DAU,WAU,MAU](https://www.pendo.io/glossary/daily-active-users-dau/)

----

## Product adaption / Feature adoption
### Product adaption
用來測量網站或app的指標. 有3種計量方法  
1. 某段時間的量值, ex MAU
2. 計量與新註冊的比值, Monthly Product Adoption Rate (%) = [new MAU / monthly signups] * 100.
3. 黏著度, 直接用量值表示在某段時間內登入的使用者個數  

此指標和onboarding息息相關, 如果使用者無法再onboarding階段習得使用方式, 便無法促使他們使用產品  

### Feature adoption
同樣的概念可套用在觀察不同的功能, 一個產品一定會有熱門功能, 觀測此指標可幫助開發目標, 有時藉由promotion來幫助使用者使用特定功能, 或觀察是否淘汰特定功能
Monthly Feature Adoption Rate (%) = [feature MAU / monthly logins] * 100.  

此指標可用來分析四個項目：
1. 使用廣度
> 某功能在整個用戶群或目標用戶群中採用了多廣泛？該功能是否已被大多數目標用戶使用或僅佔一小部分？採用的廣度顯示了該新功能的最初吸引力。
2. 使用深度
> 關鍵用戶類型多久接觸一次該功能？他們是否正在應用所需的過程來顯示粘性？他們是否以意想不到的方式表現？採用的深度可能表示與持續的需求或使用困難相關，因此，密切關注它並徵求反饋（如果可能）非常重要。
3. 接受所花的時間(Time to adopt)
> 客戶開始使用新功能需要花費多長時間？在了解某個功能時，他們會立即嘗試使用它還是要等待數天或數週才能使用它？採用功能的速度越快，就越有可能與現有的痛點相吻合。
4. 接受所花的時間(Duration of adoption)
> 用戶了解某項功能後會繼續使用多長時間？他們只是嘗試幾次還是在幾個月和幾年的時間內繼續使用它？持續時間與保留時間保持一致，並有助於顯示功能是否在提供超出其初始新穎性的實際價值，並且可以在功能需要更新時發出信號。

除了這四點,特定的使用情境也是要探討的  

Ref: [product-and-feature-adoption](https://www.pendo.io/glossary/product-and-feature-adoption/)


--- 

## App retention (Growth)



Ref: [user-retention](https://www.pendo.io/glossary/user-retention/)

---

## Important of Onboarding
onboarding重點在新的使用者轉為熟練的使用者的過程, 知道如何使用產品找到答案, 著重下面四點  
1. 快速解釋產品的工作方式和使用實例  
2. 傳達產品的好處和差異化  
3. 標示並指導用戶使用最有價值的功能  
4. 提示用戶反複使用該產品  

測量上從三個面向觀察(Self discovery,Human assisted, Automated in-app)  
- 自我發現：也就是他們自己的每個新用戶-客戶在沒有任何指導的情況下自行瀏覽產品。  
- 人工協助：用戶將接受現場培訓課程和/或教育內容的培訓。  
- 自動化的產品內部通知：此策略可滿足用戶在當前所在位置的需求，提供演練和教學。  

延伸閱讀：[何謂onboarding](https://www.pendo.io/pendo-blog/what-is-onboarding/)?  

------------

## How can I improve my product engagement score?
1. 確認對使用者有高價值的功能
2. 讓產品融入使用者的工作流
> 透過了解使用者的操作流程, 觀察需求, 試著量化使用資料.  
> 你的最終目標是讓使用者可以更頻繁地使用, 因此要找出使用者痛點,直接把處理方式展示給使用者看
3. Invest in onboarding
> 觀察使用者如何上來使用產品, 一種策略是提供訓練跟資源, 教使用者如何使用產品功能  
> 學習路程要保持簡單, 並提供不同的學習途徑, 第一印象的重要會直接影響使用者是否停留在此平台.  
