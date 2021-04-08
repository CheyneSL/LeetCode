Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-231, 231 - 1], then return 0.

---

```c#
	public class Solution 
	{
		public int Reverse(int x) 
		{
			double reverse = 0;
			
			while (x != 0)
			{
				reverse = reverse * 10 + x % 10;
				x /= 10;
			}
			
			if (reverse < int.MinValue || reverse > int.MaxValue)
				return 0;
			else
				return (int)reverse;
		}
	}
```

---

**Runtime: 40 ms, faster than 82.38% of C# online submissions for Reverse Integer.**

**Memory Usage: 15.3 MB, less than 63.19% of C# online submissions for Reverse Integer.**