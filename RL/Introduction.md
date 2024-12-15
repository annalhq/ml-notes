---
created: 15-12-2024-18:17:55
modified: 15-12-2024-18:17:55
tags: 
topics: Introduction
course: Deepmind UCL
instructor: Hado van Hasslet
---
## Basis

**Motivation:**
- First automation of repeated physical solutions: *Industrial revolution* 
- Second, automation of repeated mental solutions: *Digital revolution*
- Next step: allow machines to find solution themselves: We then only needs to specify a problem and/or goal

**Alan Turing's proposition:**
In his paper *Computing machinery and intelligence*, he proposed a question to *'Can machine think ?'*

**Highlight**: Three components of process to imitate an adult mind:
1. The initial state of the mind, say at birth
2. The education to which it has been subjected
3. Other experience, not to describe as education, to which it has been subjected
Instead of trying to produce a programme to simulate the adult mind, *why not rather try to produce one which simulates the child's*. If this were then subjected to an appropiate course of education one would obtain the adult brain.

> [!note]
> **What is artificial intelligence?**
> To be able to learn to make decisions to achieve goals
  ## 
## What is reinforcement learning?
 
 - People and animals learn by **interacting with our environment**
- This differs from certain other types of learning
	- It is **active** rather than passive
	- Interactions are often sequential — future interactions can depend on earlier ones
- We are **goal-directed**
- We can learn **without examples** of optimal behaviour
- Instead, we optimise some **reward signal**

**Agent and environment**

![[agent-envrionment.png]]

At each step *t* the agent:
- Recieves observation $O_t$ (and reward $R_t$)
- Executes action $A_t$

The environment:
- Recieves action $A_t$
- Emits observation $O_{t+1}$ (and reward $R_{t+1}$)

## Rewards

- A reward $R_t$ is a scalar feedback signal
- Indicates how well agent is doing at step t - defines the goal
- The egent's job is to maximize cumulative reward
$$G_t = R_{t+1}+R_{t+2}+ \ ...$$
reinforcement learning is based on the **reward hypothesis.

> [!note] Reward Hypothesis
> Any goal can be formalized as the outcome of maximixing a cumulative reward

> [!info]
> We call the this cumulative reward as **return**

## Values

 We call the expected cumulative reward, from a state *s*, the **value**
 $$
 \begin{align}
 v(s) &= \mathbb{E}\bigl[G_t \mid S_t = s\bigr] \\ 
 &= \mathbb{E} \bigl[R_{t+1} + R_{t+2} + R_{t+3} +\ .. \mid S_t = s \bigr]
 \end{align}
$$
- The values depend on the actions the agent takes
- Goal is to **maximize value**, by picking suitable actions
- Rewards and values define **utility** of states and action (no supervised feedback)
- Returns and values can be defined recursively
$$
\begin{align}
G_t &= R_{t+1} +G_{t+1} \\
v(s) &= \mathbb{E} \bigl[R_{t+1}+v(S_{t+1}) \mid S_t = s \bigr]
\end{align}
$$



---
## References
1. Background material: Reinforcement learning: An introduction, Sutton & Barto 2018 http://incompleteideas.net/book/the-book-2nd.html
2. Computing machinery and intelligence - Alan Turing https://academic.oup.com/mind/article/LIX/236/433/986238## 
