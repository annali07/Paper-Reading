# MICRO FPGA-Based Near-Memory Acceleration (2021)

## FPGA-Based Near-Memory Acceleration of Modern Data-Intensive Applications

## Summary

- The paper identifies the inefficiency of cache optimization techniques (where spacial locality can not be exploited) for certain data-intensive applications, causing frequent data movement over power-hungry off-chip bus, thereby compounding the performance and energy efficiency dilemma.
- The paper uses HBM-based FPGA as an accelerator to accelerate the three kernels of data-intensive applications (SneakySnake, vadvc, hdiff).
- The key insight is that the paper demonstrates the capability of near-memory processing; it provides significant speed-up
    - The performance is compared among HBM + OCAPI, HBM(single PE multi HMB in parallel) + OCAPI, HMB + CAPI2, DDR4+CAPI2.
- Draws some key conclusions:
    - Tradeoff between enabling more HBM pseudo channels to provide each PE with more bandwidth, and implementing more PEs in the available area.
    - Observing adding more PEs does not lead to a linear reduction in performance
    - Concluding that increasing the number of PEs and enabled HBM channels does not always increase energy efficiency

## Strengths

- Very in-depth analysis of the computation of the two case studies/workloads (also pointing out that irregular memory access pattern and low arithmetic intensity common to both).
- Creates a unique specialized memory hierarchy from the pool of heterogeneous FPGA memories, and for each kernel, the hierarchy is different (best suited hierarchy is determined via Greedy algorithm).
    - Heterogeneous partitioning of on-chip memory blocks reduces read and write latencies across the FPGA memory hierarchy
- Provides viability of the near-memory approach

## Weakness

- The contribution of the paper could be stated more clearly. Initially I was confused as to whether this paper is novel in first building a FPGA with HBM or is the paper simply utilizing it? If it is the latter, what is the innovation and insight that the paper provides?
- Could elaborate on some sentences, i.e. “we use the on-chip heterogeneous memory hierarchy to unpack the stream data in a way that matches the data access pattern of an application” (how is it matched? Via what technique?) “we cache certain parts of data into a register file made of LUTs and FFs” (what parts of data is cached? what is the decision rule to determine what is cached?)

## Reflect and Ideas for Improvement

- The only area of improvement would be the structure of the paper.

## Takeaways/Comment

- The experiment with hardware and building the system is quite interesting and time-consuming. I enjoyed reading the performance analysis of the system.
- Adding a diagram comparing the “not near-memory” version of the system would be greatly appreciated.

##