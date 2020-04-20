# Mapping-Political-Communities-into-R^n
## Goals 
1. Summarize current approaches about cluster/latent-memberships analysis of political network with potential shortages of them. 
2. Introduce the graph embedding that complements the 1's shortages.

## Why Embedding of Lobby Network
Networks are easily and naturally represented by adjacency matrix, but such matrices are generally sparse and
high dimension,thus not well suited to statistical learning. Information preserving representation finding let us leverage different kind of statistical learning method to interpret and transform the data distribution for another/down-stream tasks. All of the above frameworks utilize the skip-gram model [33, 34] to learn a
representation of a node incorporating its topological
context, so nodes with similar topological information
will have similar numerical representations.

### Anaology to Word2Vec to Emphasize the Importance of Finding Embeddings
Word2vec [29] is the deep learning
model developed by Google to represent a word in a
low dimension dense vector, which has proven to be
successful in natural language processing [30]. By close
analogy, topological paths neighboring a node may be
handled like sequences of words, and word2vec can be
adapted to network representation learning to reduce
computing complexity and improve performance relative
to conventional approaches. Accordingly, several recent
publications have proposed word2vec-based network representation learning frameworks, such as DeepWalk [4],
GraRep [31], TADW [31], CNRL [32], LINE [5], node2vec
[6], and metapath2vec [7].

## General Trends in PolSci over Network analysis
- partitioning of political network into similarly behaving communities is their big interest.

## Literatures
### Mapping Political Communities: A Statistical Analysis of Lobbying Networks in Legislative Politics (MPC)
paper http://web.mit.edu/insong/www/pdf/network.pdf
appendix http://web.mit.edu/insong/www/pdf/appendix_network.pdf

#### Goal
- Inferring political actors’ latent memberships
- Especially focusing on weighted edge relation between interest group (e.g. corporation) and legislators
#### Starting notion
- Previous empirical studies of interest group politics have been limited by the difficulty of observing the ties between interest groups and politicians directly

#### What will be complemented of this paper in our paper
1. Manual and Boolean Distinction of Actor types

The rudimentary reason of choosing bipartite graph is actually about to handle the two different types of groups that are innately different in terms of actor role - such as polticians vs corporations. We will cover this issue not by confining the network into bipartite, but represent the graph as heterogenous and to code what makes the node difference. In this way we can also find the dense representation about node-type-characteristics. 

2. Holistic Analyses that incorporates all different types of bipartites.

This paper also analyses all different sub graphs of the entire political network independtly, sectioned by the actor types.
According to the paper, it refers following bipartites - examples include the interactions between 1) voters and politicians,
2) politicians and pieces of legislation, 3) private firms and government entities, and democratic and
4) autocratic countries - and these bipartites are all analyzed 1) independently with 2) single model. Our research will cover this issue by mapping the heterogenous graph into R^n space and densely codes the relation into the vectors where the distance between those encodes their relativities. Relativities will encodes which actor types are similar, for example politician A would be much more closer to industry or corporatin B rather than politician B regradless of its role-type-similarity. This is what this paper complements.

3. Latent memberships inferred from the mixture poisson in MPC are only from the "how many/numbers" of interactions between two different types of actors. However, the grounding assumption of the paper - how many times determines the political community membership - is too insufficient to determine the membership identity of each actors. Maybe the paper has also holds the strong assumption - if two different actor groups interacts to each other more times - such as microsoft interacts to the bill #A and so does apple, this overlapping relation to other group might be interpreted as membership identity, however, shared identity is not only constructred from the fixed 2 types of bipartite interaction, rather, it's more generally comprised from the more complex graphically structured interactions. Therfore, we are focusing on finding membership from the following, under the more generalized notions:

  - topologically similar nodes (with similar sub-structures or located near each other in the network)
  
  - the semantically similar nodes (with same node-types or logistically related attributes)
  
  - edge type information, which indicates different relationships among nodes.


#### Methodology
  
#### Pros and Cons
- Confined to Bipartite Graph. Easy to interpret and model the already-bipartitely set intuition. Not extensible to another graphical relationship. Relationship usually much more complex however, priorly confine those relationship into bipartite. 

## Our Methodologies
Heterogenous graph embedding (like metapath++) + HARP like hierarchical graph embedding + bayesian-embedding (to incorporates mixed interaction in the **MPC**)
