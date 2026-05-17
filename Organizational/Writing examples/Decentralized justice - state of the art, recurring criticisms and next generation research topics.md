
Abeer Sharma (HKU) is part of this, he sent me this as an example of an interdisciplinary paper that's more like a research agenda (straddling 4 disciplines)
(law, philosophy, computer science, game theory & mechanism design, business and markets)

Decentralized justice is a novel approach to online dispute resolution based on blockchain, crowdsourcing, game theory for adjudicating claims in a neutral and efficient way. Since the launch of the first decentralized justice platform in 2018, the field has attracted wide interest from practitioners and academics in web3 and dispute resolution - this concept is based on ideas of decentralization, economic incentives, and a claim to fairness in its decisions.
	There are a number of technical, market, legal, and ethical challenges.
The paper provides a review of the history of decentralized justice, addresses a number of recurrent topics and lays down a path for further exploration

==^ so this paper only does a part of what our 4s abstract proposes lol (it's more a review paper whereas our paper suggests it will undertake 1. novel case studies 2.even start creating design principles)==

Intro:
-> brief contextualisation of economic circumstances and how that's been changed by economics
-> introduces the focus on disputes - those taking place in online communities involving anonymous/pseudonymous agents hailing from different legal jurisdictions (there's kind of a business case here)
-> showing how the old framework and the context in which it was derived (the multi million dollar disputes involving conglomerates and governments for which the framework of the New York Convention was established in 1958)
	the New York Convention was a 1958 international treaty that facilitates the enforcement of arbitration agreements and arbitral awards across borders - core purpose is to ensure that private dispute resolution through arbitration - rather than litigation in national courts - is respected globally - requires courts of signatory countries to recognize written arbitration agreements and stay court proceedings when a valid arbitration clause exists - obliges national courts to enforce foreign arbitral awards with limited exceptions (public policy, lack of due process) - a reliable, enforceable option for international commercial disputes - reducing the risk that a winning party can't collect on an award simply because the losing party's assets are in another country
	Legal harmonization - the process of making laws, regulations, legal standards more consistent across different jurisdictions - this means aligning core principles, procedures to reduce contradictions and frictions when legal systems interact -> harmonization can happen top down (binding treaties/directives) or bottom up (soft law, model laws, or market driven convergence) processes
	 Before the convention -each country had its own rules for recognizing foreign arbitration awards -of ten required relitigating  - courts in 170 countries apply the same legal test when deciding whether to enforce a foreign arbitral award
	 Traditional litigatoin; resolving disputes through the court system (judges, lawyers, trials) - Russell and Susskind proposed reforms to make this process faster or cheaper, often by using technology
	 E-commerce/ADR - Online shopping platforms and alternative dispute resolution have also generate proposals - it exists to avoid court but the focus is on using ML to automate tasks like predicting case outcomes, sorting evidence, recommending settlements

Article set up: Review early theoretical research and empirical experience in the field of decentralized justice and will study applicable challenges, objections, recurring criticisms - it will also propose new avenues to explore to further develop this nascent field

^ so in our case are we developing a field? or more of a philosophy, or a case for changing some sets of designs/phenomena?

Section 2: unravels the mechanics of decentralized justice systems, spotlighting Kleros as a representative case study

Section 3: Navigates the technical challenges in designing these systems so that they are robust and resistant to effects such as bribery and collusion

Section 4: Delves into the market challenges, identifying use cases where these systems can solve business problems efficiently and fairly

Section 5: Legal and public policy challenges, examining issues from jurisdiction to enforcement of awards

Section  6: Grapples with moral challenges, exploring the friction between these systems and traditional understandings of fairness

Section 7: concludes the paper, reflecting on the potential decentralized justice system amidst the significant challenges they must surmount and suggesting potential research for further research in the fields of social science like law, economics, social science theory

THeir 'case study' - Kleros - a reflection of the practical realities of the decentralized justice system - it has a completed caseload exceeding 1500 disputes while other protocols have not been able to pull off anything close.

-> Justification of this choice of case study

As it is the most active platform, the insights derived from this examination will be valuable for the broader field as they provide a basis for understanding and anticipating the evolution of other emerging decentralized justice platforms -> and can generate perspectives on development and future trajectories of these defunct decentralized platforms (Aragon and Jur)

2. Smart contracts can't resolve all disputes - they cannot evaluate whether the delivered video complies with agreed aesthetic and functional specifications - contracts are considered incomplete in that they cannot foresee all of the potential for disagreement


Figure 1 contains a summary of how the dispute resolution flow works in the Kleros Protocol. Suppose Alice and Bob use a Kleros-connected smart contract. Alice sends cryptocurrency to the contract, held in escrow until Bob fulfills the contract. If a dispute arises, funds remain locked while crowdsourced jurors resolve it. Any Ethereum user can be a juror by depositing Pinakion (PNK) tokens into Kleros courts, which is essentially a platform that serves as a meeting point for jurors and disputing parties, and allows the creation of subcourts wherein disputes of a similar nature may be grouped together (Ober et al., 2019).

Jurors are randomly chosen, with selection likelihood proportional to staked PNK (but how do they get PNK). No demonstrated expertise or identity proof is required. Jurors review evidence and vote for the party they believe is right, incentivized to align with the majority
	-> what are the downsides of incentivizing convergence (perhaps prematurely) or  the Schelling point approach
Carrot and stick approach is used - if the vote is unanimous, then all jurors receive arbitration fees, if it is a split decision, dissenting jurors are not paid arbitration fees and lose their staked PNK, which is given to majority jurors along with arbitration fees
A key premise in decentralized justice is that jurors who vote consistently with the majority experience on average a financial gain
Decentralized justice as a dispute resolution system possessing three fundamental characteristics
a) DAO structure
b) mechanism design based on cryptoeconomics
c) generating a perception of fairness 

