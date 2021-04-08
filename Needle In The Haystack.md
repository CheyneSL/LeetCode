Implement strStr().

Return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.

---

```c#
public class Solution 
{
    public int StrStr(string haystack, string needle) 
    {
        if (needle == "")
        {
            return 0;
        }

        if (needle.Length > haystack.Length)
        {
            return -1;
        }

        char firstChar = needle[0];
        int needleLen = needle.Length;

        for (int i = 0; i <= haystack.Length - needle.Length; i++)
        {
            if (haystack[i] == firstChar)
            {
                string sub = haystack.Substring(i, needleLen);
                if (sub == needle)
                {
                    return i;
                }

            }
        }
        return -1;
    }
}
```

---

**Runtime: 72 ms, faster than 87.04% of C# online submissions for Implement strStr().**

**Memory Usage: 23.1 MB, less than 67.04% of C# online submissions for Implement strStr().**