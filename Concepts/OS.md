# Operating Systems. 

http://cs162.eecs.berkeley.edu
Operating Systems: Principles and Practice ANderson and Dahlin
Operating Systems: Three Easy Peices, By Remzi and Andrea Arpaci-Dusseau
Linux Kernel Development , 3rd Edition by Robert Love

Concepts: 
	1. OS concepts: how to navigate aas a Systems Programmer
		- Process, I/O, Networks and Virtual Machines
	2. Concurrency
		1. Threads, Scheduling, locks, deadlock, Scalability, fairness
	3. Address Space
		1. Virtual Memory, Address translation, protection, sharing
	4. File Systems
		1. I/O devices, file objects, storage, naming, caching, performance, paging, transactions, databases
	5. Distributed Systems
		1. Protocoals , N-Tiers, RPC, NFS, DHTs , Consistency, Scalability, multicast
	6. Reliability and Security
		1. Fault Tolerance, protection, security
### What is an operating system: 


1. Referee- 
	1. manage protection, isolation and  sharing of resources
			Resource allocation and communciation.
2. Illusionist: 
	1. Provide clean, easy to use abstarctions of physical resources
		1. Give an illusion of infinite memory, dedicated machine
		2. Higher level objects: files, users, messages
		3. Masking limitations, virtualization
	2. Provides fault containment, fault tolerance and fault recovery
	3. Simplify application development by providing standard services. 
	4. Coordinate resources and protect users from each other. 
3. Glue: 
	1. Provides common services like 
		1. Display, Storage, Window System, Networking
		2. Sharing, AUthorization
		3. Look and Feel

![[Screenshot 2025-01-20 at 4.43.08 PM.png]]

---


