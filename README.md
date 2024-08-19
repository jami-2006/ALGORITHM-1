1.4 was though not much tough but I still have tried to provide a solution which did pass 4 test cases but failed in 1 and since it took quite long time to code it I didn't have any time left to remove the error. 1.5 I have tried to solve using brute force since I don't know graphing. But it has exceeded time limit for some cases.

PROBLEM 2
one can easily observe that A&B + A|B =A+B. Using this as the logic One can develop an algorithm to solve problem 2. 
elements o array be x1,x2,x3....
if n is odd
suppose all the n elements of an array be arranged on a circle. now it will take 2*n querries to get the the sum of any two adjacent elements. let the pair wise sum be denoted as a1,a2...
add a1+a2... and divide it by 2 to get the sum of all the n elements. Now now pick out any one element you want to know say x1. so now since we have adjacent pairwise sums of elements. Just add alternate sums starting from x2 which will give you (x2+x3)+(x4+x5)..... and so on that is sum of all elements except x1.
Now you have sum of all elements in the array and sum of all elements except x1. subtract second from the first to get x1. repeat it n times to get all elements

if n is even
this time what we can do is separate out any one element. let's say x1. that means we are remaining with n-1 elements and n-1 is definitely odd. and hence using the algorithm defined above one can easily get those n-1 numbers using 2n-2 querries. now use two more querries to get the bitwise and and or of x1 with any other known element say x2. get their sum and subtract x2 to get x1.


now since you have each element using 2*n querries you can easily tell the kth smallest element in the array.

I found it quite difficult to code in interactive mode hence wrote the algorithm.