2.1 DAO structure
-> being built as a DAO architecture ensures that the dispute resolution process will be conducted exactly as programmed 
Governance rights are directly in the hands of the community and decision making is member led like a cooperative or direct democracy government
Evidence production, jury selection, other elements of the procedure are tamper proof ->system can provide credible neutrality 
(easier enforcement - but when do ambiguities and flexibility become necessary)

2.2 Cryptoeconomics based mechanism design

* A paradigm that studies and builds decentralized systems running on incentive mechanisms
* Unlike traditional dispute resolution systems, decentralized justice does not rely on expectations of moral behaviour of agents but on strict economic incentives
* Agents in a decentralized justice system vote on outcomes and depending on how they vote a collective outcome is determined and the agents are provided with financial rewards or penalties - voting - any mechanism by which agents provide information on the outcomes of the dispute that they find more or less appropriate - voting can take a number of forms - agents could choose between two possible outcomes, providing a ranking of a finite list of possible outcomes, or they could score each of several outcomes independently on a 1-10 scale
- Voting system - a function that takes as inputs the agents' votes and outputs a collective decision
- Payoff system - a function that takes as inputs the agents' votes and outputs an amount that each agent is rewarded or penalized

-> agents are not expected to act honestly (be neutral in their decisions) because of moral reasons (the case in traditional dispute resolution systems) but because these elements are chosen so that it is in their rational interest of agents to act in order to optimize economic gain
-> Schelling point - within the context of a dispute resolution mechanism that relies on game theoretic incentives - agents are likely to produce an outcome that is most commonly labeled as 'fair' while seeking their private economic interests based on their prediction of other agents' behaviour without any assumptions of ethical propriety on the part of any agent
Users that behave honestly and ethically will on average be rewarded by the payoff system whereas users that behave dishonestly/unethically will be penalized economically
	-> in this way, the cryptoeconomic based mechanism design of a decnetralized justice system ensures trustlessness - no agent is required to put faith in the honesty or reliability of any other agent in order for the system to work effectively

