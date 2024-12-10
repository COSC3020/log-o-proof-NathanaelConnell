# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$
I used chat gpt to help remind me of the base change formula.

To prove that O(log(base2) n) is the same as O(log(base5) n), we use the base change formula which states that log(base2) n = (log(base5) n) / (log(base5) 2) and log(base5) n = (log(base2) n) / (log(base2) 5).  By the definition of O(f(n)), T(n) ∈ O(f(n)) if there exists constatns c > 0 and n(sub0) > 0 such that T(n) <= c * f(n) for all n >= n(sub0).  For T(n) = log(base2) n and f(n) = log(base5) n, substituting the base change formula gives (log(base5) n) / (log(base5) 2) <= c * log(base5) n.  Simplifying, we find c = 1/(log(base5) 2) satisfies the inequality, so log(base2) n ∈ O(log(base5) n).  For log(base5) n ∈ O(log(base2) n), using log(base5) n = (log(base2) n) / (log(base2) 5), the inequality (log(base2) n) / (log(base2) 5) <= c * log(base2) n is satisfied with c = 1/(log(base2) 5.  Making O(log(base2) n) = O(log(base5) n).

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
