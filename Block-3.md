## Page 1

Block
# 3

## COUNTING PRINCIPLES

<table>
  <tr>
    <td>Unit 1<br>Combinatorics</td>
    <td style="text-align: right;">137</td>
  </tr>
  <tr>
    <td>Unit 2<br>Advanced Counting Principles</td>
    <td style="text-align: right;">157</td>
  </tr>
  <tr>
    <td>Unit 3<br>Recurence Relations</td>
    <td style="text-align: right;">171</td>
  </tr>
  <tr>
    <td>Unit 4<br>Partitions and Distributions</td>
    <td style="text-align: right;">185</td>
  </tr>
</table>

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 2

# BLOCK INTRODUCTION

## Block 3: Counting Principles

Have you ever thought about how you can decide whether a given element belongs to a collection or not? Or, how a communication engineer can find the total number of distinct ways in which a fixed number of dots and dashes can be used for telegraphic communication? Or, how we can count the number of primes less than or equal to a given number? Problems such as these are what we discuss in this block. The primary focus of this block is a variety of techniques used for counting, that is, combinatorial techniques.

In first unit we deal with permutations and combinations, the binomial and multinomial theorems, and combinatorial probability. In this context, you might find it interesting to note that the notion of permutation can be found in the Hebrew work "Sefer Yetzirah" (i.e., The Book of Creation). This is a manuscript written by a mystic some time between 200 and 600 A.D. Also, the 'binomial theorem, which everybody is so familiar with, first appeared in the work of Euclid (300 B.C.) What is of further historical interest is that Blaise Pascal (1623-1662), published in the 1650s a treatise dealing with the relationships among binomial coefficients, combinations, and polynomials. These results were used by Jakob Bernoulli (1645-1705) to prove the general form of the binomial theorem.

The second unit of this block deals with the pigeonhole principle and the principles of inclusion and exclusion. The latter principle has an interesting history, being found in different manuscripts under such names as the "Sieve Method" or the "Principle of Cross Classification". A set-theoretic version of this principle, which concerned itself with set unions and intersection, is found in "Doctrine of Chances" (1718), a text on probability theory by Abraham De Moivre (1667-1754). Somewhat earlier, in 1713, Pierre Remond de Montmort (1678-1719) used the idea behind the principle in his solution of the problem of derangements.

While programmes using recursion are elegant, it is more difficult to perform a run time analysis of such programmes as compared to the programmes that use say iteration. One tool for analysing recursive programmes is the recurrence relation. We set up a relation between the time taken to carry out a task on an input of size n(sorting a list of size n, say) to the time taken to carry out the same task on an input of size n-1 or less. Using this relation, we can get an expression for the time taken to carry out the task on an input of size n. We discuss the setting up and solution of recurrence relations in the third unit block of this block.

In the fourth, and last, unit of this block, we discuss partitions of natural numbers. We consider efficient techniques for counting the number of ways of distributing a finite number of objects into a finite number of containers, usually called boxes. It was Leonard Euler (1707-1783) who advanced the study of partitions of integers in his 1740 volume opus, "Introduction in Analysin Infinitorum"

Before we end, a note of advice! If you really want to get to grips with the content of this block, you must attempt the Miscellaneous Exercises given at the end of the block. Doing this, will help you understand the underlying reasoning better, and hence appreciate the theory of combinatorics.
&lt;watermark&gt;UNIVERSITY&lt;/watermark&gt;

---


## Page 3

# UNIT 1 COMBINATORICS

## Structure

1.0 Introduction
1.1 Objectives
1.2 Multiplication and Addition Principles
1.3 Permutations
    1.3.1 Permutations of Objects not Necessarily Distinct
    1.3.2 Circular Permutations
1.4 Combinations
1.5 Binomial Coefficients
1.6 Combinatorial Probability
1.7 Summary
1.8 Solutions/ Answers

## 1.0 INTRODUCTION

Let us start with thinking about how to assess the efficiency of a computer programme. For this we would need to estimate the number of times each procedure is called during the execution of the programme. How would we do this? The theory of combinatorics helps us in this matter, as you will see while studying this unit.

Combinatorics deals with counting the number of ways in which objects can be arranged according to some pattern (listing). Mostly, it deals with a finite number of objects and a finite number of ways of arranging them. Sometimes an infinite number of objects and infinite number of ways in which they can be arranged are also considered. However, in this unit and block, we shall restrict our discussion to a finite number of objects.

We start our discussion in Sec. 1.2, with two counting principles. These principles help us in counting the number of ways in which a task can be done when it consists of several subtasks, and there are many possible ways of doing the subtasks.

In Sec. 1.3 we look at arrangements of objects in which the order matters. Such arrangements are called permutations. Here we look at various linear and circular permutations, and how to count their number in a given situation.

In Sec. 1.4, we consider arrangements of objects in which the order does not matter. Such arrangements are called combinations. We will consider situations that require us to count combinations. You will see that most of these situations require us to apply the multiplication principle also.

In the next section, Sec. 1.5, we consider binomial and multinomial coefficients. We see how they are related to the objects studied in Sec. 1.4.

Finally, in Sec. 1.6, we consider the applications of what we have presented in the rest of the unit, for finding the probability of the occurrence of an event. As you will see, this application is natural, since we use similar counting arguments for obtaining discrete probabilities. This discussion will be useful for you, for instance, in coding theory as well as in designing **reliable** computer systems.

We continue our study of combinatorics in the next unit. We also have a section of miscellaneous exercises at the end of the block of which several are based on this unit. Doing these exercises, and every exercise given in the unit, will help you achieve the following objectives of this unit.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;137&lt;/page_number&gt;

---


## Page 4

Basic Combinatorics

# 1.1 OBJECTIVES

After going through this unit, you should be able to:

*   explain the multiplication and addition principles, and apply them;
*   differentiate between situations involving permutations and those involving combinations;
*   perform calculations involving permutations and combinations;
*   prove and use formulae involving binomial and multinomial coefficients;
*   apply the concepts presented so far for calculating combinatorial probabilities.

# 1.2 MULTIPLICATION AND ADDITION PRINCIPLES

Let us start with considering the following situation: Suppose a shop sells six styles of pants. Each style is available in 8 lengths, six waist sizes, and four colours. How many different kinds of pants does the shop need to stock?

There are 6 possible types of pants; then for each type, there are 8 possible length sizes; for each of these, there are 6 possible waist sizes; and each of these is available in 4 different colours. So, if you sit down to count all the possibilities, you will find a huge number, and may even miss some out! However, if you apply the multiplication principle, you will have the answer in a jiffy!

So, what is the multiplication principle? There are various ways of explaining this principle. One way is the following:

Suppose that a task/procedure consists of a sequence of subtasks or steps, say, Subtask 1, Subtask 2,..., Subtask k. Furthermore, suppose that Subtask 1 can be performed in n₁, ways, Subtask 2 can be performed in n₂ ways after Subtask 1 has been performed, Subtask 3 can be performed in n₃ ways after Subtask 1 and Subtask 2 have been performed, and so on. Then **the multiplication principle** says that the number of ways in which the whole task can be performed is n₁.n₂....nₖ.

Let us consider this principle in the context of boxes and objects filling them. Suppose there are m boxes. Suppose the first box can be filled up in k(1) ways. For every way of filling the first box, suppose there are k(2) ways of filling the second box. Then the two boxes can be filled up in k(1).k(2) ways. In general, if for every way of filling the first (r – 1) boxes, the rth box can be filled up in k(r) ways, for r = 2,3,..., m, then the total number of ways of filling all the boxes is k(1).k(2)... k(m).

So let us see how the multiplication principle can be applied to the situation above (the shop selling pants). Here k(1) = 6, k(2) = 8, k(3) = 6 and k(4) = 4. So, the different kinds of pants are 6 × 8 × 6 × 4 = 1152 in number.

Let’s consider one more example.

**Example 1:** Suppose we want to choose two persons from a party consisting of 35 members as president and vice-president. In how many ways can this be done?

**Solution:** Here, Subtask 1 is ‘choosing a president’. This can be done in 35 ways. Subtask 2 is ‘choosing a vice-president’. For each choice of president, we can choose the vice-president in 34 ways. Therefore, the total number of ways in which Subtasks 1 and 2 can be done is 35 × 34 = 1190.

* * *

There is another fundamental principle called the **addition principle**. This is applied in situations like the following one:

&lt;page_number&gt;138&lt;/page_number&gt;

---


## Page 5

Combinatorics – An Introduction

Suppose that a task consists of performing exactly one subtask from among a collection of disjoint (mutually exclusive) subtasks, say, Subtask 1, Subtask 2, ..., Subtask k. (i.e., the task is performed if **either** Subtask 1 is performed, **or** Subtask 2,..., or Subtask k is performed.) Further, suppose that Subtask i can be performed in n<sub>i</sub> ways, i = 1,2,..., k. Then, the number of ways in which the task can be performed is the sum n<sub>1</sub>+n<sub>2</sub>+...+n<sub>k</sub>.

Let us consider an example of its application.

**Example 2:** There are three political parties, P<sub>1</sub>, P<sub>2</sub> and P<sub>3</sub>. The party P<sub>1</sub> has 4 members, P<sub>2</sub> has 5 members and P<sub>3</sub> has 6 members in an assembly. Suppose we want to select two persons, both from the same party, to become president and vice-president. In how many ways can this be done?

**Solution:** From P<sub>1</sub>, we can do the task in 4 × 3 = 12 ways, using the multiplication principle. From P<sub>2</sub>, it can be done in 5 × 4 = 20 ways. From P<sub>3</sub> it can be done in 6 × 5 = 30 ways. So, by the addition principle, the number of ways of doing the task is 12 + 20 + 30 = 62.

***

Though both these principles seem simple, quite a number of combinatorial enumerations can be done with them. For instance, what we see from Example 2 is that the addition principle helps us to count all possible arrangements grouped into mutually exclusive and exhaustive classes.

Why don’t you try a few exercises that involve the use of these principles now?

E1) Give a situation related to computing in which the addition principle is used, and one in which the multiplication principle is used.

E2) Find the number of words of length 4, meaningful or not, made with the letters a,b,..., j.

E3) If n couples are at a dance, in how many ways can the men and women be paired for a single dance?

E4) How many integers between 100 and 999 consist of distinct even digits?

E5) Consider all the numbers between 100 and 999 that have distinct digits. How many of them are odd?

Let us now consider certain arrangements of objects, in which the order in which they are arranged matters.

## 1.3 PERMUTATIONS

Suppose we have 15 books that we want to arrange on a shelf. How many ways are there of doing it? Using the multiplication principle, you would say —

15 × 14 × 13 × ... 2 × 1 = 15!

Each of these arrangements of the books is a permutation of the books. Let us define this term formally.

**Definition:** An arrangement of a set of n objects **in a given order** is called a **permutation** of the objects (taken altogether at a time).

n! denotes ‘n factorial’, which means
n × (n − 1) × . × 2 × 1
for any n∈N.)

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;139&lt;/page_number&gt;

---


## Page 6

Basic Combinatorics

An ordered arrangement of the n objects, taking r at a time, (where r ≤ n) is called a permutation of the n objects taking r at a time. The total number of such permutations is denoted by P(n,r).

As an example, let us consider picking out books, three at a time, from the shelf of 15 books. The first book can be chosen in 15 ways, the next in 14 ways, and the third in 13 ways. So the multiplication principle tells us that the total number of permutations of the 15 books taken 3 at a time is P(15,3) = 15 × 14 × 13.

Other notations used for P(n,r) are ^nP_r, P_r^n, _nP_r.

Again, consider the permutations of a,b,c,d, taken 2 at a time. These are ab, ba, ac, ca, ad, da, bc, cb, bd, db, cd, dc. (Note that ab and ba are considered different even though they consist of the same two objects.) Or, we can argue combinatorically as above: The first letter can be chosen in 4 ways, and then the next letter can be chosen. We can list out all the cases in 3 ways. So, the total number of permutations are P(4,2) = 4 × 3 = 12.

Now, is there a formula for finding the value of P(n,r)? This is what the following theorem tells us.

**Theorem 1:** The number of permutations of n objects, taken r at a time, where 0 ≤ r ≤ n, is given by P(n,r) = n!/(n-r)!.

Consider r boxes arranged in a line. Choose one object out of n and place it in the first box. This can be done in n ways. Then from the remaining (n-1) objects choose one and place it in the second box. The first two boxes can be filled in n(n - 1) ways. We continue this operation till the rth box is filled. So, by the multiplication principle, the total number of ways of doing this is n(n - 1) (n - 2) ... (n - r+1).

P(n,r) = n(n - 1)...(n-r+1).
= n(n - 1)...( (n - - r + 1)( (n - r)( (n - - r - 1)...3.2.1
= (n - - r)...( (nn - - r - 1) ...3.2.1
= n!/(n - - r)!

**Proof:** In particular, Theorem 1 tells us that the number of permutation of n objects, taken all at a time, is given by P(n,n) = n!

and P(n, 0) = 1 ∀n∈N.

So, for example, by Theorem 1 we can find P(6,4) = 6.5.4.3 = 6!/6 - 4)! And P(6,0) = 1.

Why don’t you try some exercises now?

E6) If m and n are positive integers, show that (m+n)! ≥ m! + n!.

E7) How many 3-digit numbers can be formed from the 6 digits 2,3,5,7,8,9 if repetitions are not allowed? How many of these numbers are less than 400? How many are even?

E8) How many ways are there to rank n candidates for the job of chief engineer? In how many rankings will Ms. Sheela be in the second place.

&lt;watermark&gt;GOI THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;140&lt;/page_number&gt;

---


## Page 7

Combinatorics – An Introduction

In defining the concept of permutation we assumed that the objects were distinguishable. What does this mean, and what happens if we remove this assumption? Let’s see.

## 1.3.1 Permutation of Objects Not Necessarily Distinct

We have shown that there are P(n,r) ways to choose r objects from a set of n distinct objects and arrange them in linear order. Here we consider the same problem with the relaxed condition that some of the objects in the collection may not be distinguishable.

For example, we consider permutations of the letters of the word DISTINCT. Here there are 8 letters of which 2 are I, 2 are T, and three are 4 other different letters. To count the permutations in such a situation, we have the following result.

**Theorem 2:** Suppose there are n objects classified into k distinct types, with m₁ identical objects of the first type, m₂ identical objects of the second type,..., and mₖ identical objects of the kth type, where m₁+m₂+...+mₖ = n. Then the number of distinct arrangements of these n objects, denoted by P(n; m₁, m₂,...mₖ) is $\frac{n!}{m₁!m₂!...mₖ!}$.

**Proof:** Let x be the number of such permutations. If the objects of Type i are considered distinct, then they can be arranged amongst themselves in m₁! ways, where i = 1,2,..., k. Therefore, by the multiplication principle, the total number of permutations of these n distinct objects, taken all at a time, is xm₁!m₂!...mₖ!.

But this is precisely n! when there are n distinct objects.

Hence, xm₁!m₂!...mₖ! = n!, that is, x = n!/m₁!m₂!...mₖ!

So for example, this result tells us that the number of distinct 8 letter words, not necessarily meaningful, that we can make from the letter of the word “DISTINCT” is $\frac{8!}{2!2!1!1!1!1!} = 14$.

Here are some related exercises.

E9) How many permutations are there of the letters, taken all at a time, of the words (i) ASSESSES, (ii) PATTIVEERANPATTI?

E10) How many licence plates can be made if each should have 3 letters of the English alphabet with no letter repeated? What will be the answer if the letters can be repeated?

&lt;watermark&gt;UNIVERSITY OF PEOPLE'S&lt;/watermark&gt;

So far, we have considered permutations of objects as linear arrangements of objects; this means that we visualize arrangements of objects in a **line**. But there is a variant in which the objects are arranged along the circumference of a circle. Let us consider that now.

## 1.3.2 Circular Permutation

Consider an arrangement of 4 objects, a,b,c,d as in Fig. 1. We observe the objects in the clockwise direction. On the circumference there is no preferred origin, and hence the permutations abcd, bcda, cdab, dabc will look exactly alike. So, each linear

&lt;page_number&gt;141&lt;/page_number&gt;

---


## Page 8

Basic Combinatorics

&lt;img&gt;Fig. 1&lt;/img&gt;

permutation, when treated as a circular permutation, is repeated 4 times. Similarly, if n objects are placed in a circular arrangement, each linear arrangement is repeated n times. So, if we consider all the n! permutations of n things, each circular permutation will be indistinguishable from the (n−1) others obtained by the process of rotating the objects in the same order. So the number of distinct circular permutations will be n!/n = (n−1)!. Thus, we have shown that **the number of circular permutations of n things, taken all at a time, is (n−1)!**.

Let us consider some examples.

**Example 3:** In how many distinct ways is it possible to seat eight persons at a round table?

**Solution:** Clearly we need the number of circular permutations of 8 things. Hence the answer is 7! = 5040.

* * *

**Example 4:** In the preceding question, what would be the answer if a certain pair among the eight persons
(i) must not sit in adjacent seats?
(ii) must sit in adjacent seats

**Solution:** To answer (i), let us first solve (ii) from 7! we have to subtract the number of cases in which the pair of persons sit together. If we consider the pair as forming one unit, then we have the circular permutations of 7 objects, which is (7−1)! (Note that this is the answer for (ii).) But even as a unit they can be arranged in two ways. Hence the required answer is 2(6!). Now to answer (i), we must subtract these possibilities from the total number of ways of seating all the people. This is 7!−2(6!) = 3600.

* * *

**Example 5:** Suppose there are five married couples and they (10 people) are made to sit about a round table so that neither two men nor two women sit together. Find the number of such circular arrangements.

**Solution:** Five females can be made to sit about a round table in (5−1)! = 4! ways. One male can be seated in between two females. There are five positions, and hence they can be made to sit in 5! ways. By the multiplication principle, the total number of ways of such seating arrangements is 4! × 5! = 2880.

* * *

&lt;watermark&gt;INDIA THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;142&lt;/page_number&gt;

---


## Page 9

Combinatorics – An Introduction

**Example 6:** Consider seven people seated about a round table. How many circular arrangements are possible if at least one of them will not have the same neighbours in any two arrangements?

**Solution:** The two distinct arrangements in Fig. 2 show that each has the same neighbours.

&lt;img&gt;Fig. 2 - Two circular arrangements with the same neighbours.&lt;/img&gt;

Hence, the total number of circular arrangements = (7-1)! × $\frac{1}{2}$ = 360.

* * *

You may try the following exercise.

E11) If there are 7 men and 5 women, how many circular arrangements are possible in which women do not sit adjacent to each other?

Permutations apply to ordered arrangement of objects. What happens if order does not matter? Let’s see.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

## 1.4 COMBINATIONS

Let’s begin by considering a situation where we want to choose a committee of 3 faculty members from a group of seven faculty members. In how many distinct ways can this be done? Here order doesn’t matter, because choosing F₁, F₂, F₃ is the same as choosing F₂, F₁, F₃, and so on. (Here Fᵢ denotes the ith faculty member.) So, for every choice of members, to avoid repetition, we have to divide by 3!. Thus, the number would be $\frac{7 \times 6 \times 5}{3!} = \frac{7!}{3!4!}$.

More generally, suppose there are n distinct objects and we want to select r objects, where $r \leq n$, where the order of **the objects in the selection does not matter**. This is called a **combination** of n things taken r at a time. The number of ways of doing this is represented $_n C_r$, $_n C_r^n$, $C_r^n$, $\binom{n}{r}$ or C(n,r). We will use the notation C(n, r), in conformity with the notation P(n,r) for permutations. We read C(n,r) as ‘n choose r’ to emphasize the fact that only **choice** is involved but **not ordering**.

In the example that we started the section with, you saw that the number of combinations was 7!/3!4!, i.e., $\frac{P(7,3)}{3!}$. In fact, this relationship between C(n, r) and P(n, r) is true in general. We have the following result.

**Theorem 3:** The number of combinations of n objects, taken r at a time, where $0 \leq r \leq n$ is given by

&lt;page_number&gt;143&lt;/page_number&gt;

---


## Page 10

Basic Combinatorics

C(n,r) = P(n,r)/r! = n!/((n-r)!r!)

