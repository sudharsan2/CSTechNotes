1. so how quick sort work is, in a given array we must choose an pivot value mostly the last element and then we must have two pointer both are starting from 0th index one of the pointer must iterate through the array until it reaches the pivot value and in each of this iteration it must check whether the value where the pointer points to is less than the pivot value. if yes, then we must swap that index's element with the other pointer's index's element. and when the iterating pointer reaches the pivot value's index we must swap the pivot value to the other pointer's index. 

2. we must do this recursively so by splitting the array until the pivot value's index and the above process continues by choosing a new pivot value.

3. ![[Pasted image 20240705095806.png]]
`[6,2,4,1,3]` is the original array here the pivot value is 3 we start both the pointers from 6 which is index 0 and then iterate the array using the second pointer first it check whether 6 is less than 3(pivot value) it isn't so we do nothing an move the pointer to the next index i.e 2 which is smaller than 3 so we swap 6 and 2 and move the 1st pointer to the next position i this case it is 1  and we continue this until the second pointer reaches the pivot value, so in this example when the second pointer reaches 3 the 1st pointer will be pointing to 4 so we swap pivot value and the first pointer's value.

coming the next subarray we must split the array's into 2 subarray 1st subarray must be from the start of the original array to the index where the pivot value lies, in this case `[2,1,3]` and `[6,4]`
and the same process should be done recursively if the old pivot value lies in the subarray in this case `[2,1,3]` array contains old pivot value 3 so the new pivot value must be the index value before 3 which is 1 , the second subarray does not contain the old pivot value so the last index value must be the new pivot value.

4. to find the time complexity when we are split down array the height of the tree would be roughly log(n) and in each level we are performing O(n) operation so the the time complexity on average would be $O(n*log(n))$ similar to [[Merge Sort]] . But, if the array is already sorted 
 ![[Pasted image 20240706131604.png]]
 her we can see that the height of the tree is n and in such case the time complexity would be $O(n^2)$ 
 
5. it is an unstable sorting algorithm as it only checks whether it is lesser than the pivot or not.

example Problem:
[[QuickSort (Python)]]

practice problems:
1. https://leetcode.com/problems/sort-an-array/

2. https://leetcode.com/problems/kth-largest-element-in-an-array/

