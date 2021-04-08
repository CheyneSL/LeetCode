Given a sorted array nums, remove the duplicates in-place such that each element appears only once and returns the new length.

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

---

```c#
public class Solution 
{
    public int RemoveDuplicatesLength(int[] nums) 
    {
    if (nums.Length == 0) 
        return 0;
        
    int i = 0;
    for (int j = 1; j < nums.Length; j++) 
    {
        if (nums[j] != nums[i]) 
        {
            nums[i += 1] = nums[j];
        }
    }
    return i + 1;
    
    }
}
```

---

**Runtime: 244 ms, faster than 75.18% of C# online submissions for Remove Duplicates from Sorted Array.**

**Memory Usage: 34.4 MB, less than 8.30% of C# online submissions for Remove Duplicates from Sorted Array.**