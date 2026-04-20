# System Design 

## Concurrency Control  in Distributed System


### What is Concurrency Control ?
Concurrency control ensures that multiple users or threads can access and modify data at the same time without causing inconsistency or errors.



### What is Shared Resource ?
A shared resource is any data or object that is accessed by more than one thread at the same time.Because multiple threads use it together,
it can cause data inconsistency if not handled properly.
 
 
### What is critical section ?
A critical section is a part of the code where a shared resource is accessed or modified. 👉Only one thread at a time should execute the 
critical section to avoid data inconsistency.



### What is Data inconsistency ?
Data inconsistency occurs when multiple threads access and modify the same shared data at the same time, causing the data to become 
incorrect or unpredictable.



### What is Race Condition ?
A race condition occurs when two or more threads access shared data at the same time, which leads to data inconsistency.



###  Scenario :: Many concurrent request tries to book same Movie threater Seat


```text
User1      User2      User3

ID     Status
10     FREE

{
  Read Seat Row with ID: 10
  If Free:
      Logic to Change the Status from Free to Booked
      Update the DB
}


In above scenario there is a chance of getting data inconsistency.

----------------------------------------------------------------------

1) Using "SYNCHRONIZED" for the Critical Section:

synchronized () 
{
    Read Seat Row with ID: 10
    If Free:
        Logic to Change the Status from Free to Booked;
        Update the DB;
}

ID     Status
10     FREE


The problem is solved wiht synchronization  concept

-Will this solution works for Distributed System?
-No, Synchronization will work for Distributed System 
```
---



