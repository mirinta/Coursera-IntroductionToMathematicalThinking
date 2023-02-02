# Introduction to Mathematical Thinking
## Lecture 0
**A key feature of mathematical thinking is thinking outside the box**. It's about thinking, not learning new math techniques.

At high school, the focus is primarily on mastering procedures to solve various kinds of problems. That gives the subject very much the flavor of a cookbook, full of mathematical recipes, thinking inside boxes.

At university, the focus is on learning to think a different way, to think like a mathematician, thinking outside boxes.

## Lecture 1 - Introductory Material

## Lecture 2 - Logical Combinators
AND ($\wedge$)
| **$x$** | **$y$** | **$x \wedge y$** |
| :-----: | :-----: | :--------------: |
|    T    |    T    |        T         |
|    T    |    F    |        F         |
|    F    |    T    |        F         |
|    F    |    F    |        F         |

OR ($\vee$)
| **$x$** | **$y$** | **$x \vee y$** |
| :-----: | :-----: | :------------: |
|    T    |    T    |       T        |
|    T    |    F    |       T        |
|    F    |    T    |       T        |
|    F    |    F    |       F        |

NOT ($\neg$)
| **$x$** | **$\neg x$** |
| :-----: | :----------: |
|    T    |      F       |
|    F    |      T       |

## Lecture 3 - Implication
$\phi$ implies $\psi$.

**Implication involves causality.** Causality is an issue of great complexity that philosophers have been discussing for generations.

When we're dealing with conjunction and disconjunction, it didn't matter whether there was any kind of relationship between the two conjuncts or the two disjuncts. Clearly, they're independent.

Implication has a truth part (the conditional or the material conditional) and a causation part.

$implication = conditional + causation$

The first part, the conditional, we're going to define entirely in terms of truth values. And the second part we're going to leave to the philosophers.

$\phi \Rightarrow \psi$ is the truth part of "$\phi$ implies $\psi$".

We call $\phi$ the antecedent, and we call $\psi$ the consequent.

Define the truth $\phi \Rightarrow \psi$ in terms of the truth (falsity) of $\phi$, $\psi$.

When $\phi$ does imply $\psi$, $\phi \Rightarrow \psi$ behaves "correctly".

**Implication has a property that a true implication leads to a true conclusion from a true assumption.**

| **$\phi$** | **$\psi$** | **$\phi \Rightarrow \psi$** |
| :--------: | :--------: | :-------------------------: |
|     T      |     T      |              T              |
|     T      |     F      |              F              |
|     F      |     T      |              T              |
|     F      |     F      |              T              |

When $\phi$ is false, consider the not implication, $\phi \nRightarrow \psi$.

* If $\phi$ does not imply $\psi$ if even though $\phi$ is true, $\psi$ is nevertheless false.
* In all other circumstances, $\phi \nRightarrow \psi$ will be false.
* In all other circumstances, $\phi \Rightarrow \psi$ will be true.
* Therefore, if you have a false antecedent, the conditional is always true.

The definition of a true antecedent is based on an analysis of the truth values of genuine implication.

The definition of a false antecedent is based on an analysis of the notion does not imply.

## Lecture 4 - Equivalence
Two elements $\phi$, $\psi$ are said to be logically equivalent if each implies each other. 

In fact, equivalence is to logic as equations are to arithmetic and algebra.

Bi-conditional $\phi \Leftrightarrow \psi$. It's an abbreviation of $(\phi \Rightarrow \psi) \wedge (\psi \Rightarrow \phi)$.

$\phi \Leftrightarrow \psi$ is true if $\phi$, $\psi$ are both true or both false.

The following statements all mean "$\phi$ implies $\psi$.
* If $\phi$, then $\psi$.
* $\phi$ is sufficient for $\psi$. (in order to conclude $\psi$, it suffices to know $\phi$)
* $\phi$ only if $\psi$.  (For example, a person could ride in the Tour de France only if he has a bicycle.) <font color = red> [NOT THE SAME AS "if $\psi$ then $\phi$"] </font>
* $\psi$ if $\phi$.
* $\psi$ whenever $\phi$.
* $\psi$ is necessary for $\phi$.

<font color = red> Notes: "if", "whenever" and "necessary" change the original order in implication. </font>

"$\phi$ is equivalent to $\psi$" is self equivalent to the following statements.
* $\phi$ is necessary and sufficient to $\psi$.
* $\phi$ if and only if (iff) $\psi$.

The conditional and bi-conditional only differ from implication and equivalents in situations that do not arise in the cause of normal mathematical practice.

In any real mathematical context, the conditional effectively is implication, and the bi-conditional effectively is equivalent.

<font color = red> Notes：</font> 

1. <font color=red> $\neg (\phi \Rightarrow \psi)$ is equivalent to $\phi \wedge (\neg \psi)$. </font>
2. <font color=red> $\neg (\phi \vee \psi)$ is equivalent to $(\neg \phi) \wedge (\neg \psi)$. </font>
3. <font color=red> $\neg (\phi \wedge \psi)$ is equivalent to $(\neg \phi) \vee (\neg \psi)$. </font>
4. <font color=red> $\phi \Rightarrow \psi$ is equivalent to $(\neg \phi) \vee \psi$. </font>
5. <font color=red> $\phi \nRightarrow \psi$ is equivalent to $\phi \wedge (\neg \psi)$. </font>
6. <font color=red> $\phi \Leftrightarrow \psi$ is equivalent to $(\neg \phi) \Leftrightarrow (\neg \psi)$. </font>
7. <font color=red> $\phi \Rightarrow (\psi \wedge \theta)$ is equivalent to $(\phi \Rightarrow \psi) \wedge (\phi \Rightarrow \theta)$. </font>
8. <font color=red> $(\phi \vee \psi) \Rightarrow \theta$ is equivalent to $(\phi \Rightarrow \theta) \wedge (\psi \Rightarrow \theta)$. </font>
9. <font color=red> $\phi \Rightarrow \psi$ is equivalent to $(\neg \psi) \Rightarrow (\neg \phi)$ (contrapositive). </font>
10. <font color=red> $P \Rightarrow (Q \Rightarrow R)$ is equivalent to $(P \wedge Q) \Rightarrow R$. </font>

