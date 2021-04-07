Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

---

```c#
	public class Solution 
	{
		public int[] TwoSum(int[] nums, int target) 
		{
			int index1 = 0;
			int index2 = 0;
			
			for (int i = 0; i < nums.Length; i++)
			{
				for (int j = 0; j < nums.Length; j++)
				{
					if (nums[i] + nums[j] == target)
					{
						index1 = i;
						index2 = j;
						break;
					}
	
				}
			}
			
			return new int[] {index1, index2};
		}
	}
```

---

**Runtime beats 46.10% of csharp solutions.**

**Memory usage beats 89.42% of csharp solutions.**