# 剑指 offer 42题

## 连续指数组的最大和

输入一个整型数组，数组中的一个或连续多个整数组成一个子数组。求所有子数组的和的最大值。

要求时间复杂度为O(n)。

### 示例

`输入: nums = [-2,1,-3,4,-1,2,1,-5,4]`
`输出: 6`
`解释: 连续子数组 [4,-1,2,1] 的和最大，为 6。`

### 提示

`1 <= arr.length <= 10^5`
`-100 <= arr[i] <= 100`

## 自编代码

> class Solution {
> public:
>     int maxSubArray(vector<int>& nums) {
>         int tmp=0;
>         int max=INT_MIN;
>         for(int i=0;i<nums.size();i++){
>             if(tmp<0){
>                 tmp=nums[i];
>             }
>             else{
>                 tmp+=nums[i];
>             }
>             if(tmp>max){
>                 max=tmp;
>             }
>         }
>         return max;
>     }
> };

### 运行结果

![](C:\Users\11855\Desktop\1.JPG)

## 代码改进

class Solution {
public:
    int maxSubArray(vector<int>& nums) {
        int res = nums[0];
        for(int i = 1; i < nums.size(); i++) {
            nums[i] += max(nums[i - 1], 0);
            res = max(res, nums[i]);
        }
        return res;
    }
};

### 改进结果

![](C:\Users\11855\Desktop\2.JPG)

