## leetcode-0001-题解

地址：<https://leetcode-cn.com/problems/two-sum/>



## Java版

1、暴力解法：

``` java
public class Solution {
	public int[] twoSum(int[] nums, int target) {
		for (int i = 0; i < nums.length; i++) {
			for (int j = i+1; j < nums.length; j++) {
				if (nums[j] == target - nums[i]) {
					return new int[] {i, j};
				}
			}
		}
		throw new IllegalArgumentException("No two sum solution");
	}
```



## Python版

1、暴力解法：

``` python
class Solution:
    def twoSum(self, nums, target):
        n = len(nums)
        for i in range(n):
            for j in range(i+1, n):
                if nums[j] == (target - nums[i]):
                    return [i, j]
        raise Exception("No two sum solution")


if __name__ == '__main__':
    nums = [2, 7, 11, 15]
    target = 26
    solution = Solution()
    result = solution.twoSum(nums, target)
    print(result)
```

