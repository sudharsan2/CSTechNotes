1. so merge sort basically uses divide and conquer algorithm, the original array  of length $n$ is split in to 2 smaller arrays with each length of $n/2$ until the smaller array reach the length 1 . 
 ![[Pasted image 20240622113955.png]]
 and after dividing, from bottom it sorts the array and enters into the previous array of it (in the above picture 3 and 2 are sorted and pasted into its original array of size 2) and so on till the top and at the end the array is sorted.

2. this is how the pseudo code for merge sort algorithm looks like

![[Pasted image 20240622114519.png]]

here as we can look recursion is the great method to solve merge sort, in the code to divide the arrays into 2 the end of the first sub array is updated to $(start + end)/2$  and then same function is called (recursively) twice ,1st call if for the 1st sub array and 2nd half is for the second sub array and it is done the $(end -start +1) <=1$ this is when the subarray reaches the length of 1 and after that `merge()` function is called. and the the sorted array is returned.

3. to find the time complexity let say the original array length is n, first we have to find how many time we should divide the n by 2 so that we achieve 1 (length of the last subarray) and then while merging back we will iterate through every element in the sub arrays to put the sorted elements back in the previous subarray.

math equations looks like this:


								n/(2*2*2....) = 1
								
								n/(2^x)= 1
								
								n= 2^x
								
								log(n)= log(2^x)
								
								log(n)= x*log(2) => log(2)=1
								
								log(n) = x

and then each step takes O(n) as we discussed we need to iterate through each elements to put them back the previous sub array
so the overall time complexity is :

`O(nlog(n))`





example problem:
[[Merger Sort (Python)]]


practice problems:
1. https://leetcode.com/problems/sort-an-array/

2. https://leetcode.com/problems/merge-k-sorted-lists/

