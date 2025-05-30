# EX 1C Quick Sort
## DATE:
## AIM:
 To Write a python program to implement quick sort on the given values and print the sorted list and pivot value of each iteration

## Algorithm
1. Select a pivot element from the array (commonly the first or last element).
2. Partition the array into two subarrays: elements less than pivot and elements greater than or equal to pivot.
3. Place the pivot between the two subarrays at its correct position.
3. Recursively apply Quick Sort to the left subarray.
4. Recursively apply Quick Sort to the right subarray. 

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: ASHWIN KUMAR S
Register Number: 212222240013
*/
```
```
def partition(array, low, high):
    pivot = array[low]
    start = low + 1
    end = high
    print("pivot: ",pivot)
    while True:
        while start <= end and array[end] >= pivot:
            end = end - 1
        while start <= end and array[start] <= pivot:
            start = start + 1
        if start <= end:
            array[start], array[end] = array[end], array[start]
        else:
            break
    array[low], array[end] = array[end], array[low]
    return end
def quick_sort(array, start, end):
    if start < end:
        idx = partition(array, start, end)
        quick_sort(array, start, idx-1)
        quick_sort(array, idx+1, end)
arr1=[]
n=int(input())
for i in range(n):
    arr1.append(int(input()))
print("Input List\n",arr1)
quick_sort(arr1, 0, len(arr1)-1)
print("Sorted List\n",arr1)
 ```

## Output:
![Screenshot 2025-04-26 103158](https://github.com/user-attachments/assets/146028cb-9f62-4172-8700-fb3ab7855311)




## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
