# Deadlock
## Deadlock Characterization
Deadlock can arise if four conditions hold simultaneously.
- **Mutual exclusion:**  only one process at a time can use a resource
- **Hold and wait:**  a process holding at least one resource is waiting to acquire additional resources held by other processes
- **No preemption:**  a resource can be released only voluntarily by the process holding it, after that process has completed its task
- **Circular wait:**  there exists a set {P0, P1, …, Pn} of waiting processes such that P0 is waiting for a resource that is held by P1, P1 is waiting for a resource that is held by P2, …, Pn–1 is waiting for a resource that is held by Pn, and Pn is waiting for a resource that is held by P0.

