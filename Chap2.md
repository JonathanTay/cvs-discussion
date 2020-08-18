# CVX Book Chap 2 Solutions
https://hackmd.io/@6HZac9VfSmueW7K7dERCtg/H1BVfKwMD/edit

## Exercise 2.14

Let $x_1, x_2$ be two points in $S_\alpha$. We want to show that for $\theta_1,\theta_2 \in [0,1]$ and $\theta_1 + \theta_2 =1$, the convex combination $\theta_1 x_1 + \theta_2 x_2$ satisfies $\inf ||y-\theta_1 x_1 - \theta_2 x_2|| < \alpha$.


By the triangluar inequality, for every $y_1, y_2 \in S$, we have:
$$
\begin{aligned}
\theta_1 ||y_1 - x_1|| + \theta_2 ||y_2 - x_2|| & = ||\theta_1 y_1 - \theta_1 x_1 || + ||\theta_2 y_2 - \theta_2 x_2 || \\
& \ge ||(\theta_1y_1 + \theta_2 y_2)- (\theta_1 x_1+\theta_2x_2)|| \\
& \ge ||y_0 - (\theta_1 x_1+\theta_2x_2)||
\end{aligned}
$$
, where $y_0 = \theta_1y_1 + \theta_2 y_2$. 

Because $S$ is convex, $y_0 \in S$. Therefore:
$$
||y_0 - (\theta_1 x_1+\theta_2x_2)|| \ge \inf_{y \in S} ||y - (\theta_1 x_1+\theta_2x_2)||
$$

Combine the above two inequalities and take $\inf$ on the left side, we have:
$$
\begin{aligned}
\alpha &= \theta_1 \inf_{y_1 \in S} ||y_1 - x_1|| + \theta_2 \inf_{y_2 \in S}  ||y_2 - x_2|| \\
& \ge \inf_{y \in S} ||y - (\theta_1 x_1+\theta_2x_2)||
\end{aligned}
$$

 This completes the proof that $\theta_1 x_1 + \theta_2 x_2$ is in the set $S_\alpha$.



## Exercise 2.18
To show that $f(.)$ is invertible, it suffices to show that it is injective and surjective.

Note that:
$$
f(x) = P\left( Q \begin{pmatrix} x \\ 1 \end{pmatrix} \right)
$$
, where $P(z,t) = z/t$


To see that $f(x)$ is injective, we show that for every $x_1, x_2$, $f(x_1)=f(x_2)$ implies $x_1 = x_2$. 

Let $z_1 = Q \begin{pmatrix} x_1 \\ 1 \end{pmatrix}$ and $z_2 = Q \begin{pmatrix} x_2 \\ 1 \end{pmatrix}$. Then $f(x_1)=f(x_2)$ implies $P(z_1)=P(z_2)$.  By the definition of $P(.)$, we have $z_1 = \alpha z_2$. 

Therefore, 
$$
Q \begin{pmatrix} x_1 \\ 1 \end{pmatrix} = \alpha Q \begin{pmatrix} x_2 \\ 1 \end{pmatrix} 
=  Q \begin{pmatrix}\alpha  x_2 \\ \alpha \end{pmatrix}
$$

Because $Q$ is invertible, we immediately have $x_1=x_2$ and $\alpha=1$.

To see that $f(x)$ is surjective, we note that for every $y \in R^n$, we can let $x=P(Q^{-1} \bigl( \begin{smallmatrix}y \\ 1\end{smallmatrix}\bigr))$, such that $f(x)=y$.

