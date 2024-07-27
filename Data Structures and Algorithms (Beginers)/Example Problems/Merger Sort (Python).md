```
#Implementation of MergeSort
def mergeSort(arr, s, e):
    if e - s + 1 <= 1:
        return arr

    # The middle index of the array
    m = (s + e) // 2

    # Sort the left half
    mergeSort(arr, s, m)

    # Sort the right half
    mergeSort(arr, m + 1, e)

    # Merge sorted halfs
    merge(arr, s, m, e)
    
    return arr

#Merge in-place
def merge(arr, s, m, e):
    # Copy the sorted left & right halfs to temp arrays
    L = arr[s: m + 1]
    R = arr[m + 1: e + 1]

    i = 0 # index for L
    j = 0 # index for R
    k = s # index for arr

    # Merge the two sorted halfs into the original array
    while i < len(L) and j < len(R):
        if L[i] <= R[j]:
            arr[k] = L[i]
            i += 1
        else:
            arr[k] = R[j]
            j += 1
        k += 1

    # One of the halfs will have elements remaining
    while i < len(L):
        arr[k] = L[i]
        i += 1
        k += 1
    while j < len(R):
        arr[k] = R[j]
        j += 1
        k += 1
```


def mergeSort(nums,s,e):

if e-s+1==1:

return None

m = (s+e)//2

  

mergeSort(nums,s,m)

mergeSort(nums, m+1, e)

  

merge(nums, s, m, e)

  

def merge(arr,s,m,e):

LeftPart = arr[s:m+1]

RightPart = arr[m+1:e]

  

i=0

j=0

k=s

  

while i<len(LeftPart) and j<len(RightPart):

if LeftPart[i]<=RightPart[j]:

arr[k] = LeftPart[i]

i+=1

else:

arr[k] = RightPart[j]

j+=1

k+=1

while i<len(LeftPart):

arr[k] = LeftPart[i]

i+=1

k+=1

while j<len(RightPart):

arr[k] = RightPart[j]

j+=1

k+=1