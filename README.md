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
def linear(lst,item):
    for i in range(len(lst)):
        if (lst[i]==item):
            return i   
    return -1
lst=[5,12,7,20,9]
item=int(input("no:"))
result=linear(lst,item)
if(result!=-1):
    print("index value is : ", result)
else:
    print("index value is not found")





```
## OUTPUT:
<img width="470" height="152" alt="image" src="https://github.com/user-attachments/assets/e86f06a8-e346-4df7-82cc-8376de692d8c" />


ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binary(lst, item):
    low = 0
    high = len(lst) - 1

    while low <= high:
        mid = (low + high) // 2

        if lst[mid] == item:
            return mid
        elif lst[mid] < item:
            low = mid + 1
        else:
            high = mid - 1

    return -1

lst = [5, 12, 20, 30, 45, 50]  
item = int(input())
result=binary(lst, item)
if(result!=-1):
    print("Found at index", result)
else:
    print("Not found")









```
## OUTPUT:
<img width="450" height="138" alt="image" src="https://github.com/user-attachments/assets/5c4a03c5-2a75-4d45-9d36-0313c8411248" />


iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binary(lst, low, high, item):
    if low <= high:
        mid = (low + high) // 2

        if lst[mid] == item:
            return mid
        elif lst[mid] < item:
            return binary(lst, mid + 1, high, item)
        else:
            return binary(lst, low, mid - 1, item)
    else:
        return -1


lst = [5, 12, 20, 30, 45, 50]   # sorted list
item = int(input())

result = binary(lst, 0, len(lst) - 1, item)

if result != -1:
    print("Found at index", result)
else:
    print("Not found")








```
## OUTPUT:
<img width="471" height="158" alt="image" src="https://github.com/user-attachments/assets/ad1e7c2e-2da1-4623-be1a-c544953e7a1a" />






## Result
Thus the linear search and binary search algorithm is implemented using python programming.
