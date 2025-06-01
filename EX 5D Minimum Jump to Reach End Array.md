# EX 5D Minimum Jump to Reach End Array
## DATE:
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1. Read integer n (number of elements in array).
2. Read n integers into array a.
3. Initialize:

     max_till_now = a[0] (stores the overall maximum sum found so far)
     max_ending = 0 (stores the sum of the current subarray)

4.  Loop through each element in the array:

      Add the current element to max_ending
      If max_ending < 0, reset it to 0
      If max_till_now < max_ending, update max_till_now
5.  Return max_till_now as the maximum subarray sum. 

## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.


Developed by: Hariviswanath B
Register Number:  212222040051
*/
```
```
def maxSubArraySum(a,size):
    
    max_till_now = a[0]
    max_ending = 0
    
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        
        
        elif (max_till_now < max_ending):
            max_till_now = max_ending
            
    return max_till_now
    
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```
## Output:

![image](https://github.com/user-attachments/assets/f2d52286-058b-4062-a3d0-fbed051f589e)


## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
