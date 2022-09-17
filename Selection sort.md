# Selection sort
```
my_list = [7, 6, 5, 3, 9]
```
## From the smallest to the largest sort
### Finding the smallest number in the list function
```
def find_smallest(arr):
    smallest = arr[0]
    smallest_index = 0
    for i in range(1, len(arr)):
        if arr[i] < smallest:
            smallest = arr[i]
            smallest_index = 1
    return smallest_index
```
### Sorting function 
```
def selection_sort(arr):
    new_arr = []
    for i in range(len(arr)):
        smallest = find_smallest(arr)
        new_arr.append(arr.pop(smallest))
    return new_arr
```
### Let's try
```
print(selection_sort(my_list))
```
## From the largest to the smallest sort
### Find the largest function
```
def find_largest(arr):
    largest = arr[0]
    index_largest = 0
    for i in range(1, len(arr)):
        if arr[i] > largest:
            largest = arr[i]
            index_largest = i
    return index_largest
```
### Sorting function
```
def selection_sort_largest(arr):
    new_arr = []
    for i in range(len(arr)):
        largest = find_largest(arr)
        new_arr.append(arr.pop(largest))
    return new_arr
```
### Let's try
print(selection_sort_largest(my_list))
```
