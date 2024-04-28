[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

Sources: Used ai mainly for the second question

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  Constants/Lower Order Terms: Asymptotic analysis disregards constants and lower order terms which can be significant in practical scenarios. An algorithm with a lower asymptotic complexity might have a large constant factor making it slower for smaller inputs compared to another with a higher complexity but a smaller constant factor.

  Input Characteristics: Asymptotic complexity assumes average or worst case scenarios and does not account for the specific characteristics or distribution of the input data. In real world usage, the actual input data might not reflect these assumptions, which can affect performance. An example of this is that asymptotic analysis doesn't pay attention to small data sets.

  System Architecture/Resources: Asymptotic analysis does not consider factors like memory hierarchy (cache sizes, disk access times), parallelism, or optimizations that can significantly impact performance. Eg an algorithm that fits well within the CPU cache will generally perform better than one that does not, regardless of asymptotic complexity.

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

  Implementation: Certain implementation specifics such as recursion depth, function calls, or bad memory access patterns can potentially affect performance. If the implementation involves checks that were not accounted for in the asymptotic analysis, it can lead to increased execution time.