## Lecture 5 - Quantifiers

"there exists...", "for all..."

In mathematics, it's used to refer to the two extremes, there is at lease one and for all.

### Existential quantifier 
<font color = red> $\exists$ </font>

For example, the following statements are equivalent:
* The equation $x^2 + 2x + 1 = 0$ has a real root.
* There is a real number $x$ such that $x^2 + 2x + 1 = 0$.
* There exists a real number $x$ such that $x^2 + 2x + 1 = 0$.
* $(\exists x \in \reals)(x^2 + 2x + 1 = 0)$ 

### Universal quantifier 
<font color = red> $\forall$ </font>

For example:
* The square of any real number is greater than or equal to zero.
* $(\forall x \in \reals)(x^2 \geq 0)$
  
### Combination of quantifiers

<font color = red> The order of the quantifiers is important. </font>

* There is no largest natural number:
  $(\forall m \in \natnums)(\exists n \in \natnums)(n \gt m)$
* If we swap the quantifiers of the previous example, $(\exists n \in \natnums)(\forall m \in \natnums)(n \gt m)$, it means "There exists a natural number bigger than all natural numbers". IT IS FALSE!

Example 1: A drivers license valid in one state is valid in any state.
* $(\forall L)[(\exists S_1)Valid(L, S_1) \Rightarrow (\forall S_2)Valid(L, S_2)]$

Example 2: The <font color = red> literal meaning </font> of "Do you have a license from more than one state?"
* $(\exists L)(\exists S_1)(\exists S_2)[(S_1 \neq S_2) \wedge From(L, S_1) \wedge From(L, S_2)]$

### Assignment
1.1 The equation $x^3 = 27$ has a natural number solution.
* $(\exists x \in \natnums)(x^3 = 27)$

1.2 $1,000,000$ is not the largest natural number.
* $(\exists n \in \natnums)(x > 1,000,000)$

1.3 The natural number $n$ is not a prime.
* $(\exists p \in \natnums)(\exists q \in \natnums)[(p > 1) \wedge (q > 1) \wedge (n = pq)]$

2.1 The equation $x^3 = 28$ does not have a natural number solution.
* $(\forall x \in \natnums)(x^3 \neq 28)$

2.2 $0$ is less than every natural number.
* $(\forall n \in \natnums)(n > 0)$

2.3 The natural number $n$ is a prime.
* $(\forall p \in \natnums)(\forall q \in \natnums)[(n = pq) \Rightarrow (p = 1 \vee q = 1)]$

3.1 Everybody loves somebody.
* $(\forall P_1)(\exists P_2)Love(P_1,P_2)$

3.2 Everyone is tall or short.
* $(\forall P)[Tall(P) \vee Short(P)]$

3.3 Everyone is tall or everyone is short.
* $[(\forall P)Tall(P)] \vee [(\forall P)Short(P)]$

3.4 Nobody is at home.
* $(\forall P)(\neg AtHome(P))$ 

3.5 If John comes, all the women will leave.
* $Come(John) \Rightarrow (\forall P)[Woman(P) \Rightarrow Leave(W)]$

3.6 If a man comes, all the women will leave.
* $(\exists P)[Man(P) \wedge Come(P)] \Rightarrow (\forall P)[Woman(P) \Rightarrow Leave(P)]$

4.1 The equation $x^2 + a = 0$ has a real root for any real number $a$.
* $(\forall a \in \reals)(\exists x \in \reals)(x^2 + a = 0)$

4.2 The equation $x^2 + a = 0$ has a real root for any negative real number $a$.
* $(\forall a \in \reals)[(a \lt 0) \Rightarrow (\exists x \in \reals)(x^2 + a = 0)]$
* For any real number $a$, if it happens that $a$ is negative, then there is a $x$ which solve the equation $x^2 + a = 0$.
* <font color = red> Note: The order of $x$ and $a$ is important, the $a$ has to come first, because the $x$ depends on the $a$. </font>

4.3 Every real number is rational.
* $(\forall x \in \reals)(\exists m \in \natnums)(\exists n \in \natnums)[(m = nx) \vee (m = -nx) \vee (x = 0)]$

4.4 There is an irrational number.
* $(\exists x \in \reals)(\forall m \in \natnums)(\forall n \in \natnums)[(m \neq nx) \wedge (m \neq -nx)]$

4.5 There is no largest irrational number.
* ANSWER 1: $(\forall y \in \reals)(\exists x \in \reals)[(x > y) \wedge (\forall m \in \natnums)(\forall n \in \natnums)(m \neq nx)]$
* ANSWER 2: $(\forall y \in \reals)[(\forall m \in \natnums)(\forall n \in \natnums)(m \neq ny) \Rightarrow (\exists x \in \reals)[(x > y) \wedge (\forall m \in \natnums)(\forall n \in \natnums)(m \neq nx)]]$

5.1 All domestic cars are badly made. 
* Let $C$ be the set of all cars, let $D(x)$ mean that $x$ is domestic, and let $M(x)$ mean that $x$ is badly made.
* $(\forall x \in C)[D(x) \Rightarrow M(x)]$

5.2 All foreign cars are badly made.
* $(\forall x \in C)[\neg D(x) \Rightarrow M(x)]$

5.3 All badly made cars are domestic.
* $(\forall x \in C)[M(x) \Rightarrow D(x)]$

5.4 There is a domestic car that is not badly made.
* ANSWER 1: $(\exists x \in C)[\neg M(x) \wedge D(x)]$
* ANSWER 2: $(\exists x \in C)[D(x) \nRightarrow M(x)]$
* ANSWER 3: $(\exists x \in C)[D(x) \wedge \neg M(x)]$

