# Slave Memories (1965)

## Slave Memories and Dynamic Storage Allocation

## Context

This paper proposed the concept of cache. 

Cache was first implemented in the IBM System/360 Model 85 in 1968, making it the first commercial computer with a cache memory system. Initial industry reaction was skeptical, but IBM demonstrated the feasibility of the idea. Wide-spread adoption of cache memory in early 1970s.

## Summary

- The paper addresses the issue of inefficient memory hierarchies of the time. When transferring data between fast and slow core memories, block transfers were wasteful; many words transferred are not used in subsequent execution.
- Wilkes discusses the details of tag and index bits in address, valid bit and dirty bit in cacheline, cache hierarchy, and separate tag storage.
- Wilkes provides insight to a cache hierarchy. Data in the secondary cache is transferred into first level cache on demand. Upon a context switch, only modified and valid (dirty bit and valid bit both being 1) cachelines in the first level are “written back” to main memory.
- Introduces concepts related to virtual memory, such as mapping several virtual addresses to the same physical address in cache. He points out potential issues, which would later be known as synonym problems.

## Strengths

- This paper provides key insight into the advantages of a cache and provides practical implementation details, elaborating on functionalities of specific bits, precise numbers, and base registers.

## Weakness

- This paper is limited due to the absence of discussions regarding of hardware integration cost. There is no discussion about implementation overhead or performance trade-offs, which is a crucial aspect in computer architecture.
- The paper did not discuss replacement policies, which are a significant aspect of cache performance optimization
- Lacks solutions for cache coherence when it talks about the multi-program scenario, which is an oversight.

## Reflect and Ideas for Improvement

- Overall, the paper astutely identifies a critical issue in present computer performance, and proposes a highly reasonable and executable solution.
- This realization requires innovation and observing. Even though there are many implementation details missing, is it still a revolutionary paper.  Like many pioneering papers, implementation gaps open the door for future research

## Takeaways/Comment

- Excellent paper demonstrating the power of observing deficiencies in current architecture and the potential that lies in the solutions proposed. Reminds me of in memory processing. This is an idea may indeed be revolutionary.
- Impact stems from recognizing fundamental problem and proposing conceptual framework, not implementation completeness