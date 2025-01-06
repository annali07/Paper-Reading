# Intelligent Arch for Intelligent Computing Systems (2021)

## Intelligent Architecture for intelligent Computing Systems

## Summary

- The paper identifies the growing data bottleneck and summarizes the challenges into 3 fundamental problems:
    - moving data from memory incurs high cost and latency
    - systems failing to effectively utilize the vast amount of data they process
    - systems disregard the characteristics of the data they process
- The paper proposes 3 key principles as solutions to the present predicament:
    - data-centric: minimizing data movement by using PIM (PNM and PUM)
    - data-driven: using reinforcement/machine learning to improve system decisions
    - data-aware: understanding data characteristics to optimize system behaviour.

## Strengths

- The paper provides great insight by identifying the fundamental challenge from a widespread modern phenomenon: while CPU has been highly optimized, memory technology has failed to keep pace. The limitations of interconnects compounds the predicament as there is high data transfer overhead. However, today’s dominant workloads (ML, genome processing  etc.) are increasingly data intensive. Thus, the paper astutely recognizes that the key to accelerating these workloads.
- The paper’s proposed paradigm shift from processor-centric to data-centric architectures represents a potentially revolutionary change in computing, comparable in significance to how Von Neumann mode revolutionized computer architecture.
- The paper is supported by extensive references to practical implementations and research results, demonstrating real-world applicability.

## Weakness

- Increasing data-awareness also increases security risks, which is not explored enough in the paper. For instance, in the recent GoFetch paper, the DMP is taking advantage of data-awareness in de-referencing pointers in its pre-fetch optimization. However, this turned out to be a side channel that could be exploited.
- Shifting to a data-centric paradigm also poses burden on the way how programmers think. This may be harder of an adaption than technology-wise innovations.
- Limited discussion of tradeoffs, which is a major component in computer architecture.

## Reflect and Ideas for Improvement

- The challenge in writing this paper lies in the experience accumulated over the years, following the trend in industry in detail and identifying the future potential. It takes time to accumulate such understanding of computing systems from a broad, holistic and detailed perspective in order to construct this paper.

## Takeaways/Comment

- I really liked how the paper viewed the computing system from a different perspective. At present, while the industry continues to optimize the processor-centric model to mitigate the data bottleneck, we would eventually only get diminishing returns. Thus, rather than marginal improvements, this paper poses a radical change in the fundamentals of computer architecture. If we entirely use a different computing model, we may achieve unimaginable results. I’m really excited and look forward to how this idea will influence systems the next 10 years.

##