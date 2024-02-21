[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
1. Different machines deploy different kinds of computational mechanisms. Its possible to get different results running the same program on two different machines with distinct capabilities.

2. A machine computes programs not algorithms, meaning it runs exact instructions and not an abstract mathmatical model.

3. Asymptotic analysis often ignores constant factors and hidden multiplicative constants in algorithmic expressions.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

time complexity: O(n) 

K O(n) = 5 

K x n = 5 replace n with amount of elements

K x 1000 = 5 

K = 5/1000

K x 10000 = 50 seconds  

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

1. For larger values of n hardware optimizations may have taken place.

2. The constant factor K is dependant on various reasons such as RAM.

3. Depending on the programming language and instruction sets as mathmatical abstraction gives different values then exact instruction computation. 