5.5 There is a foreign car that is badly made.
* $(\exists x \in C)[\neg D(x) \wedge M(x)]$

6\. You can find a rational number between any two unequal real numbers.
* Let $Q(x)$ mean that $x$ is rational.
* $(\forall x \in \reals)(\forall y \in \reals)[(x < y) \Rightarrow (\exists z \in \reals)[Q(z) \wedge (x < z < y)]]$

7\. You may fool all the people some of the time, you can even fool some of the people all of the time, but you cannot fool all of the people all the time.
* Let $F(p, t)$ mean "You can fool person $p$ at time $t$".
* $[\exists t \forall p F(p, t)] \wedge [\exists p \forall t F(p, t)] \wedge \neg [\forall p \forall t F(p, t)]$

8\. Every six seconds a driver is involved in an accident.
* Let $x$ be a variable to denote a driver, $t$ a variable for a six second interval, and let $A(x, t)$ be the property that $x$ is in an accident during interval t.
* $\forall t \exists x A(x, t)$

9\. A driver is involved in an accident every six seconds. (literal meaning)

* $\exists x \forall t A(x, t)$

10\. The symbol $\exists!$ means "There exists a unique $x$ such that...". Rewrite the expression $\exists!x \phi(x)$.
* $(\exists x)[\phi(x) \wedge (\forall y)[\phi(y) \Rightarrow (x = y)]]$

11\. Rewrite "The arithmetic operation $x \uparrow y$ is not commutative.". ($\uparrow$ is just some arbitrary binary operation.)
* $\exists x \exists y [x \uparrow y \neq y \uparrow x]$

12\. There is no largest prime.
* $(\forall x)(\exists y)[Prime(y) \wedge (y > x)]$

## Lecture 6 - Working with Quantifiers

In mathematics, and in everyday life, you often find yourself having to negate a statement involving quantifiers.

You can do it simply by putting a negation symbol in front but that's not enough. You need to produce a positive assertion, less a negative one.

Roughly speaking, a positive statement is one that says what is rather what is not.

In practice, a positive statement is one that contains no negation symbol, or else one in which any negation symbols.

<font color = red> Notes: </font>

* <font color = red> $\neg [\forall x A(x)]$ is equivalent to $\exists x [\neg A(x)]$. </font>
* <font color = red> $\neg [\exists x A(x)]$ is equivalent to $\forall x [\neg A(x)]$. </font>
* <font color = red> $\forall x [A(x) \wedge B(x)]$ is equivalent to $\forall x A(x) \wedge \forall x B(x)$. </font>
* <font color = red> $\exists x [A(x) \vee B(x)]$ is equivalent to $\exists x A(x) \vee \exists x B(x) $. </font>
* <font color = red> $\forall$ is "like" $\wedge$, and $\exists$ is "like" $\vee$. </font>

The negation of "All prime number bigger than $2$ are odd."
* The origin statement: $(\forall x \gt 2)(Prime(x) \Rightarrow Odd(x))$
* The negation: $(\exists x > 2)(Prime(x) \wedge \neg Odd(x))$

### Assignment

Negate the following statements and put each answer in positive form:

1. $(\forall x \in \natnums)(\exists y \in \natnums)(x + y = 1)$
   ANSWER: $(\exists x \in \natnums)(\forall y \in \natnums)(x + y \neq 1)$

2. $(\forall x > 0)(\exists y < 0)(x + y = 0)$ ($x$, $y$ are real number variables)
   ANSWER: $(\exists x > 0)(\forall y < 0)(x + y \neq 0)$

3. $\exists x (\forall \epsilon \gt 0)(- \epsilon \lt x \lt \epsilon)$ ($x$, $\epsilon$ are real number variables)
   ANSWER: $\forall x (\exists \epsilon \gt 0)[(- \epsilon \geq x) \vee (x \geq \epsilon)]$

4. $(\forall x \in \natnums)(\forall y \in \natnums)(\exists z \in \natnums)(x + y = z^2)$
   ANSWER: $(\exists x \in \natnums)(\exists y \in \natnums)(\forall y \in \natnums)(x + y \neq z^2)$

5. The standard definition of a real function $f$ being *continuous* at a point $x = a$ is $(\forall \epsilon \gt 0)(\exists \delta \gt 0)(\forall x)[|x - a|] < \delta \Rightarrow |f(x) - f(a)| < \epsilon]$.
   ANSWER ($f$ being discontinuous at $a$): $(\exists \epsilon > 0)(\forall \delta > 0)(\exists x)[|x - a| < \delta \wedge |f(x) - f(a)| \geq \epsilon]$

Claim: If an integer $N$ is divisible by a prime $p$, then $N + 1$ is not divisible by $P$.
Proof:
* $N$ is divisible by $p$, then there is an integer $q$ such that $N = pq$.
* Suppose $(N + 1)$ is divisible by $P$, then there is an integer $r$ such that $(N + 1) = pr$.
* Then $(N + 1) - N = pq - pr = p(q - r) = 1$.
* It means $1$ is divisible by $p$, but it is a contradiction. Since $p$ is a prime number, and a prime number is at least equal to $2$. So, $p$ can not divide into $1$. 
* Thus, $(N + 1)$ is not divisible by $p$.

## Lecture 7 - Proofs

Proofs are constructed for two main purposes, to **establish truth** and to **communicate to others**.

The most important feature of a proof is its **logical structure**.

What makes a proof a proof isn't the fact that you call it a proof, it isn't the fact that you end in a QED (or $\Box$). It's the logical flow of the steps. It has to be logically precise and you have to be able to follow it.

***Theorem: There are infinitely many primes.***

1. List the primes in increasing order as $p_1, p_2, ..., p_n, ...$ and show that the list must continue for ever.
2. Given the list up to some stage $n$, $p_1, p_2, ..., p_n$, show there is another prime that can be added to the list.
3. Let $N$ be the number we get when we multiply together all the primes we have listed so far and then add 1:
   $N = (p_1 \cdot p_2 \cdot ... \cdot p_n) + 1$
