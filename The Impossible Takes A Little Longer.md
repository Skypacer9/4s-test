https://bactra.org/weblog/919.html

* Kantorovich style planning is possible when planners can be given good data, an unambiguous objective function, a problem of sufficiently limited schope - however what counts as sufficiently limited grows as computing power does - difficulties are about scale, not principle
* There are other forms of control which aren't this form of mathematical programming and have lower computational complexity - central banks are planning bodies which set certain prices 
* Intervening in existing market institutions, capitalist firms, creating non market institutions - these aren't subject to the same Kantorovich planning
* Advocating for social democracy/market socialism?
* Thirty years deliberately dismantling safeguards out of ideology and greed is folly
* 401ks have been a failure but going back to defined benefit plans which presume long term employment by a single stable firm is also a non starter  - inequalities in public educatioon are obscene - but even if we swept away obstacles like local and state school boards, what is a better system? 
* Is coming up with a viable instituion to strength workers' bargaining power st raightforward? there has been a concerted, dubiously legal effort to crush unions and the labour movement 
* Profit not the only unambiguous objective fucntion? And firms and other centres of power and planning brought under more democratic control -> democratic control by workers in an enterprise and people at large 
* How is token distribution, with tokens exchanged for goods and services, not a market?
* Decentralized planning sounds nice - but those plans have to be coordinated
	* bilateral or multilateral mutual adjustment have features of markets??
* Cockshott - Shazali disagrees with the claim the central planning is tractable
	* The linear programming problem - through language multipliers, the constrained maximization is equivalent to another form of unconstrained maximization - where the vector   contains the Lagrange multipliers, a.k.a. shadow prices, a.k.a. objectively determined valuations, for each of the constraints
	* Talking about solving the planning problem - complexity of this linear programming problem and allowing it to be solved up to a certain accuracy 
	* Since the cmoputational complexity of doing so only grow proportionally to log 1/e. If we can do this we can ask for good approximations. If some other part of the problem demands a lot of resources, we have to make slop e literally exponentially alrger to make up for it
	* What about satisficing? But still how would we come up with the value vector v
		* Shazali couldn't find literature on the complexity of linear satisfying but suspsects it is no better than that of approximate linear programming since you can sue the former as a sub routine to the do the latter - each satisficing plan is a st arting point of the next ratchett
		* Cockshott's Towards a New Socialism - is about solving a simple system of lienar equations 
			* iterative algorithms for solving sparse systems of linear equations with this complexity have been known since the 19th century 
			* Vector of residuals is used to adjust the initial guess to some x1 which would be closer to the solutoin -> a variation of Jacobi's algorithm
		* For Cockshotts' algorithm or any other linear equation solver, need to presume we have 
		* 1. settled on how much of every good and service we want the economy to produce, including indexing by time and space
		* 2. we have for e ach good in the economy, exactly one way to produce every good in the eocnomy or someone settled on one way per good
		* 3. every good in the ecoomy is produced by combining inputs in fixed, known proportions with no possibility of substitutions, alternative methods, increasing/decreasing returns 
		* 4. Do not need to chek whether we actually have sufficient resources to achieve the desired level of output with the given technology
	* Can't just replace linear programming with a system of linear equations
		* not that hard to add up all the resources the plan calls for once one has the plan
	* Parallelism - important and it's what you can do with a modern supercomputer vs a desktop, more than raw clock speeds - to get real speed up, your constraint matrix needs not to just be sparse, but specially structured - no particular plasubility for economic problems??
		* - **Structured sparse** (e.g., tridiagonal) → you can use very fast, simple, O(n) algorithms (Thomas algorithm, etc.).
		* If your matrix is sparse but unstructured - can try to partition the graph into a weakly coupled subgraphs 
	* Stafford Beer and Allende's Chile 
	* Innovation - economies of the capitalist core have been good at developing and applying new technologies. Governments have been intimately involved in every step (GPS), demanding specialised products with no comemrcial need with huge spillovers (microelectronics). If all resources are efficiently devoted to meeting current needs, there's no slack going to the development of new things 
	* Post scarcity - need some constraints or the optimum will be produce infinitity of everything - some constraints have to bite to keep the solution from going off to infinity which means non-zero prices for some things - replacing this objective function with one which allows for satiation - over the five year plan, you can only ==eat, drink, drive, wear, so many things. If the objective function can be satiated within the constraints of available resources and technologies, then shadow prices go to zero - there would be an allocation problem, that of assigning resources to prodcution processes to make sure enough was made to satiate demand 
	* ==This vision seems to presume complete automation to the point of AI or being able to count on volunteered human labour
* The non-market signals - many ways of getting feedback from consumers to producers about what to make and how, beyond the market mechanisms - peculiarities of online information goods - marginal cost is near zero - how many copies of a document is therefore - as many as people want - the question is - what should people pay attention to - and there non market signals about what other people have found worthwhile is helpful
* Does this close the loop - getting us more of what people value and less of what they don't? People liek receiving attention and will respond to it, but can't be eaten and producing content is costly - resources to support production have to come to somewhere
* People need to have reasons to respond to feedback signals and capacity to do so
* Capitalist solution - intellectual property -abandoning free markets and economic efficiency - but we could accept amatueirsm - producing goods in time left from free jobs, patronage (distribution from many patrons), creating jobs where some production is part of normal duties even if the output isn't sold (science)
    
- **Unstructured sparse** → you need general sparse solvers (e.g., sparse LU, iterative methods like CG/GMRES with preconditioners), and memory access patterns are irregular (poor cache locality).
--
For an **undirected graph** with nn vertices:

- **Adjacency matrix AA** is n×nn×n, symmetric.
    
- Aij=1Aij​=1 if there is an edge between vertex ii and jj, else 00.
    
- The graph is **weakly-coupled** if edges between sub-graphs are few (low "cut size").
    

A **partition** divides vertices into kk disjoint subsets V1,V2,…,VkV1​,V2​,…,Vk​.

--
different kinds of partitioning, for example using spectral methods

In other words:

> **Unstructured sparse matrices are harder to optimize for hardware** because you cannot predict where the non-zeros will be, unlike a banded or block-structured matrix.