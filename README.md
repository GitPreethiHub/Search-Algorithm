# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: Preethi M
RegisterNumber: 212222100037
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
    
array = eval(input())
k = eval(input()) # k-item to be seared for
n=len(array)
array.sort()
result = linearSearch(array,n,k)
print(array)
if(result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Preethi M
RegisterNumber: 212222100037
'''
def binarySearchIter(array, k, low, high):
    mid=0
    while low<=high:
        mid=(high+low)//2
        if(array[mid]<k):
            low=mid+1
        elif(array[mid]>k):
            high=mid-1
        else:
            return mid
    return -1
array = eval(input())
array.sort()
k = eval(input()) #k-item to be searched
result=binarySearchIter(array, k,0,len(array)-1)
print(array)
if(result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Preethi M
RegisterNumber: 212222100037
'''
def BinarySearch(arr, k, low, high):
    if(high>=low):
        mid=(low+high)//2
        if(arr[mid]<k):
            return BinarySearch(arr,k,mid+1,high)
        elif(arr[mid]>k):
            return BinarySearch(arr,k,low,mid-1)
        else:
            return mid
    else:
        return -1
arr = eval(input())
arr.sort()
k = eval(input()) # k is the element to be searched for
result=BinarySearch(arr,k,0,len(arr)-1)
print(arr)
if(result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)
```
## Output

![image](https://user-images.githubusercontent.com/119475585/235064374-0801ef9a-3dae-4124-970d-35acb329b004.png)

![image](https://user-images.githubusercontent.com/119475585/235064437-60c39b26-b816-4c66-9431-486ee27025f5.png)

![image](https://user-images.githubusercontent.com/119475585/235064488-cc42d41d-ef7d-44ba-9bb3-27e852f42c7a.png)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