**Proof:** C(n, r) counts the number of ways of choosing r out of n distinct objects without regard to the order. Any one of these choices is simply a subset of r objects of the set of n objects we have. Such a set can be ordered in r! ways. Thus, to each combination, there corresponds r! permutations. Hence there are r! times as many permutations as there are combinations. Hence, by the multiplication principle, we get P(n, r) = r! C(n,r)

Therefore, C(n,r) = P(n,r)/r! = n!/((n-r)!r!)

Using Theorem 3, we can very quickly find out, for instance, how many ways thereare of choosing 2 rooms out of 20 rooms offered. This is C(20,2) = 20!/18!2!

Now, to find C(20,2), I took a short cut. I cancelled 18! From the number and denominator. In practice, I only needed to calculate 20×19/(2×1). This practice is useful, in general, i.e., we use the identity C(n, r) = n(n−1)...r factors/(r(r−1)...r factors) for calculations. In fact, sometimes r is much larger than n−r, in which case we cancel r!. This is also what the following result suggests.

**Theorem 4:** C(n, r) = C(n, n−r), for 0 ≤ r ≤ n, n∈N.

**Proof 1:** For every choice of r things from n things, there uniquely corresponds a choice of n−r things from those n objects, which are the unchosen objects. This one-to-one correspondence shows that these numbers must be the same. This proves the theorem.

**Proof 2:** C(n, r) = n!/((n−r)!r!) = n!/((n−r)!(n−n−r))! = C(n, n−r).

Because of these two theorems we have, for instance,

C(n, n) = C(n, 0) = P(n, 0) = 1. C(n, 1), and = C(n, n−1) = P(n, 1) = n.

The numbers C(n, r) are also called the binomial coefficients as they occur as the coefficients of x^r in the expansion of (1+x)^n in ascending powers of x, as you will see in Sec. 1.5. At this stage, let us consider some examples involving C(n, r).

**Example 7:** Evaluate C(6, 2), C(7, 4) and C(9, 3).

**Solution:** C(6, 2) = 6.5/2.1 = 15, C(7, 4) = 7.6.5/3.2.1 = 35, and C(9, 3) = 9.8.7/3.2.1 = 84.

**Example 8:** Find the number of distinct sets of 5 cards that can be dealt from a deck of 52 cards.

**Solution:** The order in which the cards are dealt is not important. So, the required number is C(52, 5) = 52!/5!47! = (52×51×50×49×48)/(5×4×3×2×1) = 2,598,960.

&lt;page_number&gt;144&lt;/page_number&gt;
&lt;watermark&gt;GOVERNMENT OF THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 11

Combinatorics – An Introduction

**Example 9:** Suppose a valid computer password consists of 8 characters, the first of which is the digit 1, 3 or 5. The rest of the 7 characters are either English alphabets or a digit. How many different passwords are possible?

**Solution:** Firstly, the initial character can be chosen in C(3, 1) ways. Now, there are 26 alphabets and 10 digits to choose the rest of the characters from, and repetition is allowed. So, the total number of possibilities for these characters is (26+10)⁷.

Therefore, by the multiplication principle, the number of passwords possible are C(3, 1).36⁷.

Here are some exercises now.

E12) At a certain office, a committee consisting of one male and one female worker is to be constituted from among 12 men and 15 women workers. In how many distinct ways can this be done?

E13) In how many ways can a prize winner choose any 3 CDs from the ‘Ten Best’ list?

E14) How many different 7-person committees can be formed, each containing 3 women and 4 men, from a set of 20 women and 30 men?

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

So far we have been considering combinations of distinct objects. Let us now look at combinations in which repetitions are allowed. We start with considering the following situations.

Suppose five friends stop at a sweet shop where each of them has one of the following: a samosa, a dosa, and a vada. The order of consumption does not matter. How many different purchases are possible?

Let s, t, and d represent samosa, dosa, vada, respectively. In the following table we have listed some possible ways of purchasing these. For instance, the second row represents the possibility that all 5 friends order only dosas.

<table>
<thead>
<tr>
<th>s</th>
<th>d</th>
<th>v</th>
</tr>
</thead>
<tbody>
<tr>
<td>x</td>
<td>x</td>
<td>xxx</td>
</tr>
<tr>
<td>xxx</td>
<td>xxxx</td>
<td>xx</td>
</tr>
</tbody>
</table>

These orders can also be represented by x’s and |’s. For instance, the first row can be written as x | x | xxx. So, any order will consist of five x’s and two |’s.

Conversely, any sequence of five x’s and two |’s represents an order. So, there is a 1-to-1 correspondence between the orders placed and sequences of five x’s and two |’s. But the number of such sequences is just the number of distinct ways of placing 2 |’s in 7 possible places. This is C(7,2).

More generally, if we wish to select with repetition, r out of n distinct objects, we are considering all arrangements of r of one kind (say x’s) and n−1 of the other kind (say |’s) (because (n−1) |’s are needed to separate n types).

The following result gives us the total number of such possibilities.

**Theorem 5:** Let n and r be natural numbers. Then the number of solutions in natural numbers, to the equation x₁ + x₂ + ... + xₙ = r, is C(n + r − 1,r). Equivalently, the

&lt;page_number&gt;145&lt;/page_number&gt;

---


## Page 12

Basic Combinatorics

number of ways to choose r objects from a collection of n objects, with repetition allowed, is C(n + r - 1, r).

**Proof:** Any string will consist of r objects and n - 1 bars, to denote the n different categories in which these objects can fall. So, it will be a string of length n + r - 1, containing exactly r stars and n - 1 bars. The total number of such strings is the number of ways we can position (n - 1) bars in r different places. This is C(n + r - 1, r).

Now we demonstrate how such strings correspond to solution of the equation x₁ + ... + xₙ = r.

n - 1 bars in the string divide the string into n substrings of stars. The number of stars in these n substrings are the values of x₁, x₂, ..., xₙ. Since there are r stars altogether, the sum is r. Therefore, is a one-to-one correspondence between the strings and the solutions, and the theorem is proved.

Let us consider examples of the use of this result.

**Example 10:** In how many ways can a prize winner choose three books from a list of 10 best sellers, if repeats are allowed?

**Solution:** Here, note that a person can choose all three books to be the same title. Applying Theorem 5, the solution is C(10 + 3 - 1, 3) = C(12, 3) = 220.

* * *

**Example 11:** Determine the number of integer solutions to the equation x₁ + x₂ + x₃ + x₄ = 7, where xᵢ ≥ 0 for all i = 1,2,3,4.

**Solution:** The solution of the equation corresponds to a selection, with repetition, of size 7 from a collection of size 4. Hence, there are C(4 + 7 - 1, 7) = 120 solutions. (n = 4, r = 7 in Theorem 5.)

* * *

So, from this sub-section, we see the equivalence of the following:

(a) The number of integer solutions of the equation x₁ + x₂ + ... + xₙ = r, xᵢ ≥ 0, 1 ≤ i ≤ n.

(b) The number of selections, with repetition, of size r from a collection of size n.

(c) The number of ways r identical objects can be distributed among n distinct containers.

Why don't you try some exercises now?

E15) A student in a college hostel is allowed four fruits per day. There are 6 different types of fruits from which she can choose what she wants. For how many days can a student make a different selection?

E16) An urn contains 15 balls, 8 of which are red and 7 are black. In how many ways can:
i) 5 balls be chosen so that all 5 are red?
ii) 7 balls be chosen so that at least 5 are red?

&lt;page_number&gt;146&lt;/page_number&gt;
&lt;watermark&gt;GOHILL'S UNIVERSITY&lt;/watermark&gt;

---


## Page 13

Combinatorics – An Introduction

In this section we have considered choosing r objects, with repetition, out of n objects, regardless of order. What happens when order comes into the picture? Let’s consider an example.

**Example 12:** A box contains 3 red, 3 blue and 4 white socks. In how many ways can 8 socks be pulled out of the box, one at a time, if order is important?

**Solution:** Let us first see what happens if order isn’t important. In this case we count the number of solutions of r+b+w = 8, 0 ≤ r, b ≤ 3, 0 ≤ w ≤ 4. To apply Theorem 5, we write x = 3 − r, y = 3 − b, z = 4 − 10.

Then we have x+y+z = 10−8 = 2, and the number of solutions this has is C(3+2−1,2) = 6.

These 6 solutions are (1, 0, 1) (0, 1, 1), (1, 1, 0), (2, 0, 0), (0, 2, 0), (0, 0, 2). So, the corresponding solutions for (r, b, w) are

(3, 3, 2), (2, 3, 3), (3, 2, 3), (3, 1, 4), (2, 2, 4), (1, 3, 4).

Now, we consider order. From Theorem 2 we know that the number of ways of pulling out 3 red, 3 blue and 2 white socks in some order is $\frac{8!}{3!3!2!}$. This number would be the same if you had 2 red, 3 blue and 3 white socks, etc. By this reasoning and considering all different orderings, the number of possibilities is

$3\left(\frac{8!}{3!3!2!}\right) + 2\left(\frac{8!}{3!1!4!}\right) + \frac{8!}{2!2!4!} = 3220.$

* * *

What we see, via Example 13, is that if we want to find the number of possibilities wherein order matters and repetition is allowed them:

**Step 1:** Find the possibilities when order doesn’t matter, using Theorem 5;

**Step 2:** Use Theorem 2, to find the possibilities for each solution obtained in Step 1.

Why don’t you try and exercise now?

---

E17) How many 6-letter words, not necessarily meaningful can be formed from the letters of CARACAS?

Let us now consider why C(n,r) shows up as the coefficients in the binomial expansions.

## 1.5 BINOMIAL COEFFICIENTS

You must be familiar with expressions like a+b, p+q, x+y, all consisting of two terms. This is why they are called binomials. You also know that a **binomial expansion** refers to the expansion of a positive integral power of such a binomial. For instance, $(a+b)^5 = a^5 + 5a^4b + 10a^3b^2 + 10a^2b^3 + 5ab^4 + b^5$ is a binomial expansion. Consider coefficients 1, 5, 10, 10, 5, 1 of this expansion. In particular, let us consider the coefficient 10, of $a^3b^2$ in this expansion. We can get this term by selecting a from 3 of the binomials and b from the remaining 2 binomials in the product $(a+b)(a+b)(a+b)(a+b)(a+b)$. Now, a can be chosen in C(5, 3) ways, i.e., 10 ways. This is the way each coefficient arises in the expansion.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;147&lt;/page_number&gt;

---


## Page 14

Basic Combinatorics

The same argument can be extended to get the coefficients of $a^r b^{n-r}$ in the expansion of $(a+b)^n$. From the n factors in $(a+b)^n$, we have to select r for a and the remaining (n - r) for b. This can be done in C(n, r) ways. Thus, the coefficient of $a^r b^{n-r}$ in the expansion of $(a+b)^n$ is C(n, r).

In view of the fact that C(n, r) = C(n, n - r), the coefficients of $a^r b^{n-r}$ and $a^{n-r} b^r$ will be the same. r can only take the values 0, 1, 2, ..., n. We also see that C(n, 0) = C(n, n) = 1 are the coefficients of $a^n$ and $b^n$. Hence we have established the binomial expansion.

$(a+b)^n = a^n + C(n, 1) a^{n-1} b + C(n, 2) a^{n-2} b^2 + ... + C(n, r) a^{n-r} b^r + ... + b^n.$

In analogy with 'binomial', which is a sum of two symbols, we have 'multinomial' which is a sum of two or more (though finite) distinct symbols. Multinomial expansion refers to the expansion of a positive integral power of a multinomial. Specifically we will consider the expansion of $(a_1 + a_2 + ... + a_m)^n$. For the expansion we can use the same technique as we use for the binomial expansion. We consider the nth power of the multinomial as the product of n factors, each of which is the same multinomial. Every term in the expansion can be obtained by picking one symbol from each factor and multiplying them. Clearly, any term will be of the form $a_1^{r_1} a_2^{r_2} ... a_m^{r_m}$ where $r_1, r_2, ..., r_m$ are non-negative integers such that $r_1 + r_2 + ... + r_m = n$. Such a term is obtained by selecting $a_1$ from $r_1$ factors, $a_2$ from $r_2$ factors **from among the remaining (n-r_1) factors**, and so on. This can be done in

$C(n, r_1) \cdot C(n-r_1, r_2) \cdot C(n-r_1-r_2, r_3) ... C(n-r_1-r_2-...-r_{m-1}, r_m)$ ways.
If you simplify this expression, it will reduce to $\frac{n!}{r_1! r_2! ... r_m!}$.

So, we see that the **multinomial expansion** is

$(a_1 + a_2 + ... + a_m)^n = \sum \frac{n!}{r_1! r_2! ... r_m!} a_1^{r_1} a_2^{r_2} ... a_m^{r_m}$

where the summation is over all non-negative integers $r_1, r_2, ..., r_m$ adding to n.

The coefficient of $a_1^{r_1} a_1^{r_1} ... a_m^{r_m}$ in the expansion of $(a_1 + a_2 + ... + a_m)^n$ is $\frac{n!}{r_1! r_2! ... r_m!}$, and is called a **multinomial coefficient**, in analogy with the binomial coefficient. Werepresent this by C(n; r₁, r₂, ..., rₘ). This is also represented by many authors as

$\left[ \begin{matrix} n \\ r_1, r_2, ..., r_m \end{matrix} \right]$.

For instance, the coefficient of $x^2 y^2 z^2 t^2 u^2$ in the expansion of $(x + y + z + t + u)^{10}$ is C(10; 2, 2, 2, 2, 2) = 10!/(2!)⁵.

Let us see an example involving such coefficients.

**Example 13:** What is the sum of the coefficients of all the terms in the expansion of $(a+b+c)^7$?

**Solution:** The required answer is $\sum \frac{7!}{r! s! t!}$, where the summation is over all non-negative integers r, s, t adding to n. But it is also the value of $\sum \frac{7!}{r! s! t!} a^r b^s c^t$ for a = b = c = 1.

So the answer is $(1+1+1)^7 = 3^7$.

* * *

&lt;watermark&gt;GOVERNMENT OF THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;148&lt;/page_number&gt;

---


## Page 15

Combinatorics – An Introduction

This short detour was just to give you an idea of the way in which the Cs and Ps can be extended. Let us now consider some identities involving the binomial coefficients. We first consider Pascal’s formula.

**Theorem 6 (Pascal’s formula):** For all positive integers n and all r such that $1 \leq r \leq n$, $C(n + 1, r) = C(n, r) + C(n, r - 1)$.

**Proof 1:** The left hand side of the identity represents the number of ways of choosing r things out of (n+1) distinct things. Suppose we select an object from the (n+1) things and mark it. Then the number of combinations in which the marked thing is absent is $C(n, r)$, as we then choose r things out of the unmarked n things. The number of combinations in which the marked thing is present is $C(n, r-1)$, as we have to choose $(r - 1)$, things out of the unmarked things, and attach the marked thing to it to make r things. Pascal’s formula now follows from the fact that the sum of the last two numbers mentioned must be equal to $C(n+1, r)$.

**Proof : 2** $C(n,r) + C(n, r-1) = \frac{n!}{(n-r)!r!} + \frac{n!}{(n-r+1)!(r-1)!}$

$= \frac{n!}{r!(n + 1 - r)!} (n-r + 1 + r) = C(n+1,r).$

Pascal’s formula gives us a recursive way to calculate the binomial coefficients, since it tells us the value of $C(n, r)$ in terms of binomial coefficients with a smaller value of n. Note that we use the fact that $C(n, 0) = 1$ for all $n \geq 0$ to start the recursion, since Theorem 6 only applies for $1 \leq r \leq n$. This recursive approach allows us to form Pascal’s triangle, the display of the binomial coefficients shown in Fig.4.

The nth row of Pascal’s triangle gives the binomial coefficients $C(n, r)$ as r goes from0 (at the left) to n (at the right); the top row is Row D. This consists of just the number1, for the case n = 0. The left and right borders are all 1’s, reflecting the fact that $C(n,0) = C(n, n) = 1$ for all n. Each entry in the interior of the Pascal’s triangle is the sum of the two entries immediately above it to the left and right. We call this property the **Pascal property**. For example, each 15 in Row 6 (remember that we are starting the count of rows with 0) is the sum of the 10 and the 5 immediately above it.

&lt;watermark&gt;UNIVERSITY OF PEOPLE'S&lt;/watermark&gt;

<table>
  <tr>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>2</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>3</td>
    <td>3</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>4</td>
    <td>6</td>
    <td>4</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>5</td>
    <td>10</td>
    <td>10</td>
    <td>5</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>6</td>
    <td>15</td>
    <td>20</td>
    <td>15</td>
    <td>6</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>7</td>
    <td>21</td>
    <td>35</td>
    <td>35</td>
    <td>21</td>
    <td>7</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>8</td>
    <td>28</td>
    <td>56</td>
    <td>70</td>
    <td>56</td>
    <td>28</td>
    <td>8</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>9</td>
    <td>36</td>
    <td>84</td>
    <td>126</td>
    <td>126</td>
    <td>84</td>
    <td>36</td>
    <td>9</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>10</td>
    <td>45</td>
    <td>120</td>
    <td>210</td>
    <td>252</td>
    <td>210</td>
    <td>120</td>
    <td>45</td>
    <td>10</td>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
    <td>11</td>
    <td>55</td>
    <td>165</td>
    <td>330</td>
    <td>462</td>
    <td>462</td>
    <td>330</td>
    <td>165</td>
    <td>55</td>
    <td>11</td>
    <td>1</td>
  </tr>
</table>

Fig. 3: Pascal’s triangle

The diagonals of Pascal’s triangle are also interesting. The diagonal parallel to the left edge but moved one unit to the right reads (from the top down) 1, 2, 3, 4, 5,..., reflecting the fact that $C(n, 1) = n$ for $n \geq 1$. The next diagonal to the right, reading 1,

&lt;page_number&gt;149&lt;/page_number&gt;

---


## Page 16

Basic Combinatorics

3, 6, 10, 15,..., reflects the fact that differences increase by 1 as we move down the diagonal.

Let us now consider some identities involving binomial coefficients.

**Identity 1:** C(n, 0) + C(n, 1) + C(n, 2) + ... + C(n, n-1) + C(n, n) = 2^n

By setting a = b = 1 in the binomial expansion of (a+b)^n, we get this identity. In the context of sets, it tells us the number of distinct subset that can be formed from a set with n elements. Note that the number of subsets containing precisely r elements is C(n, r). Hence the total number of subsets is Σ_{r=0}^{n} C(n, r) = 2^n, by the identity. So, this identity tells us that **the number of distinct subsets of a set with n elements is 2^n.**

**Identity 2:** C(n, 0) - C(n, 1) + C(n, 2) - ... + (-1)^n C(n, n) = 0.

We get this by setting a = 1, b = -1 in the expansion of (a+b)^n.

Now, adding the two identities, we get
2 Σ_{r even} C(n, r) = 2^n, i.e., Σ_{r even} C(n, r) = 2^(n-1)

Similarly subtracting the second identity from the first leads us to the equation
Σ_{r odd} C(n, r) = 2^(n-1).

These two equations tell us that the number of subsets of a set of n elements with an even number of elements is equal to the number of subsets with an odd number of elements, both being 2^(n-1).

Why don't you try to prove some identities now?

---

E18) Show that C(n, m) C(m, k) = C(n, k) C(n-k, m-k), 1 ≤ k ≤ m ≤ n.

E19) Prove that C(k, k) + C(k + 1, k) + C(k + 2, k) + ... + C(n, k) = C(n+1, k+1) for all natural numbers k ≤ n.

---

Before ending this section, we just mention another extension of the definition of binomial coefficients. So far, we have defined C(n, r) for n ≥ r ≥ 0. We can extend this definition for any real number x, and any non-negative integer k, by
C(x, k) = (x(x-1)...(x-k+1)) / k!.

This definition coincides with that of C(n, k), when n is a non-negative integer.

So far, in this unit, we have considered various ways of counting different kinds of arrangements. These methods are, not surprisingly, helpful in finding the probability of an event. We shall now discuss this.

---

## 1.6 COMBINATORIAL PROBABILITY

