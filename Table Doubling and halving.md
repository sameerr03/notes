A method of storing arrays with dynamic sizes in python. 

### table doubling
When all the indexes are filled up in an array in python, and the append command is given, a new array of twice the length of the old array is created in a separate space in the computer's memory. The elements in the old array are copied over into the new array and all the insertions happen in the next free slot in the array until the new limit is reached (append used each time as the array size only increases by one in the metadata).

![[Pasted image 20230830003317.png]]

### table halving
The inverse case of table doubling. pop is used in python to remove a particular index from an array and shorten its length by 1.  With each pop, the length of the array is not reduced in the computer's memory, those places remain unused. When less than a certain amount of memory in the memory is used (35-45%), then a new array is created in the system memory with only half the length. 