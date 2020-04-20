# Mapping-Political-Communities-into-R^n
## Goals 
1. Summarize current approaches about cluster/latent-memberships analysis of political network with potential shortages of them. 
2. Introduce the graph embedding that complements the 1's shortages.

## General Trends in PolSci over Network analysis
- partitioning of political network into similarly behaving communities is their big interest.

## Literatures
### Mapping Political Communities: A Statistical Analysis of Lobbying Networks in Legislative Politics
paper http://web.mit.edu/insong/www/pdf/network.pdf
appendix http://web.mit.edu/insong/www/pdf/appendix_network.pdf

#### Goal
- Inferring political actors’ latent memberships
- Especially focusing on weighted edge relation between interest group (e.g. corporation) and legislators
#### Starting notion
- Previous empirical studies of interest group politics have been limited by the difficulty of observing the ties between interest groups and politicians directly

#### What will be referred about this paper in our research
The rudimentary reason of choosing bipartite graph is actually about to handle the two different types of groups that are innately different in terms of actor role - such as polticians vs corporations. We will cover this issue not by confining the network into bipartite, but represent the graph as heterogenous and to code what makes the node difference. In this way we can also find the dense representation about node-type-characteristics. 

#### Methodology
  
#### Pros and Cons
- Confined to Bipartite Graph. Easy to interpret and model the already-bipartitely set intuition. Not extensible to another graphical relationship. Relationship usually much more complex however, priorly confine those relationship into bipartite. 

## Our Methodologies
Heterogenous graph embedding (like metapath++) + HARP like hierarchical graph embedding
