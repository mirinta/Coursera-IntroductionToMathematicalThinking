# Peer-graded Assignment

1. Say whether the following is true or false and support your answer by a proof.
   $$
   (\exists m \in \natnums)(\exists n \in \natnums)(3m + 5n = 12)
   $$
   
   
   
   It's false. If $n \gt 2$, then for any $m$, $3m + 5n \geq 13$, so we need only show that there is no $m$ such that $3m + 5 = 12$, i.e. no $m$ such that $3m = 7$. This is immediate.

---

2. Say whether the following is true or false and support your answer by a proof: 
   $$
   \text {The sum of any five consecutive integers is divisible by 5 (without remainder).}
   $$

   
   
   It's true. Let $n, n + 1, n + 2, n + 3, n + 4$ be any five consecutive integers. Then the sum of them is $5n + 10 = 5(n + 2)$, which proves the result.

---

3. Say whether the following is true or false and support your answer by a proof: 
   $$
   \text{For any integer n, the number } n^2 + n + 1 \text{ is odd.}
   $$
   
   
   
   It's true. Consider the two cases $n$ even and $n$ odd separately.
   
   if $n$ is even, say $n = 2k$, then $n^2 + n + 1 = 4k^2 + 2k + 1 = 2(2k^2 + k) + 1$ which is odd.
   
   if $n$ is odd, say $n = 2k + 1$, then $n^2 + n + 1 = 4k^2 + 4k + 1 + 2k + 1 + 1 = 4k^2 + 6k + 3 = 2(2k^2 + 3k + 1) + 1$ which is odd.
   
   In both cases, $n^2 + n + 1$ is odd.

---

4. Prove that every odd natural number is of one of the forms $4n + 1$ or $4n + 3$, where $n$ is an integer. 
   
   
   
   Let $m$ be a natural number. By the Division Theorem, there are unique numbers $n, r$ such that $m = 4n + r$, where $0 \leq r \lt 4$. Thus $m$ is one of $4n$, $4n + 1$, $4n + 2$, $4n + 3$. Since $4n$ and $4n + 2$ are even, if $m$ is odd, the only possibilities are $4n + 1$ and $4n + 3$.

---

5. Prove that for any integer $n$, at least one of the integers $n$, $n + 2$, $n + 4$ is divisible by $3$.

   
   
   By the Division Theorem, $n$ can be expressed in one of the forms $3q$, $3q + 1$, $3q + 2$, for some $q$. In the first case, $n$ is divisible by $3$. In the second case $n + 2 = 3q + 3 = 3(q + 1)$, so $n + 2$ is divisible by $3$. In the third case $n + 4 = 3q + 6 = 3(q + 2)$, so $n + 4$ is divisible by $3$.

---

6. A class unsolved problem in number theory asks if there are infinitely many pairs of "twin primes", pairs of primes separated by $2$, such as $3$ and $5$, $11$ and $13$, or $71$ and $73$. Prove that the only prime triple (i.e. three primes, each $2$ from the next) is $3$, $5$, $7$.
   
   
   
   Consider any three numbers of the form $n$, $n + 2$, $n + 4$, where $n \gt 3$. By the answer to the previous question, one of these numbers is divisible by 3, and hence is not prime.

---

7. Prove that for any natural number $n$, $2 + 2^2 + 2^3 + ... + 2^n = 2^{n + 1} - 2$.

   
   
   Let $S = 2 + 2^2 + 2^3 + ... + 2^n$. Then $2S = 2^2 + 2^3 + ... + 2^n + 2^{n+1}$. Subtracting the first identity from the second equation gives $2S - S = 2^{n+1} - 2$. But $2S - S = S$, so this establishes the stated identity.

---

8. Prove (from the definition of a limit of a sequence) that if the sequence $\{a_n\}_{n=1}^{\infin}$ tends to limit $L$ as $n \rightarrow \infin$, then for any fixed number $M \gt 0$, the sequence $\{Ma_n\}_{n=1}^{\infin}$ tends to the limit $ML$.

   

   Let $\epsilon \gt 0$ be given. By the assumption, we can find an $N$ such that $n \geq N \Rightarrow \vert a_n - L \vert \lt \frac{\epsilon}{M}$. Then, $n \geq N \Rightarrow \vert Ma_n - ML \vert = M \cdot \vert a_n - L \vert \lt M \cdot \frac{\epsilon}{M} = \epsilon$ which shows that $\{Ma_n\}_{n=1}^{\infin}$ tends to the limit $ML$.

---

9. Given an infinite collection $A_n$, $n = 1,2,...$ of intervals of the real line, their intersection is defined to be $\bigcap_{n=1}^{\infin}A_n = \{x \vert (\forall n)(x \in A_n) \}$. Given an example of a family of intervals, $A_n$, $n = 1,2,...$, such that $A_{n+1} \subset A_n$ for all $n$ and $\bigcap_{n=1}^{\infin}A_n = \empty$. Prove that your example has the stated property.

   

   Let $A_n = (0, \frac{1}{n})$. Clearly, $\bigcap_{n=1}^{\infin}A_n \subseteq A_1 = (0, 1)$. Hence any element of the intersection must be a member of $(0, 1)$. But if $x \in (0, 1)$, we can find a natural number $n$ such that $1 / n \lt x$. Then $x \notin A_n$, so $x \notin \bigcap_{n=1}^{\infin}A_n$. Thus $\bigcap_{n=1}^{\infin}A_n = \empty$. 

---

10. Given an example of a family intervals $A_n$, $n = 1,2,...$, such that $A_{n+1} \subset A_n$ for all $n$ and $\bigcap_{n=1}^{\infin}A_n$ consists of a single real number. Prove that your example has the stated property.
   
    
    
    Let $A_n = [0, \frac{1}{n})$. Clearly,  $0 \in \bigcap_{n=1}^{\infin}A_n$. But the same argument as above shows that no other number is in the intersection. Hence $\bigcap_{n=1}^{\infin}A_n = {0}$.

---