* In order to be considered legitimate, any court system must produce decisions that can be considered 'fair' by disputants and outside observers 
^ here the review just directs the reader to more extensive reviews of 'fairness' if it is of interest
	^ notes that Kleros is 'fair' in accordance with formal models of defining fairness such as Daniel Dimov's model of procedural fairness
	^ the review paper refers to another review paper on four types of challenges to gain adoption - technical, market, legal, moral

Then the paper conducts a thorough review of the literature addressing the different challenges posed to the growth of decentralized justice, recurrent criticisms, paths for research 
	-> there is an explanation of the choice of literature 
	(base on the level of tangible development achieved within the decentralized ecosystem)
	(although there are many proposed projects and hypothesized solutions, few of them have actually materialized in a successful mechanism with significant adoption)

3. Technical challenges

* Several blockchain oracles have include mechanisms based on incentivizing participants to generate a consensus outcome favoured by the majority
	* examples include Augur and UMA, some mechanisms for reducing vulnerability to manipulation like a data verification mechanism - design to reflect reflect world market values - optimizing efficiency 
	* Augur - a decentralized prediction market - participants stake this on various outcomes of real world events
* Kleros goes beyond market-oriented data -> decentralized justice systems tend to present a generalized infrastructure that accommodates a broader spectrum of subject matter and tends to facilitate coordinated decisions over more nuanced questions
* The infrastructure has to be secure and attack resistant without requiring central intervention
	* ^ back to how do certain technologies privilege certain political modes?
	* No final decision maker or trusted party capable of imposing out of game penalties on abusive participants or screening participants who have a vested interest in the cases under consideration - defenses to attack need to be built into the design of the system - broad categories of attack include the corruption of voters and obtaining of disproportionate voting weight by a subset of voters
	^ okay so voting design is included here
	* Corruption of voters include malicious behaviour such as paying bribes
* ^ reference to economic literature considering the dynamics of bribing in various microeconomic models
* ^ reference to a type of attack called the p+epsilon attack which targets Schelling Point based systems - the attacker offers a bribe to participants if they vote for a malicious outcome contingent on said malicious outcome losing the vote- and design and parameter choices that have an impact on the viability of such p+epsilon attacks
* Limitations on identity systems in blockchain - there is generally no reliable way to ensure that all jurors in a decentralized justice platform are distinct, identifiable individuals
	* lots of platforms involving voting accept it is possible for individuals to obtain multiple votes but seek to make it costly to obtain additional votes - creation of a blockchain native identity sytem -> individuals should only be allowed to register on a list once, and duplicate registrations can be challenged and judged by a subjective oracle
	* Soulbound Tokens - non trasnferable tokens that can be used to represent "social" attributes of users -> individuals can submit themselves to lists reserved for participants that have some qualification or certain type of expertise
* ^ Future directions for research noted - how resistance varies over longer time scales or when considering juror pools of varying backgrounds and sizes
3.2 Incentivizing participants
^ choice of payoff structure can draw ideas from the field of peer prediction - a field that considers how payoff functions that depend on how a given participant's vote compares to that of other participants can be used to incentivize participants to exert effort in performing tasks 
-> the choice of voting system can draw ideas from the field of social choice theory - a field that has studied the degree to which voting systems can be designed that satisfy various desirable properties
-> payoff functions should disincentivize lazy strategies like voting randomly or voting in a way that does not consider information from individual cases 
^ not necessarily easy to directly apply existing systems from the peer prediction and social choice theory literature
* the bribes that an attacker will need to pay rational participants to influence their votes will depend on the costs that the payoff structure imposes on participants who accept bribes, while how many votes need to be  corrupted in order for the attacker to change the outcome depends on how the votes are aggregated -> the resistance of a decentralized justice system depends on interactions between payoff and voting systems
	* Resistance to attacks that obtain disproportionate voting weight is attained to the degree that it is expensive to obtain enough votes to alter the results of a case - many peer prediction models have requirements that voters do not collude in order to function properly
