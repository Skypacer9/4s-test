https://bactra.org/weblog/918.html

A response to the novel Red Plenty - a novel of the socialist calculation debate
* Linear programming - how the Kantorovich character split between his idea, idealistic political musings
* We need a quantity to maximize - a function of  the quantities of all the different goods and services produced by teh economic system - objective is used in the sense of goal -> in Kantorovich's world this is a linear function
	* They don't have to be called values or prices but the planning exercise begins with them
	* In the Best Use of Economic Resources Kantorovich side steps this problem with a device that has the advantages of theft over honest toil
	* Planners have to decide on relative values, or fixed desired output and minimize resources required
	* We need complete and accurate knowledge of the physical constraints on the economy and resources available to it
	* Complete and accurate knowledge of the productive capacities of the economy and how it can convert inputs to outputs 
		* Disaggregating goods and services to the point where everything inside each category is substitutable 
		* If different parts of physical and organizational plant have technical capacities that needs to be taken into account 
			* The numbers in Leonitef's input output matrices are aggregated over huge swathes of the economy and too crude to be used for planning 
		* Shadow prices enforcing constraints - shows how much production could be increased if some pollution was allowed -> logic behind cap and trade institutions for controlling pollution 
		* Work in optimization theory - don't quite need complete and perfecctly accurate knowledge 
			* if knowledge is distorted by unbiased statistical error, we could settle for stochastic optimization (which runs the risk of being badly wrong if the nosie is large) -> or people could lie to planners
	* Nonlinear optimization is possible but rarely makes things easier 
	* Little point to reasoning abstractly about optima if you can't find them, and finding an optimum is a computational task - what's the method that will continue to deliver solutions even as the problem posed is varied?
* Computational complexity - concerns itself with understanding what resources algorithms require to work - these might be resources from memory to store intermediate results, s tatistical problems, communication between cooperative problem solvers. Time is  also a resource, measured in operations of the computer
* It establishes a measure of the size of an instance of a problem and asks how much time is required to produce a solution - several aspects of size, three natural ones for linear programming problems
	* 1. number of variables optimized over n
	* 2. number of constraints on the optimization - m
	* 3. amount of approximation we are willing to tolerate in a situation
