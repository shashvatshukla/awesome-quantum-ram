# Awesome Quantum Random Access Memory
A list of awesome resources about Quantum Random Access Memory.

Feel free to create pull requests with suggestions. Accompanying descriptions to each list item are preferred. 

# List

## Reviews, overviews and surveys

* [QRAM: A Survey and Critique](https://arxiv.org/abs/2305.10310)

* [Quantum Random Access Memory for Dummies](https://www.mdpi.com/1424-8220/23/17/7462)

* [Quantum Memory: A Missing Piece in Quantum Computing Units](https://arxiv.org/abs/2309.14432)

* [Quantum Data Center: Perspectives](https://arxiv.org/abs/2309.06641)

## Theses

* [Practicality of QRAM PhD Thesis](https://elischolar.library.yale.edu/gsas_dissertations/346/)

Practicality of Quantum Random Access Memory. Connor Hann. 2021. 253 pages. 

Contains complete example circuits for QRAM architectures. Analyses the noise-resilience of bucket-brigade QRAM in a setting where the components experience noise even in the "wait" state and finds that due to limited entanglement between components the infidelity only scales poly-logarithmically with the memory size. Proposes a hardware-efficient error suppression scheme not relying on quantum error correction, but it can at most quadratically improve the error probability. Proposes experimental implementations of QRAM for hybrid quantum acoustic systems.

## Curated Papers

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

* [Resilience of QRAM to Generic Noise](https://journals.aps.org/prxquantum/abstract/10.1103/PRXQuantum.2.020311)

* [Systems Architecture for QRAM](https://arxiv.org/abs/2306.03242)

* [QRAM via Quantum Walk](https://iopscience.iop.org/article/10.1088/2058-9565/abf484/meta)

Quantum random access memory via quantum walk. Asaka et al. 2021. Quantum Sci Tech. 9 pages. 

Proposes a QRAM scheme which does not use a tree of quantum routers, switches or any kind of quantum device on the nodes of the tree. Rather, it is described in terms of classical logic done coherently on a register. A physical implementation is proposed in terms of dual-rail qubits (particles travelling along one of two paths). 
(Note that this is not a quantum walk in the sense that a variant of Grover's algorithm or Amplitude Amplification is applied. Rather, the mathematical structure of how the intermediate steps of the addressing scheme work can be modelled as a walk - but so can any classical computation. I would advise not paying too much attention to the word "walk" as it confused me during my first read.)
More details of the implementation are provided in the next paper. 

* [Two-level quantum walkers on directed graphs. II. Application to quantum random access memory](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.107.022416)

* [A QRAM using a polynomial encoding of binary strings](https://arxiv.org/abs/2408.16794)

A quantum random access memory (QRAM) using a polynomial encoding of binary strings. Priyanka Mukhopadhyay. 2024. arXiv preprint.

Presents a QRAM architecture in which the input address is first converted to a one-hot encoding using a fast $\mathcal{O}(\log \log N)$ T-depth circuit and then the memory can be read out by controlling on each qubit of this one-hot encoded register. The language of polynomials in this paper formalises this one-hot encoding idea. A quantum lookup table (aka QROM) idea is presented. The key differences are that the QROM circuit is not easily reconfigured when the stored memory is changed but rather has to be recompiled, and that it requires less space than a full QRAM. The way this quantum lookup table is implemented is by combining two of the polynomial QRAM architectures, with a hardcoded internal logic circuit. The first QRAM loads one of $\sqrt{N}$ chunks of data, each of $\sqrt{N}$ items. The second QRAM loads the right item from these $\sqrt{N}$ items. This split results in an $\mathcal{O}(\sqrt{N})$ space complexity. QRAM requires $\mathcal{O}(N)$. This paper has a very nice list of references on QRAM. 

* [Fault tolerant resource estimation of QRAM](https://arxiv.org/abs/1902.01329)

Fault tolerant resource estimation of quantum random-access memories. Olivia Di Matteo et al. 2020. arXiv preprint. 

Resource estimation of various quantum RAM proposals (including compiled circuits or "QROM") assuming a fully error corrected QRAM utilising the surface code. For millisecond query times to 8 GB memory, they estimate ~ $10^{15}$ physical qubits are required. This is about $10^5$ factor overhead on the number of bits in 8 GB ($6.4\times 10^{10}$ bits).

More about this work appears in the [PhD thesis](https://dspacemainprd01.lib.uwaterloo.ca/server/api/core/bitstreams/1cc5585b-db87-42a4-8bc1-f71d857e211f/content) of the lead author. [Code](https://github.com/glassnotes/FT_qRAM_Circuits) associated with this work. 

* [Memory Compression with Quantum Random-Access Gates](https://arxiv.org/abs/2203.05599)

* [Robust QRAM](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.86.010306)

* [Parallelizing the queries in a bucket-brigade QRAM](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.102.032608)

* [Compact and classically preprocessed data-loading quantum circuit as a quantum random access memory](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.110.012616)

* [Fundamental causal bounds of quantum random access memories](https://www.nature.com/articles/s41534-024-00848-3)

* [Efficient and Error-Resilient Data Access Protocols for a Limited-Sized Quantum Random Access Memory](https://arxiv.org/abs/2303.05207)

* [Resource-efficient simulation of noisy quantum circuits and application to network-enabled QRAM optimization](https://www.nature.com/articles/s41534-023-00773-x)

* [Multi-qubit time-bin quantum RAM](https://arxiv.org/abs/1412.2459)

* [Novel oracle constructions for quantum random access memory](https://arxiv.org/abs/2405.20225)

## Hardware 

* [Hardware-Efficient QRAM with Hybrid Quantum Acoustic Systems](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.123.250501)

* [Scalable and High-Fidelity Quantum Random Access Memory in Spin-Photon Networks](https://journals.aps.org/prxquantum/abstract/10.1103/PRXQuantum.2.030319)

* [Rapid single flux QRAM](https://ieeexplore.ieee.org/abstract/document/403223?casa_token=nYXXUrQvaTwAAAAA:DIXlyXH0ajSuDimAgos3vZf1sFej-SR-Ng4wzJO-VUpGxHI2OhLRlpb4vHQL6I10Zr0TyLuN)

* [Quantum Random Access Memory Architectures Using 3D Superconducting Cavities](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.110.012616)

* [Ultrafast Quantum Random Access Memory Utilizing Single Rydberg Atoms in a Bose-Einstein Condensate](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.111.240504)

* [Random-Access Quantum Memory Using Chirped Pulse Phase Encoding](https://journals.aps.org/prx/abstract/10.1103/PhysRevX.12.041014)

* [Photon echo quantum random access memory integration in a quantum computer](https://iopscience.iop.org/article/10.1088/0953-4075/45/12/124017/meta?casa_token=pVP5CpfQc6sAAAAA:fZUdixyOgvIOrd_VzxsW3O-ouFuaW9rRlYUvqoGS5aVRPUmONhRxTsxBOe3I1HRi7kYWmf8ZtMqJAW6Tm8Zd96mfPqY)

* [Experimental realization of 105-qubit random access quantum memory](https://www.nature.com/articles/s41534-019-0144-0)

* [Error-Mitigated Quantum Random Access Memory](https://arxiv.org/abs/2403.06340)

* [Maximizing the Yield of Bucket Brigade Quantum Random Access Memory using Redundancy Repair](https://arxiv.org/abs/2312.17483)

* [Quantum random access memory architectures using superconducting cavities](https://arxiv.org/abs/2310.08288)

## Algorithms that use QRAM, and other algorithmic aspects of QRAM

* [Quantum algorithm for finding minimum values in a Quantum Random Access Memory](https://arxiv.org/abs/2301.05122)

* [Quantum Linear Algorithm for Edit Distance Using the Word QRAM Model](https://arxiv.org/abs/2112.13005)

* [Improved Classical and Quantum Algorithms for the Shortest Vector Problem via Bounded Distance Decoding](https://arxiv.org/abs/2002.07955)

* [Optimal usage of QRAM in quantum machine learning](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.99.012326)

* [Quantum random access stored-program machines](https://www.sciencedirect.com/science/article/pii/S0022000022000599?casa_token=n_iI1fZUfTsAAAAA:ACv-YAhH5hHLYX81nxDkOlID3QVS2XxZtABd4FpBwp6JG2EogFclVAqdK0trGuKamVKBt4A34Q)

## Talks

* [The resilience of quantum random access memory to generic noise (Connor Hann, March Meeting 2020)](https://www.youtube.com/watch?v=mz3DdS-HLdM)

* [Systems Architecture for Quantum Random Access Memory](https://www.youtube.com/watch?v=5SS-LvNoVrA)

* [QRAM A Survey and Critique](https://www.youtube.com/watch?v=Wm2dowNOek4)

## Miscellany

* [Optimistic blog post on QRAM](http://nisqybusiness.com/2019/08/05/on-qram/)

On QRAM. Joe Fitzsimons. 2019. Nisqy Business (Blog). 5 min read.

* [QRAM in Nature News and Views](https://www.nature.com/articles/468044a)

* [Chirping toward a Quantum RAM](https://physics.aps.org/articles/v15/168)

* [QRAM student project](https://www.cs.umd.edu/class/fall2019/cmsc657/projects/group_11.pdf)

* [QRAM in nlab](https://ncatlab.org/nlab/show/QRAM)

## Interesting papers in a similar theme

* [Small quantum computers and large classical data sets](https://arxiv.org/abs/2004.00026)

* [Trading T gates for dirty qubits in state preparation and unitary synthesis](https://quantum-journal.org/papers/q-2024-06-17-1375/)

* [Unified Architecture for a Quantum Lookup Table](https://arxiv.org/abs/2406.18030)

## Other papers on QRAM

* [A novel efficient QRAM](https://ieeexplore.ieee.org/abstract/document/9568972)

Presents a QRAM-like circuit whose action is like reading just one memory cell of a QRAM. The circuit requires the data and address being read from to be explicitly stored in a quantum register. One merit of this technique is that it can load arbitrary quantum states, not just classical data.
Since the circuit loads one memory item, N iterations of it can be used to load all the data which might be useful in some settings, but is not usually what we want from a QRAM. 

* [Circuit-based QRAM for Classical Data](https://www.nature.com/articles/s41598-019-40439-3.pdf)

Quantum state preparation circuit that uses controlled rotation on an ancilla qubit and post-selection to get the right amplitudes. Presents a technique ("quantum forking") to compute the inner product of two states $U_1\ket{\psi}$ and $U_2\ket{\psi}$ given access to only one copy of $\ket{\psi}$.

* [Circuit-Based QRAM for Classical Data With Continuous Amplitudes](https://ieeexplore.ieee.org/abstract/document/9259210?casa_token=AVb77tRfT10AAAAA:tA5yZRDX5KSQ37OSY6rigKJPoSwuqxfOjpCdr0KzyYdB568lKck1ekJNqlvhE7jdJpBklonI)

* [Trainable PQC-Based QRAM for Quantum Storage](https://ieeexplore.ieee.org/abstract/document/10130283)

* [Data centers with QRAM and quantum networks](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.108.032610)

