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

Defines QRAM. Presents the standard fanout architecture for RAM and proposes the bucket-brigade architecture for RAM and QRAM. The bucket-brigade architecture exponentially reduces (from linear in N, the memory size, to polylog in N) the number of two-qubit interactions between "active" (not wait state) states, and so are advantageous for error models where only "active" states experience noise. A photonic implementation is discussed. 
* [Longer QRAM paper shortly after original](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.100.160501)

Architectures for a quantum random access memory. Vittorio Giovannetti, Seth Lloyd, and Lorenzo Maccone. 2008. PRA. 9 pages. 

This paper covers the same topics in more detail as the one above.

* [On the robustness of bucket brigade quantum RAM](https://arxiv.org/abs/1502.03450)

On the robustness of bucket brigade quantum RAM. Arunachalam et al. 2015. New Journal of Physics. 13 pages.

Points out a distinction between algorithms that take polylog (in N, memory size) queries to the data and those that take polynomial queries (in N) , e.g. Grover's Search that takes $\mathcal{O}(\sqrt{N})$ queries. Error correction may not be required in the former case. The paper focusses on the latter case. 
Argues that using quantum error correction causes the bucket-brigade architecture to lose its primary advantage of a small number of “active” gates, since
all components have to be actively error corrected.
Appeals to the work of Regev and Schiff on faulty oracles (which destroy Grover's search) and shows that QRAM acts as a faulty oracle in this sense. 

* [Hardware-Efficient Quantum Random Access Memory with Hybrid Quantum Acoustic Systems](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.123.250501)

* [Systems Architecture for Quantum Random Access Memory](https://arxiv.org/abs/2306.03242)

* [Circuit-based QRAM for Classical Data](https://www.nature.com/articles/s41598-019-40439-3.pdf)

* [Fault tolerant resource estimation of quantum random-access memories](https://arxiv.org/abs/1902.01329)

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

* [QRAM in Nature News and Views](https://www.nature.com/articles/468044a)

