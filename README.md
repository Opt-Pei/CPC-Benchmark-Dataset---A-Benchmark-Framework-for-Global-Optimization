# CPC-Benchmark Dataset

**CPC (Challenging Problems for Computation)** is a benchmark dataset providing a collection of challenging optimization problems for benchmarking global optimization algorithms in relatively low-dimensional spaces.

## Authors

- Peicong Cheng*, Institute of Science Tokyo.  
	Email: cheng.p.b2bf@m.isct.ac.jp
	
- Makoto Yamashita, Institute of Science Tokyo, Professor.  
	Email: Makoto.Yamashita@c.titech.ac.jp  
	Home Page Link:http://www.opt.c.titech.ac.jp/yamashita/

*: Corresponding author

## License

The CPC benchmark is licensed under **CC BY 4.0**. Users are free to use, modify, and distribute the benchmark, including for commercial purposes, **provided that the original paper is properly cited**:

The CPC Framework is currently under development.
If you use this benchmark set, please cite it as:

Peicong Cheng, Makoto Yamashita, “CPC Benchmark Dataset – A Benchmark Dataset for Global Optimization”, August 2025, GitHub Repository: github.com/Opt-Pei/CPC-framework.

A formal citation will be provided upon publication.

## Description

This repository contains the implementation of the CPC benchmark, initially introduced with 25 discontinuous and nonlinear function minimization problems. These problems are designed to test algorithmic performance under conditions of discontinuity, nonlinearity, and sensitivity to numerical precision. Detailed descriptions of each function can be found in the overview PDF file located in the corresponding problem folder.

Update: 38 nonlinear curve fitting problems have been published. 

To further facilitate practical use, we also provide general-purpose implmentation codes. These include:

**General-purpose computation scripts**, including reference implementations of well-known algorithms and professional software templates.

Genetic Algorithm (GA) - MATLAB

Simulated Annealing (SA) - MATLAB

A quasi-Newton method proposed by Broyden, Fletcher, Goldfarb, and Shanno (BFGS) + Multi-Start (MS) - MATLAB

Gradient-based Particle Swarm Optimization Algorithm (GPSO) - MATLAB + PlatEMO

Branch & Bound - LINGO

Universial Global Optimization - 1stOpt

These can be used as starting points for running multiple benchmark problems. However, there might be better ways to solve the same problems depending on the chosen method and software platform. The implementations provided here are intended only as references, users are encouraged to adapt or improve them according to their specific requirements.

These template scripts can be found in "General-purpose computation scripts" folder

**Problem-specific scripts**, provided in the corresponding folders of each benchmark problem, which directly implement the formulation and computation of that specific problem.

Problem-specific script for each problem can be found in folder such as "01-CPC-DF1", "11-CPC-DF11". 

**General function code**, written in a platform-independent form, so that users working with other optimization platforms can easily adapt the problems to their own environments.

Future extensions of CPC will include additional discontinuous and nonlinear minimization problems, as well as other categories such as equation solving, curve fitting, and black-box optimization. Each problem includes detailed data and the currently known best solutions to facilitate systematic evaluation and fair comparison of optimization algorithms.

Moreover, the benchmark problems presented in this framework were formulated with the support of several professional mathematical optimization tools, including MATLAB, LINGO, etc.

While these tools played an important role in problem construction and validation, all reported global optima were ultimately obtained using 1stOpt, whose capabilities in nonlinear global optimzation proved particularly effective across the entire benchmark set.

We gratefully acknowledge the contributions of all software platforms involved in this process, and the relevant links are as follow. 

Relevant links:

1stOpt: http://www.7d-soft.com/en/

MATLAB: https://www.mathworks.com/products/matlab.html

LINGO: https://www.lindo.com/

PlatEMO: https://github.com/BIMK/PlatEMO

## Usage Suggestions

For problems with very low feasible ratios (where finding an initial feasible solution is particularly difficult), a practical approach is to apply a Monte Carlo method to obtain at least one feasibnle solution before executing algorithm. This can significiantly improve the success rate and stability of subsequent optimization runs.




