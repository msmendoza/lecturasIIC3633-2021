# Collaborative Filtering Recommender Systems

**Reference:** Schafer, J. B., Frankowski, D., Herlocker, J., & Sen, S. (2007).
Collaborative filtering recommender systems. In The adaptive web (pp. 291-324).
Springer Berlin Heidelberg.

This paper talks about the crucial importance of recommender systems in the developing
of adaptive web pages. In that sense, authors present probabilistic and non-probabilistic
collaborative filtering algorithms, introduce challenges present in them, how to design
systems in order to acquire implicit or explicit ratings, enunciate problems related to
the time and memory complexity of recommendation and prediction procedures and finally,
an exhaustive explanation about possible evaluation metrics is given. It is important
to note how at the end of the document, authors not only reached an end with the
theoretical part, but also discussed topics about **transparency** of recommendations
for users (**explanation**) and the problem of **security and privacy** associated to the
"user with unusual tastes" that so much improves the model (in a **novel** recommendation)
way but also exposes other users.

I must add that just one thing wasn't right away clear from the paper, in the
section of **Item-based Nearest Neighbor Algorithm**, in **Equation 6**,

<img src="https://render.githubusercontent.com/render/math?math=pred(u, i) = \frac{\sum_{j\in{ratedItems(u)}} itemSim(i, j) \cdot r_{ui}}{\sum_{j\in{ratedItems(u)}} itemSim(i, j)}">

we can see that  <img src="https://render.githubusercontent.com/render/math?math=\,r_{ui}">
is incorrect because that's exactly what the algorithm tries to predict with
<img src="https://render.githubusercontent.com/render/math?math=\, predict(u, i)">.
Instead, I think that the before-mentioned expression should be replaced with
<img src="https://render.githubusercontent.com/render/math?math=\, r_{uj}"> to make
sense again.
