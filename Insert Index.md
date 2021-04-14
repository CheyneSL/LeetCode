Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

---

```c#
public class Solution 
{
    public int SearchInsert(int[] nums, int target) 
    {
            int j = 0;
            int output = 0;

            while (j < nums.Length)
            {
                if (nums[j] <= target)
                {
                    if (nums[j] == target)
                        output = j;
                    else
                        output = j + 1;
                }
                
                j++;
            }
        
        return output;
    }
}
```

---

**Runtime: 96 ms, faster than 50.05% of C# online submissions for Search Insert Position.**

**Memory Usage: 25.2 MB, less than 76.70% of C# online submissions for Search Insert Position.**