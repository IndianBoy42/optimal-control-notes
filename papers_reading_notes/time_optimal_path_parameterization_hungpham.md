# Time Optimal Path Parameterization by Reachability Analysis

-Very elegant/explainable approach.

-Needs a specialized small scale solver for good performance
	- CVXPY is bad without DPP, TODO: reimplement in DPP
	- most solvers go for large scale problems, not many small problems
	- no parallelism available (except bwd and fwd pass simul)
	- [linprog2d](https://github.com/astoeckel/linprog2d) for linear programming
	- some systems are SOCP/SDP or full nonlinear (lin obj and nonlin constraints)

- some thoughts on tracking reachable from where:
	- paper assumes that the reachable set of t=n+1 is reachable from anywhere in the reachable/controllable set of t=n
	- for 'smooth' systems this feels true: unproven
	- but in general should we repropagate bwd to ensure the path is feasible/optimal
		- repropagate till fixed point sounds inefficient?
		- maybe some kind of graph search kind of thing
	- and if the assumption is correct do we need a full optimization problem?
	- why not just integrate from the upper and lower bounds?
		- TOPP using integration is a well studied solution, accuracy of integrator is a concern
	- 
	- all these apply to the backward (controllable) sets too

- paper says this kind of solver makes it more suitable for folding into the loop of a pathplanner
	- makes sense, maybe I should try implement.
	- Q: how hard is applying reachability/controllability to directly solve path planning
	- one way would use RA/CA to build the edges in a graph and then run graph search.
	- dynamically perform RA/CA to reduce memory, parallelize as much as possible.
	- collapse nodes for efficiency
	- or using RA/CA as part of something like RRT*

## Citations

implementation: https://github.com/hungpham2511/toppra

https://www.researchgate.net/publication/318671280_A_New_Approach_to_Time-Optimal_Path_Parameterization_Based_on_Reachability_Analysis

@article{article,
author = {Pham, Hung and Pham, Quang Cuong},
year = {2018},
month = {06},
pages = {645 - 659},
title = {A New Approach to Time-Optimal Path Parameterization Based on Reachability Analysis},
volume = {34},
journal = {IEEE Transactions on Robotics},
doi = {10.1109/TRO.2018.2819195}
}
