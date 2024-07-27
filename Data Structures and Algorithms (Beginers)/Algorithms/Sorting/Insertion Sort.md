1. So, for me this is an basic sorting technique where we consider the first element as an subproblem and then increase the length of our subproblem array by 1 and check whether they are sorted or not, if not sorted then we'll sort them and continue to increase our subproblem array length.

![[Pasted image 20240617095609.png]]
this what the pseudo code for the the insertion sort looks (simple and straight forward).

2. there are two types of sorting algorithms in general one is `Stable Sorting` and another one is `Unstable Sorting` 

![[Pasted image 20240617095928.png]]
we can see with the example in the image so `[7,3,7]` is an array so the stable sorting so sort the array with first occurring 7 in the original array must occur before the second occurring if this is satisfied then that sorting algorithm is an stable sorting algorithm. the reason for this to be called as an stable sorting algorithm is there is not unwanted sorting when both the elements values are same.

3. finding the time complexity of insertion sort is kind of interesting 

![[Pasted image 20240617102804.png]]
we can take this oppositely sorted array for the worst case time complexity which must be consider for `O() notation` . here the 4 is a subproblem of array of length 1 and then 3 comes under subproblem of array of length 2 and so on until the last element that is 1.

so the iteration would look like $1+2+3+4$ which is always bounded by $4+4+4+4$ which is $4^2$ 
to explain this more clearly.

![[Pasted image 20240617104418.png]]
in this image we can see that the $1+2+3+4$ is bounded by half by $4^2$ 
so the time complexity of insertion sort is $O(n^2)$ 

example Problem:
[[Insertion Sort (Python)]]

practice problems:
1. https://leetcode.com/problems/sort-an-array/