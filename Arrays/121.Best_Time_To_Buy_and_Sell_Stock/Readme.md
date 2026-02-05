# Best Time to Buy and Sell Stock (LeetCode 121)

You are given an array `prices` where each element represents the stock price on that day.
You have to choose **one day to buy** and **a future day to sell** the stock in order to get
the maximum possible profit. If no profit can be made, return `0`.

Example:
prices = [7,1,5,3,6,4]  
Buy at price 1 and sell at price 6  
Profit = 6 - 1 = 5

If prices are always decreasing like:
prices = [7,6,4,3,1]  
Then no transaction is done and the answer is 0.


### Brute Force 
Is me hum har possible buying day ke liye aage ke saare days check karte hain.
Har pair ke liye profit nikalte hain aur maximum profit store karte hain.

Ye approach logic samajhne ke liye theek hai,
lekin large input ke liye slow ho jaati hai.

Time Complexity: O(n²)  
Space Complexity: O(1)


### Algorithm:
1. Initialize minPrice with the first element of the array.
2. Initialize maxProfit as 0.
3. Traverse the array from index 1 to the end.
4. For each element:
   a. If the current price is smaller than minPrice,
      update minPrice with the current price.
   b. Calculate profit as current price minus minPrice.
   c. If the calculated profit is greater than maxProfit,
      update maxProfit.
5. After completing the traversal, return maxProfit.


Time Complexity: O(n)  
Space Complexity: O(1)


### Important Points
- Sirf ek transaction allowed hai
- Buy hamesha sell se pehle hona chahiye
- Agar profit possible nahi hai, answer hamesha 0 hoga
