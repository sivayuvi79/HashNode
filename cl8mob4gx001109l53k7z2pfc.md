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

