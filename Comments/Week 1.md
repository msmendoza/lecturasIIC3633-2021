# Collaborative Filtering Recommender Systems

**Reference:** Schafer, J. B., Frankowski, D., Herlocker, J., & Sen, S. (2007). Collaborative filtering recommender systems. In The adaptive web (pp. 291-324). Springer Berlin Heidelberg.

This paper talks about the crucial importance of recommender systems in the developing
of adaptive web pages. In that sense, authors present ...

I must add that just one thing wasn't right away clear from the paper, in the
section of **Item-based Nearest Neighbor Algorithm**, in **Equation 6**,

<img src="https://render.githubusercontent.com/render/math?math=pred(u, i) = \frac{\sum_{j\in{ratedItems(u)}} itemSim(i, j) \cdot r_{ui}}{\sum_{j\in{ratedItems(u)}} itemSim(i, j)}">

we can see that  <img src="https://render.githubusercontent.com/render/math?math=\,r_{ui}">
is incorrect because that's exactly what the algorithm tries to predict with
<img src="https://render.githubusercontent.com/render/math?math=\, predict(u, i)">.
Instead, I think that the before-mentioned expression should be replaced with
<img src="https://render.githubusercontent.com/render/math?math=\, r_{u, j}"> to make
sense again.
