# binary search tamplate: 

keep in mind: 

  - while loop: start + 1 < end
  
  - inside while loop: calculate mid
  
  - after while loop: check start & end

```
const binarySearch = (arr, num) => {
	if(!arr || arr.length === 0) return -1; 
	let start = 0;
	let end = arr.length;

// don't do <=
	while( start + 1 < end ) {
	let mid = start + Math.floor((end - start) / 2);
	if(num === arr[mid]) {
		return "found";
	} else if (num < arr[mid]){
		end = mid;
	} else {
		start = mid;
	}
	}
	
	if(arr[start] === num) return 'found'
	if(arr[end] === num) return 'found'
	return -1;
}

```


