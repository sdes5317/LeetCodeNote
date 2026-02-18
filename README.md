# LeetCodeNote
紀錄leetcode刷題時的小技巧

### 1. 交換率  
    當if條件可能會溢位時,使用交換率來改變判斷條件
    例如,當value為正數時:
    value + 10 < int.MaxValue
              ↓
    value < int.MaxValue - 10
    使用value + 10可能導致溢位,但int.MaxValue - 10則可避免
### 2. 快慢指針
    用來取一個資料結構的中間位,很適合沒有index的tree node結構
    slow指針每次往前一步
    fast指針每次往前兩步
    故fast會是slow的兩倍速
### 3. 排序
    當需要避免重複的答案時,先把資料排序過,可以方便跳過重複的
### 4. 字母表
    var map = new int[26]
    不只可以用來計算出現的字母數, 實際是一個**已排序的陣列**
    搭配var key = new string(map)
### 5. 表回朔
    當遞迴共享Hash Table的時候, 且同步運算時, 如果結果是False, 則Remove失敗路線的值
    var hashTable = new HashSet();
    var isOk = Left(hashTable) | Right(hashTable);
    (由於左右只會有一個成功, 失敗的那個會Rollback讓表可以共用)
### 6. 單向貪婪
    類似左右雙指針的題型, 且目標是找「滿足↔失效」的邊界點
    其實是單向貪婪(複雜度更低)
    先還清(右)再精算(左), 全程不走分支, 只有一條路