Historically, counting problems have been closely associated with probability. The probability of getting at least 6 heads on 10 flips of a fair coin, the probability of finding a defective bulb in a sample of 25 bulbs if 5 percent of the bulbs from which the sample was drawn are defective — all these probabilities are essentially counting problems. In fact, Pascal's triangle (Fig. 3) was developed by Pascal around 1650 while analysing some gambling probabilities.

&lt;page_number&gt;150&lt;/page_number&gt;
&lt;watermark&gt;GOVERNMENT OF THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 17

Combinatorics – An Introduction

Let us start by recalling some basic facts about probability. An **experiment** is a clearly defined procedure that produces one of a given set of outcomes. The set of all outcomes is called **the sample space** of the experiment.

For example, the experiment could be checking the weather to see if it is raining or not on a particular day. The sample space here would be {raining, not raining}.

Given an experiment, we can often associate more than one sample space with it. For instance, suppose the experiment is the tossing of two coins.
i) If the observer wants to record the number of tails observed as the outcomes, the sample space is {0, 1, 2}.
ii) If the outcomes are the sequence of heads and tails observed, then the sample space is {HH, HT, TH, TT}.

A subset of the sample space of an experiment is called an **event**. For example, for an experiment consisting of tossing 2 coins, with sample space {HH, HT, TH, TT}, the event that two heads do **not** show up is the subset {HT, TH, TT}.

Suppose X is a sample space of an experiment with N out comes. Then, the events are all the $2^N$ subsets of X. The empty set $\phi$ is called the **impossible event**, and the set X itself is called the **sure event**.

Now, for the purpose of this course, we will assume that all the outcomes of an experiment are **equally likely**, that is, there is nothing to prefer one case over the other. For example, in the experiment of coin tossing, we assume that the coin is unbiased. This means that ‘head’ and ‘tail’ are equally likely in a toss. The toss itself is considered a random mechanism ensuring ‘equally likely’ outcomes. Of course, there are coins that are ‘loaded’, which means that one side of the coin may be heavier than the other. But such coins are excluded from our discussion. Also, in our discussions we shall always assume that our **sample space is finite**.

Given this background, we have the following definition.

**Definition:** Then the **probability of the event A**, represented by **P(A)**, is $\frac{n(A)}{n(X)}$.

For instance, the probability that a card selected from a desk of 52 cards is a spade is $\frac{13}{52}$, because A is the set of 13 spades in the deck.

We represent the number of elements of a finite set A, i.e., the **cardinality** of A, by n(A) or |A|.

From the definition, we get the following statements:
i) As n ($\phi$) = 0, it follows that P($\phi$) = 0.
ii) By definition, P(X) = $\frac{n(X)}{n(X)}$=1.
iii) If A and B are two events, then n(A$\cup$B) = n(A) + n(B) - n(A$\cap$B). Therefore, P(A$\cup$B) = P(A)+P(B) - P(A$\cap$B).
iv) (Addition Theorem in Probability) : If A and B are two mutually exclusive events, then the probability of their union is the sum of the probabilities of A and B. i.e., if A$\cap$B = $\phi$, then P(A$\cup$B) = P(A) + P(B).

[This is a consequence of (i) and (iii) above.]

v) Suppose A is an event. Then the probability of A$^c$ (also denoted by A$'$), the event complementary to A, or the event ‘not A’ is 1 – P(A), i.e.,
P(A$^c$) = 1 – P(A).

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;151&lt;/page_number&gt;

---


## Page 18

Basic Combinatorics

The reason is that the events A and A^c are mutually exclusive and exhaustive, i.e., A ∪ A^c = X and P(A) + P(A^c) = 1.

vi) (The generalised addition theorem) : If the events A₁, A₂,...,A_m are pairwise disjoint (i.e., mutually exclusive), then P(U A_i) = Σ P(A_i).

Let us consider some examples from combinatorial probability.

**Example 14:** A die is rolled once. What are the probabilities of the following events?

(i) getting an even number,
(ii) getting at least 2,
(iii) getting at most 2,
(iv) getting at least 10.

**Solution:** If we call the events A, B, C and D, then we have X = {1, 2, 3, 4, 5, 6}, A = {2,4,6}, B = {2,3,4,5,6}, C = {1,2}, and D = φ.
Hence, P(A) = 3/6, P(B) = 5/6, P(C) = 2/6, P(D) = 0.

* * *

**Example 15:** A coin is tossed n times. What is the probability of getting exactly r heads?

**Solution:** If H and T represent head and tail, respectively, then X consists of sequences of length n that can be formed using only the letters H and T. Therefore, n(X) = 2^n. The event A consists of those sequences in which there are precisely r Hs. So, n(A) = C(n, r). Hence, the required probability is C(n, r)/2^n.

* * *

**Example 16:** Two dice, one red and one white, are rolled. What is the probability that the white die turns up a smaller number than the red die?

**Solution:** If the number on the red die is x and that on the white die is y, then X consists of the 36 pairs (x, y), where x and y can be any integer from {1, 2, 3, 4, 5, 6}.
For the event A, we need x < y. For x = 1, 2, 3, 4, 5, y can be x + 1, x+2,..., 6, i.e., 6 - x in number. Thus, by the addition principle,
n(A) = Σ (6 - x) = 5 + 4 + 3 + 2 + 1 = 15.
x=1
Hence, P(A) = 15/36 = 5/12.

* * *

**Example 17:** If a five-digit number is chosen at random, what is the probability that the product of the digits is 20?

**Solution:** If X is the collection of all 5-digit numbers, then n(X) = 9.10⁴ = 90000. Now, 20 can be factored in only two ways, viz., 1.1.1.4.5 and 1.1.2.2.5, as the product of five factors. Of course, these factors can be permuted to give all possible cases for A. The numbers 5, 4, 1, 1, 1 can be permuted in 5!/1!1!1! = 20 ways, and the numbers 5, 2, 2, 1, 1 can be permuted in 5!/1!2!2! = 30 ways.
So, n(A) = 20 + 30 = 50.

&lt;page_number&gt;152&lt;/page_number&gt;
&lt;watermark&gt;GOVERNMENT OF THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 19

Hence, P(A) = 50/90000 = 1/1800.

* * *

**Example 18:** Suppose A and B are mutually exclusive events such that P(A) = 0.3 and P(B) = 0.4. What is the probability that

i) A does not occur?
ii) A or B occurs?
iii) Either A or B does not occur?

**Solution:**

i) This is P(A^c) = 0.7.
ii) This is P(A ∪ B) = 0.7.
iii) This is P(A^c ∪ B^c) = P[(A ∩ B)^c] = P(∅^c) = P(X) = 1

* * *

Try some exercises now.

E20) A,B,C and D are four candidates for a chairperson’s post. Suppose that A is twice as likely to be elected as B, B is thrice as likely as C, and C and D are equally likely to be elected. What is the probability of election of each candidate?

E21) In a ten-question true-false exam, a student must achieve six correct answers to pass. If she selects her answers randomly, what is the probability that she will pass?

There are several other methods for solving combinatorial problems. These will be taken up in the next two units. Let us now summarise what we have covered in this unit.

## 1.7 SUMMARY

In this unit we have discussed some counting techniques. Specifically, we have covered the following points.

1. The multiplication and addition principles for counting the number of ways in which a task can be completed.

2. What a permutation is, the derivation of the formula P(n,r) = n!/(n-r)!, and its application for solving problems.

3. The number of distinct arrangement of n objects of which m₁ are of Type 1, m₂ are of Type 2,..., mₖ are of Type k, where m₁, m₂ + ... ,mₖ = n, is P(n; m₁, m₂,...,mₖ) = n!/m₁!m₂ !...mₖ !

4. What a circular permutation is, and that the number of such permutations of n objects, taken all at a time, is (n-1)!

5. What a combination is, the derivation of the formula

&lt;watermark&gt;Combinatorics – An Introduction&lt;/watermark&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;153&lt;/page_number&gt;

---


## Page 20

Basic Combinatorics

C(n,r) = P(n,r) / r! = n! / (n-r)r!, and its application for solving problems.

6. The proof and applications of the fact that the number of ways of choosing r objects from a collection of n objects, with repetition allowed, is C(n+r-1,r).

7. Why C(n,r) is called a binomial coefficients, and its analogue for multinomials.

8. Some identities involving C(n,r), including Pascal's formula
   C(n+1,r) = C(n,r) + C(n,r-1).

9. The use of counting techniques for finding some discrete probabilities.

# 1.8 SOLUTIONS/ ANSWERS

E1) For instance, both principles are used to find the number of ways in which 17 files are stored if there are 3 storage locations of 1000 K each and 10 files are of 100 K, 5 of 200 K and 2 of 500 K.

E2) Here we apply the multiplication principle. Each letter has 10 possibilities. Therefore, the total number of words is 10⁴.

E3) Suppose we number the men as 1, 2, 3,..., n. Then the first man can be paired with any of the n women, the second can be paired with any from the remaining (n - 1) women, and so on. Hence, the number of ways of pairing is n(n - 1)... 1 = n!.

E4) By the multiplication principle, the number of integers between 100 and 999 with all digits even is 4.5.5 = 100 (Note that the first digit cannot be zero, but the second and third digits can be 0.)

E5) For a number to be odd the last digit should be odd. So, the last position can be filled up in 5 ways. If the middle position is filled up by 0, then the first position can be filled up in 8 ways. Thus the number of odd numbers with 0 in the middle position and all digits distinct is 40, by the multiplication principle.

If the middle position is filled up by a digit other than 0, then this can be done in 8 ways. Then the first position can be filled up in 7 ways. So, the number of odd numbers with all digits distinct with the middle digit not zero is 5.8.7 = 280.

Thus, by the addition principle the answer is 40 + 280 = 320.

E6) (m + n)! = (m + n) (m + n - 1) ... (m + 1) m!.
   => (m + n)! - m! = ≥ mⁿ + n! ≥ m! [n! + mⁿ - 1]
   => (m + n)! - m! - n! ≥ n! (m! - 1) + m! (mⁿ - 1) ≥ 0.

E7) Without repetitions, the number is P(6, 3). For the number to be less than 400, the leftmost digit can only be 2 or 3. The rest of the digits can be filled in P(5, 2) ways. So, the total number of numbers less than 400 will be 2P(5, 2). Similarly, the total number of even numbers is 3P(5, 2).

Note: That the addition principle has been used in both cases.

E8) A ranking is an ordering of the n candidates. This can be done in P(n,n) = n! ways. The total number of rankings in which Sheela is in 2nd place in P(n - 1, n - 1) = (n - 1)!

&lt;page_number&gt;154&lt;/page_number&gt;
&lt;watermark&gt;GOVERNMENT UNIVERSITY&lt;/watermark&gt;

---


## Page 21

E9) In the word 'ASSESSES', we have A once, E twice, and S five times. Thus the number of permutations is 8!/1!2!5! = 168.
In the word 'PATTIVEERANPATTI', R, N and V occur once, P, E and I occur twice, A thrice and T four times. Thus the required number of permutations is 16!/1!1!1!2!2!2!3!4! = 9.10.

E10) By the multiplication principle, the answer is 26.25.24 if the letters cannot be repeated, and 26.26.26 if the letters can be repeated.

E11) The seven men can be seated first. This can be done in 6! ways. The women can sit in between two men. There are seven such places. So, the women can sit in P(7,5) ways. Hence the answer is 6! × P(7,5).

E12) This can be done in C(12, 1).C(15,1) ways, i.e., 180 ways.

E13) This can be done in C(10, 3) ways, i.e., 120 ways.

E14) The total number of possibilities is C(20,3).C(30,4) = 31,241,700.

E15) Applying Theorem 5, we get C(9, 4) = 126 days.

E16) i) Be careful! This is not an application of Theorem 5. This is only the number of ways of choosing 5 balls out of 8 balls, i.e. C(8, 5).
ii) First pick 5 red balls, in C(8,5) ways. Then pick the remaining 2 arbitrarily. These 2 can be chosen in C(2+2-1, 2) = 3 ways. So, the total number of ways is C(8, 5)×3.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
E17) We have 2Cs, 3As, 1R and 1S. If order is not a concern, we consider the solutions of c+a+r+s = 6, 0 ≤ c ≤ 2, 0 ≤ a ≤ 3, 0 ≤ r, s ≤ 1.
We convert this to the equivalent problem x+y+z+t = 1, where x = 2 - c, y = 3 - a, r = 1 - z, s = 1 - t, The number of solutions of this is C(4 + 1 - 1, 1) = 4.
There are (1, 0, 0, 0), (0, 1, 0, 0), (0, 0, 1, 0) and (0, 0, 0, 1).
The corresponding solutions in (c, a, r, s) are (1, 3, 1, 1), (2, 2, 1, 1), (2, 3, 0, 1), (2, 3, 1, 0).
Now order becomes important to us. Applying Theorem 2, the required number is $\frac{6!}{1!3!1!1!} + \frac{6!}{2!2!1!1!} + 2\left(\frac{6!}{2!3!1!0!}\right) = 420$.

E18) The left side counts the ways to select a group of m people chosen from a set of n people and then select a subset of k leaders, say, of this group of m. This can also be done by selecting the subset of k leaders from the set of n people first, and then selecting the remaining m - k members of the group from the remaining n - k people. The number of ways in which this can be done is given on the right hand side. Therefore, the identity.
You can also prove this algebraically.

&lt;page_number&gt;155&lt;/page_number&gt;

---


## Page 22

Basic Combinatorics

E19) One can prove this by induction on the variable n. The base case is trivial, since if n = 0, then k = 0 as well, and the equation reduces to C(0, 0) = C(1, 1), which is true. The induction step is proved by Pascal's formula and the induction hypothesis.

E20) The relative weightages of A, B, C and D are 6.3, 1, 1, respectively. So, P(A) = $\frac{6}{11}$, P(B) = $\frac{3}{11}$, P(C) = $\frac{1}{11}$ = P(D).

E21) The answer is same as the probability of getting at least 6 heads in 10 tosses of a true coin. Hence, the answer is
C(10, 6)/$2^{10}$ + C(10, 7)/$2^{10}$ + C(10, 8)/$2^{10}$ + C(10, 9)/$2^{10}$ + C(10, 10)/$2^{10}$
= (210 + 120 + 45 + 10 + 1)/1024 = 193/512.

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;156&lt;/page_number&gt;

---


## Page 23

# UNIT 2 Advanced Counting Principles

## Structure

2.0 Introduction
2.1 Objectives
2.2 Pigeonhole Principle
2.3 Inclusion-Exclusion Principle
2.4 Applications of Inclusion – Exclusion
    2.4.1 Application to Surjective Functions
    2.4.2 Application to Probability
    2.4.3 Application to Derangements
2.5 Summary
2.6 Solutions/Answers

## 2.0 INTRODUCTION

In this unit, we continue our discussion of the previous unit on combinatorial techniques. We particularly focus on two principles of counting – the pigeonholeprinciple and the principle of inclusion-exclusion.

In Sec. 2.2 you will see how obvious the pigeonhole principle is. Its proof is very simple, and amazingly, it has several useful applications. We shall also include someof these in this section.

In Sec. 2.3, we focus on the principle (or formula) of inclusion-exclusion. As you willsee, this principle tells us how many elements do not fit into any of n categories. We prove this result and also give a generalisation. Following this, in Sec. 2.4 we give several important applications of inclusion-exclusion.

We shall continue our discussion on combinatorial techniques in the next unit.

## 2.1 OBJECTIVES

After studying this unit, you should be able to:

*   prove the pigeonhole principle, and state the generalised pigeonhole principle;
*   identify situations in which these principles apply, and solve related problems;
*   prove the principle of inclusion-exclusion;
*   apply inclusion-exclusion for counting the number of surjective functions,derangements and for finding discrete probability.

## 2.2 PIGEONHOLE PRINCIPLE

Let us start with considering a situation where we have 10 boxes and 11 objects to beplaced in them. Wouldn’t you agree that regardless of the way the objects are placed in the two boxes at least one box will have more than one object in it? On the face of it, this seems obvious. This is actually an application of the pigeonhole principle, which we now state.

**Theorem 1 (The Pigeonhole Principle):** Let there be n boxes and (n+1) objects. Then, under any assignment of objects to the boxes, there will always be a box withmore than one object in it.
This can be reworded as: if m pigeons occupy n pigeonholes, where m > n, then thereis at least one pigeonhole with two or more pigeons in it.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;157&lt;/page_number&gt;

---


## Page 24

Basic Combinatorics

**Proof:** Let us label the n pigeonholes 1, 2, ..., n, and the m pigeons p₁, p₂, ..., pₘ. Now, beginning with p₁, we assign one each of these pigeons the holes numbered 1, ..., n, respectively. Under this assignment, each hole has one pigeon, but there are still (m–n) pigeons left. So, in whichever way we place these pigeons, at least one hole will have more than one pigeon in it. This completes the proof!

&lt;img&gt;Fig. 1 The pigeonhole principle&lt;/img&gt;

This result appears very trivial, but has many applications. For example, using it you can show that:

*   if 8 people are picked in any way from a group, at least 2 of them will have been born on the same weekday.
*   in any group of 13 people, at least two are born in the same month.

Let us consider some examples of its application, in detail.

**Example 1:** Assuming that friendship is mutual, show that in any group of people we can always find two persons with the same number of friends in the group.

**Solution:** If there are n persons in the group, then let the number of friends the ith person has be f(i), i = 1, ..., n. Clearly, f(i) can take values only between 0 and (n – 1).

If some f(i) is 0, it means that the ith person does not have any friends in the group. In this case, no person can be friends with all the other (n – 1) people. So, no f(i) can be (n – 1). So, only one of the values 0 or (n – 1) can be present among the f(i)’s. So, the n f(i)’s can take only (n – 1) distinct values. Therefore, by the pigeonhole principle, two f(i)’s must be equal. Then the corresponding i’s have the same number of friends in the group.

&lt;watermark&gt;UNIVERSITY&lt;/watermark&gt;
* * *

**Example 2:** Suppose 5 points are chosen at random within or on the boundary of an equilateral triangle of side 1 metre. Show that we can find two points at a distance of at most ½ metre.

**Solution:** Divide the triangle into four equilateral triangles of side ½ m by joining the midpoints of the sides by three line segments (see Fig. 2). These four triangles may now be considered as boxes and the five points as objects. By the pigeonhole principle, at least one of these smaller triangles will have two points in or on it. Clearly, the distance between these two points is at most ½ metre.

&lt;img&gt;Fig. 2&lt;/img&gt;

* * *

**Example 3:** Given any ten different positive integers less than 107, show that there will be two disjoint subsets with the same sum.

**Solution:** The highest numbers we could be given would be 97, 98, ..., 106, which add up to 1015. So, consider pigeonholes marked 0, 1, 2,..., 1015. The set of 10 positive integers have 2¹⁰ = 1024 subsets. Put a subset in the pigeonhole marked with the sum of the numbers in the set. The 1024 subsets have to be put in 1016 pigeonholes. So, some pigeonhole will have more than one subset with the same sum.

Now, note that two subsets that we get with the same sum, may not be disjoint. But, by dropping the common elements in them, we are left with disjoint subsets with the same sum.

* * *

Here are some related exercises for you to do.

&lt;page_number&gt;158&lt;/page_number&gt;

---


## Page 25

Some More Counting Principles

E1) If 10 points are chosen in an equilateral triangle of side 3 cms., show that we can find two points at a distance of at most 1 cm.

E2) On 11 occasions a pair of persons from a group of 5 was called for a function. Show that some pair of persons must have attended the function at least twice.

E3) Four persons were found in a queue, independently, on 25 occasions. Show that at least on two occasions they must have been in the queue in the same order.

As you know, **mathematics develops through a process of generalisation**. You know that the principle is valid for n+1 objects and n boxes. It is natural to ask: what if we have, say, 4n+1 objects and 4 boxes? Can we prove a similar principle? In fact, we can, as given below.

**Theorem 2 (The Generalized Pigeonhole Principle):** If nm + 1 objects are distributed among m boxes, then at least one box will contain more than n objects.

This can be reworded as: Let k and n be positive integers. If k balls are put into n boxes, then some box contains at least [k/n] + 1 balls, where [x] denotes the greatest integer less than x.

**Proof:** We prove this by contradiction (see Unit 2, Block 1). Suppose all the m boxes have at most n objects in them. Then the total number of objects is at most nm, a contradiction. Hence, the theorem.