4. Obviously, $N$ is bigger than all the primes in out list.
5. If $N$ is prime, we know there is a prime bigger than $p_n$, and hence the list can be continued.
6. If $N$ is not prime, then there must be a prime $q < N$ such that $q$ divides $N$.
7. But none of $p_1, ..., p_n$ divides $N$, since the division of $N$ by any one of these leaves a remainder of $1$.
8. So, $q$ must be bigger than $p_n$. Hence there is a prime bigger than $p_n$, and the list can be continued.
9. Either way, there is another prime to add to the list.
10. It follows that there are infinitely many primes. The result is proved. $\Box$

***Theorem: $\sqrt{2}$ is irrational.***

1. Assume, on the contrary, that $\sqrt{2}$ were rational.
2. Then there are natural numbers $p, q$ with no common factors, such that $\sqrt{2} = p / q$.
3. Squaring and rearranging, $2q^2 = p^2$. So $p^2$ is even. Hence $p$ is even.
4. So for some natural number $r$, such that $p = 2r$.
5. Substituting for $p$, $2q^2 = 4r^2$. So $q^2 = 2r^2$.
6. So $q^2$ is even, then $q$ is even.
7. So $p, q$ are both even, they have $2$ as the common factor.
8. But this is impossible, since $p, q$ have no common factors.
9. Hence the original assumption that $\sqrt{2}$ were rational must be false.
10. Hence $\sqrt{2}$ must be irrational. $\Box$

### Proof by contradiction

Proof by contradiction is a general method that works as follow:

1. You want to prove some statement $\phi$.
2. You start by assuming $\neg \phi$.
3. You reason until you reach a conclusion that is false.
   * Often by deducing both $\psi$ and $\neg \psi$ for some $\psi$. (e.g. "$p, q$ have no common factors" and "$p, q$ are both even.")
4. A true assumption cannot lead to a false conclusion. 
5. Hence the assumption of $\neg \phi$ must be false.
6. In other words, $\phi$ must be true.

Proof by contradiction is a good way to prove that something does not exist.

### Proof by cases 

***Theorem: If $r, s$ are irrational, then $r^s$ is rational.***

* Consider $\sqrt{2} ^ {\sqrt{2}}$.
* If it is rational, let $r = s = \sqrt{2}.$
* If it is irrational, let $r = \sqrt{2} ^ {\sqrt{2}}, s = \sqrt{2}$. Then $r ^ s = {\sqrt{2}} ^ {{\sqrt{2}} \cdot  {\sqrt{2}}} = 2$, which is rational.
* The theorem is proved.


### Prove by contrapositive

Conditional involving quantifiers are sometimes handled by proving the contrapositive.
* To prove $\phi \Rightarrow \psi$, prove $(\neg \psi) \Rightarrow (\neg \phi)$.

To prove a bi-conditional $\phi \Leftrightarrow \psi$, we generally construct two proofs, one of $\phi \Rightarrow \psi$, the other of $\psi \Rightarrow \phi$.

Occasionally, it is easier to prove the two conditional $\phi \Rightarrow \psi$ and $(\neg \phi) \Rightarrow (\neg \psi)$.

## Lecture 8 - Proofs with Quantifiers

To prove $\forall x A(x)$, one way is to take an arbitrary $x$ and show that it satisfies $A(x)$. e.g. To prove $\forall n \exists m (m > n^2)$

* Let $n$ be an arbitrary natural number.
* Set $m = n ^ 2 + 1$, then $m > n^2$.
* This proves $\exists m (m > n^ 2)$.
* Since $n$ is an arbitrary natural number, then it follows that $\forall n \exists m (m > n^2)$.

Another approach is to use the method of contradiction. 

* To prove $\forall x A(x)$, assume $\neg \forall x A(x)$. 
* This is equivalent to $\exists x \neg A(x)$.
* Let $c$ be an object that $\neg A(c)$.
* Now reason with $c$ and the fact that $\neg A(c)$ to derive a contradiction.

### Proof by induction

Universal quantified statements of the form $(\forall n \in \natnums) A(x)$, are often proved by a method know as **induction**.

To prove $\forall n A(n)$, establish the following two statements:

1. $A(1)$, initial step.

2. $(\forall n)[A(n) \Rightarrow A(n + 1)]$, induction step.

Intuitively, this gives $\forall n A(n)$ as follows:

* By step 1, $A(1)$.
* By Step 2, $A(1) \Rightarrow A(2)$, so from $A(1)$ we can conclude $A(2)$.
* By $A(2)$ and the induction step, we can conclude $A(3)$.
* ...

***Theorem:*** $(\forall n \in \natnums) [1 + 2 + 3 + ... + n = {1 \over 2} n (n + 1)]$

* For $n = 1$, the identity reduces to $1 = {1 \over 2} \cdot 2 \cdot 1$, which is true, since both sides equal $1$.

* Assume the identity hold, for $n$, i.e., $ + 2 + 3 + ... + n = {1 \over 2} n (n + 1)]$ (*).

* Add $(n + 1)$ to both sides of the (*):
  $1 + 2 + ... + n + (n + 1) = {1 \over 2} n (n + 1) + (n + 1) = {1 \over 2} (n + 1) (n + 2)$, which is identity with $n + 1$ in place of $n$.

* Hence by the principle of mathematical induction, the identity holds for all $n$.

***Theorem:*** If $x > 0$, then for any $n$, ${(1 + x)}^{n + 1} > 1 + (n + 1)x$

* Let $A(n)$ be the statement ${(1 + x)}^{n + 1} > 1 + (n + 1)x$.

* $A(1)$ is the statement $(1 + x)^2  = 1 + 2x + x^ 2$. Since $x > 0$, then $(1 + x)^ 2 > 1 + 2x$.

