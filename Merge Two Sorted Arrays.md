Given two sorted integer arrays nums1 and nums2, merge nums2 into nums1 as one sorted array.

The number of elements initialized in nums1 and nums2 are m and n respectively. You may assume that nums1 has a size equal to m + n such that it has enough space to hold additional elements from nums2.

---

```c#
public class Solution 
{
    public void Merge(int[] nums1, int m, int[] nums2, int n) 
    {
        //Counter
        int j = 0;
        
        //Merge arrays
        for (int i = m; i < nums1.Length; i++)
        {
            nums1[i] = nums2[j];
            j++;
        }
        
        //Bubble sort
        for (int k = 0; k < nums1.Length; k++)
        {
            for (int i = nums1.Length - 1; i > 0; i--)
            {
                if (nums1[i] < nums1[i - 1])
                {
                    int temp = nums1[i - 1];
                    nums1[i - 1] = nums1[i];
                    nums1[i] = temp;
                }
            }
        }
    }
}
```

---

**Runtime: 244 ms, faster than 25.40% of C# online submissions for Merge Sorted Array.**

**Memory Usage: 30.9 MB, less than 91.13% of C# online submissions for Merge Sorted Array.**