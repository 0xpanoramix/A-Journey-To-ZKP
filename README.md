# zk-SNARKs from zero

## Abstract

Zero-Knowledge Proofs is a wide and really interesting topic which combines the beauty of mathemetics, cryptography and computer science.

The main drawback about ZKPs is probably the steep learning curve. Sure, you’ll probably be able to understand how polynomials work if you remember you classes from high-school, but it is safe to say that learning ZKPs is a difficult challenge. In the end, you’ll be stuck and need to find external resources.

A few month back, I found [this amazing step-by-step paper](https://arxiv.org/abs/1906.07221) which explains how zk-SNARKs work.

It assumes that you know fundamentals mathemetics and implicitely rely on your ability to do the maths by yourself as you’re following the given explanations. 95 % of my today’s knowledge about zk-SNARKS comes from this paper, so please have a look at it.

My goal here is to take a similar approach as the one in the paper and take it event further : I’ll try to cover every piece of math involved and implement the zk-SNARK protocol using the go programming language.

## Zero-Knowledge Proof : The Concept

### Definition

A **zero-knowledge proof** or **zero-knowledge protocol** is a method by which one party (the prover) can prove to another party (the verifier) that a given statement is true while the prover avoids conveying any additional information apart from the fact that the statement is indeed true.

[Thanks wikipedia](https://en.wikipedia.org/wiki/Zero-knowledge_proof).

### High Level Overview

Just a quick disclaimer, the following example is not the most accurate for describing a zero-knowledge proof. It’ll just help to capture the underlying idea of such a protocol.

Anyway, here is the example :

1. Bob and Alice are talking to each other.
2. Bob wants to convince Alice that he has a superpower : he has the ability to know exactly how many leafs are on any given tree.
3. Bob don’t want to reveal anything about the information itself : he does not want to tell Alice how many leafs are on the given tree.
4. Now Bob tells Alice : “You have the choice to take a leaf from the tree, or not. And I’ll close my eyes so I wont be able to know if you’ve taken the leaf or not”.
5. Bob closes his eyes, Alice decides to take a leaf from the tree.
6. Bob opens his eyes, and tells : “Well, there are less leafs than before.”.
7. Just to be sure that Bob was’nt lucky, Alice decides to repeat the process at step 5.

And every time, Bob has the right answer : either the number of leafs has been reduced, or it has not changed.

Now Alice is pretty sure that Bob has indeed the superpower he claims to have.

The best out of this example is that Bob never revealed how many leafs are on the tree to Alice.

Now let’s get to a more mathematical example : proving that Bob knows what are the solutions of a given polynomial.

## Polynomials

### Definition

A polynomial is a mathematical expression composed of sums and multiplications of unknown and constants numbers.

### High Level Overview

Here is probably the simplest polynomial you can think about :

$x$

Wait is that it ? Just the letter x ?

Yes that’s it ! Now out of this simple expression we can do many exciting things :

- Evaluate the expression for a given value `x`
- Find the polynomial solution
- Determine its degree
- And many more…

### Evaluation

Evaluate here means that we will choose a value for `x` and compute the result. The result will be called `y`.

Using the expression you’ve seen right before, we can evaluate `y` using `x` the following way :

$\begin{aligned}
y &= x \\
\end{aligned}$

We can also use the function keyword `f(x)` :

$\begin{aligned}
f(x) &= x \\
\end{aligned}$

As an example, if we choose `x = 5` we’ll obviously get :

$\begin{aligned}
f(5) &= 5 \\

y &= 5 \\
\end{aligned}$

Using a new expression, `y = x²`, and using `x = 5` we get :

$\begin{aligned}
y &= x{}^2 \\
f(x) &= {x}^2 \\
\\
f(5) &= {5}^2 \\
f(5) &= 25 \\
\end{aligned}$

So for `x = 5` we get `y = 25`.

### Polynomial Coefficient

The last two expressions can be written the following way :

- `1 * x`
- `1 * x²`

And we’ve introduced this number `1` called the **coefficient**.

Using a new polynomial `x³ - 5x² + 5x`, we can identify three coefficients :

1. `1`
2. `5`
3. `5`

### Polynomial Degree

Something interesting about these two expressions, `x` and `x²`, is the degree of the unknown value `x`.

The polynomial’s degree is the highest degree of the unknown value `x`.

In the following expression `x³ - 5x² + 5x`, the polynomial’s degree is `3`.

### Visualization

We can actually represent a polynomial on a graph using `x` and `y` values.

So far, we’ve seen three of them :

1. `x`
2. `x²`
3. `x³ - 5x² + 5x`

Let’s plot them on a graph :

![Untitled](zk-SNARKs%20from%20zero%200fea8c83882f41d4baf7906d3625c201/Untitled.png)

![Untitled](zk-SNARKs%20from%20zero%200fea8c83882f41d4baf7906d3625c201/Untitled%201.png)

![Untitled](zk-SNARKs%20from%20zero%200fea8c83882f41d4baf7906d3625c201/Untitled%202.png)

### Solutions

A polynomial has one or more solutions, also called “roots”, where the evaluation outputs `0`:

$\begin{aligned}
f(x) &= 0 \\
\end{aligned}$

No matter what `f(x)` is : `x`, `x²` or something more exotic such as `x³ - 5x² + 5x`.

### Polynomials and ZKP

Getting back to ZKP, remember that Bob wants to prove to Alice that he knows the solutions of a given polynomial without revealing the solution and the polynomial itself.

Why is this useful ? We’ll get to that in the future, now just consider that Alice and Bob are still playing together not with trees, but this time with polynomials.