* ^ another research approach is brought up - adapting results in the existing peer prediction literature, relaxing assumptions of participant behaviour
* Dispute situations often require neutral decision makers to decide between several nuanced possible outcomes in non-binary decisions - research in social choice theory has shown that under minimal hypotheses, voting systems that decide between three or more outcomes lead to pathological phenomena in some rare circumstances

3.3 Appropriately managing information

* Managing the flow of information in a decentralized justice system - it is challenging to handle private information on blockchain as enough information about each transaction must be known by miners and other nodes for them to validate the transaction
* How to avoid voting records of arbitrators becoming public and t hreatening their privacy
* Commit and reveal schemes allow for votes to remain hidden during a voting round to avoid influencing arbitrators who have not yet voted - these schemes require that votes be revealed during a subsequent step to have the results calculated
* Question asked? What voting/incentive systems would be well adapted to the requirements of decentralized justice? how might one develop on recent research in peer prediction towards designing mechanisms that have incentive compatibility properties even when one can only take assumptions on participant behaviour that are realistic in t he setting of decentralized justice, such as by assuming limits on participant collusion rather than its absence - paralleling work in social choice theory, what further properties are relevant for voting aggregation mechanisms in decentralized justice and what tradeoffs one must make between potentially conflicting desirable properties
* Zero knowledge proof protocols appropriate to better manage the flow of information in decentralized justice protocols - how to most efficiently obfuscate the link between how an arbitrator votes and rewards or penalties received so that arbitrator's voting records cannot be reconstructed based on on-chain information
^ proposla of more concrete mechanisms

4. Market challenges
A number of challenges arise regarding use cases, business models, and its future evolution

