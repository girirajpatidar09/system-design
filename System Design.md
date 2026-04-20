# System Design 

```text
# What is Concurrency Control ?
Concurrency control ensures that multiple users or threads can access and modify data at the same time without causing inconsistency or errors.
```
---

```text
# What is Shared Resource ?
A shared resource is any data or object that is accessed by more than one thread at the same time.Because multiple threads use it together,
 it can cause data inconsistency if not handled properly.
```
---

```text
# What is critical section ?
A critical section is a part of the code where a shared resource is accessed or modified. 👉Only one thread at a time should execute the 
critical section to avoid data inconsistency.
```
---

``` text
# What is Data inconsistency ?
Data inconsistency occurs when multiple threads access and modify the same shared data at the same time, causing the data to become 
incorrect or unpredictable.
```
---

``` text
# What is Race Condition ?
A race condition occurs when two or more threads access shared data at the same time, which leads to data inconsistency.
```
---


