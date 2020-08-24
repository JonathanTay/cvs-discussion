# Dynamic Programming for GA: Study Notes

## Steps to Solve a DP problem:
1. Define the sub-problem
    a. Start with prefix of the input (index with i, the last entry of prefix)
    b. Make a stricter subproblem definition (ie: prefix of input that must include last term)
    c. Use substrings of the input (ie: index with start and end of prefix i,j)
2. Write recurrence relationship between subproblems.
3. Figure out order subproblems need to be solved in.
4. Write down base-case.

### Writing Solutions:
1. Define sub-problem / table entry
2. Write base-case, recurrence, return
3. Comment on correctness of recursion
4. Pseudocode
5. Comment on running time

### Categories:
1. Prefix
2. Prefix + Endpoint
3. Substrings
4. Rooted subtrees



## Some Hints and Ideas
1. Try categories in order
2. Use known running time as a hint
3. If you want a solution that is a substring, it’s probably prefix + endpoint 






       test
       test box
     
     
        


| | |
|-|-|
|`NOTE` | This is something I want you to notice. It has a lot of text, and I want that text to wrap within a cell to the right of the `NOTE`, instead of under it.|
        
|`NOTE` | This is something I want you to notice. It has a lot of text, and I want that text to wrap within a cell to the right of the `NOTE`, instead of under it.|
|-|-|