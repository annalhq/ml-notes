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

