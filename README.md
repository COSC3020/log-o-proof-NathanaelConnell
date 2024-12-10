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

To prove tha O(log(2)n) is the same O(log(5)n), we can use the base change formula for logarithms which states that log(b)n = (log(a)n) / (log(a)b).  This allows us to express log(2)n as log(2) n = (log(5)n) / (log(5)2) and log(5)n = (log(2)n) / (log(2)5).  these relationships show that the two logarithmic functions differ only by constant factors, and since Big O notation ignores constant factos, O(log(2)n) and O(log(5)n) are equivalent.  For log(2)n ∈ O(log(5)n), we can observe that log(2)n = (log(5)n) / (log(5)2), and there exists a constant c = 1/(log(5)2) such tht log(2)n <= c * log(5)n for large n.  for log(5)n ∈ O(log(2)n we have log(5)n = (log(2)n) / (log(2)5) and there exists a constant c = 1/(log(2)5) such that log(5)n <= c * log(2)n for large n.  Since both functions differ onlu by a constatn factor O(log(2)n) = O(log(5)n).

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