Applying this result, we see, for example, that suppose 479 students are enrolled in the course Discrete Mathematics, consisting of 6 units. Then, at least = $\left\lceil \frac{479}{6} \right\rceil + 1 = 80$ 80 students are studying the same unit at a given point of time.

Let us consider a few more examples of the application of this principle.

**Example 4:** Show that in any group of 30 people, we can always find 5 people who were born on the same day of the week.

**Solution:** 30 people can be assigned to 7 days of the week. Then at least = $\left\lceil \frac{30}{7} \right\rceil + 1 = 5$ of them must have been born on the same day.

* * *

**Example 5:** 20 cards, numbered from 1 to 20, are placed face down on a table. 12 cards are selected one at a time and turned over. If two of the cards add up to 21, the player loses. Is it possible to win this game?

**Solution:** The pairs that can add up to 21 are (1, 20), (2, 19),..., (10, 11). So, there are 10 such pairs. In turning 12 cards, at least one of these pairs will be included. Therefore, the player will lose.

* * *

**Example 6:** Show that every sequence of $n^2 + 1$ distinct integers includes either an increasing subsequence of $n + 1$ numbers or a decreasing subsequence of $n + 1$ numbers.

**Solution:** Let the sequence be $a_1, a_2, ..., a_{n^2+1}$. Suppose there is no increasing subsequence of $n + 1$ numbers. For each of these $a_k$s, let s(k) be the length of the longest increasing subsequence beginning at $a_k$. Since all $n^2+1$ of the s(k)'s are

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;159&lt;/page_number&gt;

---


## Page 26

Basic Combinatorics

between 1 and n, at least $\left\lceil \frac{n^2 + 1}{n} \right\rceil + 1 = n + 1$ of these numbers are the same. (The s(k)'s are the objects and the numbers from 1 to n are the boxes.)

Now, if i < j and s(i) = s(j), then a_i > a_j. Otherwise a_i followed by the longest increasing subsequence starting at a_j would be an increasing subsequence of length s(j) + 1 starting at a_i. This is a contradiction, since s(i) = s(j).

Therefore, all the n + 1 integers a_k, for which s(k) = m, must form a decreasing subsequence of length at least n + 1.

* * *

**Example 7:** Take n integers, not necessarily distinct. Show that the sum of some of these numbers is a multiple of n.

**Solution:** Let S(m) be the sum of the first m of these numbers. If for some r and m, r < m, S(m) - S(r) is divisible by n, then a_{r+1} + a_{r+2} + ... + a_m is a multiple of n. This also means that S(r) and S(m) leave the same remainder when divided by n. So, if we cannot find such pairs m and r, then it means that the n numbers S(1), S(2),..., S(n) leave different remainders when divided by n. But there are only n possible remainders, viz., 0, 1, 2,..., (n --1). So, one of these numbers must leave a remainder of 0. This means that one of the S(i) s is divisible by n. This completes the proof.

In fact, in this example we have proved that one of the sums of consecutive terms is divisible by n.

* * *

You may like to try some exercises now.

---

E4) If any set of 11 integers is chosen from 1, ..., 20, show that we can find among them two numbers such that one divides the other.

E5) If 100 balls are placed in 15 boxes, show that two of the boxes must have the same number of balls.

E6) If a_1, a_2,..., a_n is a permutation of 1, 2,..., n and n is odd, show that the product (a_1 - 1) (a_2 - 2)... (a_n - n) must be even.

---

There are several corollaries to Theorem 2. We shall present one of them here.

**Theorem 3:** If a finite set S is partitioned into s subsets, then at least one of the subsets has $\frac{|S|}{k}$ or more elements.
**Proof:** Let A_1, ..., A_k be a partition of S. (This means that A_i ∩ A_j = ∅ for i ≠ j and S = A_1 ∪ A_2 ∪ ... ∪ A_k.) Then the average value of |A_i| is $\frac{1}{k} [ |A_i| + ... + |A_k| ] = \frac{|S|}{k}$.

A consequence of this result is the following theorem.

**Theorem 4:** Consider a function f: S → T, where S and T are finite sets satisfying |S| > r |T|. Then at least one of the sets f^{-1}(t), t∈T, has more than r elements. (f^{-1}(t) denotes the inverse image of the set {t}, i.e., f^{-1}(t) = {x ∈ S : f(x) = t}.)

&lt;page_number&gt;160&lt;/page_number&gt;
&lt;watermark&gt;GNIGOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 27

Some More Counting Principles

**Proof:** The family {f^(-1)(t): t ∈ T} partitions S into k sets with k ≤ |T|. By Theorem 3, some set in this family, say f^(-1)(t'), has at least $\frac{|S|}{k}$ members. Since $\frac{|S|}{k} \geq \frac{|S|}{T} > r$ by our hypothesis, f^(-1)(t') has more than r elements.

**Corollary:** If f: S → T and |S| > |T|, then f is **not injective**.

**Proof:** Putting r = 1 in Theorem 4, we see that at least one of the sets f^(-1)(t) has more than one element.

We conclude this section with some more extensions of the pigeonhole principle.

**Theorem 5:** Suppose we put an infinity of objects in a finite number of boxes. Then at least one box must have an infinity of objects.

**Proof:** If every box contains only a finite number of objects, then the total number of objects must be finite. Hence the theorem.

**Theorem 6 (A generalisation of Theorem 3):** Let A₁, A₂, ..., Aₖ be subsets of a finite set S such that each element of S is in at least t of the sets Aᵢ. Then the average number of elements in the Aᵢs is at least $t.\frac{|S|}{k}$. (Note that, in this statement, the sets Aᵢ may overlap.)

We leave the proof to you to do, and give you some related exercises now.

E7) Every positive integer is given one of the seven colours in VIBGYOR. Show that at least one of the colours must have been used infinitely many times.

E8) Let A be a fixed 10-element subset of {1, 2,..., 50}. Show that A possesses two different 5-element subsets, the sum of whose elements are equal.

E9) The positive integers are grouped into 100 sets. Show that at least one of the sets has an infinity of even numbers. Is it necessary that at least one set should have an infinity of even numbers and an infinity of odd numbers?

Let us now consider another very important counting principle.

## 2.3 INCLUSION-EXCLUSION PRINCIPLE

Let us begin with considering the following situation: In a sports club with 54 members, 34 play tennis, 22 play golf, and 10 play both. There are 11 members who play handball, of whom 6 play tennis also, 4 play golf also, and 2 play both tennis and golf. How many play none of the three sports?

To answer this, let S represent the set of all members of the club. Let T represent the set of tennis playing members, G represent the set of golf playing members, and H represent the set of handball playing members. Let us represent the number of elements in A by |A|. Consider the number |S| - |T| - |G| - |H|. Is this the answer to the problem? No, because those who are in T as well as G have been subtracted twice. To compensate for this double subtraction, we may now consider the number |S| - |T| - |G| - |H| + |T ∩ G| + |G ∩ H| + |H ∩ T|. Is this the answer? No, because those playing all the three games have been subtracted thrice and then added thrice. But those members have to be totally excluded also. Hence, we now consider the number

&lt;watermark&gt;QAU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;161&lt;/page_number&gt;

---


## Page 28

Basic Combinatorics

$|S| - |T| - |G| - |H| + |T \cap G| + |G \cap H| + |H \cap T| - |T \cap G \cap H|$ This is the correct answer. This reduces to $54 - 34 - 22 - 11 + 10 + 6 + 4 - 2 = 5$.

To solve this problem we have made inclusions and exclusions alternately to arrive at the correct answer. This is a simple case of **the principle of inclusion and exclusion**. It is also known as the **sieve principle** because we subject the objects to sieves of a progressively finer mesh to arrive at a certain grading.

Let us state and prove this principle now.

&lt;watermark&gt;INSTITUTE OF THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

Theorem 7 (The inclusion-exclusion formula): Let A₁, A₂, ..., Aₙ be n sets in a universal set U consisting of N elements. Let Sₖ denote the sum of the sizes of all the sets formed by intersecting k of the Aᵢs at a time. Then the number of elements in none of the sets A₁, A₂, ..., Aₙ is given by
$\left|\overline{A_1} \cap \overline{A_2} \cap ... \cap \overline{A_n}\right| = N - S_1 + S_2 - S_3 + ... + (-1)^k S_k + ... + (-1)^n S_n.$

Proof: The proof is on the same lines of the counting argument given in the ‘sports club’ example at the beginning of this section. If an element is in none of the Aᵢs, then it should be counted only once, as part of ‘N’ in the RHS of the formula above. It is not counted in any of the Sₖs since it is in none of the Aᵢs.

RHS is short for ‘right-hand side’.

Next, an element in exactly one Aᵢ, say Aᵣ, is counted once in N, and once in S₁, and in none of the other Sₖs. So the net count is 1−1 = 0.

Finally, take an element x in exactly m of the Aᵢs. This is counted once in N, m times in S₁, C(m, 2) times in S₂ (since x is in C(m, 2) intersections Aᵢ∩Aⱼ),..., C(m, k) times in Sₖ for k ≤m. x is not counted in any Sₖ for k > m. So the net count of x in the RHS of the formula is
$1 - C(m,1) + C(m,2) - ... + (-1)^k C(m, k) + ... + (-1)^m C(m, m) = 0$, by Identity 2 in Sec. 2.5.
So the only elements that have a net count of 1 in the RHS are those in $\bigcap_{i=1}^{n} \overline{A_i}$. The rest have a net count of 0. Hence the formula.

From this result, we immediately get the following one.

Corollary: Given the situation of Theorem 7,
$|A_1 \cup A_2 \cup ... \cup A_n| = S_1 - S_2 + ... + (-1)^{k-1} S_k + ... + (-1)^{n-1} S_n.$

Why don’t you try and prove this result? (see E 10.)

What the inclusion-exclusion principle tells us is that to calculate the size of A₁∪A₂∪...∪Aₙ, calculate the size of all possible intersections of the sets A₁, A₂,...,Aₙ. Add the results obtained by intersecting an odd number of the sets, and then subtract the results obtained by intersecting an even number of the sets. Therefore, this principle is ideally suited to situations in which
i) we just want the size of A₁∪A₂∪...∪Aₙ, not a listing of its elements, and
ii) multiple intersections are fairly easy to count.

Now let us consider some examples in which Theorem 7 is applied.

Example 8: How many ways are there to distribute r distinct objects into five (distinct) boxes with
i) at least one empty box?
ii) no empty box (r ≥ 5)?

&lt;page_number&gt;162&lt;/page_number&gt;

---


## Page 29

Some More Counting Principles

**Solution:** Let U be all possible distributions of r distinct objects into five boxes. Let A<sub>i</sub> denote the set of possible distributions with the ith box being empty.

i) Then the required number of distributions with at least one empty box is A<sub>1</sub> ∪ A<sub>2</sub> ∪ ... ∪ A<sub>5</sub>. We have N = 5<sup>r</sup>. Also, |A<sub>i</sub>| = (5 - 1)<sup>r</sup>, the number of distributions in which the objects are put into one of the remaining four boxes. Similarly, |A<sub>i</sub> ∩ A<sub>j</sub>| = (5 - 2)<sup>r</sup>, and so forth. Thus, by the corollary above, we have

|A<sub>1</sub> ∪ ... ∪ A<sub>5</sub>| = S<sub>1</sub> - S<sub>2</sub> + S<sub>3</sub> - S<sub>4</sub> + S<sub>5</sub>
= C(5,1)4<sup>r</sup> - C(5,2)3<sup>r</sup> + C(5,3)2<sup>r</sup> - C(5,4)1<sup>r</sup> + 0

ii) |A<sub>1</sub> ∩ A<sub>2</sub> ∩ ... ∩ A<sub>5</sub>| = 5<sup>r</sup> - C(5,1)4<sup>r</sup> + C(5,2)3<sup>r</sup> - C(5,3)2<sup>r</sup> + C(5,4)1<sup>r</sup>, by Theorem 7.

* * *

**Example 9:** How many solutions are there to the equation x + y + z + w = 20, where x, y, z, w are positive integers such that x ≤ 6, y ≤ 7, z ≤ 8, w ≤ 9?

**Solution:** To use inclusion-exclusion, we let the objects be the solutions (in positive integers) of the given equation. A solution is in A<sub>1</sub> if x > 6, in A<sub>2</sub> if y > 7, in A<sub>3</sub> if z > 8, and in A<sub>4</sub> if w > 9. Then what we need is |A<sub>1</sub> ∩ A<sub>2</sub> ∩ A<sub>3</sub> ∩ A<sub>4</sub>|.

Now, to find the total number of **positive** solutions to the given equation, we rewrite it as x<sub>1</sub>+y<sub>1</sub>+z<sub>1</sub>+w<sub>1</sub> = 16, where x<sub>1</sub>=x+1, y<sub>1</sub>=y+1, z<sub>1</sub>=z+1, w<sub>1</sub>=w+1. Any non-negative solution of this equation will be a positive solution of the given equation. So, the number of positive solutions is

N = C(16+4-1, 16) (see Example 11 of Block 3, Unit 1, Page 146)
= C(19, 3).

Similarly, |A<sub>1</sub>| = C(13,3), |A<sub>2</sub>| = C(12,3), |A<sub>3</sub>| = C(11,3),
|A<sub>4</sub>| = C(10,3), |A<sub>1</sub> ∩ A<sub>2</sub>| = C(6,3), |A<sub>2</sub> ∩ A<sub>3</sub>| = C(5,3), and so on. Note that for a solution to be in 3 or more A<sub>i</sub>s, the sum of the respective variables would exceed 20, which is not possible. By inclusion-exclusion, we obtain

|A<sub>1</sub> ∩ A<sub>2</sub> ∩ A<sub>3</sub> ∩ A<sub>4</sub>| = C(19, 3) - C(13, 3) - C(12, 3) - C(11, 3) - C(10, 3)
+ C(6, 3) + C(5, 3) + C(4, 3) + C(4, 3) + C(3, 3) = 217.

* * *

Now you may try the following exercises.

E10) Prove the corollary to Theorem 7.

E11) How many numbers from 0 to 999 are not divisible by either 5 or 7?

Let us now consider applications of the inclusion-exclusion principle to some specific problem types.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;163&lt;/page_number&gt;

---


## Page 30

Basic Combinatorics

# 2.4 APPLICATIONS OF INCLUSION-EXCLUSION

In this section we shall consider three broad kinds of applications — for counting the number of surjective functions, finding probability and finding the number of derangements.

## 2.4.1 Application to Surjective Functions

Let us first recall that a function f : S → T is called **surjective** (or **onto**) if f(S) = T, that is, if for every t ∈ T ∃s ∈ S such that f(s) = t. Now let us prove a very useful result regarding the number of such functions.

**Theorem 8:** The number of functions from an m-element set onto a k-element set is
$$\sum_{i=0}^{k} (-1)^{i} C(k,i)(k-i)m,$$ where $1 \leq k \leq m$.

**Proof:** We will use the inclusion-exclusion principle to prove this. For this, we define the objects to be all the functions (not just the onto functions) from M, an m-element set, to K, a k-element set. For these objects, we will define A_i to be the set of all f: M → K for which the ith element of K is not in f(M). Then what we want is
$$|\overline{A_1} \cap ... \cap \overline{A_k}|.$$

Now, the total number of functions from M to K is $k^m$. Also, the number of mappings that exclude a specific set of i elements in K is $(k - i)^m$, and there are C(k, i) such sets. Therefore, $|A_i| = (k - 1)^m$, $|A_i \cap A_j| = (k - 2)^m$, and so on.

Now, applying Theorem 7, we get
$$|\overline{A_1} \cap ... \cap \overline{A_k}| = k^m - C(k,1)(k - 1)^m + C(k,2)(k - 2)^m - ... + (-1)^{k-1}C(k,k-1)1^m$$

Hence the result.

For example, the number of functions from a five-element set onto a three-element set are $\sum_{i=0}^{k} (-1)^{i} C(k,i)(k - i)^m$ for m = 5 and k = 3, that is, $3^5 - 3.2^5 + 3.1^5 = 150$.

Why don’t you try some exercises now?

E12) Eight people enter an elevator. At each of four floors it stops, and at least one person leaves the elevator. After four floors the elevator is empty. In how many ways can this happen?

E13) How many six-digit numbers contain exactly three different digits?

Now we look at another application.

## 2.4.2 Application to Probability

An important application of the principle of inclusion-exclusion is used in probability. We have the following theorem.

**Theorem 9:** Suppose A_1, A_2, ..., A_n are n events in a probability space. Then

&lt;page_number&gt;164&lt;/page_number&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 31

Some More Counting Principles

P(A₁ ∪ A₂ ∪ ... ∪ Aₙ) = Σₖ₌₁ⁿ (-1)ᵏ⁺¹ Σᵢ₁<i₂<...<iₖ≤n P(Aᵢ₁ ∩ Aᵢ₂ ∩ ... ∩ Aᵢₖ))

**Proof:** Let us begin by observing that A₁ ∪ A₂ ∪ ... ∪ Aₙ means that at least one of the events A₁, A₂, ..., Aₙ occurs. Now, let the ith property be that an outcome belongs to the event Aᵢ. By De Morgan's law, A₁ ∩ A₂ ∩ ... ∩ Aₙ is the complement of A₁ ∪ A₂ ∪ ... ∪ Aₙ. But the principle of inclusion-exclusion gives

|Ā₁ ∩ Ā₂ ∩ ... ∩ Āₙ| = N - Σₖ₌₁ⁿ (-1)ᵏ Σᵢ₁<i₂<...<iₖ≤n |Aᵢ₁ ∩ Aᵢ₂ ∩ ... ∩ Aᵢₖ|, where N is the total number of outcomes.

Now, we divide throughout by N and note that

P(A₁ ∪ A₂ ∪ ... ∪ Aₙ) = 1 - P(Ā₁ ∩ Ā₂ ∩ ... ∩ Āₙ), to get the result.

Let us consider an example of the use of this result.

**Example 12:** Find the probability of a student in a college studying Japanese, given the following data:

All students have to study at least one language out of Hindi, Spanish and Japanese. 65 study Hindi, 45 study Spanish and 42 study Japanese. Further, 20 study Hindi and Spanish, 25 study Hindi and Japanese, 15 study Spanish and Japanese, and 8 study all 3 languages.

**Solution:** The total number of students is |H ∪ S ∪ J|, where H, S and J denote the number of students studying Hindi, Spanish and Japanese, respectively. By the inclusion-exclusion principle,

|H ∪ S ∪ J| = |H| + |S| + |J| - |H ∩ S| - |H ∩ J| - |S ∩ J| + |H ∩ S ∩ J|
= 65 + 45 + 42 - 20 - 25 - 15 + 8 = 100

Therefore, the required probability is $\frac{42}{100} = 0.42$.

* * *

<u>You could do the following exercises now.</u>

E14) What is the probability that a 13-card hand has at least one card in each suit?

E15) What is the probability that a number between 1 and 10,000 is divisible by neither 2, 3, 5 nor 7?

Let us now come to the use of inclusion-exclusion for counting the number of a particular kind of permutation.

## 2.4.3 Application to Derangements

As you know, a permutation of a set is an arrangement of the elements of a set.

So, for example, a rearrangement 1 → 1, 2 → 2, 4 → 3, 3 → 4 is a permutation of the 4-element set {1, 2, 3, 4}. In this permutation, the position of the elements 1 and 2 are fixed, but the positions of 3 and 4 have been interchanged. Now consider the permutation 1 → 4, 2 → 1, 3 → 2, 4 → 3, of {1, 2, 3, 4}, in which the position of

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;165&lt;/page_number&gt;

---


## Page 32

Basic Combinatorics

every element has been changed. This is an example of a derangement, a term we shall now define.

**Definition:** A **derangement** of a set S is a permutation of the elements of S which does not fix any element of S, i.e., it is a rearrangement of the elements of S in which the position of every element is altered.

So, if we treat a permutation as a 1-to-1 function from S to S, then a derangement is a function f:S → S such that f(s) ≠ s ∀ s∈S.

We have the following theorem regarding the number of derangements.

