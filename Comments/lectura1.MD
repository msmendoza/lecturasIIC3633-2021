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

In the section of **Practical Challenges of User-Based Algorithms** when talking about ways to reduce the time and memory needed for computing the best user’s neighborhood, authors fail to explain why clustering techniques become **unstable and unintuitive** when distance functions are not valid and are not true mathematical metrics because of the . I understand the mathematical foundations of why the function is no more a metric when the triangle equality does not hold (one of the three needed), but I fail to imagine the consequences in term of time, memory requirements and prediction accuracy.

From the presented challenges I encounter in the document, I was immensely attracted
to the one related to **Dimensionality Reduction Algorithms**. Not because of the
intrinsic reduction on computation time and requirements, but for the **mathematical
foundations** (optimization and advanced linear algebra) that must be addressed in order to effectively extract from this step a
minimum of **prediction accuracy**.

I must add that just one thing wasn't right away clear from the paper, in the
section of **Item-based Nearest Neighbor Algorithm**, in **Equation 6**,

<img src="https://render.githubusercontent.com/render/math?math=pred(u, i) = \frac{\sum_{j\in{ratedItems(u)}} itemSim(i, j) \cdot r_{ui}}{\sum_{j\in{ratedItems(u)}} itemSim(i, j)}">

we can see that  <img src="https://render.githubusercontent.com/render/math?math=\,r_{ui}">
is incorrect because that's exactly what the algorithm tries to predict with
<img src="https://render.githubusercontent.com/render/math?math=\, predict(u, i)">.
Instead, I think that the before-mentioned expression should be replaced with
<img src="https://render.githubusercontent.com/render/math?math=\, r_{uj}"> to make
sense again.

Personal experiences with CF systems I encounter every day are related to the **TIDAL
App** for high-quality music. When I first used the app, I was asked a few questions
about favourite genres and artists, and yes, at the beginning of my experience
I didn't have much more than a few non-personalized playlist recommendations dictated
just by the responses to the initial questions. But in time, after I rated a lot of
songs (rating is binary love/unloved), I'd say 30-50+, a lot of personalized playlists
appeared with song I really liker but hadn't added to my personal playlist or downloaded
yet. In addition to this, another playlist came around titled "Your Daily Discovery" with
songs I didn't know but really captured my attention and that's something that happens
almost every day. In that sense I can say that TIDAL has a recommender system
with high _serendipity_ properties.
