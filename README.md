[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

Sources: Used ai mainly for the second question and google

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  Constants/Lower Order Terms: Asymptotic analysis disregards constants and lower order terms which can be significant in practical scenarios. An algorithm with a lower asymptotic complexity might have a large constant factor making it slower for smaller inputs compared to another with a higher complexity but a smaller constant factor.

  Time Complexity is Not Strict: Big Oh notation is a way to give a rough idea of how slow an algorithm can get as the amount of data increases. For example, if an algorithm is described as $(O(n^2))$, it means that in the worst case, its running time will increase by the square of the number of items. But, this notation is pretty flexible. That same algorithm could also be described as $(O(n^3))$ or $(O(n^4))$ because those notations cover any performance that's as bad or worse than $(O(n^2))$. Big Omega notation works the other way around, setting a baseline for how fast an algorithm can be. Because these notations are so broad, they can sometimes give a misleading picture of how an algorithm actually performs in real situations.

  The size of the input data is important in determining the efficiency of an algorithm, especially when dealing with smaller inputs. While time complexity gives us an idea of how an algorithm will behave for large inputs, it doesn't tell us much about its performance with smaller inputs. In practice, there's often a threshold where the algorithm's efficiency becomes noticeable. For inputs smaller than this threshold, the algorithm might not be as fast or efficient as other algorithms that are designed specifically for smaller datasets. So, even if an algorithm is theoretically efficient for large inputs, it might not be the best choice for smaller inputs where a different algorithm could outperform it in terms of speed and efficiency even if we analyze the case beforehand.

 Size of Input Data: 
 
- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  For 1,000 elements, taking 5 seconds, assume time complexity is $( O(\log n) )$:
  
    $(\log_2(1000) \approx 10)$
  
  For 10,000 elements:

    $(\log_2(10000) \approx 13.3)$
  
    $( 5 \times \frac{13.3}{10}) \approx$ 6.65 seconds

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  Tree Structure: If the tree is not perfectly balanced and instead is skewed or weakens to be list like structure, the effective complexity could approach $( O(n) )$, resulting in longer search times. A height balanced tree does not always mean a perfectly balanced tree.

  System Limitations: With larger data there may be overheads such as memory management, paging, and cache inefficiency. These overheads grow as the size of the data structure increases, especially if the data no longer fits efficiently in memory or cache.

  Implementation: Certain implementation specifics such as recursion depth, function calls, or bad memory access patterns can potentially affect performance. If the implementation involves checks that were not counted in the asymptotic analysis, it can lead to worse execution time.
