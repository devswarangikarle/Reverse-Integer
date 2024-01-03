# Reverse-Integer

class Solution:
    def reverse(self, x):
        INT_MAX = 2**31 - 1
        INT_MIN = -2**31

        sign = 1 if x >= 0 else -1
        x = abs(x)
        reversed_x = 0

        while x != 0:
            pop = x % 10
            x //= 10

           
            if reversed_x > (INT_MAX - pop) // 10:
                return 0

            reversed_x = reversed_x * 10 + pop

        return sign * reversed_x


sol = Solution()

x1 = 123
print(sol.reverse(x1))  
x2 = -123
print(sol.reverse(x2)) 
x3 = 120
print(sol.reverse(x3))  
