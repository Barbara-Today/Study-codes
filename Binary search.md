## Binary search function

```
def binary_search(list, item):
    low = 0
    high = len(list)-1
    while low <= high:
        mid = int((low+high))/2
        guess = list[mid]
        if guess == item:
            return mid
        elif guess > item:
            high = mid - 1
        else:
            low = mid + 1
    return None
  ```
## Trying the function
```
my_list = list(range(1,100,2))
    
print(binary_search(my_list, 7))
```