**Theorem 10:** The number of derangements of an n-element set is D<sub>n</sub> = n! ∑<sub>i=0</sub><sup>n</sup> (-1)<sup>i</sup>/i!.

**Proof:** Let A<sub>i</sub> be the set of all permutations of the n-element set that fix i ∀ i = 1, ..., n. Then

D<sub>n</sub> = |∩<sub>i=0</sub><sup>n</sup> A<sub>i</sub><sup>-</sup>| = n! - Σ<sub>i</sub> |A<sub>i</sub>| + Σ<sub>i<j</sub> |A<sub>i</sub> ∩ A<sub>j</sub>| - ... + (-1)<sup>n</sup> |A<sub>1</sub> ∩ ... ∩ A<sub>n</sub>|

= n! - C(n,1)(n-1)! + C(n,2)(n-2)! - ... + (-1)<sup>n</sup>C(n, n)0!

= n!(1 - 1/1! + 1/2! - 1/3! + ... + (-1)<sup>n</sup>1/n!), which is the expression we wanted.

**Remark:** The expression (1 - 1/1! + 1/2! - 1/3! + ... + (-1)<sup>n</sup>1/n!) is the beginning of the expansion for e-1. Even for moderately large values of n, D<sub>n</sub> is very close to n!e<sup>-1</sup>=0.36788 n!.

As an extension of Theorem 10, we have the following results.

**Theorem 11:** For a set of n objects, the number of permutations in which
(i) Only r of these n objects are deranged is
n! - C(r, 1) (n - 1)! + C(r, 2) (n - 2)! - ... + (-1)<sup>r</sup>C(r, r) (n-r);
(ii) exactly r elements are fixed is C(n, r) D<sub>n-r</sub>.

We will not prove these formulae here, but shall consider some examples of their applications.

**Example 12:** Let n books be distributed to n children. The books are returned and distributed to the children again later on. In how many ways can the books be distributed so that no child will get the same book twice?

**Solution:** The required number is (n!)²e<sup>-1</sup>, since corresponding to each first distribution, there are (n!)e<sup>-1</sup> ways of distributing again.

* * *

**Example 13:** Suppose 10 people have exactly the same briefcases, which they leave at a counter. The cases are handed back to the people randomly. What is the probability that no one gets the right case?

**Solution:** The number of possibilities favourable to the event is D<sub>10</sub>. The total number of possibilities is 10!. Thus, the probability that none will get the right briefcase is D<sub>10</sub>/10! = 0.36788.

* * *

&lt;page_number&gt;166&lt;/page_number&gt;
&lt;watermark&gt;GOVERNMENT UNIVERSITY&lt;/watermark&gt;

---


## Page 33

Some More Counting Principles

Note that, since $D_n \approx n!e^{-1}$, the possibility in all such examples is essentially $e^{-1}$, which is independent of n.

You may now try the following exercises.

E16) Each of the n guests at a party puts on a coat when s/he leaves. None of them gets the correct coat. In how many ways can this happen? In how many ways can just one of the guests get the right coat?

E17) In how many ways can the integers 1, 2, 3,...,9 be permuted such that no odd integer will be in its natural position.

E18) Find the number of permutations in which exactly four of the nine integers 1, 2,...,9 are fixed.

With this we come to the end of this unit. In the next unit we shall continue our discussion on ‘counting’ from a slightly different perspective. Let us now summarise what we have covered in this unit.

## 2.5 SUMMARY

In this unit, you have studied the following points.
1. The pigeonhole principle, stated in several forms, its proof, and its applications.
2. The generalized pigeonhole principle, its proof, and applications.
3. The inclusion-exclusion principle, and its proof.
4. Finding the number of surjective functions, the discrete probability and the number of derangements, by using the inclusion-exclusion principle.

## 2.6 SOLUTIONS/ANSWERS

E1) By drawing lines parallel to the sides and through the points trisecting each side, we can divide the equilateral triangle into 9 equilateral triangles of side 1 cm. Thus, if 10 points are chosen, at least two of them must lie in one of the 9 triangles.

E2) 5 persons can be paired in $C(5, 2) = 10$ ways. Hence, if pairs are invited 11 times, at least one pair must have been invited twice or more times, by the pigeonhole principle.

E3) Four persons can be arranged in a line in $4! = 24$ ways. Hence, if we consider 25 occasions, at least on two occasions the same ordering in the queue must have been found, by the pigeonhole principle.

E4) Consider the following grouping of numbers:
$\{1, 2, 4, 8, 16\}, \{3, 9, 18\}, \{5, 15\}, \{6, 12\}, \{7, 14\}, \{10, 20\}, \{11\}, \{13\}, \{17\}, \{19\}.$

There are 10 groupings, exhausting all the 20 integers from 1 to 20. If 11 numbers are chosen it is impossible to select at most one from each group. So two numbers have to be selected from some group. Obviously one of them will divide the other.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;167&lt;/page_number&gt;

---


## Page 34

Basic Combinatorics

E5) Suppose x₁, x₂,..., x₁₅ are the number of balls in the 15 boxes, listed in increasing order, assuming that all these numbers are different. Then, clearly,
xᵢ ≥ i – 1 for i = 1, 2,...,15. But then, ∑ₓ₌₁¹⁵ xᵢ ≥ 14.15 / 2 = 105.

But the total number of balls is only 100, a contradiction. Thus, the xᵢs cannot all be different.

E6) In the sequence a₁, a₂,...,aₙ, there are (n+1)/2 odd numbers and (n–1)/2 even numbers because n is odd. Hence, it is impossible to pair all the aᵢs with numbers from 1, 2,..., n with opposite parity (evenness and oddness). Hence, in at least one pair (i, aᵢ), both the numbers will be of the same parity. This means that the factor (aᵢ–i) will be even, and hence the product will be even.

E7) Consider the seven colours as containers, and the integers getting the respective colour as their contents. Then we have a distribution of an infinite number of objects among 7 containers. Hence, by Theorem 5, at least one container must have an infinity of objects, that is, the colour of that container must have been used an infinite number of times.

E8) Let H be the family of 5-element subsets B of A. For each B in H, let f(B) be the sum of the numbers in B. Obviously, we must have
f(B) ≥ 1 + 2 + 3 + 4 + 5 = 15, and f(B) ≤ 46 + 47 + 48 + 49 + 50 = 240.
Hence, f: H → T where T = {15, 16,..., 240}.

Since |T| = 226 and |H| = C(10,5) = 252, by Theorem 4, H contains different sets with the same image under f, that is different sets, the sums of whose elements are equal.

E9) The 100 collections can be considered as containers. There are an infinity of even numbers. When these even numbers are distributed into 100 containers, at least one container must have an infinity of them, by Theorem 5.

E10) The inclusion-exclusion formula can be rewritten as
|A₁ ∩ ... ∩ Aₙ⁻¹| = N – (S₁ – S₂ + ... + (-1)ⁿ⁻¹Sₙ).

Also, we know that |A₁ ∩ ... ∩ Aₙ⁻¹| = N – |A₁ ∪ ... ∪ Aₙ|.
Hence the result.

E11) Let the objects be the integers 0, 1,..., 999. Let A₁ be the set of numbers divisible by 5, and A₂ the set of numbers divisible by 7. Now, N = 1000, |A₁| = 200, |A₂| = 143 and |A₁ ∩ A₂| ≠ 29. So, by Theorem 7, the answer is 1000 – 200 – 143 + 29 = 686.

E12) The answer to this problem is clearly the number of functions from an 8-element set (the set of people) onto a set of 4-elements (the set of floors). This number is
Σᶜ(4,i)(4 – i)⁸ = 4⁸ – 4.3⁸ + 6.2⁸ – 4.1⁸.
i=0

E13) We can choose three digits in C(10,3) = 120 ways.
The number of 6-digit numbers, using all the three digits, is the same as the number of functions from a 6-set onto a 3-set. This number is

&lt;page_number&gt;168&lt;/page_number&gt;
&lt;watermark&gt;GOVERNMENT UNIVERSITY&lt;/watermark&gt;

---


## Page 35

Some More Counting Principles

$3^6 - 3 \cdot 2^6 + 3 \cdot 1^6 = 540.$

Hence, the answer is $120.540 = 64800$. This will include numbers starting with 0 also.

E14) The total number of ways in which 13 cards can be chosen from a deck of 52 cards is $C(52, 13)$.

If $A_i$ is a choice of cards, none of which are from the ith suit, for $i = 1, 2, 3, 4$, then $|A_i| = C(39, 13), |A_i \cap A_j| = C(26, 13),$ and $C(A_i \cap A_j \cap A_k) = C(13, 13).$

So, $\left|\bigcap \overline{A_i}\right| = C(52, 13) - 4C(39, 13) + C(4, 2)C(26, 13) - C(4, 3)C(13, 13)$

Hence, the required probability is $\frac{\left|\bigcap \overline{A_i}\right|}{C(52, 13)}.$

E15) If A, B, C, D are the integers divisible by 2, 3, 5, 7, respectively, then

$\left|\overline{A} \cap ... \cap \overline{D}\right| = 10,000 - \left\lfloor\frac{10000}{2}\right\rfloor - \left\lfloor\frac{10000}{3}\right\rfloor - \left\lfloor\frac{10000}{5}\right\rfloor - \left\lfloor\frac{10000}{7}\right\rfloor$
$+ \left\lfloor\frac{10000}{6}\right\rfloor + \left\lfloor\frac{10000}{15}\right\rfloor + \left\lfloor\frac{10000}{35}\right\rfloor + \left\lfloor\frac{10000}{14}\right\rfloor + \left\lfloor\frac{10000}{21}\right\rfloor + \left\lfloor\frac{10000}{10}\right\rfloor$
$- \left\lfloor\frac{10000}{30}\right\rfloor - \left\lfloor\frac{10000}{42}\right\rfloor - \left\lfloor\frac{10000}{105}\right\rfloor - \left\lfloor\frac{10000}{70}\right\rfloor - \left\lfloor\frac{10000}{210}\right\rfloor$

= 2285, where [x] denote the greatest integer ≤ x.

Hence, the required probability is $\frac{2285}{10000} = 0.23.$

E16) If $A_r$ is the event that the rth person gets right coat, then by Theorem7,

$\left|\bigcap \overline{A_i}\right| = n! - \sum_{r} |A_r| + \sum_{r,s} |A_r \cap A_s| - ...$
$= n! - n(n-1)! + (n,2)(n-2)! - C(n,3)(1-3)! + ...$
$= C(n,2)(n-2)! - C(n,3)(1-3)! + ...$
$= n! \left(\sum_{r=0}^{n} (-1)^r \frac{1}{r!}\right).$

The number of ways in which only one person receives the correct coat is the sum of all possible intersections of $(n-1)\overline{A_i}$ s. This is

$n! n(n-1)! \left(\sum_{r=0}^{n-1} (-1)^r \frac{1}{r!}\right) = n! \left(\sum_{r=0}^{n-1} (-1)^r \frac{1}{r!}\right).$

E17) 1, 3, 5, 7, 9 are the odd integers.
By Theorem 11(i), the required number of ways is
$9! - C(5, 1)8! + C(5, 2)7! - C(5, 3)6! + C(5, 4)5! - C(5, 5)4!$

E18) By Theorem 11(ii), the required number of permutations is
$C(9,4)D_{9-4} = C(9,4)D_5.$

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;169&lt;/page_number&gt;

---


## Page 36

&lt;img&gt;IGOU logo&lt;/img&gt;
THE PEOPLE'S UNIVERSITY

---


## Page 37

# UNIT 3 RECURRENCE RELATIONS

## Structure

3.0 Introduction
3.1 Objectives
3.2 Three Recurrent Problems
3.3 More Recurrences
3.4 Divide and Conquer Technique to Solve Recurrences
3.5 Summary
3.6 Solutions/Answers

## 3.0 INTRODUCTION

In the previous units, you have learnt to solve various types of combinatorial problems using a varied set of tools. However, there are many problems that have to do with counting which cannot be tackled only with the techniques we have presented so far. To give you one such example, look at the problem of counting the number of binary strings of length n that do not contain two consecutive zeros.

If we denote the number of such binary strings by a<sub>n</sub>, then a<sub>1</sub> = 2 and a<sub>2</sub> = 3. Also, we can show that a<sub>n</sub> = a<sub>n-1</sub> + a<sub>n-2</sub> for n ≥ 2. This is an example of a **recurrence relation**. This relates the value of a<sub>n</sub>, a<sub>n-1</sub> and a<sub>n-2</sub>. We will show how to find an explicit expression for a<sub>n</sub> using this relation in units 2 and 3. In this unit, we will discuss how to **formulate** such recurrence relations for solving combinational problems. In Sec. 3.2, we will introduce you to recurrence relations through three famous examples, the Fibonacci recurrence, Towers of Hanoi and the number of waysof parenthesising an expression.

In Sec. 3.3, we will discuss some more examples to familiarize you with the process of formulating recurrences.

In the Sec. 3.4, we will see how the Divide and Conquer techniques used in the design of algorithms give rise to recurrences in a natural way. Here, we will discuss recurrences associated with algorithms for finding the maximum and minimum elements of a list, fast multiplication of integers etc.

In the section 3.5 We highlight the main points discussed in the unit. Finally we provide solution to questions in 3.6

## 3.1 OBJECTIVES

After going through this unit, you should be able to
* define a recurrence relation;
* give examples of recurrence relations;
* set up recurrence relations;
* write recurrences for divide and conquer algorithms.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;171&lt;/page_number&gt;

---


## Page 38

Recurrences

# 3.2 THREE RECURRENT PROBLEMS

Let us begin by exploring three sample problems that will give you an idea of what is to follow. The first two of these problems have been investigated repeatedly. All the three problems have a solution based on the idea of **recurrences**. This means that the solution to each problem depends on the solution to smaller instances of the same problem.

**Example:1 (Rabbits and the Fibonacci numbers):** Have you heard of the problem of breeding rabbits? This was originally posed by **Leonardo di Pisa**, also known as **Fibonacci**, in 1202 in his book **Liber abaci**. The problem is the following: One pair of rabbits, one male and one female, are left on an island. These rabbits begin breeding at the end of two months and produce a pair of rabbits of opposite sex at the end of each month thereafter. Let $f_n$ denote the number of pairs of rabbits after n months. Then $f_1 = 1$. Note that the rabbits start breeding only after two months and the young ones will be produced one month afterwards. So, young ones are produced only at the end of third month. Therefore the number of pairs of rabbits is still 1 at the end of the second month i.e $f_2 = 1$. At the end of the third month, the pair would have produced one more pair. See Table 1 for details. To find the number of pairs after n months, we must add the number of pairs after n – 1 months to the number of pairs born in the nth month. But the newborns come from pairs at least two months old, i.e. from the pairs that already existed after n – 2 months; there are $f_{n-2}$ of these. Therefore the sequence $\{f_n \mid n \geq 1\}$ meets the condition $f_n = f_{n-1} + f_{n-2}$ if $n \geq 3$, and the $f_n$ are called **Fibonacci numbers**.

&lt;img&gt;Fibonacci portrait&lt;/img&gt;

Fibonacci
(1170—1250)

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

Table 1: Number of Rabbits on the Island

<table>
<thead>
<tr>
<th>Months</th>
<th>Reproducing pairs<br>(at least two months old)</th>
<th>Young Pairs<br>(not more than two months old.)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td></td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
</tr>
<tr>
<td>2</td>
<td></td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
</tr>
<tr>
<td>3</td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
</tr>
<tr>
<td>4</td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
</tr>
<tr>
<td>5</td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
</tr>
<tr>
<td>6</td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
<td>&lt;img&gt;Rabbit silhouette&lt;/img&gt;</td>
</tr>
</tbody>
</table>

* * *

So, have we solved the problem? Not quite; but it uniquely defines the sequence we seek, describing its members in terms of some previous members. We can also define $f_n$ as a function of n, as in the following exercise.

E1) Using induction, verify that $\sqrt{5} f_n = \left(\frac{1+\sqrt{5}}{2}\right)^n -\left(\frac{1-\sqrt{5}}{2}\right)^n$, $n \geq 1$.

We will come back to the Fibonacci sequence later. Now let us consider another important recurrent problem.

&lt;page_number&gt;172&lt;/page_number&gt;

---


## Page 39

# Recurrence Relations

**Example 2:** (The Tower of Hanoi): This problem was invented by the French mathematician **Edouard Lucas** in 1883. We are given a tower of eight discs, initially stacked in decreasing size on one of three pegs.

&lt;img&gt;Tower of Hanoi - Initial Position&lt;/img&gt;

Fig. 2 : Initial position for the towers of Hanoi problem.

The objective is to transfer the entire tower to one of three pegs, moving only one disc at a time without ever moving a larger disc onto a smaller one. Lucas furnished this toy with a legend about a much larger **Tower of Brahma**, which supposedly had 64 discs of pure gold resting on three diamond needles. “At the beginning of time”, he said, “God placed these golden diamond needles”, “God placed these golden discs on the first needle and said that a group of priests should transfer them to a third, according to the rules above. The Tower will crumble and the world will come to an end once the task is finished.”

Let us generalise the problem and see what happens if we have n discs instead. Let us say that T<sub>n</sub> is the minimum number of moves that will transfer n disks from one peg to another under the rules. Clearly, T<sub>1</sub> = 1, and T<sub>2</sub> = 3 (see Fig.3). A little bit of experimentation on three disks leads us to the general strategy: We first transfer the n – 1 smallest disks to B (requiring T<sub>n-1</sub> moves), then move the largest (requiring one move; remember, it must move!) to C. A is now empty and can be used to transfer the discs on peg B to C. Thus, we can transfer n discs

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;Tower of Hanoi - Step 3a&lt;/img&gt;
3a) Transfer disc 2 to peg B

&lt;img&gt;Tower of Hanoi - Step 3b&lt;/img&gt;
3b) Transfer disc 1 to peg C

&lt;page_number&gt;173&lt;/page_number&gt;

---


## Page 40

# Recurrences

&lt;img&gt;A diagram showing three pegs (A, B, C) with discs on them. Peg A has one disc, peg B has two discs, and peg C has no discs.&lt;/img&gt;

3c) Transfer disc 2 to peg C.

Fig. 3 : The moves involved in transferring 2 discs.

(for n ≥ 2) in at most 2Tn-1+1 moves. So, Tn ≤ 2 Tn-1 + 1, if n ≤ 2. Why have we used “≤” instead of “=” here? Our construction proves only that 2Tn-1 + 1 moves are enough but can we transfer the disks with lesser number of moves? The answer is “No”. At some point, we must move the largest disc. When we do, the n – 1 smallest must be on a single peg (why?), and it has taken at least Tn-1 moves to put them there. After moving the largest disc for the last time, we must transfer the n – 1 smallest discs (which must again be on a single peg) back onto the largest; this too requires Tn-1 moves. Hence, Tn ≥ 2Tn-1+1 if n ≥ 2. Both the inequalities, Tn ≥ 2 Tn-1 + 1 and Tn ≤ 2 Tn-1 + 1 can be true only when Tn = 2Tn-1 + 1.

* * *

Once you have done, you will note that the priests will require a minimum of 264 − 1 = 18446 744 073 709 551 615 moves to transfer the golden disks. Even at the rate of one move per second, it will take them more than 5 × 1011 years to solve the puzzle, so the doomsday is far away!

Try the next exercise which gives an explicit expression for Tn.

E2) Using induction, show that Tn = 2n − 1, n ≥ 1.

Now let us consider the third problem we had in mind. This is the number of ways to parenthesise an expression.

