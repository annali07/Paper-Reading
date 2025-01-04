# Cache Telepathy (2020)

## Cache Telepathy: Leveraging Shared Resource Attacks to Learn DNN Architectures

## Context

When doing the reviews, be very critical

Always think about better ways of solving the problem or related problems.

Question the problem as well

## Summary

- Problem: DNN running on MLaaS is vulnerable to cache based side channel attack; their hyper-parameters can be stolen. The paper notes that DNN inference heavily relies on matrix multiplication (GEMM operations) and matrix dimensions are directly determined by DNN hyper-parameters. The key insight is that matrix dimension is correlated to the number of function loop iterations in libraries like OpenBLAS and MKL. With this realization, cache side channel attack can reveal information about hyper-parameters (mainly the number of iterations of loops).
- The attack is effective in reducing the search space down several orders of magnitude and making verification practical.

## Strengths

- Novel attack strategy with clear motivation and target, high practicality, and high significance.  Economic significance as companies using MLaaS lack funding, yet having architecture stolen hurts their revenue, so they can never grow in technology nor afford own private infrastructure.
- Impressive technical depth as the attack requires deep understanding in not only cache based side channel attack but also characteristics and features of the neural network ( i.e. how their layers are connected, how they compute)
- Uses reverse engineering and binary analysis to expand the attack scope (analyzing the MKL library and realizing the special case in Section 6, and modify attack strategy to still extract useful information) Also reverse engineering connections between layers was fascinating.
- Structure clear, procedure detailed and easy to follow.
- Clearly discuss the noise and circumstances and an instance where Prime + Probe becomes ineffective.

## Weakness

- The attack outlines that from the few search space, an architecture can be found. However, it did not cite any work of previous success in finding an architecture this way, making the verification partially incomplete.
- The attack can only be performed in an environment where resource (particularly CPU cache) is shared.

## Reflect and Ideas for Improvement

- The amount of work put into this paper is unimaginable.

## Takeaways/Comment

- Comment: Even when I try to think critically it’s difficult for me to define a weakness in this paper. The observation of an exploit and experiment conducted are absolutely fascinating.
- I’m also amazed by how this paper utilizes knowledge from 2 seemingly unrelated field, but integrated them so well; you can not perform the attack without knowing how DNN works
- This paper has had a profound impact on me personally. Prior to this paper, I viewed the deep learning boom with skepticism and found little interest in the field. However, this paper demonstrated that even from a hardware security professional perspective, it is beneficial to understand how they work.  In fact, sections explaining the neural network (first 5 pages or so) are surprisingly interesting. Thanks to this paper, I’ve been inspired to begin studying neural networks.

##