* To prove $\forall n [A(n) \Rightarrow A(n + 1)]$, pick an arbitrary $n$ and prove $A(n) \Rightarrow A(n + 1)$. We assume $A(n)$ and deduce $A(n + 1)$.

* Since $x > 0$, then $(1 + x)(1 + x)^{n + 1} > (1 + x)[1 + (n + 1)x] = 1 + (n + 1)x + x + (n + 1) x^2 = 1 + (n + 2)x + (n + 1) x^2 > 1 + (n + 2)x$.

* This proves $A(n + 1)$. The theorem follows by induction. $\Box$

**<font color = red>  Summary </font>** 

1. You want to prove that some statement $A(n)$ is valid for all natural numbers $n$.

2. First prove $A(1)$. Usually a matter of simple observation.

3. Given an algebraic argument to establish the conditional $A(n) \Rightarrow A(n + 1)$.
   - Reduce $A(n + 1)$ to a form where you can use $A(n)$.

4. Conclusion: By the principle of mathematical induction, this proves $\forall n A(n)$.

### Common variant of induction

We sometimes need to prove a statement of the form $(\forall n \geq n_0) A(n)$.

The first step is to verify $A(n_0)$. 

The induction step is to prove $(\forall n \geq n_0) [A(n) \Rightarrow A(n + 1)]$.

***Theorem:*** Every natural number greater than $1$ is either prime or a product of primes.

* The induction statement $A(n)$ is $\forall m [2 \leq m \leq n \Rightarrow m \text{ is either a prime or a product of primes}]$

* For $n = 2$, $A(2)$ says "$2$ is either prime or a product of primes", which is true.

* Assume $A(n)$ and deduce $A(n + 1)$. Let $m$ be a natural number, $2 \leq m \leq (n + 1)$.

* If $m \leq n$, then by $A(n)$, $m$ is either a prime or a product of primes.

* If $m = n + 1$, and if $n + 1$ is prime, then $m$ is prime.

* If $m = n + 1$, and $n + 1$ is not prime, then there are natural numbers $p, q$ such that $1 < p, q < n + 1$ and $n + 1 = pq$.

* Since $2 \leq p, q \leq n$, by $A(n)$, $p, q$ are either primes or products of primes.

* Hence $n + 1$ is a product of primes.

* The theorem follows by induction.

**<font color = red> Notes: </font>**

* A prime number is a positive integer $n$, greater than $1$, whose only exact divisors are $1$ and $n$.
  
* $0$ is an integer, but is not a natural number.

## Lecture 9 - Number Theory

Arithmetic is about calculation, but number theory examines the abstract properties of numbers.

### Division Theorem

***Theorem (Division Theorem):*** Let $a, b$ be integers, $b > 0$. Then there are unique integers $q, r$ such that $a = q \cdot b + r$ and $0 \leq r < b$.

* We prove existence first, then uniqueness.

* Existence: Look at all non-negative integers of the form $a - kb$, where $k$ is an integer, and show that one of then is less than $b$.

* Such integers do exist. Take $k = - |a|$. Then, since $b \geq 1$ ($b$ is positive integer), $a - kb = a + |a|b \geq a + |a| \geq 0$.

* Let $r$ be the smallest such integer. Let $q$ be the value of $k$ for which it occurs, i.e., $r = a - qb$.

* To complete the proof, we show that $r < b$. Suppose, on the contrary, that $r \geq b$.

* Then, $a - (q + 1)b  = a - qb - b = r - b \geq 0$.

* Thus, $a - (q + 1)b$ is a non-negative integer of the form $a - kb$. But $r$ is the smallest such, and yet $a - (q + 1)b < a - qb = r$. Contradiction. Hence $r < b$.

* That proves existence.

* Uniqueness: We show that if there are two representations of $a$, $a = qb + r = q^\prime b + r^\prime, 0 \leq r, r^\prime < b$, then $r = r^\prime$ and $q = q^\prime$.

* Rearranging the above equation:
  (1) $r^\prime - r = b(q - q^\prime)$

* Taking absolute values in (1):
  (2) $|r^\prime - r| = b|q - q^\prime|$ ($b$ is positive integer)

* Since $-b < -r \leq 0$ and $0 \leq r^\prime < b$, so $-b < r - r^\prime < b$, then $|r^\prime - r| < b$.

* So by (2), $b|q^\prime - q| < b$, then $|q^\prime - q| < 1$. Since $q, q^\prime$ are integers, $q = q^\prime$.

* Then by (1), $r = r^\prime$.

* That proves uniqueness.

***Theorem (General Division Theorem):*** Let $a, b$ be integers, $b \neq 0$. Then there are unique integers $q, r$ such that $a = qb + r$ and $0 \leq r < |b|$.

* We have proved the result in the case $b > 0$, so assume $b < 0$.

* Then, since $|b| > 0$, the previous theorem tells us there are unique integers $q^\prime, r^\prime$, such that $a = q^\prime |b| + r^\prime$ and $0 \leq r^\prime < |b|$.

* Let $q = -q^\prime, r = r^\prime$. Then, since $|b| = -b$, we get $a = qb + r, 0 \leq r < |b|$. It follows the previous theorem.

* The number $q$ is called the ***quotient*** of $a$ by $b$, and $r$ is called the ***remainder***.

### Divisibility

If division of $a$ by $b$ produces a remainder $r = 0$, we say $a$ is divisible by $b$.

Hence, $a$ is divisible by $b$ iff there is an integer $q$ such that $a = bq$.

NOTATION: $b|a$ denotes $a$ is divisible by $b$.

<font color = red> WARNING: $b|a$ is not the same as $a/b$. </font>

* $b|a$ denotes the relation that $b$ divides $a$, i.e., there is an integer $q$ such that $a = qb$.

* $a/b$ is a notation that denotes the rational number $a$ divided by $b$.

* In the case where $b|a$, we have $q = a/b$.

* Thus, $b|a$ iff $a/b$ is an integer.

