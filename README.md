# CS5011 Artificial Intelligence Practice

This repository demonstrates work completed as part of the **CS5011 Artificial Intelligence Practice** module at the University of St Andrews.
Specifically, four different AI practice domains were considered: Search, Uncertainty, Logic, and Learning.

## A1 - Search - Marine Navigation Planner

Several pathfinding/search algorithms have been implemented to find solutions for a _Marine Navigation Route Planner_. This projects aimed to create a simplified version of a marine navigation route planner for autonomous ferries to navigate the sea surrounding the [Republic of Izaland](https://wiki.opengeofiction.net/index.php/Izaland#Waterways) and connecting its 400 islands. An autonomous ferry is used to transport passengers from an island to another without human intervention. To better plan waypoints on the navigation charts, a map was used inspired by a[ 2D triangular mesh](https://en.wikipedia.org/wiki/Triangle_mesh), where a portion of Izaland’s sea and land is represented via a 2D triangular grid. The route finder planner is operated by an agent whose aim is to find the best route from the departure port to the destination port, this is referred to as a ferry agent. The agent moves from the centre of a triangle to the centre of an adjacent triangle but some triangles cannot be crossed as they represent portions of land.

Uninformed (depth-first and breadth-first) and informed (best-first and A*) search algorithms have been implemented to find solutions to various configurations of this problem. Additionally, the bidirectional search (BDS) algorithm has been implemented for comparison. An alternate/extension heuristic has also been implemented for weather forecast management. In all cases, experiments have been performed to evaluate and compare these search algorithms.

## A2 - Uncertainty - Bayesian Networks

Bayesian networks (BNs) are a way of representing probabilistic relationships among a set of variables. BNs are probabilistic graphical models representing a set of random variables and their conditional dependencies by directed acyclic graphs. Seminal research in the context of Bayesian networks and causal reasoning has led [Judea Pearl](http://amturing.acm.org/bib/pearl_2658896.cfm), one of the first pioneer of BNs, to being awarded the prestigious [Turing Award in 2011](http://amturing.acm.org/alphabetical.cfm). In recent years, Bayesian networks have also seen interesting applications in machine learning. In this project, I gained familiarity with modelling and making probabilistic inferences with Bayesian networks.

Three Bayesian networks were provided for the testing and evaluation of the various parts of the practical. An additional four Bayesian networks were created for further testing and evaluation. The variable elimination algorithm was implemented for general inference.

## A3 - Logic - Tornado Sweeper

The Tornado Sweeper game is inspired by the well-known [Minesweeper computer game](http://www.minesweeper.info/wiki/Main_Page). A Tornado Sweeper world is a grid in the shape of a rhombus with N cells per side, where each cell is of hexagonal shape. T tornadoes are scattered among the cells. The rules of the Tornado Sweeper game are similar to those of Minesweeper, played on a [hexagonal board](https://mzrg.com/js/hexmine/jsmine.html), but the Tornado worlds are a small subset of those. A logical agent playing the Tornado Sweeper game aims to uncover all cells on the board but those containing a Tornado. If the agent probes a cell that contains a Tornado, the game is over. Otherwise, a clue appears on the cell indicating the number of Tornadoes in the 6 adjacent neighbours of the probed cell. In this project, I aimed to develop logic-based strategies for an agent to solve the Tornado Sweeper game.

Logical (procedural and declarative) techniques were used to implement a solver and hint system for the "[Tornado Sweeper](http://puzzlepicnic.com/genre?id=8)" game using constraint programming. A rudimentary hint system for this puzzle was also developed, which follows a similar chain of logic a person would usually follow when completing the puzzle. A brief evaluation comparing the procedural and declarative techniques was performed, as well as a critical discussion of the developed hint system.

## A4 - Learning - Automated Algorithm Selection using Neural Networks

[The Automated Algorithm Selection](https://en.wikipedia.org/wiki/Algorithm_selection) (AS) problem has been extensively studied for more than a decade due to its wide range of applications across various domains. Given a portfolio of n algorithms $A = {a_1 , a_2 , ..., a_n }$, an instance distribution $D_I$ where each instance $i ∼ D_I$ can be described as a feature vector $v(i)$, a cost metric $c(i,a_k)$ that measures the cost of solving instance $i$ using algorithm $a_k ∈ A$, the AS problem involved building an automated selector $f(v(i))$ that can select the best algorithm $a ∈ A$ for an instance $i$. More formally, I wanted to find f such that $E_{i∼D_I} [c(i, f (v(i))]$ is minimised.

Several classification (including binary, random forest and a custom loss function) and regression neural networks were built to solve the AS problem. Evaluation metrics including the average loss, accuracy, average cost, SBS cost, VBS cost and, the SBS-VBS gap were implemented and evaluated for each network to determine the most effective and efficient model.
