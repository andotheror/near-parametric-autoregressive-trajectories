# Near-Parametric Learning of Autoregressive Trajectories

## Abstract

A length-$M$ autoregressive trajectory has $|\mathcal A|^M$ possible values, and generic conditional-density bounds can inherit this large response space. We show that shared algebraic parameters prevent this trajectory-alphabet explosion under full chain-of-thought supervision. If every next-token probability is a positive rational function of $p$ shared real parameters, with numerator and denominator degree at most $\Delta$, then the class of complete trajectory densities has pseudo-dimension at most $2p\log_2(8eM\Delta)$. Conditional $\rho$-estimation therefore gives a proper distribution-free learner with integrated squared-Hellinger error

$$O\\\\\\!\left(\frac{p\log(2M\Delta)\log(en/p)}{n}
 +\frac{\log(1/\delta)}{n}\right),$$

without knowing the prompt distribution and without any lower bound on token probabilities. For the unrestricted $d$-dimensional logistic delay line introduced in recent stochastic autoregressive learning, this yields $\widetilde O((d+\log(1/\delta))/\epsilon)$ full trajectories for both final-token squared error and trajectory squared-Hellinger error. The previous bound was roughly $\widetilde O(d^2\log M/\epsilon)$, and obtaining the natural $d$-dimensional rate for arbitrary horizons was left open. A horizon-one packing proves $\Omega((d+\log(1/\delta))/\epsilon)$, so the parameter dependence is optimal up to logarithms. The same method gives constant-factor misspecification oracles, sparse adaptation, bounded-length stopping, and multiclass softmax rates linear in the number of free parameters. The argument does not improve end-to-end supervision, where unobserved paths must be summed before forming a density.

## Contributions

First, we give a general closure theorem: multiplying $M$ shared rational transition probabilities increases polynomial degree by $M$ but increases pseudo-dimension only logarithmically in $M$. Second, combining this theorem with unknown-design conditional $\rho$-estimation yields a high-probability Hellinger oracle inequality independent of $|\mathcal A|^M$. Third, we resolve the CoT half of the logistic open question and prove a matching $\Omega(d/\epsilon)$ lower bound. Fourth, penalized $\rho$-estimation adapts to unknown sparsity, and the rational closure theorem gives multiclass softmax and misspecified-model corollaries.

## Keywords

near-parametric, learning, autoregressive, trajectories, length-, trajectory, possible, values, generic

## Files

- `main_old_2026-08-13.pdf`, the paper as first published, with its OpenTimestamps proof `main_old_2026-08-13.pdf.ots`.
- `supplement_old_2026-08-13.pdf`, the supplement as first published, with its OpenTimestamps proof `supplement_old_2026-08-13.pdf.ots`.
- source: `aistats2027.sty`, `main.tex`, `references.bib`, `supplement.tex`.
- also: `main.bbl`, `supplement.bbl`.