### Prime number

A prime number is an integer $p > 1$ that is divisible only by $1$ and $p$.

### Basic properties of divisibility

***Theorem:*** Let $a, b, c, d$ be integers, $a \neq 0$. Then:
1. $a | 0, a | a$.
2. $a | 1$ iff $a = \pm 1$.
3. If $a | b$ and $c | d$, then $ac|bd$ (for $c \neq 0$).
4. If $a|b$ and $b|c$, then $a|c$ (for $b \neq 0$).
5. $[a|b \text{ and } b|a]$ iff $a = \pm b$.
6. If $a|b$ and $b \neq 0$, then $|a| \leq |b|$.
7. If $a|b$ and $a|c$, then $a|(bx + cy)$ for any integers $x, y$.

### Fundamental theorem of arithmetic

***Euclid's Lemma:*** If a prime $p$ divides a product $ab$, then $p$ divides at least one of $a, b$.

***Theorem:*** Every natural number greater than $1$ is either primer or can be expressed as a product of primes in a way that is unique except for the order in which they are written.

The expression of a number as a product of primes is called its ***prime decomposition***.

Existence proof (by contradiction):

* Suppose there were a composite number (i.e. non prime) that could not be written as a product of primes.

* Then there must be a smallest such number. Call it $n$.

* Since $n$ is not prime, there are numbers $a, b$ with $1 < a, b < n$ such that $n = ab$.

* If a, b are primes, then $n = ab$ is a prime decomposition of $n$ and we have a contradiction.

* If either $a, b$ is composite, then because it is less than $n$, it must be a product of primes, so by replacing one or both of $a, b$ by its prime decomposition in $n = ab$, we get a prime decomposition of $n$, and again we have a contradiction.

* That proves existence.

Uniqueness proof (by contradiction):

* Assume there is a number $n > 1$ that has two (or more) different prime decompositions. Let $n$ be the smallest such number. 
  
* Let 
  (*) $n = p_1p_2...p_r = q_1q_2...q_s$ 
  be two different prime decompositions of $n$.

* Since $p_1$ divides $(q_1)(q_2...q_s)$, by Euclid's Lemma, either $p_1|q_1$ or $p_1 | (q_2...q_s)$.

* Hence, either $p_1 = q_1$ or else $p_1 = q_i$ for some $i$ between $2$ and $s$.

* Then we can delete $p_1$ and $q_i$ from the two decompositions in (*), which gives us a number smaller than $n$ that has two different prime decompositions, contrary to the choice of $n$ as the smallest such.

* That proves uniqueness.

## Lecture 10 - Real Analysis

***Theorem:*** If $r, s$ are rationals, $r < s$, then there is a rational $t$ such that $r < t < s$. [This property is called ***density***. The rational line is dense.]

* Let $t = {1\over2} (r + s)$. Clearly $r < t < s$. Then we need to prove $t$ is rational.

* Since $r, s$ are rational, then there are integers $m, n, p, q$ such that $r = {m \over n}, s = {p \over q}$.

* Then $t = {1 \over 2} (r + s) = {mq + np \over 2nq}$.

* So as $mq, np, 2nq$ are integers, $r$ is rational. $\Box$

<font color = red> Density does not mean there are no holes in the rational line. (e.g. $\sqrt{2}$) </font>

* Let $A = \{ x \in \mathbb{Q} | x \leq 2 \vee x^2 < 2 \}, B = \{ x \in \mathbb{Q} | x > 0 \wedge x^2 \geq 2 \}$.

* Clearly, $A \cup B = \mathbb{Q}$. But, $A$ has no greatest member and $B$ has no smallest member.

* Hence, the rational are inadequate to do mathematic. In $\mathbb{Q}$, we cannot solve the equation $x^2 - 2 = 0$.

<font color = red> Note: $\infin$ is NOT a real number. </font>

### Completeness property

The key property that the real numbers have that the rationals don't have is what's known as a completeness property.

Completeness property is what makes the real numbers great for doing mathematics, and the absence of which makes the rational inadequate for doing mathematics.

Given a set $A$ of reals, a number $b$ such that $(\forall a \in A)[a \leq b]$ is said to be an ***upper bound*** of $A$. We say $b$ is a ***least upper bound*** of $A$ if, in addition, for any upper bound $c$ of $A$, we have $b \leq c$.

The notation used for least upper bound: $$lua(A)$$ [We can make the same definition for $\natnums, \mathbb{Z}, \reals$.]

***Greatest lower bound:***

$$b \leq a \text{ for all } a \in A \text{ and if } c \leq a \text{ for all } a \in A, \text{ then } b \geq c$$

The ***completeness property*** of the real number system says that every nonempty set of reals that has an upper bound, has a least upper bound (in $\reals$). e.g.

* $7$ is the least upper bound of the interval $(-3, 7)$ (Because there is no smaller upper bound of this interval than $7$.)

<font color = red> Notes: </font>

* <font color = red> A set $A$ of integers/rationals/reals has a least upper bound, then it is unique. </font>

* <font color = red> If a set $A$ of integers/rationals/reals has a lower bound (upper bound), it has infinitely many lower bounds (upper bounds). </font>

Let $A$ be a set of integers, rationals, or reals. $b$ is the least upper bound of $A$ iff:
- (a) $(\forall a \in A)(a \leq b); and$
- (b) whenever $c \lt b$ there is an $a \in A$ such that $a \gt c$.

In addition to the completeness property, the ***Archimedean property*** is an important fundamental property of $\reals$. It says that if $x, y \in \reals$ and $x, y \gt 0$, there is an $n \in \natnums$ such that $nx > y$.

### Beginning of "Real Analysis"

***Theorem:*** The rational line is not complete. [Completeness: If $A \subset \reals$ has an upper bound, then it has a least upper bound in $\reals$.]

Proof:

* Let $A = \lbrace r \in \mathbb{Q} | r \geq 0 \wedge r^2 \lt 2 \rbrace$.

