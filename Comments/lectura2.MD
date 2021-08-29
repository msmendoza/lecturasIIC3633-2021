# Matrix Factorization Techniques for Recommender Systems

This paper talks about the best realizations of latent factor models, which are
based on matrix factorization models. Those models map users and items to a
joint latent factor space of a given dimension, then the interactions
between user and items are modeled as inner products in following sense: the
greater the inner product between a user and a given item, greater is the overall
user interest/rating in that particular item. Authors also discussed the (1) imputation and
regularization improvement to the basis SVD model to solve the
<img src="https://render.githubusercontent.com/render/math?math=\, \hat{r}_{ui} = q_i^Tp_u">
equation, (2) compare SGD and ALS as learning algorithms for learning
<img src="https://render.githubusercontent.com/render/math?math=\, q_i">
and
<img src="https://render.githubusercontent.com/render/math?math=\, p_u">
, and finally, (3) introduce three model improvements, biases, temporal dynamics and
confidence levels.

In my opinion authors explain very well each of the different improvements to the
initial SVD model, but with respect to the estimation of
<img src="https://render.githubusercontent.com/render/math?math=\, q_i, p_u">,
if all known rates are used for training (see eq. 2 in the paper), how did
author properly test their recommendation systems in a test dataset? I come to
thing that if they're using the same records for training and testing, then
are cheating or falling into a fallacy.

Authors fail to explain in equation (7)
<img src="https://render.githubusercontent.com/render/math?math=\, \hat{r}_{ui}(t) = \mu + b_i(t) + b_u(t) + q_i^Tp_u(t)">
why the term <img src="https://render.githubusercontent.com/render/math?math=\, \mu">
remains constant despite the temporal dynamics. To my knowledge, overall average rating
over all movies must change as time passes, so
<img src="https://render.githubusercontent.com/render/math?math=\, \mu">
must depend on time too.

In addition, it comes as a surprise that authors did not mention nor explain any
mixture model that includes biases, temporal dynamics and confidence levels at
the same time. I was expecting this because of the increased accuracy present in
these models separately. So a common though would be about what could happen if all
the mentioned variants are combined into one model. One possible reason why authors
didn't include this huge model, could be the increase in the number of trainable
parameters, thus making the training step to take longer times to finish. Or maybe
they couldn't explain what could happen with overfitting regarding the actual
regularization.

Knowing the advantages of the MF model, in **[2]** authors discussed the
preconditioning technique for helping iterative methods to solve linear equations
and two other ways to solve the SVD problem: Coordinate Descent (CD) and Conjugate
Gradient (CG). CG proves to reduce the training time as well as increasing recall
when using higher number of factors.

I found the explanations of the update of each parameter in the methods
were explained thoroughly and consider as well that taking into account implicit
feedback may reduce cold start problems in CF models presented in **[1]**. Finally,
I would like to highlight that the initial presented **error function** may
have a typo error when authors exchange an _n_ with a 2 in the divisor of regularization
coefficients.

**[1]** Koren, Y., Bell, R., & Volinsky, C. (2009). Matrix factorization techniques for recommender systems. Computer, 42(8), 30-37.

**[2]** Takács, G., Pilászy, I., & Tikk, D. (2011, October). Applications of the conjugate gradient method for implicit feedback collaborative filtering. In Proceedings of the fifth ACM conference on Recommender systems (pp. 297-300).
