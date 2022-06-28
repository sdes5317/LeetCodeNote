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