* $A$ is bounded above, e.g. $2$ is an upper bound. 

* We need to show that $A$ does not have a least upper bound in $\mathbb{Q}$.

* Let $x \in \mathbb{Q}$ be any upper bound of $A$, and show that there is a smaller one in $\mathbb{Q}$.

* Let $x = p/q$, where $p, q \in \natnums$ ($x$ is non-negative).

* Suppose $x^2 \lt 2$, then $2q^2 \gt p^2$. As $n$ gets larger, $$n^2 \over {2n + 1}$$ increases without bound, so we can pick an $n \in \natnums$ such that $${n^2 \over 2n + 1} \gt {p^2 \over 2q^2 - p^2}$$ Then $$2n^2q^2 \gt (n+1)^2p^2$$ Hence, $$({n+1 \over n})^2 ({p \over q})^2 \lt 2$$ Let $$y = ({n+1 \over n}){p \over q}$$ Since $n, p, q \in \natnums$, then $y \in \mathbb{Q}$ and $y^2 < 2$. 
  So $y \in A$. But $y > x$. This is contradiction, since $x$ is an upper bound of $A$. So $x^2 \geq 2$. Since $\sqrt{2}$ is not rational, $x^2 \gt 2$ ($x$ is an arbitrary upper bound of $A$ in $\mathbb{Q}$). Thus, $p^2 > 2q^2$.

* Pick $n \in \natnums$ so large that $${n^2 \over 2n + 1} \gt {q^2 \over p^2 - 2q^2}$$ Then $$p^2n^2 \gt 2q^2(n+1)^2$$ $${p^2 \over q^2} ({n \over n+1})^2 \gt 2$$
  Let $$y = ({n \over n+1}) {p \over q}$$ Then $y \in \mathbb{Q}$ and $y^2 \gt 2$. Since ${n \over n+1} \lt 1$, we have $y \lt x$. But, for any $a \in A$, $a^2 \lt 2 \lt y^2$, so $a \lt y$. Hence, $y$ is an upper bound of $A$, which is smaller than $x$.

* Since $x$ is an arbitrary upper bound of $A$, and there exists another upper bound $y$ such that $y \lt x$, then $A$ does not have a least upper bound. 
  
* That proves the theorem. $\Box$

<font color = red> The constructing of $\reals$ from $\mathbb{Q}$ can be done in several different ways, but in all cases the aim is to prevent an argument like the above going through for $\reals$. </font>

### Real number sequences

If the numbers in a sequence $\lbrace a_n \rbrace_{n=1}^{\infin}$ get arbitrarily close to some fixed number $a$, we say $\lbrace a_n \rbrace_{n=1}^{\infin}$ ***tends to the limit*** $a$, and write 

$$a_n \rightarrow a \text{ as } n \rightarrow \infin$$

Or, 

$$\lim_{n \rightarrow \infin}a_n = a$$

<font color = red> Notice that not all sequences tend to a limit. </font>

Formal definition: $$a_n \rightarrow a \text{ as } n \rightarrow \infin \iff (\forall \epsilon \gt 0)(\exists n \in \natnums)(\forall m \geq n)[\vert a_m - a \vert \lt \epsilon]$$

* The second part shows that from some point $n$ onwards, all the number in $\lbrace a_n \rbrace_{n=1}^{\infin}$ are within a distance of $\epsilon$ from $a$.

* The intuition is that we can take $\epsilon \gt 0$ as small as we want.

Example:

$$\lim_{n \rightarrow \infin}\frac{1}{n} = 0$$

Proof:

We need to show that 

$$(\forall \epsilon \gt 0)(\exists n \in \natnums)(\forall m \geq n)[\vert \frac{1}{m} - 0 \vert \lt \epsilon]$$

Let $\epsilon \gt 0$ be given (let $\epsilon \gt 0$ be arbitrary). We need to find a $n \in \natnums$ such that 

$$(\forall m \geq n)[\vert \frac{1}{m} \vert \lt \epsilon]$$

Pick any $n$ such that $n \gt \frac{1}{\epsilon}$. Then, if $m \geq n, \frac{1}{m} \leq \frac{1}{n} \leq \epsilon$. That proofs the statement. $\Box$

***The Sandwich Theorem (also called the Squeeze Theorem):*** 

If $\lbrace a_n \rbrace_{n=1}^{\infin}, \lbrace b_n \rbrace_{n=1}^{\infin}, \lbrace c_n \rbrace_{n=1}^{\infin}$ are sequences such that, from some point $n_0$ onwards, 

$$a_n \leq b_n \leq c_n,$$

and if

$$\lim_{n \rightarrow \infin}a_n = L, \lim_{n \rightarrow \infin}c_n = L,$$

then $\lbrace b_n \rbrace_{n=1}^{\infin}$ is convergent and 

$$\lim_{n \rightarrow \infin}b_n = L$$

Example:

Prove that $(n \ (n + 1))^2 \rightarrow 1$ as $n \rightarrow \infin$.
  Proof: Given $\epsilon \gt 0$, we need an $N$ s.t.,
  $$n \geq N \Rightarrow \vert (\frac{n}{n+1})^2 - 1 \vert \lt \epsilon$$,
   i.e., s.t.,
  $$n \geq N \Rightarrow \vert \frac{n^2 - n^2 - 2n - 1}{(n+1)^2} \vert \lt \epsilon$$
   i.e., s.t.,
  $$n \geq N \Rightarrow \frac{2n + 1}{(n+1)^2} \lt \epsilon$$
   Pick $N$ so big that 
  $$\frac{(N + 1)^2}{2N + 1} \gt \frac{1}{\epsilon}$$
  Then
  $$n \geq N \Rightarrow \frac{2n+1}{(n+1)^2} \leq \frac{2N+1}{(N+1)^2} \lt \epsilon$$
  This proves the statement. $\Box$

## Supplement - Set Theory

