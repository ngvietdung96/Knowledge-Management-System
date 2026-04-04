Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[Operation System]], [[Open Source]]

---
# Composite OS

https://www.youtube.com/@nothing6001

## OS research for a changing world

OSes have difficulties both scaling up to very large-scale systems, and scaling down to the smallest of IoT devices. This is especially true when providing strength in non-functional constraints such as security, reliability, predictability, and efficiency. Composite provides abstractions and mechanisms tailored toward a world in which tail-latency, system resiliency, and dependability are increasingly important.

### Key principles:
- **Component-based policy.** System policies for resource management should be defined in user-level components. There are two key implications of this principle: 1. Similar to the microkernel principle of minimality, simplified as "policies that can be implemented in user-level, should be". 2. Resources should be managed by separate components with orthogonal implementations, where possible. This principle is the foundation for the component-based design of the overall system.
- **End-to-end execution attribution.** It is difficult to understand _who_ is using each resource at all points in time, as a "client" can make many transitive requests through many components (for example, communicating with a socket component, then TCP, then scheduling). To provide full accountability and resource management (e.g. for priority management for shared resources), end-to-end tracking of principals is required.
- **Principle of least privilege.** This principle is a foundation for secure systems. Each body of code should have access to the resources needed to carry out its goals, and _only_ those resources. This implies the fine-grained decomposition of system software into separate functional components, each with limited access to system resources. Composite takes this principle to an extreme by separating even the lowest-level traditional policies (including scheduling, synchronization, and memory management) into separate policies.
- **Scalable predictability.** Predictable execution is that for which we can determine and provide an execution bound. This is an essential non-functional requirement of any real-time system, but is increasingly important as massive servers concern themselves with lowering service tail-latencies. Composite is designed to provide predictable execution even with an increasing number of cores by avoiding locks and shared, modified cache-lines.





---
# References
Official website: https://composite.seas.gwu.edu/
Github: https://github.com/gwsystems/composite
Wikipedia:
Youtube: