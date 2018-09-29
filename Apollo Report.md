# Apollo Report
#### Reporter: Zhengyu Wu
#### Report Time: 2018-09-29

This is a technical report for Apollo (Microsoft), a highly
scalable and coordinated scheduling framework.

![](https://github.com/GEORGE5961/markdown_photos/blob/master/apollo.png?raw=true)

## Characteristics
1. The framework performs scheduling decisions in a distributed manner, utilizing global cluster information via a loosely coordinated mechanism.

2. Each scheduling decision considers future resource availability
and optimizes various performance and system factors together in a single unified model.

3. Apollo is robust, with means to cope with unexpected system dynamics, and can take advantage of idle system resources gracefully while supplying guaranteed resources when needed.

## Pros&Cons

* Pros 
	1. High scheduling quality, with 95% of regular tasks experiencing a queuing delay of under 1 second.
	2. Achieving consistently high (over 80%) and balanced CPU utilization across the cluster.
	3. Coping well with the dynamics in diverse workloads and large clusters.

* Cons
	1. The estimates of Apollo are not good enough, which can be improved by leveraging statistics of recurring jobs and better understanding task internals.
	2. It is not open source which is only deployed on production
clusters at Microsoft until now.

## My own comment

Apollo schedules jobs in cloudscale production clusters at Microsoft, 
which does a good job in both performance and balance. Although it still has flaws, Apollo is the state-of-art framework in this field.

## References

1. Eric Boutin, et al. "Apollo: Scalable and Coordinated Scheduling
for Cloud-Scale Computing",  Proceedings of the 11th USENIX Symposium on Operating Systems Design and Implementation.

2. Burns, Brendan, et al. "Borg, omega, and kubernetes." Queue 14.1 (2016): 10.