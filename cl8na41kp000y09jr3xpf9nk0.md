## DSA-Array-Sorting

# Array Sorting

Already we saw definition of array in last post, and we also take some application of array's.
Sorting is also one of the application of array.

There are multiple Sorting methods available, we see one by one in this post.

We can classify the sorting into two types, Comparison Sort and Non - Comparison Sort.

** Comparison Sort **:
1. Bubble Sort
2. Selection Sort
3. Insertion Sort
4. Quick Sort
5. Merge Sort
6. Heap Sort
7. Shell Sort

** Non - Comparison Sort **:
1. Count Sort
2. Radix Sort
3. Bucket Sort


## Comparison Sort

This is nothing but comparing each element in a array to sort. It may be ascending or descending orders.
Now we see some of comparison sorting methods below,

### Bubble Sort

Bubble sort is one of the sorting algorithm, it works by repeatdely swapping the adjucent elemnt if they are in wrong order. It is not suitable for large data sets as it time complexity is higher because we need to use two loops.

Lets see code implementations.


```Python
def bubbleSort():
n = len(arr)
  for i in range(n):
    for j in range(0, n-i-1):
      if arr[i] > arr[j+1]:
        arr[i], arr[j+1] = arr[j+1], arr[i]
  return arr

arr = [1,4, 5,2,9,3,6]
print(bubbleSort(arr))
``` 

### Selection Sort:

Selection sort repeatedly finding the minimum value from unsorted part and putting it into the beginning.
It somewhat lesser time complexity than bubble sort. 


![Selection-Sort-Flowhchart.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664547948716/9pJS9vn2N.png align="left")

Steps to implement the selection sort.

- lets fix the 0 the index as a min value
- compare it with all other elements to find min
- if any min value found just swap it.
- the above steps need to follow until the last index and we can skip the sorted parts in second loop.


```Python
def selectionSort(arr):

  n = len(arr)
  for i in range(n):
    min_idx = i
    for j in range(i+1, n):
      if arr[j] < arr[min_idx]:
        min_idx = j
    arr[i], arr[min_idx] = arr[min_idx], arr[i]
return arr 

arr = [1,4, 5,2,9,3,6]
print(selectionSort(arr))
``` 




