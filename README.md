# Leetcode-1342.-Number-of-Steps-to-Reduce-a-Number-to-Zero

# Description
Given an integer num, return the number of steps to reduce it to zero.

In one step, if the current number is even, you have to divide it by 2, otherwise, you have to subtract 1 from it.

# Solution
In the following problem we have been given a number which we have to reduce until it becomes 0.

To this this operation , if the number if even divide it by 2 .
If the number is odd subtract it by 1.

Example:

Num=14

Step 1) 14 is even; divide by 2 and obtain 7. 

Step 2) 7 is odd; subtract 1 and obtain 6.

Step 3) 6 is even; divide by 2 and obtain 3. 

Step 4) 3 is odd; subtract 1 and obtain 2. 

Step 5) 2 is even; divide by 2 and obtain 1. 

Step 6) 1 is odd; subtract 1 and obtain 0.

Total number of steps = 6

# Algorithm
1. create a variable named count and initialise it by 0.
2. Use a while loop until the number becomes 0.
3. Check if the number is divisible by 2 or not .
4. If it is divisible by 2(even number) then divide the number by 2 and increment the count by 1.
5. If the number is not divisible by 2(odd number) then subract 1 from it and increment the count by1.
6. Return the count.

# Code
class Solution:

    def numberOfSteps(self, num: int) -> int:
        count=0
        while(num>0):
            if num%2==0:
                num//=2
            else:
                num-=1
            count+=1
        return count
# Time Complexity
In each step:

  If the number is even, it’s divided by 2 → reduces faster (logarithmic reduction).

  If it’s odd, 1 is subtracted → just one step closer to being even.

Hence , the time complexity would be O(log n)
