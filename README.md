Download link :https://programming.engineering/product/math-6490-nonlinear-optimization-in-machine-learning-assignment-2/

# MATH-6490.-Nonlinear-Optimization-in-Machine-Learning.-Assignment-2.
MATH 6490. Nonlinear Optimization in Machine Learning. Assignment 2.
There are 3 problems, each problem is worth 5 points, total is 15 points.

1. Let f : Rn ! R be a twice continuously di erentiable function, show that f is m{strongly convex in the sense of (2.4) in the Lecture Notes, i.e, for any x; y 2 Rn

f((1 )x + y) (1 )f(x) + f(y)

1

m (1 )kx yk22 ;

(0.1)

2

if and only if r2f(x) mI for all x, i.e., the eigenvalues 1; :::; n of r2f(x) satisfy min i m. You can make use of the following fact: Let A be a symmetric non{ negative de nite n n matrix. Then the eigenvalues 1; :::; n of A satisfy min i m

if and only if for any u 2 Rn we have uT Au mkuk2.

(Hint: Suppose that the function f is strongly{m convex with the standard in-equality (0.1) above for m{convexity. Set z = (1 )x + y. Then by (0.1) we have

f(y) f(x) f(z ) f(x) + 12m (1 )kx yk2 :

Making use of Taylor’s expansion


Since we have

z[l+1] = W [l+1] (z[l]) + b[l+1]

;

we see that we can further have

@zj[l]

@zj[l]

!

@zj[l]

=

= W

;

@zk[l+1]

@[W [l+1]

(z[l])]k

[l+1] @ (z[l])

k

Notice that

@ (z[l])

= (0; :::; 0; 0

(zj[l]); 0; :::; 0)T where the 0(zj[l]) term lies on the j-th

@zj[l]

position, we have W [l+1]

@ (z[l])

= 0(zj[l])Wj[l+1], where W [l+1]

= (Wj[l+1]). This gives

@z[l]

j

@ (z[l])

l+1]

us W [l+1]

! = 0(zj[l])Wjk[

, where Wjk is the element at the j-th column and

@z[l]

j

k

k-th row of W . So we nally get

nl+1

k[l+1] 0(zj[l])Wjk[l+1] = 0(zj[l])[(W [l+1])T [l+1]]j ;

j[l] =

X

k=1

which leads to what we wanted to prove.)

3. Consider solving an optimization problem min f(x) via a line search method of

x2Rn

the form xk+1 = xk + dk where the stepsize > 0 and the descent direction dk 2 Rn. Assume one can obtain an inequality of the form

f(xk+1) f(xk) Ckrf(xk)k2

for some constant C > 0. Assume that the objective function f is bounded from below and its gradient rf is L{Lipschitz. Suppose there is a subsequence xnk ! x as k ! 1, show that rf(x) = 0. In particular, if the function f is convex, this implies that x is a

solution to the optimization problem.

(Hint: Rewrite the inequality into krf(xk)k2

f(xk) f(xk+1)

and use the fact

C

that ff(xk)gk 1 is a monotonically decreasing sequence that is bounded from below.

This indicates that klim [f(xk) f(xk+1)] = 0, which implies that

klim krf(xk)k =

!1

!1

0. As we have xnk ! x as k ! 1, by the continuity of rf(x) we have rf(x) = lim rf(xnk ) = 0, as claimed.)

k!1
