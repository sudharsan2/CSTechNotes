1. recursion is nothing but calling the function itself until the desired outcome has been achieved.

2. this can be achieved with a classic example of factorial problem.

![[Pasted image 20240616131402.png]]
here we can say that $5! = 5 * 4!$ and $4! = 4 * 3!$ and so on until $1!$ which is equal to 1 and we don't want to go any further down. the program piece in the image explains it clearly.

3. while speaking about the time complexity of the recursion function is `O(n)` as we can see with the factorial example to compute the final answer we are going through 5 steps.

4. the time complexity for recursion may look similar to an while loop or  for loop but actually it is worse in this case because here while using recursion the space complexity is gonna be O(n) as well. Even though we are not allocating any variable to take up space, how this recursion actually works is (with this example) the function that is calculating the 5! will continue taking up the space until 4! is done and this goes down until 1! in done calculating. (all the functions are gonna be alive at the same time).

example problem - [[Factorial (Python)]]

practice problems:
1. https://leetcode.com/problems/reverse-linked-list/