## 459. Closest Number in Sorted Array  

### question

Given a target number and an integer array A sorted in ascending order, find the index i in A such that A[i] is closest to the given target. Return -1 if there is no element in the array.

### thoughts 

that means: 

  - if target exists, return its index. 

  - otherwise, return the one a little just smaller or larger than target.

So, do this: 

  - binary search. 
  
  - inside while loop, if find the target, return it directly 
  
  - otherwise, keep going, till exist the while loop
  
  - exit & compare A[start] - target vs. A[end] - target.  return the smaller one. 
  
  https://repl.it/@sisi/lin459-Closest-Number-in-Sorted-Array
  

## 458. Last Position of Target 
  
### question
  
  Find the last position of a target number in a sorted array. Return -1 if target does not exist.

### thoughts 

 - binary search
 
 - if find target : move **start** to mid, keep searching the last half --- vise versa if asking for first position 
  
  
  https://repl.it/@sisi/lin458-Last-Position-of-Target


## 28. Search a 2D Matrix

### Question

Write an efficient algorithm that searches for a value in an m x n matrix.

This matrix has the following properties:

 - Integers in each row are sorted from left to right.

 - The first integer of each row is greater than the last integer of the previous row.
 
 like this: 
 
 ```
 [
    [1, 3, 5, 7],
    [10, 11, 16, 20],
    [23, 30, 34, 50]
]

target = 3, return true

target = 0, return false
```


### thoughts 

 - two binary search: 
    
    - search one array first, find the possible target array
    
    - then go inside that array, binary search for target number 
    
  https://repl.it/@sisi/74m-Search-a-2D-Matrix
  
  
  ## 38. Search a 2D Matrix II
  
  ### question
  
Write an efficient algorithm that searches for a value in an m x n matrix, return the occurrence of it.

This matrix has the following properties:

- Integers in each row are sorted from left to right.

- Integers in each column are sorted from up to bottom.

- No duplicate integers in each row or column.


```

[
  [1, 3, 5, 7],
  [2, 4, 7, 8],
  [3, 5, 9, 10]
]
given target = 3, return 2 

```

### thoughts 

start from **upper right**. then every number on the left <= then itself, every number on the bottom >= then itself.

each time delete a row or a column -- will finish within O(m + n) time & O(1) space

Implementation : 
 
 - two pointers: colPointer = 0 & rowPointer = matrix[0].length - 1
 
 - if selectedNum === target :move one column down & one row left (colPointer++; rowPointer--) & count++
 
 - if selectedNum < target : colPointer++

 - else: rowPointer++ 
 
 https://repl.it/@sisi/240m-Search-a-2D-Matrix-II




