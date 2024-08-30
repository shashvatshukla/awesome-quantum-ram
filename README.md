# Awesome Quantum Random Access Memory
A list of awesome resources about Quantum Random Access Memory.

Feel free to create pull requests with suggestions. Accompanying descriptions to each list item are preferred. 


# List

## Reviews, overviews and surveys

* [Quantum Random Access Memory for Dummies](https://www.mdpi.com/1424-8220/23/17/7462)

* [QRAM: A Survey and Critique](https://arxiv.org/abs/2305.10310)

## Papers

* [Original QRAM paper](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.100.160501)

Quantum Random Access Memory. Vittorio Giovannetti, Seth Lloyd, and Lorenzo Maccone. 2008. PRL. 4 pages. 

Defines QRAM. Presents the standard fanout architecture for RAM and proposes the bucket-brigade architecture for RAM and QRAM. The bucket-brigade architecture exponentially reduces the number of two-qubit interactions between "active" (not wait state) states, and so are advantageous for error models where only "active" states experience noise. A photonic implementation is discussed. 
* [Longer QRAM paper shortly after original](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.100.160501)

Architectures for a quantum random access memory. Vittorio Giovannetti, Seth Lloyd, and Lorenzo Maccone. 2008. PRA. 9 pages. 

This paper covers the same scope in more detail as the one above.

* [Circuit-based QRAM for Classical Data](https://www.nature.com/articles/s41598-019-40439-3.pdf)

* [Hardware-Efficient Quantum Random Access Memory with Hybrid Quantum Acoustic Systems](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.123.250501)

* [On the robustness of bucket brigade quantum RAM](https://arxiv.org/abs/1502.03450)

* [Systems Architecture for Quantum Random Access Memory](https://arxiv.org/abs/2306.03242)

## Theses

* [Practicality of QRAM PhD Thesis](https://elischolar.library.yale.edu/gsas_dissertations/346/)

Practicality of Quantum Random Access Memory. Connor Hann. 2021. 253 pages. 

Contains complete example circuits for QRAM architectures. Analyses the noise-resilience of bucket-brigade QRAM in a setting where the components experience noise even in the "wait" state and finds that due to limited entanglement between components the infidelity only scales poly-logarithmically with the memory size. Proposes a hardware-efficient error suppression scheme not relying on quantum error correction, but as a result it can at most quadratically improve the error probability. Proposes experimental implementations of QRAM for hybrid quantum acoustic systems.

## Talks

* [The resilience of quantum random access memory to generic noise (Connor Hann, March Meeting 2020)](https://www.youtube.com/watch?v=mz3DdS-HLdM)

* [Systems Architecture for Quantum Random Access Memory](https://www.youtube.com/watch?v=5SS-LvNoVrA)

* [QRAM A Survey and Critique](https://www.youtube.com/watch?v=Wm2dowNOek4)

## Other

* [Optimistic blog post on QRAM](http://nisqybusiness.com/2019/08/05/on-qram/)

On QRAM. Joe Fitzsimons. 2019. Nisqy Business (Blog). 5 min read.
