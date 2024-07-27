1. the classic example for Two branch recursion is Fibonacci Series 

![[Pasted image 20240616140407.png]]

2. hope the image explains how the fibonacci series with recursion works. similar to the factorial problem but here we are calling the the function itself twice during the same operation.

3. and once again this is not the efficient method to find the nth fibonacci number if we use and for loop or an while loop we'll end up finding the nth fibonacci number with time complexity of $O(n)$ but here the time complexity is $O(2^n)$.

4. finding the time complexity is done by finding the longest path in the tree ![[Pasted image 20240616141749.png]]
in the image we can see that the longest path is n so if we look closely the upper bound for the last line would be $2^n$ (we start with 1 and the down the tree we are splitting by 2 so its gonna be 
{$2*2*2*2$... $n times$}) this is for the last line of the tree and by the math theory explained in point no. 7 of [[2. Dynamic Arrays]] we can conclude that the overall time complexity is gonna be $O(2^n)$

example problem - [[Fibonacci (Python)]]

practice problems:
1. https://leetcode.com/problems/fibonacci-number/

2. https://leetcode.com/problems/climbing-stairs/