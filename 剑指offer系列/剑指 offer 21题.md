# 剑指 offer 21题

#### 调整数组顺序使奇数位于偶数前面

###题目

输入一个整数数组，实现一个函数来调整该数组中数字的顺序，使得所有奇数位于数组的前半部分，所有偶数位于数组的后半部分。

#### 示例

```C++
输入：nums = [1,2,3,4]
输出：[1,3,2,4]
注：[3,1,2,4] 也是正确的答案之一。
```

##### 提示

1. `0 <= nums.length <= 50000`
2. `1 <= nums[i] <= 10000`

### 自编代码如下

class Solution {

public:

  vector<int> exchange(vector<int>& nums) {

​    vector<int> n;

​    for(int i=0;i<nums.size();i++){

​      if(nums[i]%2==1){

​        n.push_back(nums[i]);

​      }

​    }

​    for(int i=0;i<nums.size();i++){

​    if(nums[i]%2==0){

​      n.push_back(nums[i]);

​    }

​    }

​    return n;

  }

};

### 运行结果

![](C:\Users\11855\Desktop\截图.JPG)

### 代码改进

class Solution {

public:

  vector<int> exchange(vector<int>& nums) {

​    int left = 0, right = nums.size() - 1;

​    while (left < right) {

​      if ((nums[left] & 1) != 0) {

​        left ++;

​        continue;

​      }

​      if ((nums[right] & 1) != 1) {

​        right --;

​        continue;

​      }

​      swap(nums[left++], nums[right--]);

​    }

​    return nums;

  }

};

### 运行结果

![](C:\Users\11855\Desktop\2.JPG)



