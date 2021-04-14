Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.

Follow up: Could you implement a solution with a linear runtime complexity and without using extra memory?

---

```c#
public class Solution 
{
    public int SingleNumber(int[] nums) 
    {
        int output = 0;
        
        for (int i = 0; i < nums.Length; i++)
        {
            int ctr = 0;
            int temp = nums[0];
            nums[0] = nums[i];
            nums[i] = temp;
            
            for (int j = 1; j < nums.Length; j++)
            {
                if (nums[0] == nums[j])
                    ctr++;
            }
            
            if (ctr == 0)
                output = nums[0];
        }
        
        return output;
    }
}
```

---

**Runtime: 1552 ms, faster than 5.03% of C# online submissions for Single Number.**

**Memory Usage: 29.9 MB, less than 72.99% of C# online submissions for Single Number.**