**Example 3:** Let us derive the recurrence relation for the number of ways to parenthesise the expression x₁ + x₂ + ... + xₙ so that only two terms will be added at a time. For example, the expression (x₁ + x₂) + x₃ is fully parenthesized, but (x₁ + x₂) + x₃ is not. Suppose the number of ways of parenthesising the expression x₁ + x₂ + ... + xₙ is aₙ. If we split the expression into x₁ + x₂ + ... + xₙ₋₁ and xₙ, x₁ + x₂ + ... + xₙ₋₁ can be parenthesised in aₙ₋₁ ways and xₙ can be parenthesised in a₁ ways. So, in this case, we can parenthesise the expression in aₙ₋₁a₁ ways. Similarly, if we split up the expression into x₁ + x₂ + ... + xₙ₋₂ and xₙ₋₁ + xₙ₋₂, we can parenthesise the expression x₁ + x₂ + ... + xₙ₋₂ in aₙ₋₂ ways and the expression xₙ₋₂ + xₙ₋₂ in a₂ ways. The total number of ways in this case is aₙ₋₂a₂ ways. In general, if we split up the expression into two sub expressions of size n – k and k, we can parenthesise the expression in aₙ₋k aₖ ways. We can get the **total number** of parenthesising the expression by adding the different ways of parenthesising the expression by **adding** the different **ways of parenthesising the expression corresponding to different ways of splitting the expression**. This is precisely
aₙ₋₁a₁ + aₙ₋₂a₂ + ... + aₙ₋k aₖ + ... + a₁aₙ₋₁.
Therefore, the recurrence relation satisfied by aₙ is

&lt;page_number&gt;174&lt;/page_number&gt;
&lt;watermark&gt;GOVERNMENT OF THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 41

a<sub>n</sub> = a<sub>n-1</sub>a<sub>1</sub> + a<sub>n-2</sub>a<sub>2</sub> + ... + a<sub>n-k</sub>a<sub>k</sub> + ... + a<sub>1</sub>a<sub>n-1</sub> for n ≥ 2 with a<sub>1</sub> = 1.

Using the fact that a<sub>0</sub> = 0, we can extend this to

a<sub>0</sub> = 0, a<sub>1</sub> = 1, a<sub>n</sub> = a<sub>n</sub>a<sub>0</sub> + a<sub>n-1</sub>a<sub>1</sub> + ... + a<sub>1</sub>a<sub>n-1</sub> + a<sub>n-1</sub> + a<sub>0</sub>a<sub>n</sub> (n ≥ 2).

* * *

The numbers a<sub>0</sub>, a<sub>1</sub>, a<sub>2</sub>, ... are called Catalan numbers. Catalan numbers arise in several other contexts. We will state two other contexts without proofs.

**Example 4:** Suppose two candidates A and B poll the same number of votes, n each, in an election. The counting of votes is usually done in some arbitrary order and therefore, during the counting process A may lead for some period and B may lead for some period. The number of ways of counting the votes such that A never trails B is the n<sup>th</sup> catalan number. We can represent a vote for A by + and a vote for B by -. Then, the n<sup>th</sup> catalan number is the number of sequences of pluses and minuses such that there are **at least** as many pluses as there are minuses at **any stage** of the sequence. Let us call such a sequence an admissible sequence. Let us take a special case where 8 votes are cast, 4 for A and 4 for B. One voting sequence where A never trails is (+,-,+,+,-,-,+,-). If we drop the last three terms, we get the sequence (+,-,+,+,-,-) . Here, there are 3 pluses and 3 minuses i.e. there are at least as many pluses as there are minuses. If we drop the last term, we get (+,-,+,+,-,-,+). Here, there are 4 pluses and 3 minuses, i.e. there are more pluses than minuses.
***


**Example 5:** You would have come across the data structure called Stack in MCS-21 Recall that, a stack is a list which can be changed by insertions or deletions at the top of the list. An insertion is called a **push** and a deletion is called a **pop**. A sequence of pushes and pops of length 2n is called **admissible** if there are n pushes and n pops and at each stage of the sequence there are **at least** as many pushes as pops. Suppose we have the string 123...n of the set N={1,2,3,...,n} and an admissible sequence of pushes and pops of length 2n. Each push in the sequence transfers the last element in the input string to the stack and every pop transfers the element on the top of the stack to the beginning of the output string. After n pushes and pops have been performed,the output string is a permutation of N called a **stack permutation**. The number of stack permutations of 123...n is the n<sup>th</sup> Catalan number. Again, we can represent a popby a + and a push by a -. If you pause and think for a minute, you can convince yourself that every admissible sequence of pops and pushes corresponds to an admissible sequence of pluses and minuses. Let us look at an example. Suppose n=4 and we have the following admissible sequence of pops and pushes: (+,-,+,+,-,-,+,+,-) . Let us find the stack permutation corresponding to this. See Table 2.

**Table 2 : Finding the slack permutation corresponding to the Admissible sequence (+,-,+,+,-,-,+,+,-)**

<table>
<thead>
<tr>
<th>Sequence</th>
<th>Input String</th>
<th>Stack</th>
<th>Output String</th>
</tr>
</thead>
<tbody>
<tr>
<td>+ (Push 4)</td>
<td>123</td>
<td>[4]</td>
<td>Empty</td>
</tr>
<tr>
<td>- (Pop 4)</td>
<td>123</td>
<td>[]</td>
<td>4</td>
</tr>
<tr>
<td>+ (Push 3)</td>
<td>12</td>
<td>[3]</td>
<td>4</td>
</tr>
<tr>
<td>+ (Push 2)</td>
<td>1</td>
<td>[23]</td>
<td>4</td>
</tr>
<tr>
<td>- (Pop 2)</td>
<td>1</td>
<td>[3]</td>
<td>24</td>
</tr>
<tr>
<td>- (Pop 3)</td>
<td>1</td>
<td>[]</td>
<td>324</td>
</tr>
<tr>
<td>+ (Push 1)</td>
<td>Empty</td>
<td>[1]</td>
<td>324</td>
</tr>
<tr>
<td>- (Pop 1)</td>
<td>Empty</td>
<td>[]</td>
<td>1324</td>
</tr>
</tbody>
</table>

So, the permutation obtained is 1324. This is an example of a stack permutation of size 4.
***
Try the following exercises now to check if you have understood our discussion so far.

&lt;watermark&gt;UNIVERSITY OF PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;175&lt;/page_number&gt;

---


## Page 42

# Recurrences

E3) Which of the following sequences are admissible?
i) (+,-,+,-,+,-,-,)
ii) (+,-,+,-,+,-,+,-)
iii) (+,+,-,-,-,+,-,+)

E4) Is the statement “An admissible sequence has to start with a plus and end with a minus” true? Explain your answer.
E5) Consider the problem discussed in the introduction. Let $a_n$ be the number of binary sequences of length n that do not contain consecutive zeros. Show that $a_n = a_{n-1} + a_{n-2}$ for $n \geq 3$.

You will have noticed that in each of the three problems, we have been able to express the nth term of a sequence in terms of one or more previous terms and a function of n. This gives you a method to compute the terms of the sequence accurately, given enough time. At times, if the relation between the terms is in a reasonably nice form, we can even “solve” the recurrence, that is, express the nth term as a function of n. You will learn how to solve these three recurrences in the next 2 units.

Let us now consider some more recurrent problems.

## 3.3 MORE RECURRENCES

You have been exposed to some famous recurrent problems in the previous section. In this section, we shall take another look at setting up recurrence relations for combinational problems. You will find that in trying to determine recurrence, we are really attempting to describe the counting inductively. In most cases, you will see that the recurrence relation leads to an alternate method of solution, although the methods themselves will not be dealt in this Unit.

**Example 6:** Let $C_n$ be the number of comparisons needed to sort a list of n integers. Let us find a recurrence relation for $C_n$. We first find the minimum of the n elements. This will be the first element of the list. We compare the first two elements and find the minimum among the two. We compare this minimum with the third element, and so on. For finding the minimum of n elements we have to make n−1 comparisons. For example, if we want to find the minimum of the list 3, 2, 4, 1, 5, we will have to make 4 comparisons as shown in Fig.4.

<mermaid>
graph TD
    A[3] --> B[2]
    B --> C[4]
    C --> D[1]
    D --> E[5]
    E --> F[5]
    F --> G[5]
    G --> H[5]
    H --> I[1]
</mermaid>

Fig. 4: Comparisons for finding the minimum of 3,2,4,1,5

After making the minimum element the first element of the list we can sort the remaining n−1 elements with $C_{n-1}$ comparisons and append it after first element. So, n−1 + $C_{n-1}$ comparisons are required to sort a list of n elements.

&lt;page_number&gt;176&lt;/page_number&gt;

---


## Page 43

(i.e.) C<sub>n</sub> = C<sub>n-1</sub> + n-1

* * *

Try the following exercise which asks you to prove an expression C<sub>n</sub>.

---

E6) In Example 6, using the recurrence relation for C<sub>n</sub>, show that
C<sub>n</sub> = (1/2)n(n-1), n ≥ 1.

---

**Example 7:** You may recall that the set of all subsets of any non-empty set, S, is called its **power set**, and denoted by p(S). Let us determine a recurrence relation satisfied by s<sub>n</sub> = |p(S)|, where |S| = n. Let us take S = {1, 2, ..., n}. Now, any subset, A, of S either contains the number n or does not contain the number n. Let us consider these two mutually exclusive cases separately and count the number of such subsets, A. If n ∈ A, then A = A' ∪ {n}, where A' is a subset of {1, 2, ..., n - 1}, there are s<sub>n-1</sub> such subsets A. So, the number of subsets A that contain n is the same as the number of subsets of {1, 2,..., n - 1}, which is s<sub>n-1</sub>. On the other hand if n∉ A, then, in fact, A is a subset of {1, 2,..., n - 1}, and there are s<sub>n-1</sub> of these too. Combining these, we see that s<sub>n</sub> = s<sub>n-1</sub> + s<sub>n-1</sub> = 2s<sub>n-1</sub>, n ≥ 1, with s<sub>0</sub> = 1.
* * *
We ask you to prove that s<sub>n</sub> = 2<sup>n</sup> in the next exercise.

---

E7) In Example 5, using the recurrence relation for s<sub>n</sub>, show that s<sub>n</sub> = 2<sup>n</sup>, n ≥ 0.

---

**Example 8:** Recall that a **bijection** is a one-one, onto mapping of a set onto itself. It is quite easy to determine directly the number of bijections of an n-set (a set with n elements). We will, however, look at a recurrence relation satisfied by the number of bijections, b<sub>n</sub>, of any n-set, say {1,2,...,n}. To begin with, if f is any such bijection, f(n) could be any one of the n elements of the set {1, 2, ..., n}; but now we must map {1,2,..., n - 1} bijectively to {1,2,..., n} / {f(n)}; this can be done in b<sub>n-1</sub> ways. In all then, b<sub>n</sub> = nb<sub>n-1</sub>, n ≥ 2, with b<sub>1</sub> = 1.
* * *
Again, we ask you to prove an expression for b<sub>n</sub>.

---

E8) In Example 8 using the recurrence relation for b<sub>n</sub>, show that b<sub>n</sub> = n!, n ≥ 1.

---

We end this section by looking again at the problem of derangements, discussed in in the previous unit of this block.

**Example 9:** You may recall that the problem is to determine the number of derangements of n objects, d<sub>n</sub>, and that we had employed the method of **Inclusion-Exclusion** to solve it. Let us find a recurrence relation for d<sub>n</sub>. Recall that d<sub>n</sub> counts the number of permutations of n objects that leave no object fixed. Any such permutation is called a **derangement**. Let us begin by labeling the objects serially: 1, 2, ..., n. In any such derangement of n objects, 1 gets sent to some i, where i ≠ 1. Two cases arise: For the same derangement, either i gets sent back to 1 or it does not. In the first case, we can leave out 1 and i from the original set and obtain a derangement of n-2 objects; there are d<sub>n-2</sub> such possibilities. Suppose i is not sent back to 1. Then, we can get a derangement of {2, 3, ..., n} as follows. Some number must be mapped back to 1, suppose j is mapped to 1. We can define a derangement of {2,3, ..., n} as follows:
1) Map j to i
2) Every other element is mapped according to the original derangement

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;177&lt;/page_number&gt;

---


## Page 44

# Recurrences

Thus there are $d_{n-1}$ such possibilities to obtain a derangement of $n - 1$ objects. Therefore, assuming 1 gets sent to i, there is a total of $d_{n-1} + d_{n-2}$ possibilities. Observing that i could have been any number between 2 and n, we conclude that $d_n = (n - 1)(d_{n-1} + d_{n-2})$ for $n \geq 3$. To complete the recurrence relation, we note that $d_1 = 0$ and $d_2 = 1$. You will have noticed that to compute $d_n$ one needs to know the values of the two preceding terms. Can we get to compute $d_n$ on the basis of the value of only one preceding term, $d_{n-1}$? To explore this, let us write the recurrence in the form

$$d_n - nd_{n-1} = -[d_{n-1} - (n - 1)d_{n-2}]$$

We now observe that the expression on the right hand side within the brackets is got from the expression on the left hand side by merely replacing n by $n - 1$. If we write $D_n = d_n - nd_{n-1}$, we have the simplified expression $D_n = -D_{n-1}$. But then $D_{n-1} = -D_{n-2}$, and so $D_n = D_{n-2}$. Continuing this procedure, we arrive at

$$D_n = (-1)^{n-2}D_2 = (-1)^n[d_2 - 2d_1] = (-1)^n.$$

Therefore, we have $d_n = nd_{n-1} + (-1)^n$ if $n \geq 2$, with $d_1 = 0$.

* * *

In the next exercise, we ask you to prove the expression for $d_n$ but using the recurrence for $d_n$ this time.

E9) Using induction and either of the two recurrence relations for $d_n$, show that

$$d_n = n!\sum_{i=0}^n \frac{(1-)}{i!}, n \geq 1.$$

We end this section with a few problems in which you are required to set up the recurrence equations.

E10) Set up a recurrence relation for the determinant of the $n \times n$ matrix with 1 along the main diagonal and with 1 on either side of the main diagonal in each row and zero elsewhere. For example, the $3 \times 3$ determinant is

<table>
<tr><td>1</td><td>1</td><td>0</td></tr>
<tr><td>1</td><td>1</td><td>1</td></tr>
<tr><td>0</td><td>1</td><td>1</td></tr>
</table>

E11) Set up a recurrence relation for the number of n digit sequences on integers {0, 1, 2, 3} having an even number of 0's.

E12) Show that the number of r-permutations of n distinct objects, P(n,r), satisfies the recurrence relation

$$P(n, r) = P(n - 1, r) + rP(n - 1, r - 1), n \geq 1, r \geq 1.$$

E13) Let $S_r^n$ denote the Stirling numbers of the second kind, that is, the number of ways to distribute r distinct objects into n nondistinct boxes with no box left empty. Show that $S_r^n$ satisfies the recurrence relation

$$S_{r+1}^n = S_r^{n-1} + nS_r^n, 1 < n < r.$$

&lt;page_number&gt;178&lt;/page_number&gt;

---


## Page 45

# 3.4 DIVIDE AND CONQUER TECHNIQUE TO SOLVE RECURRENCES

Often, to solve a problem, we can partition the problem into smaller problems, find solutions to the smaller problems and then combine the solutions to find a solution forthe whole. We can repeatedly partition the problem till we reach a stage where we cansolve the problem quite easily. This approach is called the **divide-and-conquer** approach. Let us start with an example. **Throughout this section we will assume that n = 2^k.**

**Example 10:** Consider the problem of finding the maximum and minimum of a list ofn numbers. Here let us assume that n = 2^k for some k to make things simpler for us.
Let a_n be the number of comparisons required for finding the maximum and minimum of a list of n numbers.
We can partition the list into two lists of size n/2 each. The maximum and minimum of each of the list can be found using a_{n/2} comparisons.
We can then compare minimum (resp. maximum) of the lists to get the minimum (resp. maximum) of the list, i.e., we will need two more comparisons. So,
a_n = 2a_{n/2} + 2 for n ≥ 2. a_2 = 2. We leave it as an exercise for you to check that a_n = 3/2 n - 2, when n is power of 2.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E14) Check that a_n = 3/2 n - 2 is a solution to the recurrence a_n = 2a_{n/2} + 2 where n is a power of 2 and a2 = 1.

**Definition:** We call a recurrence a divide-and-conquer recurrence if it has the form a_n = ba_{n/a} + d(n)
where a > 1, b > 1 are integers and d(n) is a function of n.

Such a relation results when we split a problem of size n into b sub problems of size n/a. After solving each of the sub problems we may need d(n) steps to get the solutiona to the original problem of size n. In Example 10, we splitted a problem of size n into 2 sub problems of size n/2 each and we needed 2 more steps to get the answer to the original problem. So, a = b = 2 and d(n) = 2 in this example.

**Example 11:** In a tennis tournament, each entrant plays a match in the first round. Next, all winners from the first round play a second-round match. Winners continueto move on to the next round, until finally only one player is left as the tournamentwinner. Assuming that tournaments always involve n = 2^k players, for some k, find the recurrence relation for the number rounds in a tournaments of n players.

&lt;page_number&gt;179&lt;/page_number&gt;

---


## Page 46

# Recurrences

&lt;img&gt;A tournament involving 8 players&lt;/img&gt;

**Fig.5: A tournament involving 8 players**

**Solution:** The tournament is subdivided into 2 sub tournaments of n/2 players each. Here the first round of both the tournaments are held together so that they are considered as a single first round. Similarly, all the other rounds are held together. So, after a<sub>n/2</sub> rounds, one player will be left in both the sub tournaments. The winner of the match between the two is the winner of the tournament. So, a<sub>n</sub> = 2a<sub>n/2</sub> + 1. See Fig.5 for a tournament involving 8 players.

* * *

Let us now discuss some more problems where divide and conquer approach can be used.

**Example 12:** (Binary search) Suppose we have a sorted list of n=2<sup>k</sup> numbers and we want to check whether a particular number is in the list or not. If we compare the number with all the elements of the list we need n comparisons in the worst case. However, we will describe a better algorithm called the binary search algorithm which uses the divide- and-conquer paradigm. Let us look at a particular example. Suppose we want to check whether 12 is in the list 1,2,3,5,6,7,12,13. We split up the list into two parts. 1,2,3,5 and 6,7,12,13. We compare 12 with the last element of the first list which is 5. We have 5 < 12 and all the elements in the first list are less than 5. So, we can discard the first list. The second list is again split into two parts, 6,7 and 12,13. Since 7 < 12, we discard the first part. We split 12,13 into two lists of one element each. The first of these two lists, 12, contains 12. Let a<sub>n</sub> denote the number of comparisons required while searching for an element in a sorted list of size n. Then a<sub>1</sub>=1. In general, we can split up the list into two equal parts of n/2 elements each. We can compare our element with the last element, which is the largest element, of the first list. This will tell us whether we have to search in the first list or in the second list. In either case we have to search in a list of size n/2 only. So, a<sub>n</sub>=a<sub>n/2</sub>+1.

* * *

**Example 13:** (Merge sort) Suppose we want to sort a list of n=2<sup>k</sup> elements in ascending order. We can divide the list into parts of size n/2 each, sort them and merge them into a sorted list. Suppose a<sub>n</sub> is the number of comparison required to sort a list of n elements then, the two lists can be sorted using a<sub>n/2</sub> comparisons each. Let us call the lists L<sub>1</sub> and L<sub>2</sub>. We will merge them into a new sorted list L.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;180&lt;/page_number&gt;

---


## Page 47

# Recurrence Relations

We compare the first (smallest) elements of the list, add the smallest element of the two to the new list L and remove the smallest element from the list from which we selected it. We repeat this till one of the lists, say L₁ is empty. Then we append L₂ to the list L to get a sortedlist. See Table below, where we show how to merge two sorted lists 1,2,5,6 and 3,4.

<table>
<thead>
<tr>
<th>Step</th>
<th>L₁</th>
<th>L₂</th>
<th>L</th>
<th>Action taken</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>1, 2, 5, 6</td>
<td>3, 4</td>
<td>--</td>
<td>1<3. Remove 1 from L₂ and add it to L.</td>
</tr>
<tr>
<td>2</td>
<td>2, 5, 6</td>
<td>3, 4</td>
<td>1</td>
<td>2<3. Remove 2 from L₁ and add it to L.</td>
</tr>
<tr>
<td>3</td>
<td>5, 6</td>
<td>3, 4</td>
<td>1, 2</td>
<td>5>3. Remove 3 from L₂ and add it to L.</td>
</tr>
<tr>
<td>4</td>
<td>5, 6</td>
<td>4</td>
<td>1, 2, 3</td>
<td>5>4 Remove 4 from L₂ and add it to L.</td>
</tr>
<tr>
<td>5</td>
<td>5, 6</td>
<td>--</td>
<td>1, 2, 3, 4</td>
<td>L₂ is empty. No more comparisons required. Add the remaining elements of L₁ to L to get the sorted list 1,2,3,4,5,6</td>
</tr>
</tbody>
</table>

