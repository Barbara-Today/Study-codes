# Recursion examples
## Summ
```
def summ_new(arr):
    if arr==[]:
        return 0
    return arr[0]+summ_new(arr[1:])
```
```
my_list = [7, 6, 5, 3, 9]
print(summ_new(my_list))
```

## Count the elements from the list
```
def count(arr):
    if arr == []:
        return 0
    return 1 + count(arr[1:])
```
```
my_list = [1,4,6,7]
print(count(my_list))
```
## Find the largest number
```
def largest(arr):
    if  len(arr) == 2:
        return arr[0] if arr[0]>arr[1] else arr[1]
    sub_max = largest(arr[1:])
    return arr[0] if arr[0]>sub_max else sub_max
```
```
my_list = [7, 6, 5, 3, 9]
print(largest(my_list))
```
## Binary search
```
def binary_search_recursive(arr, elem):
    mid = len(arr) // 2
    if elem == arr[mid]:
        return mid
    if elem < arr[mid]:
        return binary_search_recursive(arr, elem, mid-1)
    else:
        return binary_search_recursive(arr, elem, mid+1)
```
```
print(binary_search_recursive(my_list, 5))
```
