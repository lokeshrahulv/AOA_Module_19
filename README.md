# AOA_Module_19
# EX 1A Reverse a String
## DATE:
## AIM:
To Write a Program to Create a recursive function to reverse a string

## Algorithm
1. Take input string s.
2. If length of s is 0 or 1, return s (base case).
3. Otherwise, recursively call the function with s[1:].
4. Append s[0] to the result of the recursive call.
5. Return the final reversed string. 

## Program:
```
/*
Program to implement Reverse a String
Developed by: LOKESH RAHUL V V
Register Number: 212222100024
*/
```
```

def reverse_string(s):
    """
    Recursive function to reverse a string
    """
    if len(s) <= 1:  # base case: if the string is empty or has only one character, return it as is
        return s
    else:
        return reverse_string(s[1:]) + s[0]  


input_string = input()
reversed_string = reverse_string(input_string)
print(reversed_string) 

```

## Output:
![Screenshot 2025-04-26 101504](https://github.com/user-attachments/assets/7bac129d-03e6-4500-8171-c22addc6f7f2)




## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string

# EX 1B Merge Sort
## DATE:
## AIM:
To Write a Program for Implementing merge sort using python recursion

## Algorithm
1. If the array has more than one element, split it into two halves.
2. Recursively apply merge sort on both halves.
3. Compare elements of both halves and merge them into a sorted array.
4. Copy any remaining elements from the left or right half.
5. Return the fully sorted array.  

## Program:
```
/*
Program to implement Merge Sort
Developed by: LOKESH RAHUL V V
Register Number: 212222100024
*/
```

```
def merge_sort(inp_arr):
    size = len(inp_arr)
    if size > 1:
        middle = size // 2
        left_arr = inp_arr[:middle]
        right_arr = inp_arr[middle:]
 
        merge_sort(left_arr)
        merge_sort(right_arr)
 
        p = 0
        q = 0
        r = 0
 
        left_size = len(left_arr)
        right_size = len(right_arr)
        while p < left_size and q < right_size:
            if left_arr[p] < right_arr[q]:
              inp_arr[r] = left_arr[p]
              p += 1
            else:
                inp_arr[r] = right_arr[q]
                q += 1
             
            r += 1
 
        
        while p < left_size:
            inp_arr[r] = left_arr[p]
            p += 1
            r += 1
 
        while q < right_size:
            inp_arr[r]=right_arr[q]
            q += 1
            r += 1
 
inp_arr=[]
n=int(input())
for i in range(0,n):
    inp_arr.append(int(input()))
print("Input Array:\n")
print(inp_arr)
merge_sort(inp_arr)
print("Sorted Array:\n")
print(inp_arr)
```

## Output:
![Screenshot 2025-04-26 101850](https://github.com/user-attachments/assets/f83c9b4d-5876-4040-b28f-075a5d44c42d)




## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.

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
Developed by:  LOKESH RAHUL V V
Register Number: 212222100024
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

# EX 1D Linear search
## DATE:
## AIM:
To Write a python program to implement linear search on the given tuple



## Algorithm
1. Loop through each element in the tuple.
2. Compare the current element with the target value x.
3. If the element matches x, print that the element was found and stop the search.
4. If no match is found after checking all elements, print that the element was not found.
5. End the function. 

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by:  LOKESH RAHUL V V
Register Number: 212222100024
*/
```
```
def search(tuple1,x):
    for value in tuple1:
        if(value==x):
            print("Tuple: %d found"%x)
            return 0
    print("Tuple: %d not found"%x)
    
List=[]
n=int(input())
for i in range(n):
    List.append(int(input()))
tuple1=tuple(List)
x=float(input())
search(tuple1,x)
```

## Output:
![image](https://github.com/user-attachments/assets/229f998a-4722-4e31-85b0-2e17f03f013e)



## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
