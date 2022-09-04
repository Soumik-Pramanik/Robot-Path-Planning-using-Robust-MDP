# Robot-Path-Planning-using-Robust-MDP
# Introduction
-->Optimal solutions of MDP are sensitive to the state transition probabilities.

-->Estimation of the state transition probabilities are far from accurate in real life situations.

-->Which limits the usage of MDP in real life problems
# Motivation
-->The aim is to build the robust control strategy for finite state and finite action MDP’s when transition probabilities are uncertain.

-->The solution could be obtained using variant of the classical dynamic programming algorithm, the “robust dynamic programming” algorithm.
# Model Enviornment
![image](https://user-images.githubusercontent.com/96630179/188327569-c4bc3b94-7603-4588-a10c-8bf2e778a105.png)
![image](https://user-images.githubusercontent.com/96630179/188327587-8d9deb42-16de-4516-9496-9c4e1a854813.png)
# Robust Value Iteration
1.Initialize V to zero vector as the size of the state space.

2.Repeat Until V Converges.

3.For all States i and control a assign to matrix Qmin the solution to the optimization problem.

4.Qmin(i, a) = min(Ep[R(i)+ptV] ) ∀ (p∈Pia)

5.Update V by maximizing over the control set:

6.V(i) = max( Qmin(i,a) ) ∀ (a∈A)
# Results and conclusion
1.Cost = (returns under certainty - returns under uncertainty)

2.We can observe that the cost of the nominal policy increases more than that of robust policy.

3.Intercept of nominal policy is close to close to zero under no uncertain which implies under certainty nominal policy behaves optimally.

4.While in the case of robust intercept is high which tells that robust strategy behave suboptimally.

5.As the uncertainty increases the robust strategy behaves better than that nominal strategy, which can be concluded from the slopes of the above graphs
# Nominal MDP Results
![image](https://user-images.githubusercontent.com/96630179/188327687-85a04b4b-0abe-43a0-9fd1-65af73ad80f1.png)

# Robust MDP Result
![image](https://user-images.githubusercontent.com/96630179/188327702-9d26103c-2772-4249-959d-b2da935a35d3.png)
