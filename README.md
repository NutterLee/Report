
# OmegaReport 

A technical report for omega

## Characteristics 

1. Omega stored the state of the cluster in a centralized Paxos-based transaction-oriented store that was accessed by the different parts of the cluster control plane (such as schedulers), using optimistic concurrency control to handle the occasional conflicts.
2. Expose the store directly to trusted control-plane components
3. Encapsulate the application environment, abstracting away many details of machines and operating systems from the application developer and the deployment infrastructure.
4. Because well-designed containers and container images are scoped to a single application, managing containers means managing applications rather than machines. 
5. Shared-state scheduling

## Pros&Cons 

Pros:
1. The company can has only a small number of OS versions deployed across its entire fleet of machines at any one time,and needs only a small staff of people to maintain them and push out new versions.  
2. It relieves application developers and operations teams from worrying about specific details of machines and operating systems.  
3. It provides the infrastructure team flexibility to roll out new hardware and upgrade operating systems with minimal impact on running applications and their developers.  
4. It ties telemetry collected by the management system (e.g., metrics such as CPU and memory usage) to applications rather than machines, which dramatically improves application monitoring and introspection, especially when scale-up, machine failures, or maintenance cause application instances to move.  


Cons:  
1. not open-source  
2. expose raw state


## My own comment  
1. dockers save us a lot of time to build and manage different environments
2. the HPC is much different from what we use in school, building and managing HPC needs to combine lots of things together
3. Omega shares the state within the clusters, this makes scheduling easier for scheduler, but also means it's difficult to avoid apps to get too much resources
4. Google uses its experience to develop Kubernetes, so if possible, use KUbernetes instead.


## References

1.  Burns, Brendan, et al. "Borg, omega, and kubernetes." Queue 14.1 (2016): 10.  
2.  Schwarzkopf, Malte, et al. "Omega: flexible, scalable schedulers for large compute clusters." Proceedings of the 8th ACM European Conference on Computer Systems. ACM, 2013. 

