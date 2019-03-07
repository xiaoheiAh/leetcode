#### 给定一个非空整数数组，除了某个元素只出现一次以外，其余每个元素均出现两次。找出那个只出现了一次的元素。

**说明:**

你的算法应该具有线性时间复杂度。 你可以不使用额外空间来实现吗？

`示例 1:`
```
输入: [2,2,1]
输出: 1
```
`示例 2:`
```
输入: [4,1,2,1,2]
输出: 4
```

[异或-wiki](https://zh.wikipedia.org/wiki/%E9%80%BB%E8%BE%91%E5%BC%82%E6%88%96)
0^a = a a^a = 0,异或满足交换律,a^b^a = b
```java
class Solution {
    
    public int singleNumber(int[] nums) {
        int res = 0;
        for(int i = 0; i < nums.length; i++) {
             res ^= nums[i];
        }
        return res;
    }
}
```
