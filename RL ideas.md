
AlphaZero and Leela Chess Zero
Uses a sophisticated mechanism that implicitly evaluates moves in a retrospective, counterfactual way - temporal difference learning (TD) combined with a value network
The agent asks : did this move lead to a better position than I thought I'd have
Value network - probability of winning from any given position
The agent then computes the TD error

Surprising Pivotal Move (Deep Sacrifice)- Monte Carlo Tree Search - it looks ahead, explores variations, often many moves deep - the agent finds a deep line where sacrifice leads to a crushing attack 10 moves later 
Search backs up the winning evaluation from that deep line to the position immediately after the sacrifice 
Policy vs value - policy is trained to maximize the expected future value - the pivotal move is one that maximizes the value of the resulting position after optimal play from both sides 

-> it doesn't brute force every possibility - it uses a clever four step loop to focus computational power on the most promising lines - start at the current position and traverse down the tree by picking the child node that maximizes a formula - you exploit known good moves, exploration bonus - occasionally check weird, surprising moves that havne't been tried much, descend until you hit a node you have not fully expanded
Expansion: Add one new child move to that node (a move that hasn't been explored yet)
Simulation: From this new node - play out the rest of the game extremely fast using a random or lightweight policy (in Alpha Zero, this step is replaced by neural network evaluation - no random play)
	low fidelity simulation
Backpropagation - take the result from the simulation and walk back up the tree to the root, updating the win % and visit count for every node along the path
After 100, 000+ loops, the move with the most visits at the root is chosen - the surprising sacrifice is discovered because the exploration bonus forces the algorithm to try it, backprop proves its worth

Policy Planning/Safety Teseting
Possible actions the AI could take 
Does the final outcome actually satisfy the true intent 
Simulation - fast, simplified world model
Try weird actions

This is already being explored with Anthropic's alignment faking experiments use search over possible model behaviours

In Policy - you don't have a reliable simulator - you have historical data, partial models, irreducible uncertainty - if you do build a simulation, then MCTS can be used as a decision support tool

--
Complexity of wishes
a1: If you try to manually specify what you want (write down every rule), you will fail
a2: What you want is algorithmically complex - takes many bits to specify
b1- b2: An AI's values come from some process, we want the process to land on our values
b3: we don't understand how to aim the values distribution towards something specific
c1-c2: without skillful intervention, a complex utility function is unlikely to appear by chance

* Supposedly large language models like gpt 4 understand human values surprisingly well even if they don't care about them
* The alignment part remains unsolved
* You need rankings over three or more options to even identify latent preference types - systems trying to aggregate needs have to collect rich preference data, acknowledge different groups have legitimately different values, avoiding forcing consensus where none exists
* Expressed preferences =/= True preferences - people's stated preferences are influenced by social pressure, lack of information, incoherence, change over  time 

1. Read the Hidden Complexity of Wishes essay
2. The Value Learning sequence on the AI alignment forum

---
3. **"Direct Preference Optimization With Unobserved Preference Heterogeneity"** (Chidambaram et al., AISTATS 2026)[](https://virtual.aistats.org/virtual/2026/poster/13837) — Shows mathematically why binary comparisons fail to capture diverse preferences and proposes methods for handling heterogeneous human values.
    
4. **"Distortion of AI Alignment: Does Preference Optimization Optimize for Preferences?"** (Gölz et al., 2025)[](https://www.semanticscholar.org/paper/Distortion-of-AI-Alignment%3A-Does-Preference-for-G%C3%B6lz-Haghtalab/68d3f73f48805bdcef68d45cf4401dea6bac7f42) — Draws on social choice theory to measure how much preference optimization "distorts" what people actually want.
    
5. **PRISM Framework** (Boratto et al., RecSys 2025)[](https://www.ludovicoboratto.com/prism-from-individual-preferences-to-group-consensus-through-conversational-ai-mediated-and-visual-explanations/#content) — A practical system for group decision-making that separates private preference elicitation from shared negotiation, reducing social pressure and making trade-offs legible.
    
6. **"Beyond Predictions: A Participatory Framework for Multi-Stakeholder Decision-Making"** (Vineis et al., arXiv 2025)[](https://arxiv.org/html/2502.08542v2#S2) — Proposes reward-based learning with multiple actors, bridging game theory, welfare economics, and computational social choice.
--
7. **Košice's SAM-SUD project** (European Urban Initiative)[](https://www.urban-initiative.eu/ia-cities/kosice/home) — A real-world example of what you're describing: an AI recommendation tool + digital twin platform + participatory planning. Citizens interact with 3D models of buildings and visualize transformation scenarios before decisions are made.
    
8. **Studio Bhooshan's "Make No Little Plans"** (AADRL)[](https://drl.aaschool.ac.uk/sb-make-no-little-plans) — Uses reinforcement learning and game theory to find "win-win" equilibria between institutional stewardship and economic growth, generating urban morphology through negotiated algorithmic equilibrium rather than rigid master planning.

* less optimization might be better - the robust approach invovles: 
- **Multi-objective frameworks** that keep different stakeholders' reward functions separate
    
- **Min-max regret criteria** that optimize for the worst-case across preference types
    
- **Conversational elicitation** that iteratively refines understanding