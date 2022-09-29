## DSA-Array

# Array:
- A collection of items in a contiguous manner. 
- Python list based on array data structures.
- Array index always starts from 0 and ends at n-1 where n is length of an array.
- Each index have own address ( in hexadecimal format).
- In array we can access any value by their index and time complexity for this is constant - O(1)


```Python
arr = [1, 3, 5, 2, 7]
print(arr[0]) 
## we are accessing a base address i.e 0th index value
``` 

## Applications of array:

Mostly this DS used of searching operation

Lets see some of searching operations.

### Linear search:

We don't need sorted array for this type of searching, it will search until the match found.
Most of the times developer rely on this type of searching but this is not a good practice always. Try to use upcoming optimized searching if possible. Time complexity for this is O(n) why because we have used one for loop.


```Python
arr = [1, 3, 5, 2, 7]
find_value = 3
result = -1
for i in range(0, len(arr)-1):
  if arr[i] == find_value:
    result = arr[i]
    break;
print(result)
``` 
### Binary Search:

Binary search is an algorithm to find a value by repeatedly dividing the search values by half. By default it should be sorted in nature. Because of this we could able to achieve the time complexity to O(log n).

**Steps for Binary search:**

- Split the full array into two half.
- Then starts with mid element.
- If the search value lesser than the mid element we go for left side.
- If the search value greater than the mid element we go for right side.
- The above steps repeatedly occurs until the search value found or length of array 0.
- If the search element not found, It should return -1.

To find mid value we should use below formula:
mid = (left + right)//2
              or
mid = left + (right - left)//2 -> This formula is recommended to avoid index out of range error.

Now will see the code implementation,


```Python
def binarySearch(arr, x):
  while(left < right):
    mid = left + (right - left)//2
    if arr[mid] == x:
      return mid
    elif arr[mid] < x:
      left = mid + 1
    else:
      right = mid - 1
  return -1
arr = [1, 2, 3, 4, 5, 6, 7]
x = 6
print(binarySearch(arr, x))
``` 

### Ternary Search:

This is similar to binary search, the only different here is we are splitting the array into three parts.

Lets see implementations of this,


```Python
def ternarySearch(arr, x, i, j):
  while i <= j:
    mid_1 = i + (j - i)//3
    mid_2 = j - (j - i)//3
    if arr[mid_1] == x:
      return mid_1
    elif arr[mid_2] == x:
      return mid_2
    elif arr[mid_1] < x:
      return ternarySearch(arr, x, i, mid_1 - 1)
    elif arr[mid_2] > x:
      return ternarySearch(arr, x, mid_1 + 1, j)
    else:
      return ternarySearch(arr, x, mid_1 + 1, mid_1 - 1)

arr = [1, 2,3,4,5,6,7,8,9]
x = 8
i = 0
j = len(arr) - 1
print(ternarySearch(arr, x, i, j))
``` 




