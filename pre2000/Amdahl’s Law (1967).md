# Amdahl’s Law (1967)

## Validity of the single processor approach to achieving large scale computing capabilities

## Context

In 1967, IBM announced System/360 Model 91, one of the first computers to use instruction pipelining. Early research began on parallel processing architectures. In 2001, IBM releases POWER4, first commercial dual-core processor.

## Summary

- Amdahl provides an overview of parallel architecture, the ongoing single processor versus parallel architecture debate in its applicability in real-world scenarios, and analyzes the computation nature and constraints of parallel programming.
- He challenges the main stream belief that connecting multiple processor was the only way forward for computing advancement.
- Other than the fact that every program has a serial part that do not gain from parallelism (later known as Amdahl’s law), Amdahl offers insight regarding 4 potential critical concerns, which are irregular boundaries, in-homogeneous data, dependent variables and limitations on propagation rates.
- He also explores cost-performance relationships, referencing Knight's analysis showing performance proportional to cost squared

## Strengths

- Amdahl effectively pieces together his knowledge of the current machine to speculate future shortcomings if an idea were to evolve itself. The challenges he pointed out remain highly relevant today.
- Amdahl had his discussion on an empirical basis, providing concrete percentage such as the 40% overhead observation
- The paper shows remarkable foresight in identifying fundamental limitations of an idea popular at his time.

## Weakness

- Figure 1 lacks experimental details, such as clear axis labels and specific performance numbers or scales. Methodology is lacking.
- Amdahl identified critical challenges, but his insight did not expand into discussion and exploration of potential mitigations or solutions.

## Reflect

- Amdahl’s analysis was slightly constrained in only pointing out deficiencies in parallel architectures, unlike Moore’s more speculative paper about future potential. However, criticizing is equally important as dreaming.
- His predictions about irregular boundaries and inhomogeneous interiors are remarkable; they have indeed became central challenges in HPC
- Although the paper did not present experimental results, its analytical ideas are foundational. Systematic reasoning is as important as conducting research, since a research with the wrong fundamental idea would undermine all the efforts put into it.

## Takeaways/Comment

- Takeaway: Always view the current technology, regardless of how promising everyone claims it to be, in a critical lens and identify potential deficiencies.
- Amdahl’s law established a fundamental framework for analyzing parallel system performance limitations.
- Figure 1 exemplifies what Professor Mutlu calls an "industry graph"