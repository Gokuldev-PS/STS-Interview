# STS-Interview - Array/List Question

### **Question**

> **_Given the participants' score sheet for your University Sports Day, you are required to find the runner-up score. You are given scores. Store them in a list and find the score of the runner-up._**

> **_If the following string is given as input to the program:_**
>
> ```
> 5
> 2 3 6 6 5
> ```
>
> **_Then, the output of the program should be:_**
>
> ```
> 5
> ```


### Sample Solution
```python
n = int(input())
arr = map(int, input().split())
arr = list(set(arr))
arr.sort()
print(arr[-2])
```

### Questions that can be asked to the candidate 
- If the Candidate is using sorting ask them to do without sorting
- Ask the candidate to modify the code to print the average incase there are multiple runners-up
  
### Possible/Expected Answers
Explain the purpose of this Python code:
Expected Answer:
The code defines a function predict_the_function(arr) that calculates the maximum sum of a continous subarray within the given array . It iterates through the array and maintains two variables, cs and ms, to keep track of the current sum of the subarray and the maximum sum encountered so far.
Identify any potential issues or improvements in the code:
Expected Answer:
The code assumes that the input array (arr) is non-empty. It may be a good idea to add a check for an empty array at the beginning of the function to handle this case gracefully.
The code works for arrays with all positive numbers but may not handle arrays with all negative numbers correctly. It's essential to consider such cases.
Modify the code to handle a case where all numbers in the array are negative:
Expected Answer:
Introduce a check at the beginning of the find_max_sum_subarray function to handle the case when all numbers in the array are negative. In this case, return the maximum negative number in the array
