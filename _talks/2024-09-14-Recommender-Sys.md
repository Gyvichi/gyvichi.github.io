---
title: "Recommender System Basic"
collection: talks
type: "Talk"
permalink: /talks/2024/kisti
venue: "UNIST"
date: 2024-09-14
location: 
---

UNIST에서 들은 추천 시스템 강의 필기.

Traditional techniques :
- Content-based approach : recommends similar contents to those of the user's favorites.
- CF (Collaborative filtering) : recommends items rated high by neighbors.
- Hybrid : Combines the above.

# 1. Content-based approach

1. Calculate similarity between user's item and the item.
2. Search similar contents to the profile of the user.

# 2. CF

1. Find a group of users whose preferences are similar to that of a target user.
2. Recommend items rated high by neighbors.

There is heuristic method called **rating matrix** which can be used to measure similarity by PCC (Pearson correlation coefficient).

$$w(u, v)=\frac{\sum_f(v_{u, f}-\bar{v}_u)(v_{v, f}-\bar{v}_v)}{\sqrt{\sum_f(v_{u, f}-\bar{v}_u)^2\sum_f(v_{v, f}-\bar{v}_v)^2}}$$

Cosine similarity is also possible.

$$w(u, v) = \sum_j \frac{v_{u, f}}{\sqrt{\sum_{k \in I_u}v^2_{u, k}}} \frac{v_{v, f}}{\sqrt{\sum_{k \in I_v}v^2_{u, k}}}$$

Now calculate aggregation of each ratings ; there are various methods.
$$r_{c, s} = aggr_{c' \in C}r_{c', s}$$

$$r_{c, s} = \frac{1}{N}\sum_{c' \in \hat{C}}r_{c', s}$$

$$r_{c, s} = k\sum_{c' \in \hat{C}}sim(c, c') \times r_{c'
, s}$$

$$r_{c, s} = \bar{r}+k\sum_{c' \in \hat{C}}sim(c, c') \times (r_{c', s}-\bar{r}_{c'})$$

# Evaluation : Recall@K
Among the measures used to evaluate the top-k recommendations inferred by the evaluation system, **Recall@K** is the most widely used.

- $P_u$ : A set of positive items the user will interact in the future
- $R_u$ : A set of items recommended by the model, $\vert R_u \vert = K$ for top-k recommendation.

$$Recall@K = \frac{\vert P_u \cap R_u\vert}{P_u}$$
Final Recall@K is computed by averaging the recall values across all users.

# 3. GNN (Graph NN)

Recommender system can be represented by bipartite graph between users and items. Main task would be analyzing the edges.

Graph NN 내 task 또한 다양한데, graph-level, community (subgraph) level, node level, edge level의 모든 종류가 있기 때문이다. 
예를 들어 AlphaFold가 node-level, recommendation system이 edge-level, traffic prediction이 graph-level task가 될 것이다. 

GRL (Graph representation learning)은 node들을 구조적 특성을 보존하며 저차원 embedding space (벡터) 에 보내는 task이다.  

cf. Bipartite graph : A graph whose nodes can be divided into two DSUs.
Heterogenous graph $G=(V, E, R, T)$가 대부분의 real-world graph에 해당한다.
# Problems

1. Filter-bubble 현상

사용자의 과거 행동을 우선하는 알고리즘에 의해 노출되는 컨텐츠가 점점 제한적으로, 혹은 극단적인 방향으로 향한다.