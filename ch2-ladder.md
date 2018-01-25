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
