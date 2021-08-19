---
title: 'Degree and Weight Distributions'
collection: algorithms
permalink: /algorithms/degreeDistribution/
cat: "static"
tags:
  - algorithms
  - degree
  - connectivity
  - distributions

---

<p style="margin-left: 1.5em;"> Returns the degree, weighted degree and edge weight distributions.</p>

The _degree_ of a node in an undirected networks counts the number of neighbours that node has. Its _weighted degree_ counts the number of interactions each node has. Finally the _edge weight_ counts the number of interactions which have happened across an edge.

<p align="center">
	<img src="../../images/degree.png" style="width: 30vw;" alt="node degree and weighed degree example"/>
</p>

For example, in the graph above with all edges aggregated between time $t_1$ and $t_3$, node $A$ has degree 2 (having neighbours $B$ and $C$) but weighted degree 3 (from the interactions at times $t_1$, $t_2$ and $t_3$). In the same way, edge $AB$ has weight 2.

## Returns
* `degDist`-- the _degree distribution_, an array of dictionaries of the form `{"degree": d, "freq": f}` counting the number of nodes `f` (type _Int_) of degree `d` (type _Int_)
* `weightDist` -- the _weighted degree distribution_, an array of dictionaries of the form `{"weight": w, "freq": f}` counting the number of nodes with weighted degree `w` (type _Int_)
* `edgeDist` -- the _edge weight distribution_, an array of dictionaries of the form `{"eweight": w, "freq": f}` counting the number of edges of weight `w` (type _Int_)

## Example
In [recent work](https://arxiv.org/abs/2009.08322) studying the Gab social network as an interaction graph, the degree, weighted degree and edge weight distribution was obtained from the aggregate graph, displayed below.

<p align="center">
	<img src="../../images/gabDistributions.png" style="width: 30vw;" alt="degree, interaction degree and edge weight distributions of the Gab social network"/>
</p>

The edge weight distribution is heavy-tailed, and shows that the majority of interactions between users occurred once and never again.

## Notes
* The edge weight as described here counts the number of times the edge appears (in social interaction graphs the number of interactions that occur over one edge) but the analyser code could be easily modified to compute instead the sum of user defined weights across the edge.
* This algorithm treats the graph as undirected, focusing on just node degree, rather than in/out degree. This can also be modified to address directed networks by considering incoming and outgoing edges rather than the union of these edges.
* This algorithm outputs a relatively large amount of data for each view of the graph (three arrays of dictionaries which could each have a number of entries similar magnitude to the number of nodes in worst case), therefore caution is advised against jobs with finely grained time ranges.