* Optimizing many variables, subject to many constraints to a high degree of optimization is going to take more time than optimizing a few variables with a handful of constraints and a lot of slop
	* The fastest known algorithms for solving linear programming - interior point methods - useful for a wide class of problems (convex programming) - revolutionizing numerical optimization
		* Convex functions - these have nice global optima and efficient solutions (whereas in general numerical optimization you might only have a local minimum)
		* In convex programming - every local minimum is a global minimum, the feasible set is a convex set
		* For msot real world problems we can't solve for the optimum directly - we start from a guess and iteratively update (like gradient descent/newton's method - and challenges involve convergence speed, constraints, step sizes, local minima)
			* Convex sets - every straight line segment connecting any two points inside the blob lie inside the blob - no holes, indentations, missing interior
				* Discs, squares, triangles - convex
				* Donuts, crescent moon, star shaped polygon - non-convex
					* Linear transformations and affine mappings preserve convexity
					* The hyperplane, polyhedron etc are also convex
	  Truly intractable optimization problems - are ones where the steps needed grow exponentially (but linear and convex programming are in P while most common optimization problems are in NP)
	* Complexity grows super linearly - expanding the problem size by a factor of a thousand takes us 30 billion times as long 
	* A good modern commercial linear programming package can handle a problem with 12 or 13 million variables in a few minutes on a desktop machine -> to handle a problem with 12 or 13 billion variables would take 30 billion seconds (this paper is outdated)
	* In the USSR there were 12 million identifiably different products (from Alec Nove, the Economics of Feasible Socialism)
		* The problem of a production complex - if we don't index physical goods by location, plan won't account for transport  - goods which can spoil or are needed at a particular occasion also need to be indexed by time (look up how Walmart and Uber plan)
		* A thousand locations is very conservative
		* With 12 million kinds of goods and a thousand locations, to have the plan ready in less than a year would need computers 1000 times faster 
	* Setting prices instead of administering things or people doesn't give one a more tractable, less computationally complex problem 
		*  optimal prices turn out to have the same complexity as computing the optimal plan itself 
		* Maybe there is some shortcut to computing prices along but author doesn't know how yet
	* It won't do to say it's enough for planners to approximate the optimal plan - the computational complexity formula already allows for needing to come close to the optimum - complexity depends only very slowly, alogarithmically on the approximation to the optimum 
	* Maybe the formula is an upper bound, the time required to solve an arbitrary linear programming problem - maybe there's some special structure which can e exploited?
		* Most plausible candidate - look fro separable problems - where constraints create few connections among variables - if we could divide variables into two sets, can solve each sub problem much more quickly - the supra linear scaling applies within each problem
		* However - everything is connected to everything else - labour is required for all production and is in finite supply, creating coupling between all spheres of the economy
			* The national economy just doesn't break up into separate, non communicating spheres which can be optimized independently
			* If we pretended overall high dimensional economic planning problems could be split into many low dimensional problems, we could speed things up immensely by exploiting parallelism or distributed processing 
			* Then each processor is like a firm, which a scope dictated by information-processing power, and mismatches introduced by ignoring each other in their own optimization - like the anarachy of the market (these could look like other forms - stock market socialism, worker's coops)
			* Forcing the processor to take some account of what others are doing through prices and quantities removes some grosser pathologies (weak coupling)
			* But it won't provide enough of a communication channel to compute prices swiftly if we want one set of prices available to others 
				* Rob Axtell wrote a paper showing bilateral exchange come come within a certain range of an equilibrium set of prices in a time proportional to n^2log 1/e, much faster than any known centralized scheme -> but equilibrium reached in this way has strange, ill controlled properties
				* -> there are lower bounds on the complexity of optimization problems - no algorithms exist and no reason to think alt computing methods help (qcs don't provide a general exponential speedup)
				* We need to increase computation by a factor of 10^21?? 
	* Nonlinearity and nonconvexity
		* In linear programming, constraints facing the planner are linear - constant returns to scale
		* Mathematically- the linear constraints are a special c ase of convex constraints - not all convex constraints are linear 
			* economically this could allow decreasing returns to scale 
	* Unfortunately for planners, increasing returns to scale in production means non-convex constraints and increasing returns are common - if the plan calls for regular flights each flight has a fixed minimum cost no matter how much or little the plan carrier . For optimizatoin software you can't make copies of the program without first expending programmeres' labour and the computer time they need to write and debug code. 
	* There are other sources of increasing returns, beyond fixed costs. 
	* ==Allowing nonconvexity messes up the markets are always optimal theorem
	* Markets with non convex production are apt to see things like monopolies, monopolistic competition, path dependence, actual profits and power 
		* If planners just wanted to look at the profit (supposedly value added) of the whole economy, they set the prices of consumption goods, which turn shadow prices of inputs to production - the rule maximize the objective function does not help pick an objective function 
		* ==Planning a given assortment - making choices which express preferences/values-> there are values or preferences implicit in any choice of objective function==
		* The cognitive or computational problem is simply coming up with relative preferences or weights over all the goods in the economy, indexed by space and time- a human planner would have to make up most of these - to do so otherwise is beyond the bounds of humanity
	* ==The objective function in the plan is an expression of values or preferences, and people have different preferences
	* Institutions try to reconcile or adjust divergent values - this is a problem of SOCIAL CHOICE
		* one could imagine democratic debate/voting over plans - given sheer complexity of plans, hard to make up mind about competing plans or how they might be changed - every citizen is put in the position of the solitary planner - excpet they have to listen to one another
			* Citizens debate, vote over highly aggregated summaries of various plans
			* But then the planning apparatus has to fill in detials left unfixed 
			* Filling in these details is driven by values and preferences as making choices about the aggregated aspects
	* Dictatorship -can't come up with real preferences over everything in the economy than any other person
	* The collective dictatroship of the party gives the worst of both worlds
	* Second political problem - that the plan is perfectly implmented - that there is reason to think people won't be happy with the outcome - Monkey's Paw - need some way for citizens to provide feedback on the plan 
		* the market system is a way for providing feedback from users to producers 
		* Feedback doesn't have to be just or even through prices - inventories sometimes work as well
		* Maybe there is an alternative feedback mechanism which is as rich, adaptive, and easy to use as the market but is not the market?? (deliberative pltaforms??)
	* Both neoclassical and Austrian economics make a fetish of markets nad market prices - even under capitalism, immese areas are not coordinated through the market - organizations are the dominant form 
		* The conditions under which equilibrium prices are really all a decision maker needs to know and are sufficient for coordination are so extreme to be absurd - the market only lets people serve notice of their needs and relative strength up to a limit set by how much money they have  - careful economists talk about balancing supply and 'effective' demand, demand backed by money
		* Implicit choice of values -> values are not pretty - whims of the rich matter more than needs of the poor, keeping bond traders in strippers and cocaine than to feed hungry children - at the extreme markets starve people to death because feeding them is a 'less efficient' use of food than helping rich people e at moe
			* -> this isn't intrinsic to markets -? comes from market exchange and gross inequality?
			* We should ensure people have roughly comparable amounts of money to spend?
		* Turning over everything to a market isn't effective, always inefficient in healthcare nad information goods (beyond impossibility of informationally efficient prices)
			* Working through the market imposes its own costs - time and effort in searching out information about prices and qualities, negotiating deals 
	* Planning is possible in limited domains and these will expand as computing power grows - but only possible because making money gives firms an objective function which is both unambiguous and blinkered - planning for the whole economy would be intractable for the foreseeable future and deiciding on a plan runs into difficulties we have no idea how to solve 
	* The planning is not a viable alternative to capitalism should be disturbing

Calling the Tune for the Dance of Commodities
* There is a level at which Marx' nightmare vision is right: capitalism, the market system, whatever you want to call it, is a product of humanity, but each and every one of us confronts it as an autonomous and deeply alien force. Its ends are inhuman
* But human beings confront all the structures which emerge from our massed interactions this way - we have no choice but live among alien powers of our creations and try to direct them to human ends - it is beyond us to find a human measure intelligible to all chosen by all which says how everyone should go
	* Sometimes this might mean more market mechanisms, sometimes this means moving goods to public provision or other institutional ar rangements. 
	* Expanding the scope of democratic decision making - in firms, narrowing its scope - not allowing cnesorhip
	* Leaving tasks to experts, recognizeing claims to be mere assertions of authority, to be resisted or countered 

The conditions under which equilibrium prices really are all a decision-maker needs to know, and really are sufficient for coordination, are so extreme as to be absurd. ([Stiglitz is good on some of the failure modes](http://dx.doi.org/10.1162/003355300555015) [[PDF](https://www8.gsb.columbia.edu/faculty/jstiglitz/sites/jstiglitz/files/2000_Contributions_of_the_Economics_of_Information.pdf)].) Even if they hold, the market only lets people "serve notice of their needs and of their relative strength" up to a limit set by how much money they have. This is why careful economists talk about balancing supply and "effective" demand, demand backed by money.


Sequel [[The Impossible Takes A Little Longer]]

