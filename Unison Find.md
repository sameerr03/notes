A data structure that is a set of linked lists with a representative element for each one. 
![[Pasted image 20230830004026.png|400]]

The operations in a union find are
**Operation 1 (Find):** given a number output its representative
**Operation 2(Unison):** Merge 2 linked lists into a third linked list with a single representative. 

A metadata block can be used in front of each list. This block can point to both the head and the tail of the list (tail to connect the last node from one linked list to the first in another in order to merge the lists for a unison). Each node will have an additional pointer to the metadata block. 

**Unison Rule:** The smaller list is merged to the larger list than the opposite. This is to ensure that less nodes in the smaller list have to change the metadata pointer now to the metadata block of the longer list. This rule implies that when the representative to a particular node is reassigned the list it is a part of has at least doubled. 

