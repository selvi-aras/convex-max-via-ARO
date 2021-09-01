# convex-max-via-ARO
Data and codes of the paper _Convex Maximization via Adjustable Robust Optimization_ by _Aras Selvi, Aharon Ben-Tal, Ruud Brekelmans, and Dick den Hertog (2021)_.

The preprint (version of 1 September 2021) is available on [Optimization Online](http://www.optimization-online.org/DB_FILE/2020/07/7881.pdf). The paper is presented at [Robust Optimization Webinars](https://youtu.be/GEGUlTXfVX0) and [Imperial-LBS-UCL Brown Bag Seminar](https://sites.google.com/view/phdmsorseminars/).
Aras received the [2021 ICS Best Student Paper Award](https://connect.informs.org/computing/awards/ics-student-paper-award) with this paper.

## Introduction
This repository provides the following:
- Example scripts that generate the random data explained in Appendix G of the paper
- The **exact** problem data that is used in the numerical experiments (Section 4) of the paper
- The scripts that implement upper and lower bound approximation algorithms of convex maximization problems
- The **exact** upper and lower bound values found, and the solutions of the upper and lower bound problems

## Dependencies
**MATLAB** - We use MATLAB 2018b to run the scripts. The scripts are compatible with the [latest release](https://uk.mathworks.com/downloads/) 2021a of MATLAB.

**YALMIP** - We use [YALMIP](https://yalmip.github.io/download/) to call optimization solvers. The code is compatible with the [latest release](https://github.com/yalmip/YALMIP/releases/tag/R20210331) (as of 1 September 2021) R20210331 of YALMIP. As a minimum requirement, YALMIP R20181012 is required (for the support of exponential cone modeling). 

**MOSEK** -  Version >= 9.0 is required for exponential cone optimization purposes. The code is compatible with the [latest release](https://www.mosek.com/documentation/) (as of 1 September 2021) 

**CPLEX** - Version >= 12.6 is required to solve nonconvex quadratic problems (for benchmark purposes). The code is compatible with [version 12.10](https://www.ibm.com/support/pages/downloading-ibm-ilog-cplex-optimization-studio-v12100). Note that the most recent version (as of 1 September 2021) 20.1 does not come with a MATLAB connector with anymore. 

**GUROBI** - Version >= 9.0 is used, and the code is compatible with the [latest release 9.1](https://www.gurobi.com/) (as of 1 September 2021). We use GUROBI to solve mixed integer linear optimization problems.

Moreover, although our upper/lower bound approximation algorithms only use the solvers mentioned above, we also compared our solutions with the solutions obtained by directly solving the original convex maximization problem with various solvers such as [BARON](https://minlp.com/download), [Artelys KNITRO](https://www.artelys.com/solvers/knitro/), [COIN-OR IPOPT](https://coin-or.github.io/Ipopt/), and [BMIBNB](https://yalmip.github.io/solver/bmibnb/). Please reach out to me (a.selvi19@imperial.ac.uk) for any question about using these solvers for global optimization.

## Description


## Final Notes
The following scripts are also available upon request:
- Implementation of an algorithm to solve the upper bound problem, i.e., [The Adversarial Approach](https://www.sciencedirect.com/science/article/pii/S1572528607000382), which is useful when the perspective function is hard to optimize in the UB problem
- Implementation of the [FME algorithm to eliminate the adjustable variables](https://pubsonline.informs.org/doi/abs/10.1287/opre.2017.1714) in the equivalent ARO problem of the convex maximization problem
- The global optimization benchmark scripts (i.e., using global optimization solvers to attempt solving the convex maximization problem directly)
- A branch and bound algorithm where convex maximization over a polyhedron is consecutively being split into smaller regions and our upper/lower bound approximations are applied on each split
- Vertex enumeration in small polyhedra to find the global optimal values
- 
## Thank You
Thank you for your interest in our work. If you found this work useful in your research and/or applications, please star this repository and cite:
```
@article{selvi2020convex,
  title={Convex maximization via adjustable robust optimization},
  author={Selvi, Aras and Ben-Tal, Aharon and Brekelmans, Ruud and den Hertog, Dick},
  journal={Available on Optimization Online},
  year={2020}
}
```
Please contact Aras (a.selvi19@imperial.ac.uk) if you encounter any issues using the scripts. For any other comment or question, please do not hesitate to contact us:

[Aras Selvi](https://www.imperial.ac.uk/people/a.selvi19) _(a.selvi19@imperial.ac.uk)_

[Aharon Ben-Tal](https://web.iem.technion.ac.il/site/academicstaff/aharon-ben-tal/) _(abental@technion.ac.il)_

[Ruud Brekelmans](https://www.tilburguniversity.edu/staff/r-c-m-brekelmans) _(r.c.m.brekelmans@tilburguniversity.edu)_

[Dick den Hertog](https://www.uva.nl/en/profile/h/e/d.denhertog/d.den-hertog.html) _(d.denhertog@uva.nl)_