Here L₁ and L₂ are not of the same size. We needed 4+2-1=5 comparisons to sort lists of sizes 4 and 2. In general, to merge two sorted lists of size m and n under this method at most m+n-1 comparisons are required. So, to merge the two lists of size n/2 each, at most n-1 comparisons are required. So, aₙ=2aₙ/₂+n-1.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E15) Finding the nth power of an integer i, by successive multiplications by i requires n - 1 multiplications. Assuming n = 2ᵏ, describe a divide and conquer algorithm such that if aₙ is the number of multiplications to find the nth power, then aₙ = aₙ/₂ + 1. Is the algorithm desirable given that the solution is given by aₙ = log₂(n)?

E16) Finding the product of a list of n integers by successive multiplication requires n - 1 multiplications. Assuming n = 2ᵏ, describe a divide and conquer algorithm for which the number of multiplications aₙ satisfies the recurrence relation aₙ = 2aₙ/₂ + 1

E17) To multiply two n-digit numbers, one must do normally n² digit-times-digit multiplications. Use a divide and conquer algorithm to do better when n is a power of 2.

With this we have come to the end of this unit. Next two units will deal with the methods of solving recurrence relations. Now let us take a quick look at what we have discussed in this unit.

## 3.5 SUMMARY

In this Unit **recurrence relations** we:
1) discussed several examples of recurrence relations, drawn from well-known problems and from routine exercises in combinatorics.
2) discussed how to set up recurrence relations after having read this unit.
3) discussed setting up of recurrence relations with the help of divide and conquerparadigm.

&lt;page_number&gt;181&lt;/page_number&gt;

---


## Page 48

Recurrences

# 3.6 SOLUTIONS/ANSWERS

E1) It is easy to check that f₁ = 1 = f₂. With α = (1+√5)/2, β = (1-√5)/2, we observe that αβ are solutions to the equation x² - x - 1 = 0. ∴ α² = α + 1, β² = β + 1.

If n ≥ 3,
√5(fⁿ⁻¹ + fⁿ⁻²) = (αⁿ⁻¹ - βⁿ⁻²)
= αⁿ⁻²(α + 1) - βⁿ⁻²(β + 1)
= αⁿ⁻²α² - βⁿ⁻²β²
= αⁿ - βⁿ = √5fₙ,
as desired.

E2) Observe that T₁ = 1. If n ≥ 2, 2Tₙ₋₁ + 1 = 2(2ⁿ⁻¹ - 1) + 1 = 2ⁿ - 1 = Tₙ, verifying the formula.

E3) 1) and 2) are admissible. If we drop the last three terms from 3), we get (+,+,-,-,-) which has two pluses and three minuses. So, 3) is not admissible.

E4) Yes, this is true. If an admissible sequence starts with a -, the sequence got by removing all the terms except the first one has more minuses (1 minus) than pluses (0 Plus). Suppose an admissible sequence ends in a plus. The sequence we get by removing a plus has more pluses than minuses. If we put back the plus, the sequence will still have more pluses than minuses. But, an admissible sequence must have equal number of pluses and minuses.

E5) Consider any string of length n. The last bit of the sequence is either 0 or 1. If the last bit is 0, the previous bit must be 1. So, it can be obtained by adding ‘10’ to a string of length n - 2 . (Note that 2 consecutive 1s are allowed!) If the last bit is 1, this can be obtained by adding 1 to a string of length n-1.
∴ aₙ = aₙ₋₁ + aₙ₋₂
Note that, aₙ satisfies the same recurrence satisfied by the Fibonacci sequence. We have f₁ = 1, f₂ = 1, but a₁ = 2, a₂ = 3.

E6) It is easy to see that C₁ = 0. If n ≥ 2,
Cₙ₋₁ + n - 1 = 1/2(n - 1)(n -2) + n - 1 = 1/2n(n - 1) = Cₙ, as desired.

E7) Observe that s₀ = 1. If n ≥ 1, 2sₙ₋₁ = 2.2ⁿ⁻¹ = 2ⁿ = sₙ, verifying the formula.

E8) We note that b₁ = 1. If n ≥ 2, nbₙ₋₁ = n. (n -1)!n! = bₙ, as required.

E9) We check that d₁ = 0, d₂ = 1. To verify the first order recurrence, note that if n ≥ 2,
ndₙ₋₁ + (-1) n = n[(n -1)!∑ᵢ₌₀ⁿ⁻¹ (-1)ⁱ / i!) + (-1)ⁿ]
= n!(∑ᵢ₌₀ⁿ⁻¹ (-1)ⁱ / i!) - (-1)ⁿ / n!)
= n! ∑ᵢ₌₀ⁿ⁻¹ (-1)ⁱ / i! = dₙ
as desired.

&lt;watermark&gt;GOI THE GOPI'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;182&lt;/page_number&gt;

---


## Page 49

Recurrence Relations

In case of the second order recurrence relation, if n ≥ 1,

$(n-1)(d_{n-1} + d_{n-2}) = (n-1)\left\{\left((n-1)!\sum_{i=0}^{n-1}\frac{(-1)^i}{i!}\right) + \left((n-2)!\sum_{i=0}^{n-2}\frac{(-1)^i}{i!}\right)\right\}$

$= n.\left(n-1)!\sum_{i=0}^{n-1}\frac{(-1)^i}{i!} - (n-1)!\sum_{i=0}^{n-1}\frac{(-1)^i}{i!} + (n-1)!\sum_{i=0}^{n-2}\frac{(-1)^i}{i!}\right)$

$= n!\sum_{i=0}^{n-1}\frac{(-1)^i}{i!} - (n-1)!\frac{(-1)^{n-1}}{(n-1)} = n!\sum_{i=0}^{n-1}\frac{(-1)^i}{i!} + (-1)^n$

$= \sum_{i=0}^{n}\frac{(-1)^i}{i!} = d_n$

As desired.

E10) Let Δₙ denote the required n × n determinant. Expanding about the first row, we get Δₙ₋₁ minus the determinant which when expanded about its first row yields Δₙ₋₂. The corresponding recurrence relation is
Δₙ = Δₙ₋₁ − Δₙ₋₂, n ≥ 3, with Δ₁ = 1, Δ₂ = 0.

E11) Let aₙ denote the number of n-digit sequences containing an even number of 0's. Then there are aₙ₋₁ (n − 1)-digit sequences that have an even number of 0's and 4ⁿ⁻¹ − aₙ₋₁ (n − 1)-digit sequences that have an odd number of 0's. To each of the aₙ₋₁ sequences that have an even number of 0's, the digit 1,2 or 3 can be appended to yield sequences of length n that contain an even number of 0's. To each of the 4ⁿ⁻¹ − aₙ₋₁ sequences that have an odd number of 0's, the digit 0 must be appended to yield sequences of length n that contain an even number of 0's. Therefore, for n ≥ 2, aₙ = 3aₙ₋₁ + 4ⁿ⁻¹ − aₙ₋₁ = 2aₙ₋₁ + 4ⁿ⁻¹, with a₁ = 3.

E12) Of the n distinct objects, pick any one object and call it “special”. Then, the number of r-permutations in which this “special” object does not appear is P(n−1, r) because this is the number of r-permutations of the remaining (n−1) objects. On the other hand, if the “special” object does appear, thenumber of r-permutations is rP(n−1, r−1) because the “special” object couldbe in any one of r positions between objects or at either end, and we have thento determine the number of (r−1)-permutations of n−1 objects. Combining the two, we get the required recurrence.

E13) This is somewhat similar to the previous one; choose a “special” object first. The box containing this object either contains no other object or contains at least one more. In the first case, we need to distribute r distinct objects into n−1 nondistinct boxes, with no empty box; the number of ways in which to do this is S_r^(n−1). Otherwise, the special “object” may be placed into any one of the n (nondistinct) boxes (there are n choices), and we still need to distribute r objects into n nondistinct boxes, with no empty box; there are S_r^n such choices for each choice of the box the “special” object is placed in. Combining the two cases gives the recurrence relation.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;183&lt;/page_number&gt;

---


## Page 50

Rcurrences

E14) When n = 2, $\frac{3}{2}n --2=1$. Let us suppose n = $2^k$. Let us apply induction on k.
Suppose it is true for k, say m = $2^k$, then
$a_m = 2a_{m/2} + 2$
$= 2\left(\frac{2m}{4}-2\right)+2$
$= \frac{3m}{2}=4+2$
$= \frac{3}{2}m-2$
Thus it is true for k+1.

E15) Divide n by 2, find i^n/2, and square it. Thus $a_n = a_{n/2} + 1$. The algorithm is desirable since log₂(n) grows more slowly than n.

E16) Divide n by 2. Find the product of n/2 integers and the product of last n/2 integers Multiply two products obtained. Thus $a_n = 2a_{n/2} + 1$.

E17) Let n be a power of 2. Let the two n-digit numbers b A and B. We split each of these numbers into two n/2 digit parts:
A = A₁ 10^(n/2) + A₂ and
B = B₁ 10^(n/2) + B₂ (like 1235 = 12 × 100 + 35)
Then A.B = A₁ B₁ 10ⁿ + A₁ B₂ 10^(n/2) + A₂ B₁ 10^(n/2) + A₂ B₂ 10^(n/2) A₂ B₂
We need only to make three n/2 digit multiplications, A₁. B₁, A₂. B₂ and (A₁+A₂). (B₁+B₂) to determine A. B since
A₁ . B₂ + B₂ . A₁ = (A₁ + A₂). (B₁ + B₂) - A₁ . B₁ - A₂ . B₂
Actually (A₁ + A₂) or (B₁ + B₂) may be $\left(\frac{n}{2}+1\right)$ digit numbers but this slight variation does not effect the general magnitude of our solution (like 1295 = 12 × 10² + 95). If $a_n$ represents the number of digit-times multiplications needed to Multiply two n-digit numbers by the above procedure, this gives the recurrence relation $a_n = 3a_{n/2}$
$a_n$ proportional to $n^{\log_2 3} = n^{1.6}$ – a substantial improvement over n².

&lt;watermark&gt;© THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;184&lt;/page_number&gt;

---


## Page 51

# UNIT 4 PARTITIONS AND DISTRIBUTIONS

## Structure

4.0 Introduction
4.1 Objectives
4.2 Integer Partitions
4.3 Distributions
    4.3.1 Distinguishable Objects into Distinguishable Containers
    4.3.2 Distinguishable Objects into Indistinguishable Containers
    4.3.3 Indistinguishable Objects into Distinguishable Containers
    4.3.4 Indistinguishable Objects into Indistinguishable Containers
4.4 Summary
4.5 Solutions /Answers

## 4.0 INTRODUCTION

In the last two units we have exposed you to a variety of combinatorial techniques. In this unit we look at a few more ways of counting arrangements of objects when order matters, and when it doesn’t.

In Sec. 4.2, we focus on the ways in which a natural number can be written as a sum of natural numbers. In the process you will be introduced to a useful ‘recurrence relation’.

We link this, in Sec. 4.3, with the different ways in which n objects can be distributed among m containers. As you will see, there are four broad possible kinds of distributions. In each case, we consider ways of counting all the distributions. In the process you will also be introduced to Stirling numbers.

You should attempt the assignment based on the course after studying this unit, and this block.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

## 4.1 OBJECTIVES

After going through this unit, you should be able to:

*   define an integer partition, and count the number of partitions of an integer;
*   count the number of ways of distributing distinguishable and indistinguishable objects, respectively, into distinguishable containers;
*   count the number of ways of distributing distinguishable and indistinguishable objects, respectively, into indistinguishable containers.

## 4.2 INTEGER PARTITIONS

Suppose a detergent manufacturer wants to promote her product by giving a gift token with 100 bars out of the whole stock. The lucky persons among her customers will get the gift. Some of them may buy more than one bar at a time with the hope of getting gifts. In how many ways can the 100 gift tokens get distributed? One possible way is that all the 100 bars with gifts are bought by 100 different customers. We can indicate this situation by $100 = \underbrace{1 + 1 + ... + 1}_{\text{100 times}}$. Another possibility is that somebody buys 2 bars, somebody else buys 3 bars, and the remaining 95 bars are distributed amongst 95 different people. We are not interested in the order in which the bars are bought.

&lt;page_number&gt;185&lt;/page_number&gt;

---


## Page 52

Basic Combinatorics

Forexample, here we are not interested in whether the person who bought 2 bars bought them before the person who bought the 3 bars. So, we can indicate this situation by $100 = \frac{1 + 1 + ... 1}{95 \text{ times}} + 2+3$. More generally, we can indicate each way of distributing the 100 bars with gifts by $100 = p_1 + p_2 + p_2 + ... + p_k$, where the $p_i$ are natural numbers, and $p_1 \leq p_2 \leq ... \leq p_k$. Each way of writing 100 in this form is called an **integer partition** of 100. More generally, we have the following definition.

**Definition:** Any representation of $n \in \mathbb{N}$ as a sum of positive integers in non-increasing order is called a **partition** (or **integer partition**) of $n$. Each such partition can be written in the form $n = p_1 + p_2 + ... + p_k$, where $p_1 \leq p_2 \leq ... \leq p_k$.

Here, $p_1, p_2, ..., p_k$ are called the **parts** of the partition, and the **number of parts** of the partition is $k$.

While we chose 100 in the example above, it is really a huge number in the context of integer partitions. Let us consider a smaller number, say 5. How many partitions of 5 can you think of? There are 7 altogether, namely, 5, 1+4, 2+3, 1+1+3, 1+2+2, 1+1+1+2 and 1+1+1+1+1.

In books, you will often come across the notation $p(n)$ for the number of partitions of $n$.

If we represent the number of partitions of the integer $n$ by $P_n$, we have shown that $P_5 = 7$. These partitions have 1, 2, 2, 3, 3, 4 and 5 parts, respectively.

If we represent the number of partitions of $n$ with exactly $k$ parts by $P_n^k$, then we have $P_5^1 = P_5^2 = P_5^3 = P_5^4 = P_5^5 = 1$.

To check your understanding of the material so far, try the following exercises.

E1) Write down all the partitions of 7. Also find $P_7^4$ and $P_7^5$.

E2) Let us consider the situation of the detergent manufacturer again. Suppose she only wants to distribute 10 gift tokens in 5 specific sales districts, where the sales are low. What is the number of ways of doing this?

You may wonder if you've found all the partitions in E2. One way to check is by finding out the required number in terms of partitions of smaller numbers, which may be easier to find. One such relation between partitions of $n$ and $n+1$, $n+2$, etc. is given in the following theorem.

**Theorem 1:** $P_n^1 + P_n^2 + ... + P_n^k = P_{n+k}^k$, $P_n^1 = P_n^n = 1$, for $1 \leq k \leq n$, that is, the number of partitions of $n$ with at most $k$ parts is the same as the number of partitions of $n+k$ with exactly $k$ parts.

Before we begin the proof of this theorem, let us consider an example. Let us take $n=4$, $k=3$. According to Theorem 1, we must have $P_4^1 + P_4^2 + P_4^3 = P_7^3$. Note that $P_4^1 + P_4^2 + P_4^3$ is the total number of partitions of 4 with 1, 2 or 3 parts, i.e., the number of partitions with **at most** 3 parts. There is one partition of 4 with one part, $4=4$. Let us write this as a 3-tuple, $(4, 0, 0)$, adding two more zeroes since we are considering partitions with at most 3 parts. If we add 1 to all the entries of this 3-tuple, we get $(4+1, 0+1, 0+1) = (5, 1, 1)$ and $(1+1+5$ is a partition of 7 with three parts. Similarly, consider the partition $4=1+3$ of 4 into two parts. Again, we can write this as $(1, 3, 0)$.

&lt;page_number&gt;186&lt;/page_number&gt;
&lt;watermark&gt;GOVERNMENT OF THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 53

Partitions and Distributions

Now, if we add 1 to each of the entries, we get (2, 4, 1) and 1+2+4 is a partition of 7 into three parts. Conversely, if we take the partition 7 = 1 + 3 + 3 of 7 into three parts, write it as (1, 3, 3) and **subtract** 1 from all the entries, we get (0, 2, 2) which corresponds to the partition 4 = 2+2 of 4 into 2 parts. In this way, we can match every partition of 4 with **at most 3** parts with a partition of 7 with **exactly 3** parts, and vice versa. This is the basic idea behind our proof of Theorem 1, which we now give.

**Proof of Theorem 1:** The cases P<sub>n</sub><sup>1</sup> = 1 = P<sub>n</sub><sup>n</sup> follow from the definition.

We will prove the general formula now. Let M be the set of partitions of n having k or less parts. We can consider each partition belonging to M as a k-tuple after adding as many zeroes as necessary. Define the mapping

(p<sub>1</sub>, p<sub>2</sub>, ..., p<sub>m</sub>, <u>0, 0, ..., 0</u>) ... (p<sub>1</sub>+1, p<sub>2</sub>+1, ..., p<sub>m</sub>, <u>+ 1, 1, ..., 1</u>), m ≤ k

from M into the set M' of partitions of n+k into exactly k parts. This mapping is bijective, since

i) two distinct k-tuples in M are mapped onto two distinct k-tuples in M';
ii) every k-tuple in M' is the image of a k-tuple of M. This is because, if (p<sub>1</sub>, p<sub>2</sub>,...,p<sub>k</sub>) is a partition of n+k with k parts, then it is the image of (p<sub>1</sub> - 1, p<sub>2</sub> - 1,..., p<sub>k</sub> - 1) under the mapping above.

Therefore, |M| = P<sub>n</sub><sup>1</sup> + ... + P<sub>n</sub><sup>k</sup> = |M'| = P<sub>n+k</sub><sup>k</sup>, and the theorem is proved.

**Note that** P<sub>n</sub><sup>k</sup> = 0 **if** n < k, since there is no partition of n with k parts if n < k. Also,

P<sub>n</sub><sup>n</sup> = P<sub>n</sub><sup>1</sup> = 1

The formula in Theorem 1 is an identity which allows us to find P<sub>n</sub><sup>r</sup> from values of P<sub>m</sub><sup>k</sup>, where m < n, k ≤ r. This is why it is also called a **recurrence relation** for P<sub>n</sub><sup>k</sup>.

Theorem 1 is every useful. For instance, to verify your count in E2, you can use it because P<sub>10</sub><sup>5</sup> = P<sub>5</sub><sup>1</sup> + P<sub>5</sub><sup>2</sup> + ... + P<sub>5</sub><sup>5</sup> = 7.

From Theorem 1, the P<sub>n</sub><sup>k</sup> s may be calculated recursively as shown in Table 1.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

Table 1 : P<sub>n</sub><sup>k</sup> for 1 ≤ n, k ≤ 6

<table>
<thead>
<tr>
<th>n</th>
<th>k</th>
<th>1</th>
<th>2</th>
<th>3</th>
<th>4</th>
<th>5</th>
<th>6</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td></td>
<td>1</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>2</td>
<td></td>
<td>1</td>
<td>1</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>3</td>
<td></td>
<td>1</td>
<td>1</td>
<td>1</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>4</td>
<td></td>
<td>1</td>
<td>2</td>
<td>1</td>
<td>1</td>
<td>0</td>
<td>0</td>
</tr>
<tr>
<td>5</td>
<td></td>
<td>1</td>
<td>2</td>
<td>2</td>
<td>1</td>
<td>1</td>
<td>0</td>
</tr>
<tr>
<td>6</td>
<td></td>
<td>1</td>
<td>3</td>
<td>3</td>
<td>2</td>
<td>1</td>
<td>1</td>
</tr>
</tbody>
</table>

In this table, the second entry in the row corresponding to n = 4 is P<sub>4</sub><sup>2</sup>. By Theorem 1, P<sub>4</sub><sup>2</sup> = P<sub>2</sub><sup>1</sup> = P<sub>2</sub><sup>2</sup>, which is the sum of the entries in the row corresponding to n = 2

Similarly, P<sub>6</sub><sup>3</sup> is the sum of the entries in the row corresponding to n = 3.

&lt;page_number&gt;187&lt;/page_number&gt;

---


## Page 54

Basic Combinatorics

