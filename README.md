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
- Ask the candidate to modify the code to print the sum incase there are multiple runners-up
  
### Possible/Expected Answers
Sample Python Code without sorting :
Expected Answer:
```python
scores = [45, 30, 40, 40, 50]  # example list of scores

# initialize the maximum and runner-up scores to the first two elements of the list
max_score = scores[0]
runner_up_score = scores[1]

# iterate over the list starting from the third element
for i in range(2, len(scores)):
    # if the current score is greater than the maximum score, update both maximum and runner-up scores
    if scores[i] > max_score:
        runner_up_score = max_score
        max_score = scores[i]
    # if the current score is greater than the runner-up score but less than the maximum score, update only the runner-up score
    elif scores[i] > runner_up_score:
        runner_up_score = scores[i]

print("The runner-up score is:", runner_up_score)
```

Sample Python code which calcuates the sum if there are two second postitions
Expected Answer:

```python
scores = [10, 20, 30, 40, 50, 40]  # example list of scores

# initialize the maximum and runner-up scores to the first two elements of the list
max_score = scores[0]
runner_up_score = scores[1]

# iterate over the list starting from the third element
for i in range(2, len(scores)):
    # if the current score is greater than the maximum score, update both maximum and runner-up scores
    if scores[i] > max_score:
        runner_up_score = max_score
        max_score = scores[i]
    # if the current score is greater than the runner-up score but less than the maximum score, update only the runner-up score
    elif scores[i] > runner_up_score and scores[i] != max_score:
        runner_up_score = scores[i]

# count the number of occurrences of the runner-up score in the list
count = scores.count(runner_up_score)

# if there are multiple runner-up scores, calculate their average
if count > 1:
    runner_up_score = count * runner_up_score
    

print("The runner-up score is:", runner_up_score)
```
