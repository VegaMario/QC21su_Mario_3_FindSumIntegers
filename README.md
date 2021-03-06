# QC21su_Mario_3_FindSumIntegers

## This Quantum Annealing program solves the following problem:

  For a given set S of n numbers, in the form of {1, 2, 3,..., n}, find a subset of C numbers that sum up to an integer N.
  For example, suppose that we have the set {1, 2, 3, 4, 5} and we want to find three integers that sum up to 8. A possible solution may be {1, 2, 5}. 
  This program should be able to do this, but in a much larger scale if desired, like if given a set of 1000 numbers, find 357 numbers that sum up to 88,876. 
  
  This program requires the Dwave Ocean tools to run successfully. It is based on the QUBO model and is solved by the Quantum Annealer.
  
  The following is the QUBO equation I came up with for this problem:

<img src="https://latex.codecogs.com/svg.latex?\text{QUBO}&space;=&space;min\left&space;(&space;\left&space;(&space;\sum_i^{n}s_i^2q_i&space;-&space;2N\sum_i^ns_iq_i&space;&plus;&space;2\sum_i^n\sum_{j>i}^ns_is_jq_iq_j&space;&plus;&space;N^2&space;\right&space;)&space;&plus;&space;\gamma&space;\left&space;(&space;\sum_i^nq_i&space;-&space;2C\sum_i^nq_i&space;&plus;&space;2&space;\sum_i^n&space;\sum_{j>i}^nq_iq_j&space;&plus;&space;C^2&space;\right&space;)&space;\right&space;)" title="\text{QUBO} = min\left ( \left ( \sum_i^{n}s_i^2q_i - 2N\sum_i^ns_iq_i + 2\sum_i^n\sum_{j>i}^ns_is_jq_iq_j + N^2 \right ) + \gamma \left ( \sum_i^nq_i - 2C\sum_i^nq_i + 2 \sum_i^n \sum_{j>i}^nq_iq_j + C^2 \right ) \right )" />

  The QUBO consists of an objective function, on the left, and a constraint function, on the right. The objective function states that we want to find a subset of         numbers that sum up to the integer N. The constraint function states that we want to choose C numbers that form the solution subset. The q terms and s terms in the       eqeuation represent the qubits and numbers in the set, respectively. 
  
  In other words, C represents the number of integers that will sum up to the number N. These are not given because it is up to us to decide what N and C will be. 
  
  In this program, I translate this equation into a QUBO matrix to be solved on a Quantum Annealer. 
  
  https://github.com/VegaMario/Assignment_3_FindSumIntegers