Now, here is an exercise for you.

E3) Use Table 1 to find the values of P<sub>7</sub><sup>k</sup>, 1 ≤ k ≤ 6.

The partition of a number n into k parts also tells us how n objects can be distributed among k boxes. We will now consider all possibilities of such distributions.

## 4.3 DISTRIBUTIONS

By a distribution we mean a way of placing several objects into a number of containers. For example, consider the distribution of 6 balls among 3 boxes. We may have all 6 balls of different shapes, sizes and colours, i.e., they are all distinguishable. Or, all the balls could be exactly the same, i.e., they are all indistinguishable.

Similarly, all 3 boxes may look different, or all 3 could be exactly the same. So, we see that there are 4 possibilities here.

In fact, we have the following possibilities for any set of n objects and m boxes.

**Case 1:** The objects are distinguishable, and so are the boxes;

**Case 2:** The objects are distinguishable and the boxes are indistinguishable;

**Case 3:** The objects are indistinguishable and the boxes are distinguishable;

**Case 4:** The objects are indistinguishable, and so are the boxes.

You may be surprised to know that in each of the cases the number of such distributions is different. In fact, the distribution problem is to count all possible distributions in any of these situations, or in a combination of these cases.

A general guideline for modelling a ‘distribution problem’ is that a distribution of distinct objects corresponds to an arrangement, and a distribution of identical objects corresponds to a selection. Let us consider examples of each of the four cases given above.

(a) There are twenty students and four colleges. In how many ways can the students be accommodated in the four colleges?

In this example the students, as well as the colleges, are clearly distinguishable. This comes under Case (1).

(b) Suppose we want to group 100 students into 10 groups of 10 each for the purpose of a medical examination. In how many ways can this be done?

Here the groups are indistinguishable, though the students in them are distinguishable. Hence, this falls under Case (2).

(c) An employer wants to distribute 100 one-rupee notes among 6 employees. What is the number of ways of doing this?

Though the one-rupee notes can be distinguished by their distinct numbers, we don’t consider them to be distinguishable as far as their use is concerned. The employees, of course, are distinguishable. Hence, this is an example of Case (3).

(d) There are 1000 one-rupee notes. In how many ways can they be bundled into 20 bundles?

&lt;watermark&gt;GOVERNMENT UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;188&lt;/page_number&gt;

---


## Page 55

Partitions and Distributions

As before, the rupee notes are treated as indistinguishable. Clearly, the bundles are, by themselves, not distinguishable. Only the quantity in each may vary. Hence, this falls under Case (4).

Let us consider each case in some detail now.

## 4.3.1 Distinguishable Objects into Distinguishable Containers

Let us consider the example (A) above. Since any number of students can be put in a college, there are $20 \times 20 \times 20 \times 20$ possibilities, by the multiplication principle.

More generally, suppose we are distributing n objects into m containers, both being distinguishable. Then the total number of such distributions is $n^m$.

Let us look at an example.

**Example 1:** Show that the number of words of length n on an alphabet of m letters is $m^n$.

**Solution:** The m letters of the alphabet can be used any number of times in a word of n letters. The word can be considered as n ordered boxes, each holding a letter from the alphabet. The boxes become distinguishable because they are ‘ordered’. The letters of the alphabet are clearly distinguishable. So, the number of ways of doing this is $m^n$.

* * *

Several people are confused while solving the problem above. They tend to take the m letters as the containers instead! Let’s consider another example.

**Example 2:** Suppose we have a set S with n objects. An m-sample from this set S is an ordered arrangement of m letters taken from S, with replacement at every draw, in m draws. Find the number of m-samples from an n-element set.

**Solution:** Every m-sample is a word of length m from the ‘alphabet’ S containing n letters. Hence, the required number is $n^m$.

* * *

Now here are some exercises for you to solve.

---

E4) Find the number of three-letter words that can be formed using the letters of the English alphabet. How many of them end in x? How many of them have a vowel in the middle position?

E5) How many five-digit numbers are even? How many five-digit numbers are composed of only odd digits?

E6) There are 4 women and 5 men. A committee of three, a president, a vice-president, and a secretary, has to be formed from them. In how many ways can this be done if
i) the vice-president should be a woman?
ii) exactly one out of the vice-president and the secretary should be a woman?
iii) there is at least one woman in the committee?

---

Now suppose, we want to find the number of distributions of n distinguishable objects into m distinguishable containers, with **the extra condition** that no container should

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;189&lt;/page_number&gt;

---


## Page 56

Basic Combinatorics

contain more than one object. It is clear that this requires m ≥ n. Then we can get all these arrangements by first choosing n containers to contain exactly one object, and then permuting the n objects among the chosen containers. This can be done in C(m, n). n! = P(m, n) ways.
So, we have proved the following result.

**Theorem 2:** The number of ways of distributing n distinguishable objects into m distinguishable containers such that no container contains more than one object is P(m, n).

For example, the cardinality of the set of 5-digit numbers with all digits being distinct odd numbers is P(5,5). This is because the possible digits are 1, 3, 5, 7, 9.

Why don’t you try an exercise now?

E7) Find the number of m-letter words with distinct letters, all taken from an alphabet with n letters, where n ≥ m. Is this different from the number of injective mappings from an m-element set into an n-element set, where n ≥ m? Give reasons for your answer.

Let us now consider the second type of distribution.

## 4.3.2 Distinguishable Objects into Indistinguishable Containers

Here we shall find the number of ways of distributing n distinguishable objects into m indistinguishable containers. For this, we first find the number when exactly k of the containers are occupied. This brings us to Stirling numbers of the second kind, named after James Stirling (1692-1770).

Suppose n ≥ m. The number of distributions of n distinguishable objects into m indistinguishable containers **such that no container is empty** is represented by S<sup>m</sup><sub>n</sub>. This number is called the Stirling number of the second kind. As you can see, this is also the number of partitions of a set of n objects into m classes.

**Definition:** For natural numbers n and m, the **Stirling number of the second kind**, S<sup>m</sup><sub>n</sub>, is the number of partitions of an n-element set into exactly m parts.

Note that:

i) S<sup>m</sup><sub>n</sub> = 0 if n < m, for, if the number of containers exceeds the number of objects, then it is impossible to have all the containers non-empty.

ii) S<sup>n</sup><sub>n</sub> = 1, since there is only one way of putting n distinguishable objects in nindistinguishable boxes so that no box is empty.

iii) S<sup>1</sup><sub>n</sub> = 1.

Now, we shall use the inclusion exclusion principle to find the value of S<sup>m</sup><sub>n</sub>.

**Theorem 3:** S<sup>m</sup><sub>n</sub> = $\frac{1}{m!} \sum_{k=0}^{m} (-1)^k C(m, m-k)(m-k)^n$, n ≥ m.

**Proof:** If the m classes are distinguishable, the number of partitions is the same as the number of functions from an n-element set onto an m-element set. As the classes are distinguishable here, we have to divide this number by m!. The result follows from Theorem 8, Block 3 Unit 2.

&lt;page_number&gt;190&lt;/page_number&gt;
&lt;watermark&gt;GO THE PEOPLE UNIVERSITY&lt;/watermark&gt;

---


## Page 57

Partitions and Distributions

For example, to obtain the Stirling number, $S_5^3$, we know that the number of functions from a 5-element set onto a three-element set is 150. So, by Theorem 3, $S_5^3 = 150/3! = 25$.

**Remark:** You may be wondering how we have jumped straightaway to the Stirling numbers of the second kind. What about the first kind? We won’t be using them in any way here. However, for a the sake of completeness, we define **Stirling numbers of the first kind**, $s(n, k)$, as follows.

For a positive integer n, and $0 \leq k \leq n$, $s(n, k)$ is the coefficient of $x^k$ in the expansion of the multinomial $x(x - 1)(x - 2) \ldots (x - n + 1)$.

Getting back to $S_n^m$, you may feel that the formula in Theorem 3 is a little cumbersome. Sometimes, the following recurrence relation for $S_n^m$ may be more useful.

**Theorem 4:** If $1 < m \leq n$, then $S_{n+1}^m = S_n^{m-1} + mS_n^m$.

**Proof:** Let us take n+1 objects, mark one of them, and consider the distribution of these n+1 objects into m indistinguishable containers. Then we have 2 situations.

**Case (1)** (The marked object is placed in one container without any other objects.): In this case, the remaining n objects can be placed in $(m - 1)$ containers in $S_n^{m-1}$ ways.

**Case (2)** (The marked object is placed with at least one more object in a container.): In this case, we can first distribute the n unmarked objects into m containers, and then put the marked objects m to one of these m containers. So, the number of such partitions is $mS_n^m$.

Therefore, by the addition principle, we get $S_{n+1}^m = S_n^{m-1} + mS_n^m$.

There is a generalisation of Theorem 4 that is of independent interest, which we now state.

**Theorem 5:** $S_{n+1}^m = \sum_{k=0}^n C(n, k) \cdot S_k^{m-1}$

**Proof:** Let us mark one object in a set of (n+1) objects. Suppose the marked object is present in a box with $(n - k + 1)$ elements, where $m - 1 \leq k \leq n$. Then we can choose n-k more objects to go with the marked object in $C(n, n-k)$ ways. The remaining k objects can be distributed into $(m - 1)^n$ boxes in $S_k^{m-1}$ ways. So the number of ways of distributing the n-k objects is $C(n, n-k) \cdot S_k^{m-1}$. The result now follows from the addition principle by allowing k to vary from 0 to n.

Let us see some examples of the use of these recurrences.

**Example 3:** Calculate $S_3^2$ and $S_4^2$.

**Solution:** Using Theorem 4, we get $S_3^2 + S_2^1 = 2 \times S_2^2 = 1 + 2 \times 1 = 3$, and $S_4^2 + S_3^1 = 2 \times S_3^2 = 1 + 2 \times 3 = 7$.

* * *

Now let us find what we had started with in this sub-section.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;191&lt;/page_number&gt;

---


## Page 58

Basic Combinatorics

**Theorem 6:** The number of ways of distributing n distinguishable objects into m indistinguishable containers is $S_n^1 + S_n^2 + ... + S_n^m$, where n ≥ m. (Note that here we do not insist that no container is empty.)

**Proof:** When we distribute n distinguishable objects into m indistinguishable containers there are m cases. Case (k) is that exactly k containers are non-empty. Here k varies from 1 to m. The number of distributions in Case (k) is $S_k^n$. The result now follows from the addition principle.

Let us consider an example.

**Example 4:** In how many ways can 20 students be grouped into 3 groups?

**Solution:** Theorem 6 says that this can be done in $S_{20}^1 + S_{20}^2 + S_{20}^3$ ways.

Now, using Theorem 3, we get this number to be

$1 + \frac{1}{2} \sum_{k=0}^{2} (-1)^k C(2, 2-k)(2-k)^{20} + \frac{1}{6} \sum_{k=0}^{3} (-1)^k C(3, 3-k)(3-k)^{20}$

$= 581,130,734.$

Try some exercises now.

* * *

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E8) Find the number of surjective functions from an n-element set onto an m-element set.

E9) Find the number of ways of placing n people in n - 1 rooms, no room being empty.

Let us now consider the third possibility for distributing objects into containers.

## 4.3.3 Indistinguishable Objects into Distinguishable Containers

Suppose there are n indistinguishable objects and m distinguishable containers. As the objects are indistinguishable, the distributions depend only on the number of objects in each container. As the containers are distinguishable, they can be assumed to be arranged in a line. Hence, the number of distributions is the number of ways of writing the number n as the sum x₁ + x₂ + ... + xₘ, where the xᵢ's are non-negative integers.

We have covered this situation in Theorem 5 of Block 3 Unit 1. Over there we have shown that **the number of distributions of n indistinguishable objects into m distinguishable containers is C(m+n-1, n)**. In particular, the number of non-negative integral solutions of the equation x₁ + x₂ + ... + xₘ = n is C(m+n-1, n).

Incidentally, we note that the number of distributions of n indistinguishable objects into m distinguishable containers with at most one object per container is C(m, n).

Let us consider an example.

**Example 5:** How many distinct solutions are there of x + y + z + w = 10
i) in non-negative integers?
ii) in positive integers?

&lt;page_number&gt;192&lt;/page_number&gt;

---


## Page 59

Partitions and Distributions

**Solution:**

i) From the result quoted above, the answer is C(4 + 10 - 1, 10) = 286.

ii) We want x, y, z, w to be positive. Hence, we can write them respectively as X+1, Y+1, Z+1, W+1, where X, Y, Z, W are non-negative. Hence we want the number of non-negative solutions of the equation X+1+Y+1+Z+1+W+1=10, i.e., X+Y+Z+W=6. The answer, now, is C (4 + 6 - 1, 6) = 84.
Try some exercises now.

---

E10) Show that the number of positive solutions of the equation x₁+x₂+...+xₙ=m is C(m-1, m-n).

E11) In how many ways can an employer distribute 100 one-rupee notes among 6 employees so that each gets at least one note?

Let us now consider the fourth case.

## 4.3.4 Indistinguishable Objects into Indistinguishable Containers

Suppose there are n indistinguishable objects and m indistinguishable containers. Any distribution is determined purely by an **unordered** m-tuple of non-negative integers with sum n. This is equivalent to the number of increasing sequences of length m of non-negative integers with sum n. But this is precisely the number of partitions of the integer n with at most m parts, viz., Pⁿ¹ + Pⁿ² + ... + Pⁿᵐ = Pⁿᵐ⁺ⁿ, from Theorem 1 of this unit.

Let us consider an example of this case.

**Example 6:** In how many ways can 20 identical books be placed in 4 identical boxes?

**Solution:** The answer is P²₀ + P³₀ + P⁴₀ = P⁴₂₄

Why don't you try some exercises now?

---

E12) In how many ways can 1000 one-rupee notes be bundled into a maximum of 20 bundles?

E13) A car manufacture has 5 service centres in a city. 10 identical cars were served in these centres for a particular mechanical defect. In how many ways could the cars have been distributed at the various centres?

With this we have come to the end of this unit. Let us take a quick look at what we have studied in this unit.

## 4.4 SUMMARY

1. A partition of n∈N into k parts is x₁+x₂+...+xₖ=n, where x₁ ≤ x₂ ≤ ... ≤ xₖ. Pⁿ is the set of all partitions of n, and Pⁿᵏ is the set of all partitions into exactly k parts.

2. The proof and applications of the recurrence relation,
Pⁿ¹ + Pⁿ² + ... + Pⁿᵏ + = Pⁿᵏ⁺ⁿ, + Pⁿ¹ = Pⁿ = 1, 1 ≤ k ≤ n.

3. The number of ways of distributing n objects into m containers is :

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;193&lt;/page_number&gt;

---


## Page 60

**Basic Combinatorics**

i) n^m, if the objects and containers are distinguishable.
ii) $\sum_{i=1}^{m} S_n^i$, if the objects are distinguishable but the containers are not.
(Here $S_n^i$ is a Stirling number of the second kind).
iii) C(m+n-1, n) if the objects are not distinguishable but the containers are distinguishable.
iv) P_{n+m}^m, if neither the objects nor the containers are distinguishable.

Further, in (i) above, if there is an extra requirement that each container contain at most one object, then the number of distributions is P(m, n). Again, in (iii) above, with the same extra requirement, the number of distributions is C(m, n).

## 4.5 SOLUTIONS / ANSWERS

E1) In the table below we give all possible partitions of 7.

Table 2

<table>
<thead>
<tr>
<th>Number of parts</th>
<th>Partitions</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>7</td>
</tr>
<tr>
<td>2</td>
<td>1+6, 2+5, 3+4</td>
</tr>
<tr>
<td>3</td>
<td>1+1+5, 1+2+4, 1+3+3, 2+2+3</td>
</tr>
<tr>
<td>4</td>
<td>1+1+1+4, 1+1+2+3, 1+2+2+2</td>
</tr>
<tr>
<td>5</td>
<td>1+1+1+1+3, 1+1+1+2+2</td>
</tr>
<tr>
<td>6</td>
<td>1+1+1+1+1+2</td>
</tr>
<tr>
<td>7</td>
<td>1+1+1+1+1+1+1</td>
</tr>
</tbody>
</table>

From the table, we see that P_7^4 = 3, P_7^5 = 2.

E2) The required number is P_10^5 = 7.

E3) P_7^1 = 1 = P_7^7.

P_7^2 = P_5^1 + P_5^2 = 1 + 2 = 3, from Table 1.

P_7^3 = P_4^1 + P_4^2 + P_4^3 = 1 + 2 + 1 = 4, from Table 1.

Similarly, P_7^4 = P_3^1 + P_3^2 + P_3^3 + P_3^4 = 3, P_7^5 = P_2^1 + P_2^2 = 2 and P_7^6 = P_1^1.

E4) The 26 letters are distinguishable objects. We have to fill then in three distinguishable containers, viz., the first, second, and third positions of a three-lettered word. The solution is 26^3.

If the last letter is to be x, the number is only 26^2 × 1.

If the middle letter is a vowel, then then by the multiplication principle, the answer is 26 × 5 × 26.

E5) The total number of even numbers is 9 × 10 × 10 × 10 × 5 = 45,000, since the last digit can only by 0, 2, 4, 6 or 8.

The number of 5-digit numbers composed of only odd digits (i.e., 1, 3, 5, 7, 9) is clearly 5^5 = 3125.

&lt;page_number&gt;194&lt;/page_number&gt;

---


## Page 61

Partitions and Distributions

E6) i) We can choose a woman for vice-president in 4 ways. To fill the remaining 2 positions we can select 2 from the remaining 8 persons in $8 \times 7 = 56$ ways. Hence, the required number is $4 \times 56 = 224$.

ii) If the vice-president is a woman (chosen in 4 ways), others can be selected in $5 \times 4 = 20$ ways. Similarly, if the woman is a secretary, the others can be chosen in 20 ways. Hence, by the addition and multiplication principles, the answer is $20 \times 4 + 20 \times 4 = 160$.

iii) Without any restriction, three can be selected in $9 \times 8 \times 7 = 504$ ways. If no woman is to be selected, then it can be done in $5 \times 4 \times 3 = 60$ ways. What we need is the complement of this. Thus, the required answer is $504 - 60 = 444$.

E7) If the alphabet has n letters, the m-letter words with distinct letters can be formed in $n(n-1)(n-2) \ldots (n-m+1) = P(n,m)$ ways.

Now, in an injective mapping, images of distinct elements should be distinct (see Unit 1). There are n possible images for the first element of the m-set, n−1 possible images for the second, and so on. Hence, the number of such mappings is also P(n, m).

E8) Suppose N = {1, 2, ..., n} and M = {1, 2, ..., m}. If f is an onto function from N to M, then the inverse images, $f^{-1}(1)$, $f^{-1}(2)$, ..., $f^{-1}(k)$ constitute a partition of N into m classes. The number of ways in which this can be done is $S_n^m$, where the order of partition is immaterial. But, in functions, the order cannot be ignored. So, the distribution can be done in m!.$S_n^m$ways.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E9) This is $S_n^{n-1}$. This can be done by putting one person each in n − 2 rooms and 2 persons in 1 room. This can be done in C(n, 2) ways. So $S_n^{n-1} = C(n,2)$.

E10) If a positive solution is x₁, x₂, ..., xₙ, then it can be written as X₁+1, X₂+1,..., Xₙ+1, where the Xᵢ’s are non-negative. Thus, the required number is the number of non-negative solutions of X₁+X₂+...+Xₙ+n = m, which is C(n + m − n − 1, m − n) = C(m − 1, m − n).

E11) This is the number of positive solutions of x₁+...+x₆ = 100.
So, the required number is C(100 − 1, 100 − 6) = C(99, 94) = 71,523,144.

E12) $P_{1000}^1 + P_{1000}^{20} + P_{1020}^{20}$.

Had the requirement been that there be exactly 20 bundles, then the number would have been $P_{1000}^{20}$.

E13) $P_{10}^1 + P_{10}^2 + P_{10}^3 + P_{10}^4 + P_{10}^5 = P_{15}^5$.

&lt;page_number&gt;195&lt;/page_number&gt;

---


## Page 62

&lt;img&gt;IGOU logo&lt;/img&gt;
THE PEOPLE'S UNIVERSITY