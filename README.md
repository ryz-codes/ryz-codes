# Research software

Software accompanying my work in **large-scale optimization** and **computational electromagnetics**, together with several reusable numerical tools.

## Sparse semidefinite optimization

### [Chordal conversion (CC)](https://github.com/ryz-codes/chordalConv)

MATLAB/MOSEK implementation of chordal conversion for sparse semidefinite programs with small treewidth. The accompanying theory gives $O(m+n)$ time per interior-point iteration under suitable sparsity assumptions; the implementation includes examples with up to one million variables.

**Paper:** Richard Y. Zhang, [*Complexity of chordal conversion for sparse semidefinite programs with small treewidth*](https://doi.org/10.1007/s10107-024-02137-5), *Mathematical Programming* **213** (2025), 201–237. [arXiv](https://arxiv.org/abs/2306.15288)

### [Dualized clique-tree conversion (CTC)](https://github.com/ryz-codes/dual_ctc)

MATLAB implementation of dualized clique-tree conversion for sparse SDPs, with SeDuMi/MOSEK interfaces and examples for MAXCUT and Lovász-theta problems. For the problem classes studied in the paper, the method achieves $O(n)$ time and memory per interior-point iteration.

**Paper:** Richard Y. Zhang and Javad Lavaei, [*Sparse semidefinite programs with guaranteed near-linear time complexity via dualized clique tree conversion*](https://doi.org/10.1007/s10107-020-01516-y), *Mathematical Programming* **188** (2021), 351–393. [arXiv](https://arxiv.org/abs/1710.03475)

### [Modified SeDuMi (MoDuMi)](https://github.com/ryz-codes/MoDuMi)

A modified version of **SeDuMi** for large, sparse, low-rank semidefinite programs. It replaces the dense interior-point Hessian solve with preconditioned conjugate gradients, exploiting the low-rank structure responsible for ill-conditioning.

**Paper:** Richard Y. Zhang and Javad Lavaei, [*Modified Interior-Point Method for Large-and-Sparse Low-Rank Semidefinite Programs*](https://doi.org/10.1109/CDC.2017.8264510), *IEEE Conference on Decision and Control (CDC)*, 2017. [arXiv](https://arxiv.org/abs/1703.10973)

### [FastMDMC](https://github.com/ryz-codes/fastmdmc)

MATLAB implementation of thresholding and maximum-determinant matrix completion for large-scale graphical lasso. When the thresholded covariance has sparse Cholesky structure, the max-det stage has linear time and memory complexity for fixed solution accuracy.

**Paper:** Richard Y. Zhang, Salar Fattahi, and Somayeh Sojoudi, [*Large-Scale Sparse Inverse Covariance Estimation via Thresholding and Max-Det Matrix Completion*](https://proceedings.mlr.press/v80/zhang18c.html), *ICML*, 2018. [arXiv](https://arxiv.org/abs/1802.04911)

## Computational electromagnetics and Precorrected FFT

### [FastLitz](https://github.com/ryz-codes/fastlitz)

Three-dimensional simulator for realistic litz-wire constructions. FastLitz resolves individual strands and twisting geometry to compute current-driven and externally induced copper losses, using pFFT to accelerate the electromagnetic interactions.

**Paper:** Richard Y. Zhang, Jacob K. White, and John G. Kassakian, [*Fast Simulation of Complicated 3-D Structures Above Lossy Magnetic Media*](https://doi.org/10.1109/TMAG.2014.2323933), *IEEE Transactions on Magnetics* **50**(10), 2014.

Richard Y. Zhang, Jacob K. White, John G. Kassakian, and Charles R. Sullivan, [*Realistic litz wire characterization using fast numerical simulations*](https://doi.org/10.1109/APEC.2014.6803390), *IEEE APEC*, 2014.

### [pFFT inductance / planar-media codes](https://github.com/ryz-codes/pfft-induct-m)

Earlier MATLAB codes for inductance and magnetoquasistatic integral-equation calculations using pFFT, including $1/r$ and Hankel-type kernels and serial/parallel $N$-dimensional examples.

### [pFFT-m](https://github.com/ryz-codes/pfft-m)

A general-purpose, dimension-independent MATLAB implementation of the **precorrected fast Fourier transform (pFFT)** for accelerating dense kernel matrix-vector products. It supports user-supplied Green's functions, general $N$-dimensional point sets, Toeplitz/Hankel-type kernels, and parallel/GPU execution.

This is the numerical engine underlying **FastLitz** and my earlier integral-equation work on structures above planar magnetic media.

**Related paper:** Richard Y. Zhang, Jacob K. White, and John G. Kassakian, [*Fast Simulation of Complicated 3-D Structures Above Lossy Magnetic Media*](https://doi.org/10.1109/TMAG.2014.2323933), *IEEE Transactions on Magnetics* **50**(10), 2014.

---

More about my research is available at [ryz.nz](https://ryz.nz/).
