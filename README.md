# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

## My Approach
The only way to test a function like this is to approach it from many different angles. Any sorting algorithm should, in theory, be able to sort any list given to it. The only way to ensure it is indeed better than the competition is to compare its runtimes for any given style of list to every other known general sorting algorithm.

The fastest way I can think of to test this, is to feed the program a series of lists that matches each other general sorting algorithm's worst case scenario and compare the performances of every general sorting algorithm and the new algorithm.

For example, competing against insertion sort, we would compare the new algorithms ability to process a reverse sorted list, i.e. [10,9,8,7...,3,2,1]
Insertion sort handles this at a time of $O(n^2)$, if the new algorithm can process this list, and other lists following the same pattern of varying lengths and complexities, then the algorithm can be said to outperform insertion sort. This exact method, applied to every other general sorting algorithm is how we would prove that this new algorithm was superior to every general sorting algorithm.

So, if X is faster for each sorting algorithm's worst case, then we can prove X is correct.

In addition, we can also run this algorithm and compare the expected time to $O(n)$ as the expected time. One way we could do this is to give a set of lists which increase by a factor of 10. If the algorithm really does process all lists at $O(n)$, then regardless of the ordering of the lists, the algorithm will be increased in time by exactly a factor of 10 from the previous example. So if a list of length 12 took 2.5 seconds, a list of length 120 should take 25 seconds and so on. This would prove that this algorithm can sort arbitrary elements in $O(n)$ time. 

## Plagarism Statement and Sources

Spoke to student Lily Brongo in class, asked her about the difficulty of the problem, she told me it wasn't too bad, just involved comparing runtimes for different lists. Other than that brief conversation, no other sources were used.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
