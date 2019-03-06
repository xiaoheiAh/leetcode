#### 给定一个大小为 n 的数组，找到其中的众数。众数是指在数组中出现次数大于 ⌊ n/2 ⌋ 的元素。你可以假设数组是非空的，并且给定的数组总是存在众数。
`示例1:`
```
输入: [3,2,3]
输出: 3
```
`示例2:`
```
输入: [2,2,1,1,1,2,2]
输出: 2
```

#### 解题思路
[摩尔投票法](http://www.cnblogs.com/grandyang/p/4233501.html)
```java
class Solution {
    public int majorityElement(int[] nums) {
        int res = 0; int cnt = 0;
        for(int i=0;i<nums.length;i++){
            if(cnt == 0 ){
                res=nums[i];
                ++cnt;
            } else if (res==nums[i]) {
                ++cnt;
            } else {
                --cnt;
            }
        }
        return res;
    }
}
```
