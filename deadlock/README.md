# Deadlock
## Deadlock Characterization
Deadlock can arise if four conditions hold simultaneously.
- **Mutual exclusion:**  only one process at a time can use a resource
- **Hold and wait:**  a process holding at least one resource is waiting to acquire additional resources held by other processes
- **No preemption:**  a resource can be released only voluntarily by the process holding it, after that process has completed its task
- **Circular wait:**  there exists a set {P0, P1, …, Pn} of waiting processes such that P0 is waiting for a resource that is held by P1, P1 is waiting for a resource that is held by P2, …, Pn–1 is waiting for a resource that is held by Pn, and Pn is waiting for a resource that is held by P0.
## Deadlock Prevention
Restrain the ways request can be made
- **Mutual Exclusion-** not required for sharable resources (e.g., read-only files); must hold for non-sharable resources
- **Hold and Wait-** must guarantee that whenever a process requests a resource, it does not hold any other resources
- **No Preemption-**
If a process that is holding some resources requests another resource that cannot be immediately allocated to it, then all resources currently being held are released
Preempted resources are added to the list of resources for which the process is waiting
Process will be restarted only when it can regain its old resources, as well as the new ones that it is requesting
- **Circular Wait-** impose a total ordering of all resource types, and require that each process requests resources in an increasing order of enumeration