4.1. Use case taxonomy
* A lot of applications for decentralized justice including the field of intellectual property disputes, translation freelancing, production traceability, leasing contracts, online marketplaces, crowdfunded financing, online gaming, real world asset tokenization, decentralized finance compliance, social media moderation, insurance, DAO governance, prediction markets, metaverse and others
* It has also been suggested as a way to protect basis property rights
* Industry participants organized use cases into three main categories: escrow (a financial arrangement where a neutral third party holds and regulates payment of funds or assets on behalf of two other parties involved in a transaction - the ecrow agent releases the funds or assets only when all the terms of the agreement are met, curation, oracle - escrow use cases are typical in insurance claims, freelance work, bounty payments
* curation use cases - all those where the goal of the mechanism is to verify the compliance of some item with a number of critieria to be accepted into a list - token curated acceptance 
	* wide range of applications including cryptoasset compliance, online identity, NFT certification
	* Oracle use cases - disputed claim of a factual nature - like the number of COVID deaths in the US
* It can be argued that all of the decentralized justice industry falls within the subjective oracle category as questions asked to jurors act as an oracle for that specific question
* Categorizing use cases of decentralized justice - focusing on functionality - decentralized justice systems could be categorized in optimistic mechanisms (a curation type case where a claim is considered true after a period without being challenged), price discovery, assets custody, sybil resistance - decentralized justice can be categorized as a governance mechanism (supreme court as a service, content moderation), finance infrastructure (decentralized finance, insurance, real world asset curation), e commerce infrastructure (price discovery, escrow), decentralized implementation of bounties for remote workers
* ^ Another research direction suggested - taxonomizing the decentralized justice ecosystem

4.2 Industry structure and evolution -
* Although the online dispute resolution industry has been around for decades, most initial platforms failed to achieve success - explained by the failure to introduce a significant change over traditional methods for alternative dispute resolution - most parties met over the internet instead of a hearing room
* A core component of the digital revolution is the ability to enable new ways of organizing human effort based on collective intelligence and labor on demand
* Decentralized justice - combines crowdsourcing into dispute resolution with a  DAO architecture - enjoying an exponential improvement in resolution speed and cost while it enjoyed credible neutrality guarantees for earning the trust of parties
	* ==incremental vs disruptive innovation
* some kind of network effect - as more cases come into the system, the higher the incentive for jurors to join the network (profit by providing adjudication services) - and a higher amount and variety of jurors increases the quality, speed, cost of arbitration
* being built on blockchain means that decentralized justice systems can operate globally through jurisdictional boundaries thus accommodating the global nature of many economic activities

4.3 Inclusion in traditional dispute resolution systems
* Commonly framed as a contrast to traditional systems - represented as a replacement for traditional systems. On a more moderated note, they may be discussed in the context of existing side by side with conventional centralized mechanisms each addressing a different subset of use cases 
	* Or have decentralized justice systems partially merged into traditional dispute resolution mechanisms to bolster the effectiveness of the latter
* A substantial number of legal disputes center around inherently subjective concepts and interpretations that do not have a reliable gauge for reference - several contracts use terms that are subjective by design - like 'reasonable' wear and tear, 'adequate' quality - laying down comprehensive rules to cover every potential circumstance is impossible - the flexibility also causes a significant number of disputes 
* Decentralized justice systems serve as better reference points for interpretation - the judge/arbitrator would need to refer the interpretation of specific subjective terms to a decentralized jury in order to arrive at the most appropriate likely understanding of the term - harnessing the wisdom of the crowd - but these instruments are susceptible to manipulation by disputing parties with a vested interest
* A decentralized jury of appropriate critical mass might be able to capture consumer sentiments in a faster, cheaper more accurate manner -> determining a fair price or evaluating whether all steps taken by a party are reasonable
	* -> replacing surveys or other costly legal tools during the negotiation/pre dispute stage
	* legal analytics seeks to draw insights from data in order to help lawyers make better informed decisions to build their legal strategies 
	^another research idea -> opportunities for the use of decentralized justice systems as a fact finding or heuristic device to provide decision support to centralized tribunals, legal firms, support in mediation processes

4.4 Interactions with other dispute resolution technologies:
* acceleration in the interest of the use of technology in dispute resolution - new machine learning techniques combined with massive availability of data to train models promise great transformations in ODR systems
* Possibility of using AI to build robo lawyers
* Automation is unlikely to resolve a wide number of cases - those where the ability to understand the context, intentionality and emotions of agents is important Whenever a party appeals a ruling made by an automated method, likely to trigger a new decision making round with humans involved to ensure diverse approaches to the problem -> automation might not be socially acceptable

4.5. More research directions generated for market direction
^ research needed to better understand the taxonomy of decentralized justice use cases, topology of decentralized justice networks, opportunities for application of decentralized justice as a component of broader dispute resolution processes
^WInner take all dynamics or network fragmentations?

5. Legal Challenges
* Tech regulation is a hotbed of debate with several interests at play - from the desire to maximize innovation to ensuring the protection of consumers and public goods - law and technology can influence each other, both regulate the behaviour of individuals
* Decentralized justice systems are a source of controversy due to their lack of compliance with prevailing laws - commentators have expressed concerns about the design mechanisms of decentralized arbitration, including about the lack of centralized coordination over crowdsourced jurors potentially resulting in information cascades by incentivizing aligmment with the majority, lack of party autonomy over the dispute resolution procedure, the perceived supremacy of 'common sense' over 'law' 
* Decentralized justice systems are a form of alternative dispute resolution (ADR) - facilitating the resolution of disputes outside of the formal court system - the closest traditional ADR analogue for decentralized justice systems is arbitration - lacks a unified approach to regulation of myriad soft laws and guidance documents
	* it seems to contradict the main tenets of due process and impartiality on which arbitration has traditionally founded its claims to render fair decisions -also since jurors ar


formal models of fairness?
constitutionalism and blockchain
(blockchain gov)
tara merk
https://blockchaingov.eu/event123/blockchain-constitutionalism-the-role-of-legitimacy-in-polycentric-systems/

(is this where economic sociology should come in tbh)
(but do humans just run on this? do they need trust to be or stay motivated?)
(what if fairness is not what any participants desire)
(identity systems?)
(what quantitative language can we use to make sense of the polycrisis? to integrate broad swathes of information at a high resolution?)
(the building out of the ai safety field is a good example of how to build a integrated research/action agenda)