The concept of a *set* is extremely basic and pervades the whole of a present-day mathematical thought. Any well-defined collection of objects is a set. For instance we have:

* the set of all students in your class

* the set of all prime numbers

* the set whose only member is you

All it takes to determine a set is some way of specifying the collection. (Actually, that is not correct. In the mathematical discipline called abstract set theory, arbitrary collections are allowed, where there is no defining property.)

If $A$ is a set, then the objects in the collection $A$ are called either the *members* of $A$ or the *elements* of $A$. We write $$x \in A$$ to denote that $x$ is an element of $A$.

Some sets occur frequently in mathematics, and it is convenient to adopt a standard notation for them:

* $\mathbb{N}$: the set of all natural numbers (i.e., the numbers $1, 2, 3, etc.) [Note that $0$ is not regarded as a natural number.]

* $\mathbb{Z}$: the set of all integers ($0$ and all positive and negative whole numbers)

* $\mathbb{Q}$: the set of all rational numbers (fractions)

* $\mathbb{R}$: the set of all real numbers.

Thus, for example, $$x \in \mathbb{R}$$ means that $x$ is a real number. And $$(x \in \mathbb{Q}) \wedge (x > 0)$$ means that $x$ is a positive real number.

There are several ways of specifying a set. If it has a small number of elements we can list them. In this case we denote the set by enclosing the list of the elements in curly brackets; thus, for example, $$\{1, 2, 3, 4, 5\}$$ denotes the set of consisting of the natural numbers $1, 2, 3, 4$ and $5$.

By use of 'dots' we can extend this notation to any finite set; e.g. $$\{1, 2, 3, ..., n\}$$ denotes the set of the first $n$ natural numbers. Again $$\{ 2,3,5,7,...,53 \}$$ could (give the right context) be used to denote the set of all primes up to $53$.

Certain infinite sets can also be described by the use of dots (only now the dots have no end), e.g. $$\{ 2,4,6,8,...,2n,...\}$$ denotes the set of all even natural numbers. Again, $$\{ ..., -8, -6, -4, -2, 0, 2, 4, 6, 8, ...\}$$ denotes the set of all even numbers.

In general, however, except for finite sets with only a small number of elements, sets are best described by giving the property which defines the set. If $A(x)$ is some property, the set of all those $x$ which satisfy $A(x)$ is denoted by $$\{ x | A(x) \}$$ Or, if we wish to restrict the $x$ to those which are members of a certain set $X$, we would write $$\lbrace x \in X | A(x) \rbrace$$ This is read "the set of all $x$ in $X$ such that $A(x)$." For example: $$\mathbb{N} = \lbrace x \in \mathbb{Z} | x > 0 \rbrace$$ $$\mathbb{Q} = \lbrace x \in \mathbb{Q} | (\exists m, n \in \mathbb{Z}) [(m > 0) \wedge (mx = n)]\rbrace$$ $$\lbrace -\sqrt{2}, \sqrt{2} \rbrace = \lbrace x \in \mathbb{R} | x ^ 2 = 2 \rbrace$$ $$\lbrace 1,2,3 \rbrace = \lbrace x \in \mathbb{N} | x < 4 \rbrace$$

Two sets, $A, B$ are *equal*, written $A = B$, if they have exactly the same elements. As the above example shows, equality of sets does not mean they have identical definitions; there are often many different ways of describing the same set. <font color = red> The definition of equality reflects rather the fact that a set is just a collection of objects. </font>

If we have to prove that the sets $A$ and $B$ are equal, we usually split the proof into two parts:

(a) Show that every member of $A$ is a member of $B$.
(b) Show that every member of $B$ is a member of $A$.

Taken together, (a) and (b) clearly imply $A = B$. (The proof of both (a) and (b) is usually of the 'take an arbitrary element' variety. To prove (a), for instance, we must prove $(\forall x \in A)(x \in B)$; so we take an arbitrary element $x$ of $A$ and show that $x$ must be an element of $B$.)

The set notations introduced have obvious extensions. For instance we can write $$\mathbb{Q} = \lbrace m/n | m, n \in \mathbb{Z}, n \neq 0 \rbrace$$ and so on.

It is convenient in mathematics to introduce a set which has no elements: the *empty* set (or *null* set). There will only be one such set, of course, since any two such will have exactly the same elements and thus be (by definition) equal. The empty set is denoted by the Scandinavian letter $$\emptyset$$ [Note that this is not the Greek letter $\phi$.] The empty set can be specified in many ways; e.g. $$\emptyset = \lbrace x \in \mathbb{R} | x^2 < 0 \rbrace$$ $$\emptyset = \lbrace x \in \mathbb{N} | 1 < x < 2 \rbrace$$ $$\emptyset = \lbrace x | x \neq x \rbrace$$  

<font color = red> Notice that $\emptyset$ and $\lbrace \emptyset \rbrace$ are quite different sets. </font> $\empty$ is the empty set: it has NO elements. $\lbrace \emptyset \rbrace$ is a set which has ONE member. Hence $$\empty \neq \lbrace \emptyset \rbrace$$ What is the case here is that $$\empty \in \lbrace \emptyset \rbrace$$ (The fact that the single element of $\empty$ is the empty set is irrelevant in this connection: $\lbrace \emptyset \rbrace$ does have an element, $\empty$ does not.)

A set $A$ is called a *subset* of a set $B$ if every element of $A$ is a member of $B$. For example, $\lbrace 1, 2 \rbrace$ is a subset of $\lbrace 1, 2, 3 \rbrace$. We write $$A \subseteq B$$ to mean that $A$ is a subset of $B$. If we wish to emphasize that $A$ and $B$ are unequal here, we write $$A \subset B$$ and say that $A$is a *proper subset* of $B$ (This usage compares with the ordering relations $\leq$ and $\lt$ on $\mathbb{R}$.)

Clearly, for any sets $A, B$, we have $$A = B \text{ iff } (A \subset B) \wedge (B \subset A)$$