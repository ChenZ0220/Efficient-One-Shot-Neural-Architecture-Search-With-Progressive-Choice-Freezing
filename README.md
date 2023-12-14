# Efficient-One-Shot-Neural-Architecture-Search-With-Progressive-Choice-Freezing

Neural Architecture Search (NAS) is a fast-developing research field to promote automatic machine
learning. Among the recently popular NAS methods, one-shot NAS has attracted significant attention
since it greatly reduces the training cost compared with the previous NAS methods. In one-shot NAS,
different architectures are encoded in a supernet, which is a stack of basic blocks, and each block
contains multiple architecture choices. The supernet is usually trained only once and can be reused
for different search scenarios. For each search scenario, the best candidate network architecture is
searched within the supernet, and each candidate is formed by selecting one choice for each block
in the supernet and inheriting the corresponding weights. In practice, the searching process involves
numerous inference processes for each user case, which causes high overhead in terms of latency
and energy consumption. To tackle this problem, we first observe that the choices of the first few
blocks that belong to different candidate networks will become similar at the early search stage.
Furthermore, these choices are already close to the optimal choices obtained at the end of the search.
Leveraging this interesting feature, we propose a progressive choice freezing evolutionary search
(PCF-ES) method that gradually freezes block choices for all candidate networks during the searching
process. This approach gives us an opportunity to reuse the intermediate data produced by the frozen
blocks instead of re-computing them. The experiment results show that the proposed PCF-ES with
importance sampling provides up to 76% speedup and reduces carbon dioxide emissions by 71%
during the searching stage.

![frozen.pdf](https://github.com/ChenZ0220/Efficient-One-Shot-Neural-Architecture-Search-With-Progressive-Choice-Freezing/files/13669908/frozen.pdf)
