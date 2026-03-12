## Page 1

Block
# 2

## SETS, RELATIONS AND FUNCTIONS

<table>
  <tr>
    <td>Unit 1<br>Sets, Relations and Functions</td>
    <td>71</td>
  </tr>
  <tr>
    <td>Unit 2<br>Automata and Languages</td>
    <td>93</td>
  </tr>
  <tr>
    <td>Unit 3<br>Computability and Complexity</td>
    <td>117</td>
  </tr>
</table>

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 2

# BLOCK INTRODUCTION

## Block 2: Sets, Relations and Functions

The block comprises three units: (i) Sets, Relations and Functions (ii) Automata and Languages (iii) Computability and Complexity. In the first unit we introduce you to various kinds of sets and operations like, ‘union’ and ‘intersection’. While doing so you will see in what way Venn diagrams are a useful tool for understanding and working with sets. Next we discuss what a relation is, and expose you to some important types of relations. Finally, we lead you detailed discussion of functions.

In the second unit we introduce a special kind of a set i.e., a language which is a set of strings over an alphabet. First we describe what a language is and what the operations we perform on languages. Certain set of strings or languages are represented in algebraic fashion, then these algebraic expressions of languages are called regular expressions. A language represented by a regular expression is called a regular language. Then we introduce a notion of finite automata, also called finite state machine or deterministic finite automata. that recognizes regular languages. Finally, we introduce another kind of a theoretical machine, called nondeterministic finite automata (NFA). In deterministic finite automata (DFA), there is a unique next state for transition on input in a given state. If we relax this condition of uniqueness of the next state in DFA, we get NFA. But any set accepted by NFA can be also accepted by DFA. However, the concept of non-determinism plays an important role in both the theory of computation and design and analysis of algorithm, especially in defining complexity classes.

In the last unit of the block we examine a more powerful machine called Turing machine which recognizes more languages than the Finite Automata and also explain the terms computability and complexity classes. In this unit we define the complexity classes through a language theoretic framework.

&lt;watermark&gt;UNIVERSITY&lt;/watermark&gt;

---


## Page 3

# UNIT 1 SETS, RELATIONS AND FUNCTIONS

## Structure

1.0 Introduction
1.1 Objectives
1.2 Introducing Sets
1.3 Operations on Sets
    1.3.1 Basic Operations
    1.3.2 Properties Common to Logic and Sets
1.4 Relations
    1.4.1 Cartesian Product
    1.4.2 Relations and their types
    1.4.3 Properties of Relations
1.5 Functions
    1.5.1 Types of Functions
    1.5.2 Operations on Functions
1.6 Summary
1.7 Solutions/Answers

## 1.0 INTRODUCTION

In common parlance, we find people using the words given in the title of this unit. Do they have the same meaning in mathematics? You'll find this out by studying this unit. You will also see how basic the concept of 'set' and 'function' or to any area of mathematics and subjects depend on mathematics.

In this unit we will begin by introducing you to various kinds of sets. You will also study operations like, 'union' and 'intersection'. While doing so you will see in what way Venn diagrams are a useful tool for understanding and working with sets.

Next we will discuss what a relation is, and expose you to some important types of relations. You will come across while studying banking, engineering, information technology and computer science, of course mathematics. As you will see in your study of computer science, an extensive use of functions is made in problem-solving.

Finally, we lead you detailed discussion of functions. Over here we particularly focus on various points of functions and fundamental operations on functions.

## 1.1 OBJECTIVES

After studying this unit, you should be able to:

*   Explain what a set, a relation or a function is
*   Give examples and non-examples of sets, relations and functions
*   Perform different operations on sets
*   Establish relationships between operations on sets and those on statements in logic
*   Use Venn diagrams
*   Explain the difference between a relation and a function.
*   Describe different types of relations and functions.
*   Define and perform the four basic operations on functions

## 1.2 INTRODUCING SETS

In our daily life we encounter collections, like the collection of coins of various countries, a collection of good students in a class, a collection of faculty members of IGNOU, etc. In the first of these examples, it is easy for anybody

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;71&lt;/page_number&gt;

---


## Page 4

Basic Combinatorics

anywhere to tell whether an object belongs to this collection or not. If we take the collection of coins of a country, then a coin will be in the collection if it is a coin of that country, not otherwise. The criterion for being a member of the collection is objective and clear. However, if we take the collection of all good students, it is very difficult to say whether a person belongs to this collection or not because the characteristic *good* is not very clearly defined. In this case the collection is not ‘well-defined’, while the previous collection is ‘well-defined’. Similarly, the collection of all the IGNOU students is well-defined.

**Definition:** A **set** is a well-defined collection. The objects belonging to a set are called **elements** or **members** of that set.

We write the elements of a set within curly brackets. For instance, consider the set A of stationary items used by Nazia. We write this as

A = {pen, pencil, eraser, sharpener, paper}

Another example is the set

B = {Lucknow, Patna, Bhopal, Itanagar, Shillong} of the capitals of 5 states of India.

Note that A and B are well-defined collections. However, the collection of short people is not well-defined, and therefore, itis not a set.

Also note that the elements of a set don’t have to appear ‘similar’. For example, {Pen, Lucknow, 4} is a set consisting of 3 clearly defined elements.

As you have seen, we usually, denote sets by capital letters of the English alphabet. We usually denote the elements by small letters a, b, x, y…. If x is an element of a set A, we write this as x∈A (read as ‘x belongs to A’). If x is not an element of A, we write this as x∉A (read as ‘x does not belong to A’).

There are three ways of representing sets: ‘Set-builder form’, ‘Tabular form’ and the pictorial representation through Venn diagrams.

In the ‘Set-builder form’, or ‘property method’ of representation of sets, we write between brackets { } a variable x, which stands for each of the elements of the set which have the properties p(x), and separate x and p(x) by a symbol ‘:’ or ‘|’ (read as ‘such that’). So the set looks like {x: p(x)} or {x | p(x)}.

For instance, the set {x | x is a white flower} is the set of all white flowers, or {x: x isanaturalnumberand2<x<11} is the set of natural numbers lying between 2 and 11.

In ‘Tabular form’, or the ‘listing method’, the elements of a set are listed one by one within the brackets { }, each separated from the other by a comma, as in the examples A and B given above.

The accepted convention for writing a set by the listing method is that elements will not be repeated. For example, in the set A= {4, 2, 8, 2, 6}, 2 is repeated, which is not necessary. So we will write A = {4, 2, 8, 6}.

We shall introduce you to Venn diagrams a little later. For now, let us consider a few more sets.

**Definition:** A set with no element is called the **empty (or null, or void) set**, and is denoted by φ or { }.

For example, A = {x:x is an integer between 13and 17which is divisible by 6}, has no element, i.e., A is the **empty set**.
**Definition:** A set having a finite number of elements is called a **finite set**.

&lt;page_number&gt;72&lt;/page_number&gt;
&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 5

Sets, Relations and Functions

For example, { 1,2,4,6} is a finite set because it has four elements,∅, the null set, is also a finite set because it has zero number of elements; the set of stars in the sky is also a finite set.

**Definition:** A set having infinitely many elements is called an **infinite set.**

For example, the set **N** of natural numbers is infinite. Similarly, **Q**, **Z**, **R** and **C**, these to fractional numbers, integers, real numbers and complex numbers, respectively, are infinite set.

Now try the following exercises.

E1) How would you represent the set of all students who have offered the IGNOU course?

E2) Explain, with reason, whether or not
i) The collection of all good teachers is a set
ii) The set of points on a line is finite.

E3) Represent the set of all integers by the listing method.

When we deal with several sets, we need to understand the nature of the elements of those sets, whether the elements of two given sets have some elements in common or not, and so on. These questions involve concepts, which we now define.

**Definition:** A set A is said to be a **subset** of a set B if each element of A is also an element of B. In this case B is called a **superset** of A. If A is a subset of B, were present this by **A⊆B**.

As a statement in logic we represent this situation as,

A⊆B ⇔ [x∈A⇒x∈B]

‘B contains A’ or ‘B is a super set of A’ is represented by **B⊇A**.
If A is not a subset of B, were present this by **A⊈B**.

For example, if A = {4,5,6}and B = {4,5,7,8,6}, then A⊆B. But if C = {3,4} then C⊈B.

**Remark:** If A⊆B and B⊆C, then A⊆C.

**Definition:** Two sets A and B are **equal** if every element of A belongs to B and every element of B belongs to A. We represent this by **A=B**.

For example, if A={ 1,2,3 }, B = {2,3,1},then A⊆B and B⊆A, so that A =B.

**Definition:** A set A is said to be a **proper subset** of a set B if A is a subset of B and A and B are not equal. We represent this by **A⊂B**.

For example, if A = {4,5,6}and B = {4,5,7,8,6}, then A⊂B; and if A={ Java, C, C++,Cobol}and B={ Java, C++},then A⊃B.

**Note:** A set can have many subsets and many supersets. For example A={ 1,2,3,4,5 },B={2,3,4,5,6,7 },and C={2,3},then for C, A and B can be used as supersets.
Similarly, if X= { Ram, Rani, Sita, Gita }, Y= { Rani }, and Z= { Sita }, then Y and Z both are subsets of X.

**Definition:** The **power set** of a set A is the set of all the subsets of A, and is denoted by **P(A)**.

&lt;watermark&gt;IGNOU&lt;/watermark&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;John Venn&lt;/img&gt;
(1834 -1923)
Fig1: JohnVenn

&lt;page_number&gt;73&lt;/page_number&gt;

---


## Page 6

Basic
Combinatorics

Mathematically, P(A)={x:x⊆A}.

Note that ∅∈P(A) and A∈P(A) for all sets A. For example, if A={1}, then P(A)={∅,{1}} and if A={1,2}, then P(A)={∅,{1},{2},{1,2}}
Similarly, if A={1,2,3},then P(A)={∅,{1},{2},{3},{1,2},{1,3},{2,3},{1,2,3}}.

**Definition:** Any set which is a **superset** of all the sets **under consideration** is known as the **universal set**. This is usually denoted by Ω, S or U.

For example, if A = {1,2,3}, B = {3,4,6,9} and C = {0,1}, then we can take U= {0,1,2,3,4,5,6,7,8,9} or U= N, or U=Z as the universal set.

Note that the universal set can be chosen arbitrarily for a given problem. But once chosen, it is fixed for the discussion of that problem.

**Theorem1:** If A is a set with n elements, then |P(A)|=2^n.

**Proof:** We shall prove this by mathematical induction.
For this, we first check if it is true for n= 1.Then assuming that it is true for n = m, we prove it for the case n=m+1. It will, then, follow that the result will be true ∀n ∈ N.

**Step I:** If A=1, then P(A)=2=2^1.

**Step II:** Assume that the theorem holds for all sets A of cardinality k, i.e. if |A| = k, then A has 2^k subsets.

**Step III:** Now consider any set A = {x₁, x₂, x₃,...,xₖ, xₖ₊₁}, with k+1 elements. Consider its subset B= {x₁, x₂, x₃,...,xₖ }. Now B has 2^k subsets, each being a subset of A. Now, take any such subset{xᵢ₁,xᵢ₂,...,xᵢᵣ} of B. Then{xᵢ₁,xᵢ₂,...,xᵢᵣ,xₖ₊₁} is a subset of A that is not a subset of B. So, for each of the 2^k subsets of B, we attach xₖ₊₁ to it to get 2^k more subsets of A.

You can see that this covers all the subsets of A.

So the number of subsets of A=2^k+2^k =2.2^k=2^{k+1}. Hence the theorem.

Now try these exercises.

E4) Give two proper subsets and two supersets of the set of vowels of the English alphabet.

E5) Find the power set of the set A = {a,e,i,o,u}.

E6) For which set A, is P(A) = 1?

E7) If A⊆B, is P(A)⊆P(B)?Why?

E8) P(A)= P(B) ⇒A= B. True or false? Why?

Let us conclude this section with the **pictorial** representation of sets. You know that the pictorial representation of any object helps in understanding the object. This is why a pictorial representation of sets, known as a **Venn diagram**, helps in understanding and dealing with sets.

The English priest and logician John Venn invented the Venn diagram. Through Venn diagrams we can easily visualize the abstract concept of a set and operations

&lt;page_number&gt;74&lt;/page_number&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 7

Sets, Relations and Functions

on sets. In this diagram, the universal set is usually represented by a rectangle and its subsets are shown as circles or other closed geometrical figures inside this rectangle.

For example, A={Lucknow, Patna, Bhopal, Itanagar, Shillong} can be represented using a Venn diagram in Fig.2. Here U could be any super set of A.

&lt;img&gt;
A Venn diagram with a rectangle labeled "U" containing a circle labeled "A". Inside the circle "A", there are five elements listed vertically:
*   *Lucknow
*   *Patna
*   *Bhopal
*   *Itanagar
*   *Shillong
&lt;/img&gt;

**Fig. 2: A Venn diagram**

Now that you are familiar with basic definitions related to sets, let us discuss some basic operations that can be performed on sets. This is when we shall appeal to Venn diagrams very often, as you will see.

## 1.3 OPERATIONS ON SETS

Let us now study sets obtained by applying operations on sets. We will cover four operations here, namely, union of sets, intersection of sets, complement of sets and symmetric difference. While studying them you will see how useful a Venn diagram can be for proving results related to these operations. In this section we will also look at some rules that are common to operations on sets and operations on statements.

### 1.3.1 Basic Operations

In this sub-section we shall define each of the operations one by one.

**Definition:** The **union** of two sets A and B is the set of all those elements which are either in A or in B or in both A and B. This set is denoted by $A \cup B$, and read as ‘A union B’.

Symbolically, $A \cup B = \{ x : x \in A \text{ or } x \in B \}$

For example, if $A = \{ x : x \text{ is a stamp} \}$ and $B = \{ 4 , 5 \}$, then
$A \cup B = \{ x : x \text{ is a stamp or a natural number lying between 3 and 6} \}$.

And $A = \{ \text{Ram, Mohan, Ravi} \}$ and $B = \{ \text{Ravi, Rita, Neetu} \}$,
then $A \cup B = \{ \text{Ram, Mohan, Ravi, Rita, Neetu} \}$.

If $A \subseteq B$, then $A \cup B = B$, and vice versa. This can be shown immediately using a Venn diagram, as in Fig.3.(a), where A is shown as the square contained in the circle representing B. In Fig.3(b), $A \cup B$ is shown when A and B have some elements in common, and in Fig.3(c), we depict $A \cup B$ when A and B have no element in common.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;
Venn diagram (a): A rectangle labeled "U" contains a circle labeled "B" with a smaller circle labeled "A" inside it.
&lt;/img&gt;
(a)

&lt;img&gt;
Venn diagram (b): A rectangle labeled "U" contains two overlapping circles labeled "A" and "B".
&lt;/img&gt;
(b)

&lt;img&gt;
Venn diagram (c): A rectangle labeled "U" contains two separate circles labeled "A" and "B".
&lt;/img&gt;
(c)

**Fig.3: Venn diagram for union**

&lt;page_number&gt;75&lt;/page_number&gt;

---


## Page 8

Basic Combinatorics

**Definition:** The **intersection** of sets A and B is the set of all the elements which are common to both A and B. This set is denoted by $A \cap B$, and read as ‘A intersection B’.

Symbolically, $A \cap B = \{x : x \in A \text{ and } x \in B\}$;

For example $A = \{1, 2, 3\}$ and $B = \{2, 1, 5, 6\}$, then $A \cap B = \{1, 2\}$.

A gain if $A = \{1\}$ and $B = \{5\}$ then $A \cap B = \{\}$ or $\emptyset$.

**Remark:** For any two sets A and B, $A \cap B \subseteq A \subseteq A \cup B$ and $A \cap B \subseteq B \subseteq A \cup B$.

What is $A \cap B$ if $A \subseteq B$? Do you agree that it is A? Let us use a Venn diagram to check this (see Fig.4(a)). If A and B have some elements in common, then the Venn diagram for $A \cap B$ looks like Fig 4.(b), and if A and B have no element in common, then the Venn diagram will be as in Fig.4(c).

<mermaid>
graph TD
    subgraph U
        A
        B
    end
    A -- "A" --> A
    B -- "B" --> B
    A --- B
</mermaid>
(a)

<mermaid>
graph TD
    subgraph U
        A
        B
    end
    A -- "A" --> A
    B -- "B" --> B
    A --- B
    A --- A
    B --- B
</mermaid>
(b)

<mermaid>
graph TD
    subgraph U
        A
        B
    end
    A -- "A" --> A
    B -- "B" --> B
    A --- A
    B --- B
</mermaid>
(c)

Fig. 4: Venn diagram for intersection of sets

**Definition:** The **difference of two sets** A and B is the set of all those elements of A which are not elements of B. Sometimes, we call this set the **relative component** of Bin A. It is denoted by $A - B$ or $A \setminus B$, and is read as ‘A complement B’.

Symbolically, $A - B = \{x : x \in A \text{ and } x \notin B\}$ and
$B - A = \{x : x \in B \text{ and } x \notin A\}$

For example, if $A = \{4, 5, 6, 7, 8, 9\}$ and $B = \{3, 5, 2, 7\}$, then $A - B = \{4, 6, 8, 9\}$ and $B - A = \{3, 2\}$. From this example it is clear that $A - B \neq B - A$. In fact, this is usually the case. So, **the difference of sets is not a commutative operation.**

In Fig.5(a), $A \subseteq B$, so that $A - B = \emptyset$.

In Fig.5(b) we show $A - B$ when $A \supseteq B$, and in Fig.5(c) we show $A -$ when neither $A \subseteq B$ nor $B \subseteq A$.

In Fig.5(d), we show $A - B$ when A and B are disjoint.

<mermaid>
graph TD
    subgraph U
        A
        B
    end
    A -- "A" --> A
    B -- "B" --> B
    A --- A
    B --- B
    A --- A
    B --- B
</mermaid>
(a)

<mermaid>
graph TD
    subgraph U
        A
        B
    end
    A -- "A" --> A
    B -- "B" --> B
    A --- A
    B --- B
    A --- A
    B --- B
</mermaid>
(b)

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;76&lt;/page_number&gt;

---


## Page 9

Sets, Relations and Functions

&lt;img&gt;A Venn diagram with two circles A and B intersecting within a universal set U. The intersection area is shaded.&lt;/img&gt;
(c)

&lt;img&gt;A Venn diagram with one circle A intersecting with another circle B within a universal set U. The intersection area is shaded.&lt;/img&gt;
(d)

**Fig. 5: A~B in different situation is the shaded portion.**

There is one particular ‘difference’ that shows up very often, which we now define.

**Definition:** The **complement of a set** A, is the set U\A, and is denoted by A' or A^c. For example, U= {Physics, Chemistry, Mathematics} and A= {Mathematics}, then the complement of A is A'= {Physics, Chemistry}.

The Venn diagram showing the complement of A is the set of those elements of the universal set U which are outside A (see Fig.6).

&lt;img&gt;A Venn diagram showing the complement of set A. The universal set U is represented by a rectangle, and the complement of A is the unshaded portion of this rectangle.&lt;/img&gt;
Fig. 6: Venn diagram for A'.

**Definition:** The **symmetric difference** of two sets A and B is the set of all those elements which are in A or in B, but not in both. It is denoted by AΔB.
i.e., AΔB= (A~B)∪ (B~A).

Note that AΔB =BΔA, i.e. the symmetric difference is commutative.

For example A={1,2,3,4,5}and B={3,5,6,7},then A~B={1,2,4},and B~A={6,7}
∴ AΔB={(A~B)∪(B~A)}={1,2,4,6,7}

Now you may try these exercises.

E9) Make a Venn diagram for AΔB for each of the situations i) A⊆B, ii) A<B,
iii) B<A and A∩B≠∅; iv) A∩B=∅.

E10) Let A= {Math, Physics, Science}, B= {Computer, Math, Chemistry}, C= {Math}.
Find A∪(B∩C).

E11) If A={1,2,3,4,5,6}, B={4,5,6,7,8,9}, find i) A~ B, ii) B~ A, iii) AΔB.

E12) For which sets A and B would A~B=B~A?

E13) Write a program in C toper form E 10.

E14) Under what conditions can A∩B=A∪B?

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;77&lt;/page_number&gt;

---


## Page 10

Basic Combinatorics

While discussing these operations, you may be wondering that they seem to satisfy properties very similar to those of propositional logic covered in Block 1 of this course. You are right! Let us look at this aspects now.

## 1.3.2 Properties Common to Logic and Sets

Before looking into the properties we shall first present a very useful principle to you. This will allow you to see how one property can be proved in several situations simultaneously.

**Duality Principle:** The ‘duality principle’ is very convenient for dealing with theorems about sets. Basically if any theorem is given to you, by applying the duality principle you can get another theorem (the dual of the previous one). In any statement involving the union and intersection of sets, we can get from one of the statements to the other by inter changing ∩ with ∪ and φ with U.

For example, the dual of A∪(B∩C) is A∩(B∪C) and the dual of U∪φ=U is U∩φ=φ. So, for example what is true for A∪(B∩C) will be true for A∩(B∪C) too. This is why if the first property in each of the pairs below is proved the second one follows immediately.

For any universal set U and subsets A, B and C of U, **the following properties hold.**

i) **Associative properties:**
Union: A∪(B∪C)=(A∪B)∪C
Intersection: A∩(B∩C) = (A∩B)∩C

ii) **Commutative properties:**
Union: A ∪B= B ∪ A
Intersection: A∩B = B∩A.

iii) **Identity:**
Union: A∪φ=A
Intersection: A∩U=A.

iv) **Complement:**
Union: A ∪A' = U
Intersection: A∩A'=φ

v) **Distributive properties:**
Union: A ∪(B ∩C) = (A ∪B) ∩(A ∪C)
Intersection: A∩(B∪C) = (A∩B)∪(A∩C)

**DeMorgan’s Laws:**

For any two sets A and B the following laws known as DeMorgan’s laws, hold

1. (A∪B)'= A'∩B ', and
2. (A∩B)'= A'∪B'

DeMorgan’s law scan also be expressed as

1. A~(B∪C) = (A~ B)∩(A~ C)
2. A~(B∩C)= (A~ B)∪(A~ C)

Each of the properties above corresponds to a related property for mathematical statements in logic (which we have covered in Unit 2 and Unit 3 of Block 1 of this course).

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;Fig.7: Augustus De Morgan (1806–1871)&lt;/img&gt;
&lt;page_number&gt;78&lt;/page_number&gt;

---


## Page 11

Sets, Relations and Functions

Now try these exercises.

E15) Find the dual of
i) A∩(B∩C) = (A∩B)∩C, and ii) (A∪B)∩(A∪C).

E16) Draw a Venn diagram to represent A∪(B∩C).

E17) Check whether (A∪B)∩C = A∪(B∩C) or not using a Venn diagram.

Let us now focus on subsets of a particular kind of product of sets.

# 1.4 RELATIONS

Sometimes we need to establish relations between two or more sets. For example, a software development company has a set of specialists in different technology domains, or a company gets some projects to develop. Here the company needs to establish a relation between professionals and the project in which they will participate. To solve this type of problem the following concepts are required.

## 1.4.1 Cartesian Product

Very often we deal with several sets at a time, and we need to study their combined action. For instance, combinations of a set of teachers and a set of students. In such a situation we can take a product of these sets to handle them simultaneously. To understand this product let us first consider the following definitions.

**Definition:** An **ordered pair**, usually denoted by (x,y), is a pair of elements x and y of some sets. This is ordered in the sense that (x,y)≠(y,x) whenever x≠y, that is, the order of placing of the element in the pair matters.
Any two ordered pairs (x,y) and (a,b) are equal if f x = a and y = b.
For example if, A= {a,b,c}and B={x,y,z}, then
A×B= {a,b,c}×{x,y,z}= {(a,x),(a,y),(a,z),(b,x),(b,y),(b,z),(c,x),(c,y),(c,z)}, and
B ×A= {x,y,z}× {a,b,c}= {(x,a),(x,b),(x,c),(y,a),(y,b),(y,c),(z,a),(z,b),(z,c)}.

Now let us think about how B×A can be represented geometrically? For instance what is the geometric view of{2}×R? This is the line x=2 given in Fig.8(a).

Now, after seeing geometric representation of{2}×R, can you tell what {1,3}×{2,3} = {(1,2),(3,2),(1,3),(3,3) }looks like? You will get four points in the first quadrant, as shown in Fig.8(b).

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;
Fig. 8(a): {2} × R,i.e., x= 2
&lt;/img&gt;
&lt;img&gt;
Fig. 8 (b): {1,3}×{2,3}
&lt;/img&gt;

Now multiplication the Cartesian of numbers is commutative. Is the Cartesian product of sets also commutative? For instance, is {1}×{2}={2}×{1}? No, because (1,2)≠(2,1).
So, A×B≠B×A usually.

We can extend the definition of A×B to define the Cartesian product of n sets A₁,A₂,...,Aₙ as follows.
A₁×A₂×A₃×...×Aₙ={(x₁,x₂,x₃,...,xₙ) :x₁∈A₁∧x₂∈A₂∧x₃∈A₃∧...,∧xₙ∈Aₙ}. &lt;page_number&gt;79&lt;/page_number&gt;

---


## Page 12

*Error processing this page: OCR extraction failed: modal streaming failed after 7.8s: modal API error: 408 - Missing request, possibly due to expiry or cancellation*


## Page 13

*Error processing this page: OCR extraction failed: modal streaming failed after 7.4s: modal API error: 408 - Missing request, possibly due to expiry or cancellation*


## Page 14

Basic Combinatorics

Now we shall study a particular kind of relation, which is very useful in mathematics, as well as in computer science, as you will soon see.

## 1.5 FUNCTIONS

A function is a special kind of relation. If we take the example of the set A of students of IGNOU, and the set B of their enrolment numbers. Now consider R= {(a,b)∈ A×B | b is enrollment number of a }, this is a relation between A and B. It is a ‘special’ relation, ‘special’ because to each a ∈ A ∃!b such that aRb. We call such a relation a function from A to B.

Let us define this term formally.

**Definition:** A **function** from a non-empty set A to a non-empty set B is a subset R of A×B such that for each a ∈ A ∃ a unique b∈ B such that (a,b)∈ R. So, this relation satisfies the following two conditions:

(i) For each a∈ A, there is some b∈ B such that (a,b)∈ R
(ii) If (a,b)∈ R and (a,b')∈ R then b=b'.

We usually present functions as a rule associating elements of one set with another. So, let us present the definition again, with this view.

**Definition:** Let A and B be non-empty sets. A **function** (or a **mapping**) f from A to B is a rule that assigns to each element x in A exactly one element y in B. We write this as f: A → B, read it as ‘f is a function from A to B’.

Note that

(i) To each a∈ A, f assigns an element of B; and
(ii) To each a∈ A, f assigns only **one element** of B.

So, for example, suppose A = {1,2,3}, B= {1,4,9,11} and f assigns to each member in A its square values. Then f is a function from A to B. But if A={1,2,3,4}, B={1,4,9,10} and f is the same rule, then f is not a function from A to B since no member of B is assigned to the element 4 in A.

Note that the former example, 11∈ B, but there is no element in A which is assigned to 11. This does not matter. It is not necessary that every element of B be related to some element of A.

Functions are not restricted to sets of numbers only. For instance, let A be the set of mothers and B be the set of human beings. Then the rule that assigns to every mother her eldest child is a **function**. But the rule that assigns to each mother her children is **not a function** because it does not relate a unique element of B to each element of A. Now, given a function, we have certain sets and terms that are associated with it. Let us give them some names.

**Definitions:** Let f be a function from A to B. The set A is called the **domain** of the function f and B is called the **co-domain** off. The set {f(x)|x∈ A} is called the **range** off, and is also denoted by f(A).

Given an element x∈ A, the unique element of B to which the function f associates, it is denoted by f (x) and is called the **f-image** (or **image**) of x or the value of the function f for x. We also say that f **maps** x to f(x). The element x is referred to as the **pre-image** off (x).

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;82&lt;/page_number&gt;

---


## Page 15

Sets, Relations and Functions

For example, if A = { 1,2,3,4 }, B = { 1,8,27,64,125 }, and the rule f assigns to each member in A its cube, then f is a function from A to B. The domain of f is A, its codomain is B and its range is { 1,8,27,64 }.

Can you tell what will be the domain and codomain for rule f:f(x)= x / (1-x) ?

You can see that 1-x = 0, if x = 1, in this case f(x) will be undefined.
Domain off can be taken as R~{ 1 }and codomain can be **R**.

**Remark:** Each element of A has a **unique image**, and each element of B need not appear as the image of an element in A. Further, more than one element of A can have the same image in B.

Let us look at some examples of functions, and non-functions now.

i) If b is be a fixed element of B, then f:A→B:f(x)=b ∀x∈A is called a **constant function**.

Note that if b=0, then f is called the **zero map**, and is denoted by **0**.

ii) f:A→A:f(x)=x ∀x∈A is called the **identity function**, and is denoted by **I**.

iii) Consider A= { 1,2,3,4 }, B= { 1,4,5 } and the rule f which associates 1→1, 2→4,3→5,4→5. Then f is a function from A to B.

<mermaid>
graph LR
    subgraph A
        1
        2
        3
        4
    end
    subgraph B
        1
        4
        5
        6
        7
    end
    A -- f --> B
    1 --- 1
    2 --- 4
    3 --- 5
    4 --- 5
</mermaid>
Fig. 11: The rule f is a function

iv) The function f from **R** to **Z**, defined by the rule that f maps any real number x to the greatest integer less than or equal to x. is known as the **greatest integer** function or the **floor function**. We denote this function's action by f(x)=[x], where [x] is the greatest integer ≤ x.

For example, if x=0.6 then f(x)=[x]=0, if x=2.3 then f(x)=[x]=2, and if x= -5, then[x]'=-5 .

v) Function f: **R**→**R**: f(x)= | x | is known as the modulus (or absolute value) function, where | x | is the absolute value of x.

For example, if x=10 then f(x)=| x |=10 and if x=-10,then f(x)=| x |=10.

vi) Now take, A={a,b,c} and B={1,2,3,4,5}. Consider the rule f which associates a→1,a→3,b→2,c→3.This is not a function from A to B because, elements 1 and 3 ∈ B are assigned to the same element a∈ A.

<mermaid>
graph LR
    subgraph A
        a
        b
        c
    end
    subgraph B
        1
        2
        3
        4
        5
    end
    A -- f --> B
    a --- 1
    a --- 3
    b --- 2
    c --- 3
</mermaid>
Fig. 9: The rule f is not a function

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;83&lt;/page_number&gt;

---


## Page 16

*Error processing this page: OCR extraction failed: modal streaming failed after 6.6s: modal API error: 408 - Missing request, possibly due to expiry or cancellation*


## Page 17

*Error processing this page: OCR extraction failed: modal streaming failed after 6.4s: modal API error: 408 - Missing request, possibly due to expiry or cancellation*


## Page 18

Basic Combinatorics

Now we can see how different operations like addition, subtraction, multiplication and division can be applied on functions.

## 1.5.2 Operations on Functions

If given whose domains ranges are subsets of the **real numbers**, we define the function f+g by (f + g)(x) to be the function whose value at x is the sum of f(x) and g(x). Symbolically,

(f+g)(x)=f(x)+g(x). This is called point wise addition of f and g.

The domain of f+g is the **intersection** of the domains of f and g since to compute (f+g) (x) it is necessary and sufficient to compute both f(x) and g(x).

Other operations on functions are defined similarly:

*   (fg)(x)=f(x)g(x)(point wise multiplication)
*   fp(x)=(f(x))p for any real exponent p with the domain offp consisting of those points for which the p-th power of f(x) makes sense.
*   (f/g)(x)=f(x)/g(x), for g(x)≠0 (point wise division)

For example, if f(x) = 3 sin (x) and g(x) = x², then

(f+g)(x)= 3 sin(x) + x²
(fg)(x)=3sin(x)*x²
(f-g)(x)=3sin(x) -x²
(f/g)(x)=3 sin(x)/x²

The domains of both f and g are all **real numbers**, but the domain of f/g is { x |x≠0}.

Now let us consider two functions f and g from A= {1,2} to, B= {1,2,3,4}, where f={(1,1),(2,4)}. Let g be defined by the rule g(x)=x² where the domain of g is the set {1,2}. Here both have the same domain. Since f and g assign the same image to each element in the domain, they have the same effect throughout. This is why we treat them as the same, or equal.

**Definition:** If f and g are two functions defined on the same domain A and if f(a)=g(a) for every a∈ A, then the functions f and g are **equal**, i.e., f = g.

For example f(x) = x²+5, where x is a real number, and g(x) = x²+5, where x is a complex number. Then the function f is not equal to the function since they have different domains although f(x)= x²+5= g(x ∀x∈ R). By this example we can conclude that even if f(a)=g(a), f and g may not be the same.

So far, the operations you have seen are the same as those for member systems. However, there is yet another operation on functions which we now define.

**Definition:** Let f and g be the operation of combining two functions by applying them one after the other. That is, the composition off(x) and g(x), denoted by, fog.

For example, consider f:R→R:f(x)=(x³+2x)³. We can write it as the composition of g and h, where the value off(x) can be obtained by first calculating x³ +2x and then taking its third power. We can write g for first or inside function g(x) = x³ + 2x. We write h for the second function: h(x) = x³. The use of the variable x is irrelevant, we could as well write h(y)=y³ for y∈ R. We can see that go h(x)=g(x³ +2x) =(x³ +2x)³=f(x).

In general (fog) ≠ (gof).

For example, if, f(x) = x² and g(x) = x+1, then (fg)(x) = (x + 1)² and (gf)(x) =x²+1.

Here we can see that fg≠gf.

Let us see another example, where f(x)= x², g(x)= x+1, h(x) =x³

&lt;watermark&gt;IGNOU&lt;/watermark&gt;
&lt;watermark&gt;THE PEOPLE UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;86&lt;/page_number&gt;

---


## Page 19

Sets, Relations and Functions

Then, f(g h) (x) = (x³ + 1)² and (f g) h (x) = (x³ + 1)². Here we can see f(g h) = (f g) h.

Now let us see how you can get **product** of two permutations f and g of the same set,

Let $f = \begin{pmatrix} a_1 & a_2...a_n \\ f(a_1) & f(a_2)...f(a_n) \end{pmatrix}$ and

$g = \begin{pmatrix} a_1 & a_2...a_n \\ g(a_1) & g(a_2)...g(a_n) \end{pmatrix}$ Then $f\circ g = \begin{pmatrix} a_1 & a_2...a_n \\ f[g(a_1)] & f[g(a_2)]...f[g(a_n)] \end{pmatrix}$ is itself a perfmutatio.

For example if, $f = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 1 \end{pmatrix}$, $g = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 3 \end{pmatrix}$ then

$fg = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 2 \end{pmatrix}$, $g = \begin{pmatrix} 1 & 2 & 3 \\ 3 & 2 & 1 \end{pmatrix}$ then

Note that fg≠g in f. Thus the multiplication of permutations is not commutative general.

However, the multiplication of permutations is associative. For example, if

$f = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 1 & 3 & 4 & 2 \end{pmatrix}$, $g = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 2 & 3 & 4 & 1 \end{pmatrix}$, $h = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 4 & 2 & 1 & 3 \end{pmatrix}$ be the permutations on A = {1,2,3,4}, then

$fg = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 2 & 4 & 1 & 3 \end{pmatrix}$, $gf = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 4 & 2 & 1 \end{pmatrix}$, $gh = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 4 & 2 & 1 \end{pmatrix}$

$f(gh) = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 2 & 3 & 4 & 1 \end{pmatrix}$, $(fg)\circ h = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 4 & 2 & 1 \end{pmatrix}$.

Here we can see the multiplication of permutation is commutative.

Now try these exercises.

E 29) Let f(x) = 1/x and g(x) = x³ + 2. Find the following functions, where x∈R.
i) (f+ g)(x)
ii) (f- g)(x)
iii) (fg)(x)
iv) (f/g)(x)

E30) Let f(x) = √(x+1) ∀x≥−1 and g (x) = x³∀x∈R. Define the following functions. Also give their domains.
i) (f+g)
ii) (f- g)
iii) (fg)
iv) (f/g)
v) (f g)

With this we have come to the end of this unit. Let us now summaries what we have covered in this unit.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;87&lt;/page_number&gt;

---


## Page 20

*Error processing this page: OCR extraction failed: modal streaming failed after 5.7s: modal API error: 408 - Missing request, possibly due to expiry or cancellation*


## Page 21

Sets, Relations and Functions

You can try them for the other situations. We are showing in Fig. 12 for the second situation.

E10) A∪(B∩C)={Math, Physics, Science}=A.

E11) i) A~B={1,2,3}
ii) B~A = {7,8,9}
iii) AΔB = {1,2,3,7,8,9}

E12) Only if A and B are φ.

E13) Write separate functions to find A~B, B~A and AΔB with passing sets A and B as argument, return the resultant set.

E14) A∩B can be equal to A∪B if either A⊆B or B⊆A.

E15) i) Dual of A∩(B∩C) = (A∩B)∩C is A∪(B∪C) = (A∪B)∪C.
ii) Dual of (A∪B)∩(A∪C) is (A∩B)∪(A∩C).

E16)
&lt;img&gt;A Venn diagram with three circles labeled A, B, and C. The intersection of A and B is shaded. The union of A and B is shown outside the circles.&lt;/img&gt;
AU(B∩C)

Fig. 13: The lined portion represents AU(B∩C)

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E17)
&lt;img&gt;A Venn diagram with three circles labeled A, B, and C. The intersection of A and B is shaded. The union of A and B is shown outside the circles.&lt;/img&gt;
(A∪B)∩C

Fig. 14(a)

&lt;img&gt;A Venn diagram with three circles labeled A, B, and C. The intersection of A and B is shaded. The union of A and B is shown outside the circles.&lt;/img&gt;
(A∪B∩C)

Fig. 14(b)

Shaded area in Fig. 14(a) and Fig. 14(b) are not same so(A∪B)∩C is not equal to AU(B∩C).

E18) i) X × X={(a,a), (a,b), (a,c), (b,b), (b,c), (c,c)}.
ii) X × Y={(a,1), (b,1), (c,1), (a,2), (b,2), (c,2), (a,3), (b,3), (c,3)}.
iii) X × φ=φ.

&lt;page_number&gt;89&lt;/page_number&gt;

---


## Page 22

Basic Combinatorics

E19) A×B=B×A iff A=B.

E20) The geometric diagram for
RX{2} will be the line parallel to
Y axis. See Fig.15.
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
Fig.15: y=2

E21) i) For a∈A, aRa is reflexive because everyone loves herself for himself.
ii) R is not symmetric because if a loves b then b need not love a, i.e., aRb does not always imply bRa. Thus R is not symmetric.
iii) R is not transitive, because if a loves b and b loves c then a need not love c;i.e., if aRb and bRc, aRc need not be. Thus, R is not transitive.
Hence, R is reflexive but is n either symmetric n or transitive.

E22) R is a function because each element of A is assigned to a unique element of B.

E23) Not every relation is a function. For example, this relation does not satisfy the property that,
a) Each element of A must have assigned one element in B.
b) If a∈A is assigned b∈B and a∈A is assigned b′∈B then b=b′.
That is why relations those who don’t satisfy above properties are not a function

E24) We can see that the code has no effect on the value of n≤0.In the While loop, the value of n is halved whenever it is even. If n becomes odd before reaching 1, the second part of the while loop is invoked, and n remains odd and increases forever.
This shows that f:N → N is the function defined by f(n)=
```
{
    0 if n = 0
    1, if n is a power of
    undefined otherwise
}
```

E25) The domain off is {1,2,3,4} and range off is {2,3,4,5}.

E26) Function f(x) = x² is one-to-one because for every value of x, x² will be a number that is different for different x. Hence, f(x)=x²isone-onemapping.

E27) One-to-one function will be used for providing identity card number, because each person must have unique identity numbers.

E28) Step 1: y = x³ - 3
Step 2: x = y³ - 3
Step 3: y = ∛(x + 3)
Step 4: f⁻¹(x) = ∛(x + 3)

E29) i) (f+g)(x) = 1/x + x³ + 2
ii) (f-g)(x) = 1/x - (x³ + 2)
iii) (f.g)(x) = (1/x) + (x³ + 2)
iv) (f/g)(x) = 1/(x(x³ + 2)) ∀ x∈R.

&lt;page_number&gt;90&lt;/page_number&gt;

---


## Page 23

Sets, Relations and Functions

E30) i) (f+g)(x)= √(x+1) + x³ ∀ x≥-1
ii) (f-g)(x)= √(x+1) - x³ ∀ x≥-1
iii) (f.g)(x)= √(x+1) x³ ∀ x≥-1
iv) (f/g)(x)= √(x+1) / x³ ∀ x≥-1, x≠0
v) (f g)(x)=f(x³)= √(x³+1) ∀ x≥-1.

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;91&lt;/page_number&gt;

---


## Page 24

&lt;img&gt;IGU logo&lt;/img&gt;
THE PEOPLE'S UNIVERSITY

---


## Page 25

# UNIT 2 AUTOMATA AND LANGUAGES

2.0 Introduction
2.1 Objectives
2.2 Regular Expansion
    2.2.1 Introduction to Defining of Languages
    2.2.2 Kleene Closure Definition
    2.2.3 Formal Definition of Regular Expressions
    2.2.4 Algebra of Regular Expressions
2.3 Regular Language
2.4 Finite Automata
    2.4.1 Finite Automata
    2.4.2 Another Method to Describe FA
    2.4.3 Finite Automata as Output Devices
2.5 Non Deterministic Finite Automata
2.6 Summary
2.7 Solution/Answers

## 2.0 INTRODUCTION

In the previous unit we have examined sets, relations and functions. In this unit we will introduce a special kind of a set i.e., a language which is a set of strings over an alphabet. First we describe what is a language and what are the operations we perform on languages. Certain set of strings or languages are represented in algebraic fashion, then these algebraic expressions of languages are called **regular expressions**. A language represented by a regular expression is called a regular language. Then we introduce a notion of finite automata, also called finite state machine or deterministic finite automata. that recognizes regular languages. Finally, we introduce another kind of a theoretical machine, called nondeterministic finite automata (NFA). In deterministic finite automata (DFA), there is a unique next state for transition on input in a given state. If we relax this condition of uniqueness of the next state in DFA, we get NFA. But any set accepted by NFA can be also accepted by DFA. However the concept of non-determinism plays an important role in both the theory of computation and design and analysis of algorithm, specially in defining complexity classes. In the next unit we will examine a more powerful machine and explain the terms computability and complexity classes.

## 2.1 OBJECTIVES

After studying this unit, you should be able to:

*   Define alphabet, substring;
*   Define a language and various operations on languages;
*   Define and use a regular expression;
*   Define a finite automata for computation of a language;
*   Design a finite automata for a known language;
*   Define the term nondeterministic finite automata
*   Design nondeterministic finite automata for a known language

&lt;watermark&gt;UNIVERSITY OF PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;93&lt;/page_number&gt;

---


## Page 26

Auto Mata and Languages

# 2.2 REGULAR EXPENSION

In this unit, first we shall discuss the definitions of alphabet, string, and language with some important properties.

## 2.2.1 Introduction to Defining of Languages

For a language, defining rules can be of two types. The rules can either tell us how to test a string of alphabet letters that we might be presented with, to see if it is a valid word, i.e., a word in the language or the rules can tell us how to construct all the words in the language by some clear procedures.

**Alphabet:** A finite set of symbols/characters. We generally denote an alphabet by Σ. If we start an alphabet having only one letter, say, the letter z, then Σ = {z}

**Letter:** Each symbol of an alphabet may also be called a letter of the alphabet or simply a letter.

**Language over an alphabet:** A set of words over an alphabet. Languages are denoted by letter L with or without a subscript.

**String/word over an alphabet:** Every member of any language is said to be a string or a world.

**Example 1:** Let L₁ be the language of all possible strings obtained by L₁ = {z, zz, zzz, zzzz……}

This can also be written as
L₁ = {zⁿ} for n = 1, 2, 3,……

A string of length zero is said to be **null string** and is represented by λ.

Above given language L₁ does not include the null string. We could have defined it so as to include λ. Thus, L = {zⁿ | n=0, 1, 2, 3…} contains the null string.

In this language, as in any other, we can define the operation of concatenation, in which two strings are written down side by side to form a new longer string. Suppose u = ab and v = baa, then uv is called concatenation of two strings u and v and is uv = abbaa and vu = baaab. The operation of concatenation is analogous to addition:

zⁿ concatenated with zᵐ is the word zⁿ⁺ᵐ.

**Example 2:** If the word zzz is called c and the word zz is called d, then the word formed by concatenating c and d is
cd = zzzzz

When two words in our language L₁ are concatenated they produce another word in the language L₁. However, this may not be true in all languages.

**Example 3:** If the language is L₂ = {z, zzz, zzzzz, zzzzzzz……}
= {z⁰d}
= {z²ⁿ⁺¹ for n = 0, 1, 2, 3……}

&lt;page_number&gt;94&lt;/page_number&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 27

Set Theory Computability & Complexity

then c = zzz and d = zzzzz are both words in L₂, but their concatenation cd = zzzzzzzz is not a word in L₂. The reason is simple that member of L₂ are of odd length while after concatenation it is of even length.

Note: The alphabet for L₂ is the same as the alphabet for L₁.

**Example 4:** A Language L₃ may denote the language having strings of even lengths include of length 0. In other words, L₃ = { λ zz, zzzz, …… }

Another interesting language over the alphabet Σ = {z} may be

**Example 5:** L₄ = { zᵖ : p is a prime natural number }.
There are infinitely many possible languages even for a single letter alphabet Σ = {z},

In the above description of concatenation we find very commonly, that for a single letter alphabet when we concatenate c with d, we get the same word as when we concatenate d with c, that is cd = dc **But this relationship does not hold for all languages.** For example, in the English language when we concatenate “Ram” and “goes” we get “Ram goes”. This is, indeed, a word but distinct from “goes Ram”.

Now, let us define the reverse of a language L. If c is a word in L, then reverse (c) is the same string of letters spelled backward.
The reverse (L) = {reverse (w), w ∈ L}

**Example 6:** Reverse (zzz) = zzz
Reverse (173) = 371

Let us define a new language called PALINDROME over the alphabet Σ = {a,b}.

PALINDROME = { λ , and all strings w such that reverse (w) = w }
= { λ , a, b, aa, bb, aaa, aba, bab, bbb, aaaa, abba, … }

Concatenating two words in PALINDROME may or may not give a word in palindrome, e.g., if u = abba and v = abbcba, then uv = abbaabbcba which is not palindrome.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

### 2.2.2 Kleene Closure Definition

Suppose an alphabet Σ , and define a language in which any string of letters from Σ is a word, even the null string. We shall call this language the closure of the alphabet. We denote it by writing * after the name of the alphabet as a superscript, which is written as Σ *. This notation is sometimes also known as **Kleene Star**.

For a given alphabet Σ , the language Σ * (sigma*) consists of all possible strings, including the null string.

For example, If Σ = {z}, then, Σ * = L₁ = { λ, z, zz, zzz …… }

**Example 7:** If Σ= {0, 1 }, then, Σ * = { λ, 0, 1, 00, 01, 10, 11, 000, 001 …… }
So, we can say that Kleene Star is an operation that makes an infinite language of strings of letters out of an alphabet, if the alphabet, Σ ≠ φ. However, by the definition alphabet Σ may also be φ. In that case, Σ * is finite. By “infinite language, we mean a language with infinitely many words.

&lt;page_number&gt;95&lt;/page_number&gt;

---


## Page 28

Auto Mata and Languages

Now, we can generalise the use of the star operator to languages, i.e., to a set of words, not just sets of alphabet letters.

**Definition:** If s is a set of words, then by s* we mean the set of all finite strings formed by concatenating words from s, where any word may be used as often.

**Example 8:** If s = {cc, d}, then

s* = {λ or any word composed of factors of cc and d}
= {λ or all strings of c's and d's in which c's occur in even clumps}.
The string ccddcc is not in s* since it has a clump of c's of length 3.
{x : x λ = or x = (cc)i₁ dj₁ (cc)i₂ dj₂ ..... (cc)im (d)jm } where i₁, j₁,..... im, jm ≥ 0

**Positive Closure:** If we want to modify the concept of closure to refer to only the concatenation leading to non-null strings from a set s, we use the notation + instead of *. This plus operation is called positive closure.

**Theorem 1:** For any set s of strings prove that s* = (s*)* = s**

**Proof:** We know that every word in s** is made up of factors from s*. Also, every factor from s* is made up of factors from s. Therefore, we can say that every word in s** is made up of factors from s.

First, we show s** ⊆ s*.
(i)
Let x ∈ s** .... Then x = x₁....xₙ for some x₁ ∈ s* which implies s** ⊆ s*

Next, we show s* ⊆ s**.
(ii)
s* ⊆ s**

By above inclusions (i) and (ii), we prove that
s* = s**

Now, try some exercises.

Ex.1) If u = ababb and v = baa then find
(i) uv (ii) vu (iii) uv (iv) vu (v) uuv.

Ex.2) Write the Kleene closure of the following
(i) {aa, b}
(ii) {a, ba}

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

## 2.2.3 Formal Definition of Regular Expressions

Certain sets of strings or languages can be represented in algebraic fashion, then these algebraic expressions of languages are called **regular expressions**. Regular expressions are in **Bold** face. The symbols that appear in regular use of the letters of the alphabet Σ are the symbol for the null string λ, parenthesis, the star operator, and the plus sign.

The set of regular expressions is defined by the following rules:

1. Every letter of Σ can be made into a regular expression λ itself is a regular expression.
2. Φ is a regular expression
3. 3 If l and m are regular expressions, then so are

&lt;page_number&gt;96&lt;/page_number&gt;

---


## Page 29

Set Theory Computability
& Complexity

(i) (I)
(ii) lm
(iii) l+m
(iv) l*
(v) l+ = ll*

4. Nothing else is regular expression.

For example, now we would build expression from the symbols 0,1 using the operations of union, concatenation, and Kleene closure.
(i) **01** means a zero followed by a one (concatenation)
(ii) **0+1** means either a zero or a one (union)
(iii) **0*** means λ+0+00+000+…… (Kleen closure).

With parentheses, we can build larger expressions. And, we can associate meanings with our expressions. Here's how

<table>
<thead>
<tr>
<th>Expression</th>
<th>Set represented</th>
</tr>
</thead>
<tbody>
<tr>
<td>(0+1)*</td>
<td>all strings over {0,1}</td>
</tr>
<tr>
<td>0*10*10*</td>
<td>strings containing exactly two ones</td>
</tr>
<tr>
<td>(0+1)*11</td>
<td>strings which end with two ones.</td>
</tr>
</tbody>
</table>

The language denoted/represented by the regular expression R is L(R).

**Example 9:** The language L defined by the regular expression **ab***a** is the set of all strings of a's and b's that begin and end with a's, and that have nothing but b's inside.
L = {λ aa, aba, abba, abbbba, }

**Example 10:** The language associated with the regular expression **a***b*** contains all the strings of a's and b's in which all the a's (if any) come before all the b's (if any).
L = {λ, a, b, aa, ab, bb, aaa, aab, abb, bbb, aaa,...}

Note that ba and aba are not in this language. Notice also that there need not be the same number of a's and b's.

**Example 11:** Let us consider the language L defined by the regular expression (**a+b)**\* **a(a+b)**\*. The strings of the language L are obtained by concatenating a string from the language corresponding to (**a+b)**\* followed by a followed by a string from the language associated with (**a+b)**\*. We can also say that the language is a set of all words over the alphabet Σ = {a,b} that have an a in them somewhere.

To make the association/correspondence/relation between the regular expressions and their associated languages more explicit, we need to define the operation of multiplication of set of words.

**Definition:** If S and T are sets of strings of letters (they may be finite or infinite sets), we define the product set of strings of letters to be. ST = {all combinations of a string from S concatenated with a string from T in that order}.

**Example 12:** If S = {a, aa, aaa}, T = {bb, bbb} Then, ST = {abb, abbb, aabb, aabbb, aaabb, aaabbb}.

**Example 13:** If S = {a bb bab}, T = {λ bbbb}
Then, ST = {a, bb, bab, abbbb, bbbbbbb ,babbbbbbb}

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;97&lt;/page_number&gt;

---


## Page 30

Auto Mata and Languages

Ex.3) Find a regular expression to describe each of the following languages:
(a) {a,b,c}
(b) {λ,a,abb,abbbb,...}

Ex.4) Find a regular expression over the alphabet {0,1,} to describe the set of all binary numerals without leading zeroes (except 0 itself). So the language is the set
{0,1,10,11,100,101,110,111,...}.

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

## 2.2.4 Algebra of Regular Expressions

There are many general equalities for regular expressions. We will list a few simple equalities together with some that are not so simple. All the properties can be verified by using properties of languages and sets. We will assure that R,S and T denote the arbitrary regular expressions.

### Properties of Regular Expressions

1. (R+S)+T = R+(S+T)
2. R+R = R
3. R+ φ = φ +R = R.
4. R+S = S+R
5. R φ = φ R = φ
6. R ∧ = ∧ R = R
7. (RS)T = R(ST)
8. R(S+T) = RS+RT
9. (S+T)R = SR+TR
10. φ * = ∧ * = ∧
11. R * R * = R * = (R *) *
12. RR * = R *R = R * = ∧ +RR *
13. (R+S) * = (R *S *) * = (R *+S *) * = R *S * = (R *S) *R * = R *(SR *) *
14. (RS) * = (R *S *) * = (R *+S *) *

**Theorem 2: Prove that R+R = R**

**Proof :** We know the following equalities:

L(R+R) = L(R)UL(R) = L(R)

So **R+R = R**

&lt;page_number&gt;98&lt;/page_number&gt;

---


## Page 31

Set Theory Computability
& Complexity

**Theorem 3: Prove the distributive property**

R(S+T) = RS+RT

**Proof:** The following set of equalities will prove the property:

L(R(S+T)) = L(R)L(S+T)
= L(R)(L(S)UL(T))
= (L(R)L(S))U(L(R)L(T))
= L(RS+RT)

Similarly, by using the equalities we can prove the rest. The proofs of the rest of the equalities are left as exercises.

**Example 15:** Show that R+RS*S = a*bS*, where R = b+aa*b and S is any regular expression.

R+RS*S = R ∧+RS*S (property 6)
= R(∧+S*S) (property 8)
= R(∧+SS*) (property 12)
= RS* (property 12)
= (b+aa*b)S* (definition of R)
= (∧+aa*) bS* (properties 6 and 8)
= a*bS*. (Property 12)

Try an exercise now.

Ex.5) Establish the following equality of regular expressions:
b*(abb*+aabb*+aaabb*)* = (b+ab+aab+aaab)*

As we already know the concept of language and regular expressions, we have an important type of language derived from the regular expression, called **regular language.**

**2.3 REGULAR LANGUAGE**

Language represented by a regular expression is called a regular language. In other words, we can say that a regular language is a language that can be represented by a regular expression.

**Definition:** For a given alphabet , the following rules define the regular language associated with a regular expression.

**Rule 1:** φ, {∧} and {a} are regular languages denoted respectively by regular expressions φ and ∧.

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;99&lt;/page_number&gt;

---


## Page 32

Auto Mata and Languages

**Rule 2:** For each a in , the set {a} is a regular language denoted by the regular expression **a**.

**Rule 3:** If **l** is a regular expression associated with the language L and **m** is a regular expression associated with the language M, then:

(i) The language = {xy : x ∈ L and y ∈ M} is a regular expression associated with the regular expression **lm**

(ii) The regular expression **l+m** is associated with the language formed by the union of the sets L and M.
language (**l+m**) = LUM

(iii) The language associated with the regular expression (**l**)∗ is L∗, the Kleen Closure of the set L as a set of words:
language (**l**)∗ = L∗.

Now, we shall derive an important relation that, all finite languages are regular.

**Theorem 4:** If L is a finite language, then L can be defined by a regular expression.

In other words, all finite languages are regular.

**Proof:** A language is finite if it contains only finitely many words.

To make one regular expression that defines the language L, turn all the words in L into bold face type and insert plus signs between them. For example, the regular expression that defines the language L = {baa, abbba, bababa} is **baa + abbba + bababa**

**Example16:** If L = {aa, ab, ba, bb}, then the corresponding regular expression is aa + ab +ba + bb.

Another regular expression that defines this language is (a+b) (a+b).

So, a particular regular language can be represented by more than one regular expressions. Also, by definition, each regular language must have at least one regular expression corresponding to it.

Try some exercises.

Ex.6) Find a language to describe each of the following regular expressions:
(a) **a+b**
(b) **a+b\***
(c) **a\*bc\*+ac**

Ex.7) Find a regular expression for each of the following languages over the alphabet {a,b}:
(a) strings with even length.
(b) strings containing the sub string aba.

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;100&lt;/page_number&gt;

---


## Page 33

Set Theory Computability
& Complexity

# 2.4 FINITE AUTOMATA

Finite automata are important in science, mathematics, and engineering. Engineers like them because they are superb models for circuits (and, since the advent of VLSI systems sometimes finite automata represent circuits.) computer scientists adore them because they adapt very likely to algorithm design. For example, the lexical analysis portion of compiling and translation. Mathematicians are introduced by them too due to the fact that there are several nifty mathematical characterizations of the sets they accept.

Can a machine recognise a language? The answer is yes for some machine and some an elementary class of machines called finite automata. Regular languages can be represented by certain kinds of algebraic expressions by Finite automaton and by certain grammars. For example, suppose we need to compute with numbers that are represented in scientific notation. Can we write an algorithm to recognise strings of symbols represented in this way? To do this, we need to discuss some basic computing machines called finite automaton.

An automata will be a finite automata if it accepts all the words of any regular language where language means a set of strings. In other words,

## 2.4.1 Finite Automata

A system where energy and information are transformed and used for performing some functions without direct involvement of man is called automaton. Examples are automatic machine tools, automatic photo printing tools, etc.

A finite automata is similar to a finite state machine. A finite automata consists of five parts:

(1) a finite set of states;
(2) a finite set of alphabets;
(3) an initial state;
(4) a subset of set of states (whose elements are called “yes” state or; accepting state;) and
(5) a next-state function or a transition state function.

A finite automata over a finite alphabet A can be thought of as a finite directed graph with the property that each node emits one labelled edge for each distinct element of A. The nodes are called states. There is one special state called **the start** (or **initial**) state, and there is a subset of states called **final states** (which could be possibly empty)

For example, the labelled graph in Figure 1 given below represents a DFA over the alphabet A = {a,b} with start state 1 and final state 4.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;101&lt;/page_number&gt;

---


## Page 34

Auto Mata and Languages

<mermaid>
graph LR
    A((1)) -->|a| B((2))
    B -->|b| B
    B -->|a| C((3))
    C -->|a| C
    C -->|b| D((4))
    D -->|a.| D
    D -- Final --> D
    A -- Start --> A
</mermaid>

Fig. 1: Finite Automata

We always indicate the start state by writing the word start with an arrow painting to it. Final states are indicated by double circle.

The single arrow out of state 4 labelled with a,b is short hand for two arrows from state 4, going to the same place, one labelled a and one labelled b. It is easy to check that this digraph represents a DFA over {a,b} because there is a start state, and each state emits exactly two arrows, one labelled with a and one labelled with b.

So, we can say that a finite automaton is a collection of three tuples:

1. A finite set of states, one of which is designated as the initial state, called the start state, and some (may be none) of which we designated as final states.
2. An alphabet Σ of possible input letters from which are formed strings that are to be read one letter at a time.
3. A finite set of transitions that tell for each state and for each letter of the input alphabet which state to go to next.

For example the input alphabet has only two letters a and b. Let us also assume that there are only three states, x, y and z. Let the following be the rules of transition:

1. from state x and input a go to state y;
2. from state x and input b go to state z;
3. from state y and input b go to state x;
4. from state y and input b go to state z; and
5. from state z and any input stay at state z.

Let us also designate state x as the starting state and state z as the only final state.

Let us examine what happens to various input strings when presented to this FA. Let us start with the string aaa. We begin, as always, in state x. The first letter of the string is an a, and it tells us to go state y (by rule 1). The next input (instruction) is also an a, and this tells us (by rule 3) to go back to state x. The third input is another a, and (by Rule 1) again we go to the state y. There are no more input letters in the input string, so our trip has ended. We did not finish in the final state (state z), so we have an unsuccessful termination of our run.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;102&lt;/page_number&gt;

---


## Page 35

Set Theory Computability
& Complexity

The string aaa is not in the language of all strings that leave this FA in state z. The set of all strings that do leave as in a final state is called the language defined by the finite automaton. The input string aaa is not in the language defined by this FA. We may say that the string aaa is not accepted by this FA because it does not lead to a final state. We may also say “aaa is rejected by this FA.” The set of all strings accepted is the language associated with the FA. So, we say that L is the language accepted by this FA. FA is also called a language recogniser.

Let us examine a different input string for this same FA. Let the input be abba. As always, we start in state x. Rule 1 tells us that the first input letter, a, takes us to state y. Once we are in state y we read the second input letter, which is a b. Rules 4 now tells us to move to state z. The third input letter is a b, and since we are in state z, Rule 5 tells us to stay there. The fourth input letter is an a, and again Rule 5 says state z. Therefore, after we have followed the instruction of each input letter we end up in state z. State z is designated as a final state. So, the input string abba has taken us successfully to the final state. The string abba is therefore a word in the language associated with this FA. The word abba is accepted by this FA.

It is not difficult for us to predict which strings will be accepted by this FA. If an input string is made up of only the letter a repeated some number of times, then the action of the FA will be jump back and forth between state x and state y. No such word can ever be accepted.

To get into state z, it is necessary for the string to have the letter b in it as soon as a b is encountered in the input string, the FA jumps immediately to state z no matter what state it was before. Once in state z, it is impossible to leave. When the input strings run out, the FA will still be in state z, leading to acceptance of the string.

So, the FA above will accept all the strings that have the letter b in them and strings not of this form are never accepted. Therefore, the language associated with this FA is the one defined by the regular expression (a+b)* b(a+b)*.

The list of transition rules can grow very long. It is much simpler to summarise them in a table format. Each row of the table is the name of one of the states in FA, and each column of this table is a letter of the input alphabet. The entries inside the table are the new states that the FA moves into the transition states. The transition table for the FA we have described is:

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

Table 1: Transition Table

<table>
<thead>
<tr>
<th>State</th>
<th colspan="2">Input</th>
</tr>
<tr>
<th></th>
<th>a</th>
<th>b</th>
</tr>
</thead>
<tbody>
<tr>
<td>Start x</td>
<td>y</td>
<td>z</td>
</tr>
<tr>
<td>y</td>
<td>x</td>
<td>z</td>
</tr>
<tr>
<td>Final z</td>
<td>z</td>
<td>z</td>
</tr>
</tbody>
</table>

The machine we have already defined by the transition list and the transition table can be depicted by the state graph in Figure 2.

&lt;page_number&gt;103&lt;/page_number&gt;

---


## Page 36

Auto Mata and Languages

&lt;img&gt;State Transition graph with states x, y, z and arrows labeled a, b.&lt;/img&gt;

**Fig. 2: State Transition graph**

**Note:** A single state can be start as well as final state both. There will be only one start state and none or more than one final states in Finite Automaton.

## 2.4.2 Another Method to Describe FA

There is a traditional method to describe finite automata which is extremely intuitive. It is a picture called a graph. The states of the finite automaton appear as vertices of the graph while the transitions from state to state under inputs are the graph edges. The state graph for the same machine also appears in Figure 3 given below:

&lt;img&gt;Finite automata diagram with states 1, 2, 3 and arrows labeled 1, 0, 0,1.&lt;/img&gt;

**Fig. 3: Finite automata**

The finite automata shown in Figure 3 can also be represented in Tabular form as below:

**Table 2: Tabular form of Figure 3**

<table>
<thead>
<tr>
<th></th>
<th>State</th>
<th colspan="2">Input</th>
<th>Accept?</th>
</tr>
<tr>
<th></th>
<th></th>
<th>0</th>
<th>1</th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>Start</td>
<td>1</td>
<td>1</td>
<td>2</td>
<td>No</td>
</tr>
<tr>
<td>Final</td>
<td>2</td>
<td>2</td>
<td>3</td>
<td>Yes</td>
</tr>
<tr>
<td></td>
<td>3</td>
<td>3</td>
<td>3</td>
<td>No</td>
</tr>
</tbody>
</table>

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

Before continuing, let's examine the computation of a finite automaton. Our first example begins in state one and reads the input symbols in turn changing states as necessary. Thus, a computation can be characterized by a sequence of states. (Recall that Turing machine configurations needed the state plus the tape content. Since a finite automaton never writes, we always know what is on the tape and need only look at a state as a configuration.) Here is the sequence for the input 0001001.

<table>
<thead>
<tr>
<th>Input Read:</th>
<th>0</th>
<th>0</th>
<th>0</th>
<th>1</th>
<th>0</th>
<th>0</th>
<th>1</th>
</tr>
</thead>
<tbody>
<tr>
<td>State:</td>
<td>1 → 1 → 1 → 1 → 2 → 2 → 2 → 3</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

**Example 17 (An elevator controller):** Let's imagine an elevator that serves two floors. Inputs are calls to a floor either from inside the elevator or from the floor itself. This makes three distinct inputs possible, namely:

&lt;page_number&gt;104&lt;/page_number&gt;

---


## Page 37

Set Theory Computability
& Complexity

0 - no calls
1 - call to floor one
2.- call to floor two
The elevator itself can be going up, going down, or halted at a floor. If it is on a floor, it could be waiting for a call or about to go to the other floor. This provides us with the six states shown in Figure 4 along with the state graph for the elevator controller.

W1 Waiting on first floor
U1 About to go up
UP Going up
DN Going down
W2 Waiting-second floor
D2 About to go down

<mermaid>
graph LR
    W(W) -->|0,2| W(W)
    W(W) -->|1| U(U)
    W(W) -->|0,2| D(D)
    D(D) -->|2| D(D)
    D(D) -->|0,1| W(W)
    D(D) -->|2| D(D)
    U(U) -->|2| W(W)
    U(U) -->|0,2| D(D)
    D(D) -->|1| D(D)
    D(D) -->|0,1| W(W)
</mermaid>

Fig. 4: Elevator Control

A transition state table for the elevator is given in Table 3:

Table 3: Elevator Control
<table>
<thead>
<tr>
<th>State</th>
<th colspan="3">Input</th>
</tr>
<tr>
<th></th>
<th>None</th>
<th>call to 1</th>
<th>call to 2</th>
</tr>
</thead>
<tbody>
<tr>
<td>W1 (wait on 1)</td>
<td>W1</td>
<td>W1</td>
<td>UP</td>
</tr>
<tr>
<td>U1 (start up)</td>
<td>UP</td>
<td>U1</td>
<td>UP</td>
</tr>
<tr>
<td>UP</td>
<td>W2</td>
<td>D2</td>
<td>W2</td>
</tr>
<tr>
<td>DN</td>
<td>W1</td>
<td>W1</td>
<td>U1</td>
</tr>
<tr>
<td>W2 (wait on 2)</td>
<td>W2</td>
<td>DN</td>
<td>W2</td>
</tr>
<tr>
<td>D2 (start down)</td>
<td>DN</td>
<td>DN</td>
<td>D2</td>
</tr>
</tbody>
</table>

Accepting and rejecting states are not included in the elevator design because acceptance is not an issue. If we were to design a more sophisticated elevator, it might have states that indicated:

Finite automata

a) power failure
b) overloading, or
c) breakdown

In this case, acceptance and rejection might make sense.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;105&lt;/page_number&gt;

---


## Page 38

Auto Mata and Languages

Let us make a few small notes about the design. If the elevator is about to move (i.e., in state U1 or D2) and it is called to the floor it is presently on it will stay. (This may be good Try it next time you are in an elevator.) And, if it is moving (up or down) and gets called back the other way, it remembers the call by going to the U1 or D2 state upon arrival on the next floor. Of course, the elevator does not do things like open and close doors (these could be states too) since that would have added complexity to the design. Speaking of complexity, imagine having 100 floors.

That is our levity for this section. Now that we know what a finite automaton is, we must (as usual) define it precisely.

**Definition :** A finite automata M is a quintuple M = (Q, Σ, δ, qo, F) where :
* Q is a finite set (of states)
* Σ is a finite alphabet (of input symbols)
* δ : Q × Σ → Q (next state function)
* qo ∈ Q (the starting state)
* F ⊆ Q (the accepting states)

We also need some additional notation. The next state function is called the transition function and the accepting states are often called final states. The entire machine is usually defined by presenting a transition state table or a transition diagram. In this way, the states, alphabet, transition function, and final states are constructively defined. The starting state is usually the lowest numbered state. Our first example of a finite automaton is:

M = ({q1, q2, q3}, {0,1}, , q1, {q2})

Let us look again at a computation by our first finite automaton. For the input 010, our machine begins in q1, reads a 0 and goes to δ(q2,0) = q2 after reading the final 0. All that can be put together as:

δ(δ(δ(q1,0),1)0) = q2

We call this transition on strings δ * and define it as follows:

**Definition :** Let M = (Q,Σ,δ,qo,F). For any input string x, input symbol a, and state qi, the transition function on strings δ * takes the values:
* δ *(qi,(*e)) = w_i
* δ *(qi,a) = δ (qi,,a) a
* δ*(qi,xa)= δ(δ *(qi,x),a) ∀ a ∈ Σ , x ∈ Σ *

That certainly was terse. But δ* is really just what one expects it to be. It merely applies the transition function to the symbols in the string.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;106&lt;/page_number&gt;

---


## Page 39

Set Theory Computability & Complexity

<mermaid>
graph TD
    A(( )) --> B(q₀)
    B -- "a" --> C(q₃)
    C -- "a,b" --> C
    D(( )) --> E(q₁)
    E -- "b" --> F(q₂)
    F -- "b"--> F
    B -- "b" -> E
</mermaid>

Fig. 5: Finite automata

This machine has a set of states = {q₀, q₁, q₂, q₃} and operates over the input alphabet {a,b}. In the above Figure 5 q₀ is the starting state and its set of final or accepting states, F = {q₂} an accepting state can also be shown by two concentric circles as shown in the Figure 5.

The transition function is fully described twice once in Figure 6 as a state graph and once in Table 4 as a state table.

Table 4: State Table

<table>
<thead>
<tr>
<th>State</th>
<th colspan="2">Input</th>
<th>Accept?</th>
</tr>
<tr>
<th></th>
<th>A</th>
<th>b</th>
<th></th></tr>
</thead>
<tbody>
<tr><td>0</td><td>3</td><td></td><td>No</td></tr>
<tr><td></td></tr>
<td>1</td><td>|</td><td><strong>3</strong></td><td><em>2</em></td><td>Yes</td></tr><tr>
<td></td><td></td><td>|<strong>2</strong></td>
<td></td></tr>
<tr><td>2</td><td><strong>2</td></td><strong>|</strong><td><strong><em>2</em></strong></td><td></td></tr><tr>
<td></td><td><em>3</td></td>
<td><strong>3</td><td><strong>3<em></em></strong></strong></td>
<td>No</td></tr>
</tbody>
</table>

If the machine receives the input bbaa, it goes through the sequence of states:
q₀,q₁,q₂,q₂,q₂

While when it gets an input such as abab, it goes through state transition:
q₀,q₃,q₃,q³,q₃

Now we shall become a bit more abstract. When a finite automaton receives an input string such as:
x = x₁x₂...xₙ

where the xᵢ are symbols from its input alphabet, it progresses through the sequence:
qk₁, qk₂, ... qkn+1

where the states in the sequence are defined as:
qk₁ = q₀
qk₂ = δ(qk₁, x₁) = δ(q₀, x₀)
qk₃ = δ(qk₂, x₂) = δ*(q₀, x₁ x₂)
qkn+1 = δ(qkn, xₙ) = δ*( q₀, x₁x₂ ... xₙ)

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;107&lt;/page_number&gt;

---


## Page 40

Auto Mata and Languages

Getting back to a more intuitive reality, the following table provides an assignment of values to the symbols used above for an input of bbaba to the finite automaton of figure 3.

<table>
<thead>
<tr>
<td>i</td>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
<td>5</td>
<td>6</td>
</tr>
</thead>
<tbody>
<tr>
<td>x<sub>i</sub></td>
<td>b</td>
<td>b</td>
<td>a</td>
<td>b</td>
<td>a</td>
<td></td>
</tr>
<tr>
<td>q<sub>k<sub>1</sub></sub></td>
<td>q<sub>0</sub></td>
<td>q<sub>1</sub></td>
<td>q<sub>2</sub></td>
<td>q<sub>2</sub></td>
<td>q<sub>2</sub></td>
<td>q<sub>2</sub></td>
</tr>
</tbody>
</table>

**Definition:** The set (of strings) **accepted** by the finite automaton M = (Q, Σ, δ, q<sub>0</sub>, F) is T(M) = {x / δ*(q<sub>0</sub>, x) ∈ F}

This set of accepted strings (L(M) to mean for language accepted by M) is merely all of the strings for which M ended up in a final or accepting state after processing the string. For our first example (Figure 1) this was all strings of 0's and 1's that contain exactly one 1. Our last example (Figure 3) accepted the set of strings over the alphabet {a,b} which began with exactly two b's.

## 2.4.3 Finite Automata as Output Devices

The automata that we have discussed so far have only a limited output capability to the extent that only outputs are ‘accepted’ and ‘not accepted’ to indicating the acceptance or rejection of an input string. We want to introduce two classic models for finite automata that have additional output capability. We will consider machines that transform input strings into output strings. These machines are basically DFAs, except that we associate an output symbol with each state or with each state transition. But there are no final states because we are not interested in acceptance or rejection.

### Mealy and Moore Machines

The first model invented by Mealy [1955] is called a Mealy machine. It associates an output letter with each transition. For example, if the output associated with the edge labelled with the letter a is x, we shall write a/x on that edge. A state transition for a Mealy machine can be presented in Figure 7 as follows:

<mermaid>
graph LR
    subgraph Fig. 7: Mealy machine
        i((i)) -- a/x --> j((j))
    end
</mermaid>

Indicating that the machine in state i and on input a gives output x and enters state j.

In a Mealy machine, an output always takes place during a transition of the states. The second model invented by Moore [1956], is called a Moore machine. It associates an output letter with each state. For example, if the output associated with state I is x, we will always write i/x inside the state circle. A typical state transition for a Moore machine can be presented in Figure 8 as follows:

<mermaid>
graph LR
    subgraph Fig. 8: Moore machine
        i[/i/] -- a --> j[/j/]
    end
</mermaid>

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;108&lt;/page_number&gt;

---


## Page 41

Set Theory Computability & Complexity

In a Moore machine, each time a state is entered, simultaneously an output takes place. So, the first output always occurs as soon as the machine is started. Mealy and Moore machines are equivalent. In other words, any problem that is soluble by one type of machine can also be solved by the other type of machine.

**Example 18:** Suppose we want to compute the number of sub strings of the form bab that occurs in an arbitrary input string over the alphabet {a,b}.

The diagrammatic representation of a Mealy machine for the task is given below in figure 9:

<mermaid>
graph LR
    A(( )) -- "a/0" --> B(0)
    B -- "b/0" --> C(1)
    C -- "a/0" --> D(2)
    D -- "b/1" --> E(3)
    E -- "b/0" --> F(1)
    F -- "b/0" --> G(2)
    G -- "b/0" --> H(3)
    H -- "a/0" --> I(0)
    I -- "a/0" --> J(1)
    J -- "a/0" --> K(2)
    K -- "a/0" --> L(3)
    L -- "a/0" --> M(0)
    M -- "a/0" --> N(1)
    N -- "a/0" --> O(2)
    O -- "a/0" --> P(3)
    P -- "a/0" --> Q(0)
    Q -- "a/0" --> R(1)
    R -- "a/0" --> S(2)
    S -- "a/0" --> T(3)
    T -- "a/0" --> U(0)
    U -- "a/0" --> V(1)
    V -- "a/0" --> W(2)
    W -- "a/0" --> X(3)
    X -- "a/0" --> Y(0)
    Y -- "a/0" --> Z(1)
    Z -- "a/0" --> AA(2)
    AA -- "a/0" --> BB(3)
    BB -- "a/0" --> CC(0)
    CC -- "a/0" --> DD(1)
    DD -- "a/0" --> EE(2)
    EE -- "a/0" --> FF(3)
    FF -- "a/0" --> GG(0)
    GG -- "a/0" --> HH(1)
    HH -- "a/0" --> II(2)
    II -- "a/0" --> JJ(3)
    JJ -- "a/0" --> KK(0)
    KK -- "a/0" --> LL(1)
    LL -- "a/0" --> MM(2)
    MM -- "a/0" --> NN(3)
    NN -- "a/0" --> OO(0)
    OO -- "a/0" --> PP(1)
    PP -- "a/0" --> QQ(2)
    QQ -- "a/0" --> RR(3)
    RR -- "a/0" --> SS(0)
    SS -- "a/0" --> TT(1)
    TT -- "a/0" --> UU(2)
    UU -- "a/0" --> VV(3)
    VV -- "a/0" --> WW(0)
    WW -- "a/0" --> XX(1)
    XX -- "a/0" --> YY(2)
    YY -- "a/0" --> ZZ(3)
    ZZ -- "a/0" --> AAA(0)
    AAA -- "a/0" --> BBB(1)
    BBB -- "a/0" --> CCC(2)
    CCC -- "a/0" --> DDD(3)
    DDD -- "a/0" --> EEE(0)
    EEE -- "a/0" --> FFF(1)
    FFF -- "a/0" --> GGG(2)
    GGG -- "a/0" --> HHH(3)
    HHH -- "a/0" --> III(0)
    III -- "a/0" --> JJJ(1)
    JJJ -- "a/0" --> KKK(2)
    KKK -- "a/0" --> LLL(3)
    LLL -- "a/0" --> MMM(0)
    MMM -- "a/0" --> NNN(1)
    NNN -- "a/0" --> OOO(2)
    OOO -- "a/0" --> PPP(3)
    PPP -- "a/0" --> QQQ(0)
    QQQ -- "a/0" --> RRR(1)
    RRR -- "a/0" --> SSS(2)
    SSS -- "a/0" --> TTT(3)
    TTT -- "a/0" --> UUU(0)
    UUU -- "a/0" --> VVV(1)
    VVV -- "a/0" --> WWW(2)
    WWW -- "a/0" --> XXX(3)
    XXX -- "a/0" --> YYY(0)
    YYY -- "a/0" --> ZZZ(1)
    ZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "a/0" --> VVVV(1)
    VVVV -- "a/0" --> WWWW(2)
    WWWW -- "a/0" --> XXXX(3)
    XXXX -- "a/0" --> YYYY(0)
    YYYY -- "a/0" --> ZZZZ(1)
    ZZZZ -- "a/0" --> AAAA(2)
    AAAA -- "a/0" --> BBBB(3)
    BBBB -- "a/0" --> CCCC(0)
    CCCC -- "a/0" --> DDDD(1)
    DDDD -- "a/0" --> EEED(2)
    EEED -- "a/0" --> FFFF(3)
    FFFF -- "a/0" --> GGGG(0)
    GGGG -- "a/0" --> HHHH(1)
    HHHH -- "a/0" --> IIII(2)
    IIII -- "a/0" --> JJJJ(3)
    JJJJ -- "a/0" --> KKKE(0)
    KKKE -- "a/0" --> LLLE(1)
    LLLE -- "a/0" --> MMME(2)
    MMME -- "a/0" --> NNNE(3)
    NNNE -- "a/0" --> OOOF(0)
    OOOF -- "a/0" --> PPPL(1)
    PPPL -- "a/0" --> QQQL(2)
    QQQL -- "a/0" --> RRRL(3)
    RRRL -- "a/0" --> SSSS(0)
    SSSS -- "a/0" --> TTTT(1)
    TTTT -- "a/0" --> UUUU(2)
    UUUU -- "a/0" --> VVVV(3)
    VVVV -- "a/0" --> WWWW(0)
    WWWW -- "a/0" --> XXXX(1)
    XXXX -- "a/0" --> YYYY(2)
    YYYY -- "a/0" --> ZZZZ(3)
    ZZZZ -- "a/0" --> AAAA(0)
    AAAA -- "a/0" --> BBBB(1)
    BBBB -- "a/0" --> CCCC(2)
    CCCC -- "a/0" --> DDDD(3)
    DDDD -- "a/0" --> EEED(0)
    EEED -- "a/0" --> FFFF(1)
    FFFF -- "a/0" --> GGGG(2)
    GGGG -- "a/0" --> HHHH(3)
    HHHH -- "a/0" --> IIII(0)
    IIII -- "a/0" --> JJJJ(1)
    JJJJ -- "a/0" --> KKKE(2)
    KKKE -- "a/0" --> LLLE(3)
    LLLE -- "a/0" --> MMME(0)
    MMME -- "a/0" --> NNNE(1)
    NNNE -- "a/0" --> OOOF(2)
    OOOF -- "a/0" --> PPPL(3)
    PPPL -- "a/0" --> QQQL(0)
    QQQL -- "a/0" --> RRRL(1)
    RRRL -- "a/0" --> SSSS(2)
    SSSS -- "a/0" --> TTTT(3)
    TTTT -- "a/0" --> UUUU(0)
    UUUU -- "

---


## Page 42

Auto Mata and Languages

<mermaid>
graph LR
    A((0/GR)) -->|0| A
    A -->|1| B(1/YR)
    B -->|0,1| C(2/RG)
    C -->|0,1| D(3/RY)
    D -->|0,1| A
</mermaid>

Fig. 11: Traffic signal transition diagram

Mealy machines appear to be more useful than Moore machines. But problems like traffic signal control have hic Moore machine solutions because each state is associated with a new output configuration.

Let us try some exercises:

Ex.8) Build a new FA that accepts only the word λ. Also write the corresponding regular expression.

Ex.9) Build an FA that accepts only those words that have even lengths. Also write the regular expression.

Ex.10) Build an FA that accepts only the word baa, ab and abb and no other words. Also write the corresponding regular expression.

Ex.11) Build an FA that will accept the language of all words each having twice as many a's as the number of b's. Also write the corresponding regular expression.

Ex.12) Describe the languages accepted by the following FA's:

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;Diagram (a): A finite automaton with three states. State 1 has transitions labeled 'a,b' to itself and to state 2. State 2 has transitions labeled 'a,b' to state 1 and 'a,b' to state 3. State 3 has a loop labeled 'a,b'. The initial state is indicated by an arrow pointing to state 1.&lt;/img&gt;
(a)

&lt;img&gt;Diagram (b): A finite automaton with four states. State 1 has transitions labeled 'a,b' to state 2. State 2 has transitions labeled 'a,b' to state 1 and 'a' to state 3. State 3 has transitions labeled 'a,b' to state 2 and 'a' to state 4. State 4 has a loop labeled 'a,b'. The initial state is indicated by an arrow pointing to state 1.&lt;/img&gt;
(b)

&lt;img&gt;Diagram (c): A finite automaton with five states. State 1 has transitions labeled 'a,b' to state 2. State 2 has transitions labeled 'a' to state 3 and 'b' to state 4. State 3 has transitions labeled 'a,b' to state 2 and 'a' to state 5. State 4 has transitions labeled 'b' to state 2 and 'a,b' to state 5. State 5 has a loop labeled 'a,b'. The initial state is indicated by an arrow pointing to state 1.&lt;/img&gt;
(c)

Fig. 12: Finite Automatas

2.5 NON DETERMINISTIC FINITE AUTOMATA

You have already studied finite automata (though ‘automata’ is a plural form of the

&lt;page_number&gt;110&lt;/page_number&gt;

---


## Page 43

Set Theory Computability & Complexity

noun ‘automaton’, the word ‘automata’ is also used in singular sense). Now consider an automata that accepts all and only strings ending in 01, represented diagrammatically, as follows:

<mermaid>
graph LR
    A(( )) -- 0 --> B(( ))
    B -- 1 --> C(( ))
    C --> A(0,1)
</mermaid>

**Fig. 13: Transition Diagram**

In the case of the finite automata shown in Figure 1, the following points may be noted:
(i) On input 0 in state q₀, the next state may be either of the two states viz., q₀ or q₁.
(ii) There is no next state on input 0 in the state q₁.
(iii) There is no next state on input 0 and 1 in the state q₂.

In this transition system, what happens when this automata processes the input .00101?

<mermaid>
graph LR
    subgraph Processing of string 00101
        A(( )) -- 0 --> B(q₀)
        B -- 0 --> C(q₁)
        C -- 0 --> D(q₀)
        D -- 0 --> E(q₁)
        E -- 0 --> F(q₀)
        F -- 1 --> G(q₀)
        G -- 1 --> H(q₀)
        I(( )) -- 0 --> J(q₀)
        J -- 0 --> K(q₁)
        K -- 0 --> L(q₀)
        L -- 0 --> M(q₁)
        M -- 0 --> N(q₀)
        N -- 1 --> O(q₀)
        O -- 1 --> P(q₀)
    end
    subgraph (Stuck)
        C
        E
    end
    subgraph (Stuck)
        L
        M
    end
</mermaid>

**Fig. 14: Processing of string 00101**

Here from the initial state q₀, for the processing of alphabet 0, there are two states at once or viewed another way, it can be ‘guessed” which state to go to next. Such a finite automata allows to have a choice of 0 or more next states for each state input pair and is called a non-deterministic finite automata. An NFA can be in several states at once.

<mermaid>
graph LR
    A(( )) -- 0,1 --> B(q₀)
    B -- 0,1 --> C(q₀)
    C -- 0,1 --> D(q₀)
    D -- 0,1 --> E(q₀)
    E -- 0,1 --> F(q₀)
    F -- 0,1 --> G(q₀)
    G -- 0,1 --> H(q₀)
    I(( )) -- 0,1 --> J(q₀)
    J -- 0,1 --> K(q₀)
    K -- 0,1 --> L(q₀)
    L -- 0,1 --> M(q₀)
    M -- 0,1 --> N(q₀)
    N -- 0,1 --> O(q₀)
    O -- 0,1 --> P(q₀)
    Q(( )) -- 0,1 --> R(q₀)
    R -- 0,1 --> S(q₀)
    S -- 0,1 --> T(q₀)
    T -- 0,1 --> U(q₀)
    U -- 0,1 --> V(q₀)
    V -- 0,1 --> W(q₀)
    W -- 0,1 --> X(q₀)
    X -- 0,1 --> Y(q₀)
    Y -- 0,1 --> Z(q₀)
    Z -- 0,1 --> AA(q₀)
    AA -- 0,1 --> AB(q₀)
    AB -- 0,1 --> AC(q₀)
    AC -- 0,1 --> AD(q₀)
    AD -- 0,1 --> AE(q₀)
    AE -- 0,1 --> AF(q₀)
    AF -- 0,1 --> AG(q₀)
    AG -- 0,1 --> AH(q₀)
    AH -- 0,1 --> AI(q₀)
    AI -- 0,1 --> AJ(q₀)
    AJ -- 0,1 --> AK(q₀)
    AK -- 0,1 --> AL(q₀)
    AL -- 0,1 --> AM(q₀)
    AM -- 0,1 --> AN(q₀)
    AN -- 0,1 --> AO(q₀)
    AO -- 0,1 --> AP(q₀)
    AP -- 0,1 --> AQ(q₀)
    AQ -- 0,1 --> AR(q₀)
    AR -- 0,1 --> AS(q₀)
    AS -- 0,1 --> AT(q₀)
    AT -- 0,1 --> AU(q₀)
    AU -- 0,1 --> AV(q₀)
    AV -- 0,1 --> AW(q₀)
    AW -- 0,1 --> AX(q₀)
    AX -- 0,1 --> AY(q₀)
    AY -- 0,1 --> AZ(q₀)
    AZ -- 0,1 --> BA(q₀)
    BA -- 0,1 --> BB(q₀)
    BB -- 0,1 --> BC(q₀)
    BC -- 0,1 --> BD(q₀)
    BD -- 0,1 --> BE(q₀)
    BE -- 0,1 --> BF(q₀)
    BF -- 0,1 --> BG(q₀)
    BG -- 0,1 --> BH(q₀)
    BH -- 0,1 --> BI(q₀)
    BI -- 0,1 --> BJ(q₀)
    BJ -- 0,1 --> BK(q₀)
    BK -- 0,1 --> BL(q₀)
    BL -- 0,1 --> BM(q₀)
    BM -- 0,1 --> BN(q₀)
    BN -- 0,1 --> BO(q₀)
    BO -- 0,1 --> BP(q₀)
    BP -- 0,1 --> BQ(q₀)
    BQ -- 0,1 --> BR(q₀)
    BR -- 0,1 --> BS(q₀)
    BS -- 0,1 --> BT(q₀)
    BT -- 0,1 --> BU(q₀)
    BU -- 0,1 --> BV(q₀)
    BV -- 0,1 --> BW(q₀)
    BW -- 0,1 --> BX(q₀)
    BX -- 0,1 --> BY(q₀)
    BY -- 0,1 --> BZ(q₀)
    BZ -- 0,1 --> CA(q₀)
    CA -- 0,1 --> CB(q₀)
    CB -- 0,1 --> CC(q₀)
    CC -- 0,1 --> CD(q₀)
    CD -- 0,1 --> CE(q₀)
    CE -- 0,1 --> CF(q₀)
    CF -- 0,1 --> CG(q₀)
    CG -- 0,1 --> CH(q₀)
    CH -- 0,1 --> CI(q₀)
    CI -- 0,1 --> CJ(q₀)
    CJ -- 0,1 --> CK(q₀)
    CK -- 0,1 --> CL(q₀)
    CL -- 0,1 --> CM(q₀)
    CM -- 0,1 --> CN(q₀)
    CN -- 0,1 --> CO(q₀)
    CO -- 0,1 --> CP(q₀)
    CP -- 0,1 --> CQ(q₀)
    CQ -- 0,1 --> CR(q₀)
    CR -- 0,1 --> CS(q₀)
    CS -- 0,1 --> CT(q₀)
    CT -- 0,1 --> CU(q₀)
    CU -- 0,1 --> CV(q₀)
    CV -- 0,1 --> CW(q₀)
    CW -- 0,1 --> CX(q₀)
    CX -- 0,1 --> CY(q₀)
    CY -- 0,1 --> CZ(q₀)
    CZ -- 0,1 --> DA(q₀)
    DA -- 0,1 --> DB(q₀)
    DB -- 0,1 --> DC(q₀)
    DC -- 0,1 --> DD(q₀)
    DD -- 0,1 --> DE(q₀)
    DE -- 0,1 --> DF(q₀)
    DF -- 0,1 --> DG(q₀)
    DG -- 0,1 --> DH(q₀)
    DH -- 0,1 --> DI(q₀)
    DI -- 0,1 --> DJ(q₀)
    DJ -- 0,1 --> DK(q₀)
    DK -- 0,1 --> DL(q₀)
    DL -- 0,1 --> DM(q₀)
    DM -- 0,1 --> DN(q₀)
    DN -- 0,1 --> DO(q₀)
    DO -- 0,1 --> DP(q₀)
    DP -- 0,1 --> DQ(q₀)
    DQ -- 0,1 --> DR(q₀)
    DR -- 0,1 --> DS(q₀)
    DS -- 0,1 --> DT(q₀)
    DT -- 0,1 --> DU(q₀)
    DU -- 0,1 --> DV(q₀)
    DV -- 0,1 --> DW(q₀)
    DW -- 0,1 --> DX(q₀)
    DX -- 0,1 --> DY(q₀)
    DY -- 0,1 --> DZ(q₀)
    DZ -- 0,1 --> EA(q₀)
    EA -- 0,1 --> EB(q₀)
    EB -- 0,1 --> EC(q₀)
    EC -- 0,1 --> ED(q₀)
    ED -- 0,1 --> EE(q₀)
    EE -- 0,1 --> EF(q₀)
    EF -- 0,1 --> EG(q₀)
    EG -- 0,1 --> EH(q₀)
    EH -- 0,1 --> EI(q₀)
    EI -- 0,1 --> EJ(q₀)
    EJ -- 0,1 --> EK(q₀)
    EK -- 0,1 --> EL(q₀)
    EL -- 0,1 --> EM(q₀)
    EM -- 0,1 --> EN(q₀)
    EN -- 0,1 --> EO(q₀)
    EO -- 0,1 --> EP(q₀)
    EP -- 0,1 --> EQ(q₀)
    EQ -- 0,1 --> ER(q₀)
    ER -- 0,1 --> ES(q₀)
    ES -- 0,1 --> ET(q₀)
    ET -- 0,1 --> EU(q₀)
    EU -- 0,1 --> EV(q₀)
    EV -- 0,1 --> EW(q₀)
    EW -- 0,1 --> EX(q₀)
    EX -- 0,1 --> EY(q₀)
    EY -- 0,1 --> EZ(q₀)
    EZ -- 0,1 --> FA(q₀)
    FA -- 0,1 --> FB(q₀)
    FB -- 0,1 --> FC(q₀)
    FC -- 0,1 --> FD(q₀)
    FD -- 0,1 --> FE(q₀)
    FE -- 0,1 --> FF(q₀)
    FF -- 0,1 --> FG(q₀)
    FG -- 0,1 --> FH(q₀)
    FH -- 0,1 --> FI(q₀)
    FI -- 0,1 --> FJ(q₀)
    FJ -- 0,1 --> FK(q₀)
    FK -- 0,1 --> FL(q₀)
    FL -- 0,1 --> FM(q₀)
    FM -- 0,1 --> FN(q₀)
    FN -- 0,1 --> FO(q₀)
    FO -- 0,1 --> FP(q₀)
    FP -- 0,1 --> FQ(q₀)
    FQ -- 0,1 --> FR(q₀)
    FR -- 0,1 --> FS(q₀)
    FS -- 0,1 --> FT(q₀)
    FT -- 0,1 --> FU(q₀)
    FU -- 0,1 --> FV(q₀)
    FV -- 0,1 --> FW(q₀)
    FW -- 0,1 --> FX(q₀)
    FX -- 0,1 --> FY(q₀)
    FY -- 0,1 --> FZ(q₀)
    FZ -- 0,1 --> GA(q₀)
    GA -- 0,1 --> GB(q₀)
    GB -- 0,1 --> GC(q₀)
    GC -- 0,1 --> GD(q₀)
    GD -- 0,1 --> GE(q₀)
    GE -- 0,1 --> GF(q₀)
    GF -- 0,1 --> GG(q₀)
    GG -- 0,1 --> GH(q₀)
    GH -- 0,1 --> GI(q₀)
    GI -- 0,1 --> GJ(q₀)
    GJ -- 0,1 --> GK(q₀)
    GK -- 0,1 --> GL(q₀)
    GL -- 0,1 --> GM(q₀)
    GM -- 0,1 --> GN(q₀)
    GN -- 0,1 --> GO(q₀)
    GO -- 0,1 --> GP(q₀)
    GP -- 0,1 --> GQ(q₀)
    GQ -- 0,1 --> GR(q₀)
    GR -- 0,1 --> GS(q₀)
    GS -- 0,1 --> GT(q₀)
    GT -- 0,1 --> GU(q₀)
    GU -- 0,1 --> GV(q₀)
    GV -- 0,1 --> GW(q₀)
    GW -- 0,1 --> GX(q₀)
    GX -- 0,1 --> GY(q₀)
    GY -- 0,1 --> GZ(q₀)
    GZ -- 0,1 --> HA(q₀)
    HA -- 0,1 --> HB(q₀)
    HB -- 0,1 --> HC(q₀)
    HC -- 0,1 --> HD(q₀)
    HD -- 0,1 --> HE(q₀)
    HE -- 0,1 --> HF(q₀)
    HF -- 0,1 --> HG(q₀)
    HG -- 0,1 --> HH(q₀)
    HH -- 0,1 --> HI(q₀)
    HI -- 0,1 --> HJ(q₀)
    HJ -- 0,1 --> HK(q₀)
    HK -- 0,1 --> HL(q₀)
    HL -- 0,1 --> HM(q₀)
    HM -- 0,1 --> HN(q₀)
    HN -- 0,1 --> HO(q₀)
    HO -- 0,1 --> HP(q₀)
    HP -- 0,1 --> HQ(q₀)
    HQ -- 0,1 --> HR(q₀)
    HR -- 0,1 --> HS(q₀)
    HS -- 0,1 --> HT(q₀)
    HT -- 0,1 --> HU(q₀)
    HU -- 0,1 --> HV(q₀)
    HV -- 0,1 --> HW(q₀)
    HW -- 0,1 --> HX(q₀)
    HX -- 0,1 --> HY(q₀)
    HY -- 0,1 --> HZ(q₀)
    HZ -- 0,1 --> IA(q₀)
    IA -- 0,1 --> IB(q₀)
    IB -- 0,1 --> IC(q₀)
    IC -- 0,1 --> ID(q₀)
    ID -- 0,1 --> IE(q₀)
    IE -- 0,1 --> IF(q₀)
    IF -- 0,1 --> IG(q₀)
    IG -- 0,1 --> IH(q₀)
    IH -- 0,1 --> II(q₀)
    II -- 0,1 --> IJ(q₀)
    IJ -- 0,1 --> IK(q₀)
    IK -- 0,1 --> IL(q₀)
    IL -- 0,1 --> IM(q₀)
    IM -- 0,1 --> IN(q₀)
    IN -- 0,1 --> IO(q₀)
    IO -- 0,1 --> IP(q₀)
    IP -- 0,1 --> IQ(q₀)
    IQ -- 0,1 --> IR(q₀)
    IR -- 0,1 --> IS(q₀)
    IS -- 0,1 --> IT(q₀)
    IT -- 0,1 --> IU(q₀)
    IU -- 0,1 --> IV(q₀)
    IV -- 0,1 --> IW(q₀)
    IW -- 0,1 --> IX(q₀)
    IX -- 0,1 --> IY(q₀)
    IY -- 0,1 --> IZ(q₀)
    IZ -- 0,1 --> JA(q₀)
    JA -- 0,1 --> JB(q₀)
    JB -- 0,1 --> JC(q₀)
    JC -- 0,1 --> JD(q₀)
    JD -- 0,1 --> JE(q₀)
    JE -- 0,1 --> JF(q₀)
    JF -- 0,1 --> JG(q₀)
    JG -- 0,1 --> JH(q₀)
    JH -- 0,1 --> JJ(q₀)
    JJ -- 0,1 --> JK(q₀)
    JK -- 0,1 --> JL(q₀)
    JL -- 0,1 --> JM(q₀)
    JM -- 0,1 --> JN(q₀)
    JN -- 0,1 --> JO(q₀)
    JO -- 0,1 --> JP(q₀)
    JP -- 0,1 --> JQ(q₀)
    JQ -- 0,1 --> JR(q₀)
    JR -- 0,1 --> JS(q₀)
    JS -- 0,1 --> JT(q₀)
    JT -- 0,1 --> JU(q₀)
    JU -- 0,1 --> JV(q₀)
    JV -- 0,1 --> JW(q₀)
    JW -- 0,1 --> JX(q₀)
    JX -- 0,1 --> JY(q₀)
    JY -- 0,1 --> JZ(q₀)
    JZ -- 0,1 --> KA(q₀)
    KA -- 0,1 --> KB(q₀)
    KB -- 0,1 --> KC(q₀)
    KC -- 0,1 --> KD(q₀)
    KD -- 0,1 --> KE(q₀)
    KE -- 0,1 --> KF(q₀)
    KF -- 0,1 --> KG(q₀)
    KG -- 0,1 --> KH(q₀)
    KH -- 0,1 --> KK(q₀)
    KK -- 0,1 --> KL(q₀)
    KL -- 0,1 --> KM(q₀)
    KM -- 0,1 --> KN(q₀)
    KN -- 0,1 --> KO(q₀)
    KO -- 0,1 --> KP(q₀)
    KP -- 0,1 --> KQ(q₀)
    KQ -- 0,1 --> KR(q₀)
    KR -- 0,1 --> KS(q₀)
    KS -- 0,1 --> KT(q₀)
    KT -- 0,1 --> KU(q₀)
    KU -- 0,1 --> KV(q₀)
    KV -- 0,1 --> KW(q₀)
    KW -- 0,1 --> KX(q₀)
    KX -- 0,1 --> KY(q₀)
    KY -- 0,1 --> KZ(q₀)
    KZ -- 0,1 --> LA(q₀)
    LA -- 0,1 --> LB(q₀)
    LB -- 0,1 --> LC(q₀)
    LC -- 0,1 --> LD(q₀)
    LD -- 0,1 --> LE(q₀)
    LE -- 0,1 --> LF(q₀)
    LF -- 0,1 --> LG(q₀)
    LG -- 0,1 --> LH(q₀)
    LH -- 0,1 --> LI(q₀)
    LI -- 0,1 --> LJ(q₀)
    LJ -- 0,1 --> LK(q₀)
    LK -- 0,1 --> LL(q₀)
    LL -- 0,1 --> LM(q₀)
    LM -- 0,1 --> LN(q₀)
    LN -- 0,1 --> LO(q₀)
    LO -- 0,1 --> LP(q₀)
    LP -- 0,1 --> LQ(q₀)
    LQ -- 0,1 --> LR(q₀)
    LR -- 0,1 --> LS(q₀)
    LS -- 0,1 --> LT(q₀)
    LT -- 0,1 --> LU(q₀)
    LU -- 0,1 --> LV(q₀)
    LV -- 0,1 --> LW(q₀)
    LW -- 0,1 --> LX(q₀)
    LX -- 0,1 --> LY(q₀)
    LY -- 0,1 --> LZ(q₀)
    LZ -- 0,1 --> MA(q₀)
    MA -- 0,1 --> MB(q₀)
    MB -- 0,1 --> MC(q₀)
    MC -- 0,1 --> MD(q₀)
    MD -- 0,1 --> ME(q₀)
    ME -- 0,1 --> MF(q₀)
    MF -- 0,1 --> MG(q₀)
    MG -- 0,1 --> MH(q₀)
    MH -- 0,1 --> MJ(q₀)
    MJ -- 0,1 --> MK(q₀)
    MK -- 0,1 --> ML(q₀)
    ML -- 0,1 --> MM(q₀)
    MM -- 0,1 --> MN(q₀)
    MN -- 0,1 --> MO(q₀)
    MO -- 0,1 --> MP(q₀)
    MP -- 0,1 --> MQ(q₀)
    MQ -- 0,1 --> MR(q₀)
    MR -- 0,1 --> MS(q₀)
    MS -- 0,1 --> MT(q₀)
    MT -- 0,1 --> MU(q₀)
    MU -- 0,1 --> MV(q₀)
    MV -- 0,1 --> MW(q₀)
    MW -- 0,1 --> MX(q₀)
    MX -- 0,1 --> MY(q₀)
    MY -- 0,1 --> MZ(q₀)
    MZ -- 0,1 --> NA(q₀)
    NA -- 0,1 --> NB(q₀)
    NB -- 0,1 --> NC(q₀)
    NC -- 0,1 --> ND(q₀)
    ND -- 0,1 --> NE(q₀)
    NE -- 0,1 --> NF(q₀)
    NF -- 0,1 --> NG(q₀)
    NG -- 0,1 --> NH(q₀)
    NH -- 0,1 --> NJ(q₀)
    NJ -- 0,1 --> NK(q₀)
    NK -- 0,1 --> NL(q₀)
    NL -- 0,1 --> NM(q₀)
    NM -- 0,1 --> NN(q₀)
    NN -- 0,1 --> NO(q₀)
    NO -- 0,1 --> OP(q₀)
    OP -- 0,1 --> OQ(q₀)
    OQ -- 0,1 --> OR(q₀)
    OR -- 0,1 --> OS(q₀)
    OS -- 0,1 --> OT(q₀)
    OT -- 0,1 --> OU(q₀)
    OU -- 0,1 --> OV(q₀)
    OV -- 0,1 --> OW(q₀)
    OW -- 0,1 --> OX(q₀)
    OX -- 0,1 --> OY(q₀)
    OY -- 0,1 --> OZ(q₀)
    OZ -- 0,1 --> PA(q₀)
    PA -- 0,1 --> PB(q₀)
    PB -- 0,1 --> PC(q₀)
    PC -- 0,1 --> PD(q₀)
    PD -- 0,1 --> PE(q₀)
    PE -- 0,1 --> PF(q₀)
    PF -- 0,1 --> PG(q₀)
    PG -- 0,1 --> PH(q₀)
    PH -- 0,1 --> PJ(q₀)
    PJ -- 0,1 --> PK(q₀)
    PK -- 0,1 --> PL(q₀)
    PL -- 0,1 --> PM(q₀)
    PM -- 0,1 --> PN(q₀)
    PN -- 0,1 --> PO(q₀)
    PO -- 0,1 --> PP(q₀)
    PP -- 0,1 --> PQ(q₀)
    PQ -- 0,1 --> PR(q₀)
    PR -- 0,1 --> PS(q₀)
    PS -- 0,1 --> PT(q₀)
    PT -- 0,1 --> PU(q₀)
    PU -- 0,1 --> PV(q₀)
    PV -- 0,1 --> PW(q₀)
    PW -- 0,1 --> PX(q₀)
    PX -- 0,1 --> PY(q₀)
    PY -- 0,1 --> PZ(q₀)
    PZ -- 0,1 --> QA(q₀)
    QA -- 0,1 --> QB(q₀)
    QB -- 0,1 --> QC(q₀)
    QC -- 0,1 --> QD(q₀)
    QD -- 0,1 --> QE(q₀)
    QE -- 0,1 --> QF(q₀)
    QF -- 0,1 --> QG(q₀)
    QG -- 0,1 --> QH(q₀)
    QH -- 0,1 --> QI(q₀)
    QI -- 0,1 --> QJ(q₀)
    QJ -- 0,1 --> QK(q₀)
    QK -- 0,1 --> QL(q₀)
    QL -- 0,1 --> QM(q₀)
    QM -- 0,1 --> QN(q₀)
    QN -- 0,1 --> QO(q₀)
    QO -- 0,1 --> QQ(q₀)
    QQ -- 0,1 --> QR(q₀)
    QR -- 0,1 --> QS(q₀)
    QS -- 0,1 --> QT(q₀)
    QT -- 0,1 --> QU(q₀)
    QU -- 0,1 --> QV(q₀)
    QV -- 0,1 --> QW(q₀)
    QW -- 0,1 --> QX(q₀)
    QX -- 0,1 --> QY(q₀)
    QY -- 0,1 --> QZ(q₀)
    QZ -- 0,1 --> RA(q₀)
    RA -- 0,1 --> RB(q₀)
    RB -- 0,1 --> RC(q₀)
    RC -- 0,1 --> RD(q₀)
    RD -- 0,1 --> RE(q₀)
    RE -- 0,1 --> RF(q₀)
    RF -- 0,1 --> RG(q₀)
    RG -- 0,1 --> RH(q₀)
    RH -- 0,1 --> RJ(q₀)
    RJ -- 0,1 --> RK(q₀)
    RK -- 0,1 --> RL(q₀)
    RL -- 0,1 --> RM(q₀)
    RM -- 0,1 --> RN(q₀)
    RN -- 0,1 --> RO(q₀)
    RO -- 0,1 --> RP(q₀)
    RP -- 0,1 --> RQ(q₀)
    RQ -- 0,1 --> RR(q₀)
    RR -- 0,1 --> RS(q₀)
    RS -- 0,1 --> RT(q₀)
    RT -- 0,1 --> RU(q₀)
    RU -- 0,1 --> RV(q₀)
    RV -- 0,1 --> RW(q₀)
    RW -- 0,1 --> RX(q₀)
    RX -- 0,1 --> RY(q₀)
    RY -- 0,1 --> RZ(q₀)
    RZ -- 0,1 --> SA(q₀)
    SA -- 0,1 --> SB(q₀)
    SB -- 0,1 --> SC(q₀)
    SC -- 0,1 --> SD(q₀)
    SD -- 0,1 --> SE(q₀)
    SE -- 0,1 --> SF(q₀)
    SF -- 0,1 --> SG(q₀)
    SG -- 0,1 --> SH(q₀)
    SH -- 0,1 --> SJ(q₀)
    SJ -- 0,1 --> SK(q₀)
    SK -- 0,1 --> SL(q₀)
    SL -- 0,1 --> SM(q₀)
    SM -- 0,1 --> SN(q₀)
    SN -- 0,1 --> SO(q₀)
    SO -- 0,1 --> SP(q₀)
    SP -- 0,1 --> SQ(q₀)
    SQ -- 0,1 --> SR(q₀)
    SR -- 0,1 --> SS(q₀)
    SS -- 0,1 --> ST(q₀)
    ST -- 0,1 --> SU(q₀)
    SU -- 0,1 --> SV(q₀)
    SV -- 0,1 --> SW(q₀)
    SW -- 0,1 --> SX(q₀)
    SX -- 0,1 --> SY(q₀)
    SY -- 0,1 --> SZ(q₀)
    SZ -- 0,1 --> TA(q₀)
    TA -- 0,1 --> TB(q₀)
    TB -- 0,1 --> TC(q₀)
    TC -- 0,1 --> TD(q₀)
    TD -- 0,1 --> TE(q₀)
    TE -- 0,1 --> TF(q₀)
    TF -- 0,1 --> TG(q₀)
    TG -- 0,1 --> TH(q₀)
    TH -- 0,1 --> TJ(q₀)
    TJ -- 0,1 --> TK(q₀)
    TK -- 0,1 --> TL(q₀)
    TL -- 0,1 --> TM(q₀)
    TM -- 0,1 --> TN(q₀)
    TN -- 0,1 --> TO(q₀)
    TO -- 0,1 --> TP(q₀)
    TP -- 0,1 --> TQ(q₀)
    TQ -- 0,1 --> TR(q₀)
    TR -- 0,1 --> TS(q₀)
    TS -- 0,1 --> TT(q₀)
    TT -- 0,1 --> TU(q₀)
    TU -- 0,1 --> TV(q₀)
    TV -- 0,1 --> TW(q₀)
    TW -- 0,1 --> TX(q₀)
    TX -- 0,1 --> TY(q₀)
    TY -- 0,1 --> TZ(q₀)
    TZ -- 0,1 --> UA(q₀)
    UA -- 0,1 --> UB(q₀)
    UB -- 0,1 --> UC(q₀)
    UC -- 0,1 --> UD(q₀)
    UD -- 0,1 --> UE(q₀)
    UE -- 0,1 --> UF(q₀)
    UF -- 0,1 --> UG(q₀)
    UG -- 0,1 --> UH(q₀)
    UH -- 0,1 --> UI(q₀)
    UI -- 0,1 --> UJ(q₀)
    UJ -- 0,1 --> UK(q₀)
    UK -- 0,1 --> UL(q₀)
    UL -- 0,1 --> UM(q₀)
    UM -- 0,1 --> UN(q₀)
    UN -- 0,1 --> UO(q₀)
    UO -- 0,1 --> UP(q₀)
    UP -- 0,1 --> UQ(q₀)
    UQ -- 0,1 --> UR(q₀)
    UR -- 0,1 --> US(q₀)
    US -- 0,1 --> UT(q₀)
    UT -- 0,1 --> UU(q₀)
    UU -- 0,1 --> UV(q₀)
    UV -- 0,1 --> UW(q₀)
    UW -- 0,1 --> UX(q₀)
    UX -- 0,1 --> UY(q₀)
    UY -- 0,1 --> UZ(q₀)
    UZ -- 0,1 --> VA(q₀)
    VA -- 0,1 --> VB(q₀)
    VB -- 0,1 --> VC(q₀)
    VC -- 0,1 --> VD(q₀)
    VD -- 0,1 --> VE(q₀)
    VE -- 0,1 --> VF(q₀)
    VF -- 0,1 --> VG(q₀)
    VG -- 0,1 --> VH(q₀)
    VH -- 0,1 --> VI(q₀)
    VI -- 0,1 --> VJ(q₀)
    VJ -- 0,1 --> VK(q₀)
    VK -- 0,1 --> VL(q₀)
    VL -- 0,1 --> VM(q₀)
    VM -- 0,1 --> VN(q₀)
    VN -- 0,1 --> VO(q₀)
    VO -- 0,1 --> VP(q₀)
    VP -- 0,1 --> VQ(q₀)
    VQ -- 0,1 --> VR(q₀)
    VR -- 0,1 --> VS(q₀)
    VS -- 0,1 --> VT(q₀)
    VT -- 0,1 --> VU(q₀)
    VU -- 0,1 --> VV(q₀)
    VV -- 0,1 --> VW(q₀)
    VW -- 0,1 --> VX(q₀)
    VX -- 0,1 --> VY(q₀)
    VY -- 0,1 --> VZ(q₀)
    VZ -- 0,1 --> WA(q₀)
    WA -- 0,1 --> WB(q₀)
    WB -- 0,1 --> WC(q₀)
    WC -- 0,1 --> WD(q₀)
    WD -- 0,1 --> WE(q₀)
    WE -- 0,1 --> WF(q₀)
    WF -- 0,1 --> WG(q₀)
    WG -- 0,1 --> WH(q₀)
    WH -- 0,1 --> WI(q₀)
    WI -- 0,1 --> WJ(q₀)
    WJ -- 0,1 --> WK(q₀)
    WK -- 0,1 --> WL(q₀)
    WL -- 0,1 --> WM(q₀)
    WM -- 0,1 --> WN(q₀)
    WN -- 0,1 --> XO(q₀)
    XO -- 0,1 --> XP(q₀)
    XP -- 0,1 --> XQ(q₀)
    XQ -- 0,1 --> XR(q₀)
    XR -- 0,1 --> XS(q₀)
    XS -- 0,1 --> XT(q₀)
    XT -- 0,1 --> XU(q₀)
    XU -- 0,1 --> XV(q₀)
    XV -- 0,1 --> XW(q₀)
    XW -- 0,1 --> XX(q₀)
    XX -- 0,1 --> XY(q₀)
    XY -- 0,1 --> XZ(q₀)
    XZ -- 0,1 --> YA(q₀)
    YA -- 0,1 --> YB(q₀)
    YB -- 0,1 --> YC(q₀)
    YC -- 0,1 --> YD(q₀)
    YD -- 0,1 --> YE(q₀)
    YE -- 0,1 --> YF(q₀)
    YF -- 0,1 --> YG(q₀)
    YG -- 0,1 --> YH(q₀)
    YH -- 0,1 --> YI(q₀)
    YI -- 0,1 --> YJ(q₀)
    YJ -- 0,1 --> YK(q₀)
    YK -- 0,1 --> YL(q₀)
    YL -- 0,1 --> YM(q₀)
    YM -- 0,1 --> YN(q₀)
    YN -- 0,1 --> YO(q₀)
    YO -- 0,1 --> YP(q₀)
    YP -- 0,1 --> YQ(q₀)
    YQ -- 0,1 --> YR(q₀)
    YR -- 0,1 --> YS(q₀)
    YS -- 0,1 --> YT(q₀)
    YT -- 0,1 --> YU(q₀)
    YU -- 0,1 --> YV(q₀)
    YV -- 0,1 --> YW(q₀)
    YW -- 0,1 --> YX(q₀)
    YX -- 0,1 --> YY(q₀)
    YY -- 0,1 --> YZ(q₀)
    YZ -- 0,1 --> ZA(q₀)
    ZA -- 0,1 --> ZB(q₀)
    ZB -- 0,1 --> ZC(q₀)
    ZC -- 0,1 --> ZD(q₀)
    ZD -- 0,1 --> ZE(q₀)
    ZE -- 0,1 --> ZF(q₀)
    ZF -- 0,1 --> ZG(q₀)
    ZG -- 0,1 --> ZH(q₀)
    ZH -- 0,1 --> ZI(q₀)
    ZI -- 0,1 --> ZJ(q₀)
    ZJ -- 0,1 --> ZK(q₀)
    ZK -- 0,1 --> ZL(q₀)
    ZL -- 0,1 --> ZM(q₀)
    ZM -- 0,1 --> ZN(q₀)
    ZN -- 0,1 --> ZO(q₀)
    ZO -- 0,1 --> ZP(q₀)
    ZP -- 0,1 --> ZQ(q₀)
    ZQ -- 0,1 --> ZR(q₀)
    ZR -- 0,1 --> ZS(q₀)
    ZS -- 0,1 --> ZT(q₀)
    ZT -- 0,1 --> ZU(q₀)
    ZU -- 0,1 --> ZV(q₀)
    ZV -- 0,1 --> ZW(q₀)
    ZW -- 0,1 --> ZX(q₀)
    ZX -- 0,1 --> ZY(q₀)
    ZY -- 0,1 --> ZZ(q₀)
    ZZ -- 0,1 --> AA(q₀)
    AA -- 0,1 --> AB(q₀)
    AB -- 0,1 --> AC(q₀)
    AC -- 0,1 --> AD(q₀)
    AD -- 0,1 --> AE(q₀)
    AE -- 0,1 --> AF(q₀)
    AF -- 0,1 --> AG(q₀)
    AG -- 0,1 --> AH(q₀)
    AH -- 0,1 --> AI(q₀)
    AI -- 0,1 --> AJ(q₀)
    AJ -- 0,1 --> AK(q₀)
    AK -- 0,1 --> AL(q₀)
    AL -- 0,1 --> AM(q₀)
    AM -- 0,1 --> AN(q₀)
    AN -- 0,1 --> AO(q₀)
    AO -- 0,1 --> AP(q₀)
    AP -- 0,1 --> AQ(q₀)
    AQ -- 0,1 --> AR(q₀)
    AR -- 0,1 --> AS(q₀)
    AS -- 0,1 --> AT(q₀)
    AT -- 0,1 --> AU(q₀)
    AU -- 0,1 --> AV(q₀)
    AV -- 0,1 --> AW(q₀)
    AW -- 0,1 --> AX(q₀)
    AX -- 0,1 --> AY(q₀)
    AY -- 0,1 --> AZ(q₀)
    AZ -- 0,1 --> BA(q₀)
    BA -- 0,1 --> BB(q₀)
    BB -- 0,1 --> BC(q₀)
    BC -- 0,1 --> BD(q₀)
    BD -- 0,1 --> BE(q₀)
    BE -- 0,1 --> BF(q₀)
    BF -- 0,1 --> BG(q₀)
    BG -- 0,1 --> BH(q₀)
    BH -- 0,1 --> BI(q₀)
    BI -- 0,1 --> BJ(q₀)
    BJ -- 0,1 --> BK(q₀)
    BK -- 0,1 --> BL(q₀)
    BL -- 0,1 --> BM(q₀)
    BM -- 0,1 --> BN(q₀)
    BN -- 0,1 --> BO(q₀)
    BO -- 0,1 --> BP(q₀)
    BP -- 0,1 --> BQ(q₀)
    BQ -- 0,1 --> BR(q₀)
    BR -- 0,1 --> BS(q₀)
    BS -- 0,1 --> BT(q₀)
    BT -- 0,1 --> BU(q₀)
    BU -- 0,1 --> BV(q₀)
    BV -- 0,1 --> BW(q₀)
    BW -- 0,1 --> BX(q₀)
    BX -- 0,1 --> BY(q₀)
    BY -- 0,1 --> BZ(q₀)
    BZ -- 0,1 --> CA(q₀)
    CA -- 0,1 --> CB(q₀)
    CB -- 0,1 --> CC(q₀)
    CC -- 0,1 --> CD(q₀)
    CD -- 0,1 --> CE(q₀)
    CE -- 0,1 --> CF(q₀)
    CF -- 0,1 --> CG(q₀)
    CG -- 0,1 --> CH(q₀)
    CH -- 0,1 --> CI(q₀)
    CI -- 0,1 --> CJ(q₀)
    CJ -- 0,1 --> CK(q₀)
    CK -- 0,1 --> CL(q₀)
    CL -- 0,1 --> CM(q₀)
    CM -- 0,1 --> CN(q₀)
    CN -- 0,1 --> CO(q₀)
    CO -- 0,1 --> CP(q₀)
    CP -- 0,1 --> CQ(q₀)
    CQ -- 0,1 --> CR(q₀)
    CR -- 0,1 --> CS(q₀)
    CS -- 0,1 --> CT(q₀)
    CT -- 0,1 --> CU(q₀)
    CU -- 0,1 --> CV(q₀)
    CV -- 0,1 --> CW(q₀)
    CW -- 0,1 --> CX(q₀)
    CX -- 0,1 --> CY(q₀)
    CY -- 0,1 --> CZ(q₀)
    CZ -- 0,1 --> DA(q₀)
    DA -- 0,1 --> DB(q₀)
    DB -- 0,1 --> DC(q₀)
    DC -- 0,1 --> DD(q₀)
    DD -- 0,1 --> DE(q₀)
    DE -- 0,1 --> DF(q₀)
    DF -- 0,1 --> DG(q₀)
    DG -- 0,1 --> DH(q₀)
    DH -- 0,1 --> DI(q₀)
    DI -- 0,1 --> DJ(q₀)
    DJ -- 0,1 --> DK(q₀)
    DK -- 0,1 --> DL(q₀)
    DL -- 0,1 --> DM(q₀)
    DM -- 0,1 --> DN(q₀)
    DN -- 0,1 --> DO(q₀)
    DO -- 0,1 --> DP(q₀)
    DP -- 0,1 --> DQ(q₀)
    DQ -- 0,1 --> DR(q₀)
    DR -- 0,1 --> DS(q₀)
    DS -- 0,1 --> DT(q₀)
    DT -- 0,1 --> DU(q₀)
    DU -- 0,1 --> DV(q₀)
    DV -- 0,1 --> DW(q₀)
    DW -- 0,1 --> DX(q₀)
    DX -- 0,1 --> DY(q₀)
    DY -- 0,1 --> DZ(q₀)
    DZ -- 0,1 --> EA(q₀)
    EA -- 0,1 --> EB(q₀)
    EB -- 0,1 --> EC(q₀)
    EC -- 0,1 --> ED(q₀)
    ED -- 0,1 --> EE(q₀)
    EE -- 0,1 --> EF(q₀)
    EF -- 0,1 --> EG(q₀)
    EG -- 0,1 --> EH(q₀)
    EH -- 0,1 --> EI(q₀)
    EI -- 0,1 --> EJ(q₀)
    EJ -- 0,1 --> EK(q₀)
    EK -- 0,1 --> EL(q₀)
    EL -- 0,1 --> EM(q₀)
    EM -- 0,1 --> EN(q₀)
    EN -- 0,1 --> EO(q₀)
    EO -- 0,1 --> EP(q₀)
    EP -- 0,1 --> EQ(q₀)
    EQ -- 0,1 --> ER(q₀)
    ER -- 0,1 --> ES(q₀)
    ES -- 0,1 --> ET(q₀)
    ET -- 0,1 --> EU(q₀)
    EU -- 0,1 --> EV(q₀)
    EV -- 0,1 --> EW(q₀)
    EW -- 0,1 --> EX(q₀)
    EX -- 0,1 --> EY(q₀)
    EY -- 0,1 --> EZ(q₀)
    EZ -- 0,1 --> FA(q₀)
    FA -- 0,1 --> FB(q₀)
    FB -- 0,1 --> FC(q₀)
    FC -- 0,1 --> FD(q₀)
    FD -- 0,1 --> FE(q₀)
    FE -- 0,1 --> FF(q₀)
    FF -- 0,1 --> FG(q₀)
    FG -- 0,1 --> FH(q₀)
    FH -- 0,1 --> FI(q₀)
    FI -- 0,1 --> FJ(q₀)
    FJ -- 0,1 --> FK(q₀)
    FK -- 0,1 --> FL(q₀)
    FL -- 0,1 --> FM(q₀)
    FM -- 0,1 --> FN(q₀)
    FN -- 0,1 --> FO(q₀)
    FO -- 0,1 --> FP(q₀)
    FP -- 0,1 --> FQ(q₀)
    FQ -- 0,1 --> FR(q₀)
    FR -- 0,1 --> FS(q₀)
    FS -- 0,1 --> FT(q₀)
    FT -- 0,1 --> FU(q₀)
    FU -- 0,1 --> FV(q₀)
    FV -- 0,1 --> FW(q₀)
    FW -- 0,1 --> FX(q₀)
    FX -- 0,1 --> FY(q₀)
    FY -- 0,1 --> FZ(q₀)
    FZ -- 0,1 --> GA(q₀)
    GA -- 0,1 --> GB(q₀)
    GB -- 0,1 --> GC(q₀)
    GC -- 0,1 --> GD(q₀)
    GD -- 0,1 --> GE(q₀)
    GE -- 0,1 --> GF(q₀)
    GF -- 0,1 --> GG(q₀)
    GG -- 0,1 --> GH(q₀)
    GH -- 0,1 --> GI(q₀)
    GI -- 0,1 --> GJ(q₀)
    GJ -- 0,1 --> GK(q₀)
    GK -- 0,1 --> GL(q₀)
    GL -- 0,1 --> GM(q₀)
    GM -- 0,1 --> GN(q₀)
    GN -- 0,1 --> GO(q₀)
    GO -- 0,1 --> GP(q₀)
    GP -- 0,1 --> GQ(q₀)
    GQ -- 0,1 --> GR(q₀)
    GR -- 0,1 --> GS(q₀)
    GS -- 0,1 --> GT(q₀)
    GT -- 0,1 --> GU(q₀)
    GU -- 0,1 --> GV(q₀)
    GV -- 0,1 --> GW(q₀)
    GW -- 0,1 --> GX(q₀)
    GX -- 0,1 --> GY(q₀)
    GY -- 0,1 --> GZ(q₀)
    GZ -- 0,1 --> HA(q₀)
    HA -- 0,1 --> HB(q₀)
    HB -- 0,1 --> HC(q₀)
    HC -- 0,1 --> HD(q₀)
    HD -- 0,1 --> HE(q₀)
    HE -- 0,1 --> HF(q₀)
    HF -- 0,1 --> HG(q₀)
    HG -- 0,1 --> HH(q₀)
    HH -- 0,1 --> HI(q₀)
    HI -- 0,1 --> HJ(q₀)
    HJ -- 0,1 --> HK(q₀)
    HK -- 0,1 --> HL(q₀)
    HL -- 0,1 --> HM(q₀)
    HM -- 0,1 --> HN(q₀)
    HN -- 0,1 --> HO(q₀)
    HO -- 0,1 --> HP(q₀)
    HP -- 0,1 --> HQ(q₀)
    HQ -- 0,1 --> HR(q₀)
    HR -- 0,1 --> HS(q₀)
    HS -- 0,1 --> HT(q₀)
    HT -- 0,1 --> HU(q₀)
    HU -- 0,1 --> HV(q₀)
    HV -- 0,1 --> HW(q₀)
    HW -- 0,1 --> HX(q₀)
    HX -- 0,1 --> HY(q₀)
    HY -- 0,1 --> HZ(q₀)
    HZ -- 0,1 --> IA(q₀)
    IA -- 0,1 --> IB(q₀)
    IB -- 0,1 --> IC(q₀)
    IC -- 0,1 --> ID(q₀)
    ID -- 0,1 --> IE(q₀)
    IE -- 0,1 --> IF(q₀)
    IF -- 0,1 --> IG(q₀)
    IG -- 0,1 --> IH(q₀)
    IH -- 0,1 --> II(q₀)
    II -- 0,1 --> IJ(q₀)
    IJ -- 0,1 --> IK(q₀)
    IK -- 0,1 --> IL(q₀)
    IL -- 0,1 --> IM(q₀)
    IM -- 0,1 --> IN(q₀)
    IN -- 0,1 --> IO(q₀)
    IO -- 0,1 --> IP(q₀)
    IP -- 0,1 --> IQ(q₀)
    IQ -- 0,1 --> IR(q₀)
    IR -- 0,1 --> IS(q₀)
    IS -- 0,1 --> IT(q₀)
    IT -- 0,1 --> IU(q₀)
    IU -- 0,1 --> IV(q₀)
    IV -- 0,1 --> IW(q₀)
    IW -- 0,1 --> IX(q₀)
    IX -- 0,1 --> IY(q₀)
    IY -- 0,1 --> IZ(q₀)
    IZ -- 0,1 --> JA(q₀)
    JA -- 0,1 --> JB(q₀)
    JB -- 0,1 --> JC(q₀)
    JC -- 0,1 --> JD(q₀)
    JD -- 0,1 --> JE(q₀)
    JE -- 0,1 --> JF(q₀)
    JF -- 0,1 --> JG(q₀)
    JG -- 0,1 --> JH(q₀)
    JH -- 0,1 --> JJ(q₀)
    JJ -- 0,1 --> JK(q₀)
    JK -- 0,1 --> JL(q₀)
    JL -- 0,1 --> JM(q₀)
    JM -- 0,1 --> JN(q₀)
    JN -- 0,1 --> JO(q₀)
    JO -- 0,1 --> JP(q₀)
    JP -- 0,1 --> JQ(q₀)
    JQ -- 0,1 --> JR(q₀)
    JR -- 0,1 --> JS(q₀)
    JS -- 0,1 --> JT(q₀)
    JT -- 0,1 --> JU(q₀)
    JU -- 0,1 --> JV(q₀)
    JV -- 0,1 --> JW(q₀)
    JW -- 0,1 --> JX(q₀)
    JX -- 0,1 --> JY(q₀)
    JY -- 0,1 --> JZ(q₀)
    JZ -- 0,1 --> KA(q₀)
    KA -- 0,1 --> KB(q₀)
    KB -- 0,1 --> KC(q₀)
    KC -- 0,1 --> KD(q₀)
    KD -- 0,1 --> KE(q₀)
    KE -- 0,1 --> KF(q₀)
    KF -- 0,1 --> KG(q₀)
    KG -- 0,1 --> KH(q₀)
    KH -- 0,1 --> KK(q₀)
    KK -- 0,1 --> KL(q₀)
    KL -- 0,1 --> KM(q₀)
    KM -- 0,1 --> KN(q₀)
    KN -- 0,1 --> KO(q₀)
    KO -- 0,1 --> KP(q₀)
    KP -- 0,1 --> KQ(q₀)
    KQ -- 0,1 --> KR(q₀)
    KR -- 0,1 --> KS(q₀)
    KS -- 0,1 --> KT(q₀)
    KT -- 0,1 --> KU(q₀)
    KU -- 0,1 --> KV(q₀)
    KV -- 0,1 --> KW(q₀)
    KW -- 0,1 --> KX(q₀)
    KX -- 0,1 --> KY(q₀)
    KY -- 0,1 --> KZ(q₀)
    KZ -- 0,1 --> LA(q₀)
    LA -- 0,1 --> LB(q₀)
    LB -- 0,1 --> LC(q₀)
    LC -- 0,1 --> LD(q₀)
    LD -- 0,1 --> LE(q₀)
    LE -- 0,1 --> LF(q₀)
    LF -- 0,1 --> LG(q₀)
    LG -- 0,1 --> LH(q₀)
    LH -- 0,1 --> LI(q₀)
    LI -- 0,1 --> LJ(q₀)
    LJ -- 0,1 --> LK(q₀)
    LK -- 0,1 --> LL(q₀)
    LL -- 0,1 --> LM(q₀)
    LM -- 0,1 --> LN(q₀)
    LN -- 0,1 --> LO(q₀)
    LO -- 0,1 --> LP(q₀)
    LP -- 0,1 --> LQ(q₀)
    LQ -- 0,1 --> LR(q₀)
    LR -- 0,1 --> LS(q₀)
    LS -- 0,1 --> LT(q₀)
    LT -- 0,1 --> LU(q₀)
    LU -- 0,1 --> LV(q₀)
    LV -- 0,1 --> LW(q₀)
    LW -- 0,1 --> LX(q₀)
    LX -- 0,1 --> LY(q₀)
    LY -- 0,1 --> LZ(q₀)
    LZ -- 0,1 --> MA(q₀)
    MA -- 0,1 --> MB(q₀)

---


## Page 44

Auto Mata and Languages

result in the transition to a unique state, but results a chain of states. Let us consider a machine given in figure 3.

For the sake of convenience, let us check the processing of any input symbol. Fromthe state q₀, after processing 0, resulting states are q₀, q₁, q₂ and for input symbol 1, there are three possible states q₀, q₁ and q₂ not a unique state. It clarifies that a non-deterministic automata can have more than one possible state or none state after processing any input symbol from Σ.

Let us check how the string 01 is processed by the above automata. Here we havethree paths to reach to the final state:

(i) q₀ → q₀ → q₂
(ii) q₀ → q₁ → q₂
(iii) q₀ → q₂ → q₂

A generalisation which is obtained here by allowing of several states as a result of the processing of an input symbol is called non-determinism. If from any state, we can reach to several states or none state, then the finite automata becomes non-deterministic in nature.

Formally, a non-deterministic finite automata is a quintuple

A = (Q, Σ , δ , q₀, F)
Where
* Q is a finite set of states
* Σ is a finite alphabet for inputs
* δ is a transition function from Q × Σ to the power set of Q i.e. to 2^Q
* q₀ ∈ Q is the start/initial state
* F ⊆ Q is a set of final/accepting states.

The NFA, for the example just considered, can be formally represented as:
({q₀, q₁, q₂}, {0,1}, δ , q₀, {q₂})

Where the transition function, is given by the Table 1:

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

Table 1: Transition Function
<table>
<thead>
<tr>
<th>States</th>
<th>0</th>
<th>1</th>
</tr>
</thead>
<tbody>
<tr>
<td>→q₀</td>
<td>{q₀,q₁}</td>
<td>{q₀}</td>
</tr>
<tr>
<td>q₁</td>
<td>Ø</td>
<td>{q₂}</td>
</tr>
<tr>
<td>q₂</td>
<td>Ø</td>
<td>Ø</td>
</tr>
</tbody>
</table>

Now, let us prove that the NFA

&lt;page_number&gt;112&lt;/page_number&gt;

---


## Page 45

mermaid
stateDiagram-v2
    [*] --> q0
    q0 --> q1 : 0
    q0 --> q0 : 0, 1
    q1 --> q2 : 1
    q2 --> q0 : 0, 1
```

Set Theory Computability & Complexity

**Fig. 16:** NFA accepting x01

accepts the language {x01 : x ∈ Σ * } of all the strings that terminate with the sub-string 01. A mutual induction on the three statements below proves that the NFA accepts the given language.

1. w ∈ Σ * ⇒ q₀ ∈ δ (q₀,w)
2. q₁ ∈ δ (q₀, w) ⇔ w = x0
3. q₂ ∈ δ (q₀, w) w = x01

If |w| = 0 then w = λ. Then statement (1) follows from def., and statement & (2) and (3) show that all the string x01 will be accepted by the above non-deterministic automata.

**Example 20:** Consider the NFA with the formal description as (Q, Σ ,δ, q₀, F) where Q = {q₀, q₁, q₂}, Σ = {a, b}, q₀ is the initial state and q₁ is only the final state, and δ is given by the following Table 2:

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

**Table 2**

<table>
<thead>
<tr>
<th>State</th>
<th colspan="2">Input from</th>
</tr>
<tr>
<th></th>
<th>a</th>
<th>b</th>
</tr>
</thead>
<tbody>
<tr>
<td>→q₀<br>(q₁)<br>q₂</td>
<td>q₁, q₂<br>q₁<br>q₁</td>
<td>q₀<br>-<br>q₂</td>
</tr>
</tbody>
</table>

In NFA, though the function maps to a sub-set of the set of states, yet we generally drop braces, i.e., instead of {q₀, q₁}, we just write q₀, q₁.

The computation for an NFA is also similar to that of DFA. Let N = (Q, Σ , δ, q₀, F) be an NFA and w is a string over the alphabet Σ. The string w is accepted by NFA if corresponding to the input sequence, there exists a sequence of transitions from the initial state to any of the possible final states.

Now, let us check computations (in NFA, there are many possible computations) of the string aba.

δ (q₀, aba) = δ(δ(q₀, a), ba)

= δ (q₁, ba) or δ (q₂, ba)

= δ (δ (q₁, b), a) or δ (δ (q₂, b), a)

= stuck or δ (q₂, a)

= q₁ (an accepting state)

&lt;page_number&gt;113&lt;/page_number&gt;

---


## Page 46

Auto Mata and Languages

The above sequence of states shows the final state q₁ which is an accepting state.
Hence, the string aba is accepted by the system and the input sequence of states for the input is
<mermaid>
graph LR
    A(q₀) -->|a| B(q₂)
    B -->|b| C(q₂)
    C -->|a| D(q₁)
</mermaid>

Try some exercises:

Ex.13) Consider an NFA given in Figure 17. Check whether the strings 001, 011101, 01110, 010 are accepted by the machine, or not?

<mermaid>
graph LR
    subgraph Fig. 17: Non Deterministic Finite Automata
        A0((q₀)) -- "0,1" --> A1((q₁))
        A1 -- "0" --> A2((q₂))
        A2 -- "1" --> A3((q₃))
    end
</mermaid>

Ex.14) Give an NFA which accepts all the strings starting with ab over {a,b}.

## 2.6 SUMMARY

In this unit we introduced the concepts of languages, regular expressions and regular langyages. Finite Automata are machines that recognize regular languages. From regular expressions, we can derive regular languages. In deterministic finite automata (DFA), there is a unique next state for transition on input in a given state. If we relax this condition of uniqueness of the next state in DFA, we get NFA.

## 2.7 SOLUTION/ANSWERS

Ex.1) (i) ababbbaa
(ii) baaababb
(iii) ab abb ab abb
(iv) baa baa
(v) ababbababb baa

Ex.2) (i) Suppose aa = x

Then { x, b } * = { λ , x, b, xx, bb, xb, bx, xxx, bxx, xbx, xxb, bbx, bxb, xbb, bbb }
substituting x = aa
{ aa,b } * = { λ , aa, b, aaaa, bb, aab, baa, aaaaaa, baaaa, aabaa, ... }

(ii) { a,ba } * = { λ , a, ba, aa, baba, aba, baa, ... }

Ex.3) (a) a+b+c

(b) ab * +ba *

(c) λ+a(bb) *

Ex.4) 0+1(0+1) *

Ex.5) Starting with the left side and using properties of regular expressions, we get

b * (abb * + aabb * +aaabb *)
= b * ((ab+aab+aaab)b *) * (property 9)
= (b + ab + aab + aaab) * (property 7).

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;114&lt;/page_number&gt;

---


## Page 47

Set Theory Computability & Complexity

Ex.6) (a) {a,b}
(b) {a, λ,b,bb,...b^n,...}
(c) {a,b,ab,bc,abb,bcc,...ab^n,bc^n,...}

Ex.7) (a) (aa+ab+ba+bb)*
(b) (a+b)*aba(a+b)*

Ex.8)

<mermaid>
graph LR
    q0 -->|a| q1
    q0 -->|b| q1
    q1 -->|a,b| q1
</mermaid>

Fig. 18: Regular Expression of a null string

Ex.9)

<mermaid>
graph LR
    subgraph Top Row
        A(( )) -- a --> B(( ))
        B(( )) -- b --> C(( ))
        C(( )) -- a --> D(( ))
    end

    subgraph Bottom Row
        E(( )) -- b --> F(( ))
        F(( )) -- a --> G(( ))
        G(( )) -- b --> H(( ))
        H(( )) -- a --> I(( ))
    end

    A --- E
    C --- G
    D --- H
    I --- B
</mermaid>

Fig. 19: Regular Expression is (aa+ba+ab+bb)

Ex.10) R.E. is (baa + ab + abb)

Ex.11) (i) All the words of odd lengths.
(ii) All the words ended with a.
(iii) All the words with a at even places.

Ex.12) is given by

<table>
<thead>
<tr>
<th>State</th>
<th colspan="2">Input</th>
</tr>
<tr>
<td></td>
<td>0</td>
<td>1</td>
</tr>
</thead>
<tbody>
<tr>
<td>q₀</td>
<td>q₀, q₁</td>
<td>q₀</td>
</tr>
<tr>
<td>q₁</td>
<td>-</td>
<td>-</td>
</tr>
<tr>
<td>q²</td>
<td>-</td>
<td>-</td>
</tr>
</tbody>
</table>

δ(q₀, 001) = δ (q₀, 01) = δ (q₁, 1) = q₂(Accepting state)
δ (q₀, 011101) = δ (q₀, 11101)
= δ (q₀, 1101)

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;115&lt;/page_number&gt;

---


## Page 48

Auto Mata and Languages

= δ (q₀, 101)
= δ (q₀, 01)
= δ (q₀, 1)
= q₂ (accepting state)
δ (q₀, 01110) = δ (q₀, 1110)
= δ (q₀, 110)
= δ (q₀, 10)
= δ (q₀, 0)
= q₀ or q₁ (Not an accepting state)
δ (q₀, 010) = δ (q₀, 10)
= δ (q₀, 0)
= q₀ or q₁ (Not an accepting state)

So, strings 001 and 011101 are accepted by the given automata.

Ex.13)

<mermaid>
graph LR
    A(( )) -- a --> B(( ))
    B -- b --> C(( ))
    C -- "a.b" --> C
</mermaid>

Fig. 20

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;116&lt;/page_number&gt;

---


## Page 49

# UNIT 3 COMPUTABILITY AND COMPLEXITY

## Structure

*   3.0 Introduction
*   3.1 Objectives
*   3.2 Turing Machine
*   3.3 Nondeterministic Turing Machine
*   3.4 Undecidable and Halting Problems
*   3.5 Complexity
*   3.6 Summary
*   3.7 Solutions/ Answers

## 3.0 INTRODUCTION

Every system—natural or man-made, must be continuously, involved in some form of computation in its attempt at preserving its identity as a system.

In the previous unit, we discussed two major approaches to modeling of computation viz. the automata/machine approach and linguistic/grammatical approach. Under the automata approach, we discussed two models viz. Finite Automata and Nondeterministic Finite Automata. Under grammatical approach, we discussed only one model viz Regular Languages. We stated that the Finite Automata is a computational model which is equivalent to Regular Language Model and differentiated between a Deterministic Finite Automata and Nondeterministic Finite Automata.

In this unit we discuss a computational model called Turing Machine(TM) which is more powerful in terms of recognizing more languages and will help us define and understand complexity classes.

Turing Machine is named so, in Honor of its inventor Alan Mathison Turing (1921-1954). A.M. Turing, a British, was one of the greatest scholars of the twentieth century, and made profound contributions to the foundations of computer science.

We make an introduction to the concepts of a simple Turing Machine and Nondeterministic TM. Many notations and keywords are used to discuss the topics which are listed below:

**Key words:** Turing Machine (TM), Deterministic Turing Machine, Non-Deterministic Turing Machine, Turing Thesis, Computation, Configuration of TM, Turing-Acceptable Language, Turing DecidableLanguage,

**Notations**

<table>
<tr><td>TM</td><td>:</td><td>Turing Machine</td></tr>
<tr><td>$\Gamma$</td><td>:</td><td>Set of tape symbols, includes #, the blank symbol</td></tr>
<tr><td>$\Sigma$</td><td>:</td><td>Set of input/machine symbols, does not include #</td></tr>
<tr><td>Q</td><td>:</td><td>the finite set of states of TM</td></tr>
<tr><td>F</td><td>:</td><td>Set of final states</td></tr>
<tr><td>a,b,c...</td><td>:</td><td>Members of</td></tr>
<tr><td>$\sigma$</td><td>:</td><td>Variable for members of $\Sigma$</td></tr>
<tr><td>x or x</td><td>:</td><td>Any symbol of other than x</td></tr>
</table>

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;117&lt;/page_number&gt;

---


## Page 50

Computability
and Complexity

# : The blank symbol
α,β,γ : Variables for String over
L : Move the Head to the Left
R : Move the Head to the Right q : A state of TM, i.e, q ε Q
s or q₀ : The start/initial state

Halt or h: The halt state. The same symbol h is used for the purpose of denoting halt state for all halt state versions of TM. And then h is not used for other purposes.
e or ε : The empty string
C₁ ⊢<sub>M</sub> C₂: Configuration C₂ is obtained from configuration C₁ in one moveOf the machine M
C₁ ⊢*<sub>M</sub> C₂: Configuration C₂ is obtained from configuration C₁ in finite numberof moves.

w₁ a w₂: The symbol a is the symbol currently being scanned by the Head
Or
w₁ a w₂: The symbol a is the symbol currently being scanned by the Head ↑

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

## 3.1 OBJECTIVES

After going through this unit, you should be able to:

*   Define all the terms listed under the keywords
*   Illustrate a basic Turing machine.
*   Explain the symbols used in a Turing Machine
*   Explain the operations of a Turing Machine
*   Differentiate between TM and NDTM
*   Define Complexity Classes: P and NP

## PRELUDE TO FORMAL DEFINITION

In the next section, we will notice through a formal definition of TM that a TM is an abstract entity constituted of mathematical objects like sets and a (partial) function. However, in order to help our understanding of the subject-matter of TMs, we can visualize a TM as a physical computing device that can be represented as a diagram as shown in below.

&lt;page_number&gt;118&lt;/page_number&gt;

---


## Page 51

Set theory, Computability
and Complexity

Infinite Tape
<table>
  <tr>
    <td>d</td>
    <td>a</td>
    <td>b</td>
    <td>#</td>
    <td>c</td>
    <td>b</td>
    <td>.....</td>
    <td>.....</td>
    <td>.....</td>
  </tr>
</table>

&lt;img&gt;A diagram showing a Turing Machine. It has a tape with symbols d, a, b, #, c, b, .... on it. A read/write head is positioned over the tape. The head has arrows indicating it can move left or right. Below the head is a box labeled "Finite Control".&lt;/img&gt;

**Fig. 3.1: Turing Machine**

As shown in the above figure, TM consists of

(i) **a tape**, with an end on the left but infinite on the right side. The tape is divided into squares or cells, with each cell capable of holding one of the tape symbols including the blank symbol #. At any time, there can be only finitely many cells of the tape that can contain non-blank symbols. The set of **tape symbols** is denoted by

As the very first step in the sequence of operations of a TM, **the input**, as a **finite sequence of the input symbols** is placed in the **left-most cells of the tape**. The set of **input symbols** denoted by Σ, does not contain the blank symbol #. However, during operations of a TM, a cell may contain a **tape symbol** which is not necessarily an input symbol.
*There are versions of TM, to be discussed later, in which the tape may be infinite in both left and right sides having neither left end nor right end.*

(ii) **a finite control**, which can be in any one of the finite number of states. The states in TM can be divided in three categories viz.

(a) the Initial state, the state of the control just at the time when TM starts its operations. The initial state of a TM is generally denoted by q₀ or s.
(b) the Halt state, which is the state in which TM stops all further operations. The halt state is generally denoted by h. The halt state is distinct from the initial state. Thus, a TM HAS AT LEAST TWO STATES.
(c) Other states

(iii) **a tape head** (or simply *Head*), is always stationed at one of the tape cells and provides communication for interaction between the tape and the finite control. The Head can read or scan the symbol in the cell under it. The symbol is communicated to the finite control. The control taking into consideration the symbol and its current state decides for further course of action including the change of the symbol in the cell being scanned and/or change of its state and/or moving the head to the Left or to the Right. The control may decide not to move the head.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;119&lt;/page_number&gt;

---


## Page 52

Computability
and Complexity

The course of action is called a move of the Turing Machine. In other words, the move is a function of current state of the control and the tape symbol being scanned.

In case the control decides for change of the symbol in the cell being scanned, then the change is carried out by the head. This change of symbol in the cell being scanned is called writing of the cell by the head.

**Initially, the head scans the left-most cell of the tape.**

Now, we are ready to consider a **formal definition** of a Turing Machine in the next section.

---

# 3.2 TURING MACHINE

---

## 3.2.1 Turing Machine: Formal Definition

There are a number of versions of a TM. We consider below Halt State version of formal definition of a TM.

**Definition: Turing Machine (Halt State Version)**
A Turing Machine is a sextuple of the form (Q, Σ, Γ, δ, q₀, h), where

(i) Q is the finite set of states,
(ii) Σ is the finite set of non-blank information symbols,
(iii) Γ is the set of tape symbols, including the blank symbol #,
(iv) δ is the **next-move** partial function from Q x Γ to Q x Γ x {L, R, N},
where ‘L’ denotes the tape Head moves to the left adjacent cell, ‘R’ denotes tape Head moves to the Right adjacent cell and ‘N’ denotes Head does not move, i.e., continues scanning the same cell.

In other words, for qᵢ ∈ Q and aₖ ∈ Γ, there exists (not necessarily always, Because δ is a partial function) some qⱼ ∈ Q and some aⱼ ∈ Γ such that δ(qᵢaₖ) = (qⱼ, aⱼ, x), where x may assume any one of the values ‘L’, ‘R’ and ‘N’.

The meaning of δ(qᵢ, aₖ) = (qⱼ, aⱼ, x) is that if qᵢ is the current state of the TM, and aₖ is cell currently under the Head, then TM writes aⱼ in the cell currently under the Head, enters the state qⱼ and the *Head moves to the right adjacent cell, if the value of x is R, Head moves to the left adjacent cell, if the value of x is L* and continues scanning the same cell, if the value of x is N.

(v) q₀ ∈ Q, is the initial/start state.
(vi) h ∈ Q is the ‘Halt State’, in which the machine stops any further activity.

In order to illustrate the ideas involved, let us consider the following simple examples.

&lt;watermark&gt;GOVERNMENT UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;120&lt;/page_number&gt;

---


## Page 53

Set theory, Computability
and Complexity

**Example 1**

Consider the Turing Machine (Q,Σ , Γ , δ , qo, h) defined below that erases all the non-blank symbols on the tape, where the sequence of non-blank symbols does not contain any blank symbol # in-between:

Q= {qo, h} Σ= {a, b}, Γ = {a, b, #}

*and the next-move function is defined by the following table:*

<table>
<thead>
<tr>
<th>q: State</th>
<th>σ: Input Symbol</th>
<th>δ (q, σ)</th>
</tr>
</thead>
<tbody>
<tr>
<td></td>
<td></td>
<td>Type equation here.</td>
</tr>
<tr>
<td></td>
<td></td>
<td>)</td>
</tr>
<tr>
<td>q0</td>
<td>A</td>
<td>{q0, #, R}</td>
</tr>
<tr>
<td>q0</td>
<td>B</td>
<td>{q0, #, R}</td>
</tr>
<tr>
<td>q0</td>
<td>#</td>
<td>{h, #, N}</td>
</tr>
<tr>
<td>H</td>
<td>#</td>
<td>ACCEPT</td>
</tr>
</tbody>
</table>

Next, we consider how to design a Turing Machine to accomplish some computational task through the following example. For this purpose, we need the definition.

**A string Accepted by a TM**

A string over is said to be accepted by a TM M = (Q, Σ, Γ, δ, qo, h) **if** when the string is placed in the left-most cells on the tape of M and TM is started in the initial state qo then after a finite number of moves of the TM as determined by δ, TM is in state h (and hence stops any further operations. Further, a string is said to be rejected if under the conditions mentioned above, the TM enters a state q ≠ h .

**3.2.2 Instantaneous Description And Transition Diagrams**

**Instantaneous Description**

Some authors use the term *Instantaneous Description* instead of *Total Configuration*.

**Initial Configuration:** The total configuration at the start of the (Turing) Machine is called the initial configuration.

**Halted Configuration:** is a configuration whose state component is the Halt state There are various notations used for denoting the total configuration of a Turing Machine.

**Notation 1:** We use the notations, illustrated below through an example:

Let the TM be in state q₃ scanning the symbol g with the symbols on the tape as follows:

<table>
<tbody>
<tr>
<td>#</td>
<td>#</td>
<td>b</td>
<td>D</td>
<td>a</td>
<td>f</td>
<td>#</td>
<td>G</td>
<td>h</td>
<td>K</td>
<td>#</td>
<td>#</td>
<td>#</td>
<td>#</td>
</tr>
</tbody>
</table>

Then one of the notations is

<table>
<tbody>
<tr>
<td>#</td>
<td>#</td>
<td>b</td>
<td>D</td>
<td>a</td>
<td>f</td>
<td>#</td>
<td>g</td>
<td>h</td>
<td>k</td>
<td>#</td>
<td>#</td>
<td>#</td>
<td>#</td>
</tr>
</tbody>
</table>
&lt;img&gt;q₃&lt;/img&gt;

&lt;page_number&gt;121&lt;/page_number&gt;

---


## Page 54

Computability
and Complexity

**Notation 2:** However, the above being a two-dimensional notation, is sometimes inconvenient. Therefore the following linear notations are frequently used: (q₃, ##bdaf#, g,hk), in which third component of the above 4-component vector, contains the symbol being scanned by the tape head.

Alternatively, the configuration is also denoted by (q₃,## bdaf#ghk), where the symbol under the tape head is underscored but two last commas are dropped.

It may be noted that the sequence of blanks after the last non-blank symbol, is not shown in the configuration. The notation may be alternatively written (q₃, w, g, u) where w is the string to the left and u the string to the right respectively of the symbol that is currently being scanned.

In case g is the left-most symbol then we use the empty string e instead of w. Similarly, if g is being currently scanned and there is no non-blank character to the right of g then we use e, the empty string instead of u.

**Notation 3:** The next notation neither uses parentheses nor commas. Here the state is written just to the left of the symbol currently being scanned by the tape Head. Thus the configuration (q₃, ##bdaf#, g, h, k) is denoted as ## bdaf#q₃ghk

Thus if the tape is like

<table>
<tr><td>g</td><td>w</td><td>#</td><td>...........</td></tr>
</table>
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;watermark&gt;GJOU&lt;/watermark&gt;

q₅

then we may denote the corresponding configuration as (q₅, e, g, u). And, if the tape is like

<table>
<tr><td>A</td><td>b</td><td>c</td><td>g</td><td>#</td><td>#</td><td>...</td></tr>
</table>

q₆

Then the configuration is (q₆, abc, g, e) or (q₆, abcg) or alternatively as abcq₆g by the following notation.

### 3.2.3 Transition Diagrams

In some situations, graphical representation of the next-move (partial) function δ of a Turing Machine may give better idea of the behavior of a TM in comparison to the tabular representation of δ.

A **Transition Diagram** of the next-move functions δ of a TM is a graphical representation consisting of a finite number of nodes and (directed) labelled arcs between the nodes. Each node represents a state of the TM and a label on an arc from one state (say p) to a state (say q) represents the information about the required input symbol say x for the transition from p to q to take place and the action on the part of the control of the TM. The action part consists of (i) the symbol say y to be written in the current cell and (ii) the movement of the tape Head.

&lt;page_number&gt;122&lt;/page_number&gt;

---


## Page 55

Set theory, Computability and Complexity

Then the label of an arc is generally written as x/(y, M) where M is L, R or N.

**Example 2**

Let M = {Q, Σ, Γ, δ, q₀, h}
Where
Q = {q₀, q₁, q₂, h}
Σ = {0, 1}
Γ = {0, 1, #}
and δ be given by the following table.

<table>
<thead>
<tr>
<th></th>
<th>0</th>
<th>1</th>
<th>#</th>
</tr>
</thead>
<tbody>
<tr>
<td>q₀</td>
<td>-</td>
<td>-</td>
<td>(q₂, #, R)</td>
</tr>
<tr>
<td>q₁</td>
<td>(q₂, 0, R)</td>
<td>(q₁, #, R)</td>
<td>(h, #, N)</td>
</tr>
<tr>
<td>q₂</td>
<td>(q₂, 0, L)</td>
<td>(q₁, 1, R)</td>
<td>(h, #, N)</td>
</tr>
<tr>
<td>H</td>
<td>-</td>
<td>-</td>
<td>-</td>
</tr>
</tbody>
</table>

Then, the above Turing Machine may be denoted by the Transition Diagram shown below, where we assume that q₀ is the initial state and h is a final state.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;A transition diagram showing three states: q₀, q₁, and h. Arrows indicate transitions:
- From q₀ to q₁ with label 1/1, R.
- From q₀ to q₂ with label #/#, R.
- From q₁ to q₂ with label 0/0, R.
- From q₁ to h with label #/#, N.
- From q₂ to q₁ with label 0/0, L.
- From q₂ to h with label 1/#, R.&lt;/img&gt;

Fig. 3.2: Transition Diagram

## 3.2.4 Some Formal Definitions

L(M), the language accepted by the TM M is the set of all finite strings over which are accepted by M.

### Definition: Turing Acceptable Language

A language L over some alphabet is said to be Turing Acceptable Language, if there exists a Turing Machine M such that L = L (M)

### Definition: Turing Decidable Language

A language over some alphabet is said to be Turing acceptable language if there exists a Turing Machine M such that L= L(M) and M halts on every input.

Remark 3.5.1

&lt;page_number&gt;123&lt;/page_number&gt;

---


## Page 56

Computability
and Complexity

A very important fact in respect of Turing acceptability of a string (or a language) needs our attention. The fact has been discussed in very brief in a later section about undecidability. However, we briefly mention it below.

**For a TM M and an input string w ∈ Σ\*, even after a large number of moves we may not reach the halt state. However, from this we can neither conclude that ‘Halt state will be reached in a finite number of moves’ nor can we conclude that Halt state will not be reached in a finite number moves.**

This raises the question of how to decide that an input string w is not accepted by a TM M.

An input string w is said to be ‘not accepted’ by a TM M = (Q, Σ, Γ, δ, q₀, h) if any of the following three cases arise:

(i) There is a configuration of M for which there is no next move i.e., there may be a state and a symbol under the tape head, for which δ does not have a value.

(ii) The tape Head is scanning the left-most cell containing the symbol x and the state of M is say q and δ (x, q) suggests a move to the ‘left’ of the current cell. However, there is no cell to the left of the left-most cell. Therefore, move is not possible. The potentially resulting situation (can’t say exactly configuration) is called **Hanging configuration.**

(iii) The TM on the given input w enters an infinite loop. For example if configuration is as

<mermaid>
graph TD
    subgraph Tape
        direction LR
        A[x] --- B[y]
    end
    C[q₀] --> A
</mermaid>

and we are given
δ (q₀, x) = (q₁, x, R)
and δ (q₁, y) = (q₀, y, L)
Then we are in an **infinite loop.**

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

### 3.2.5 OBSERVATIONS

The concept of TM is one of the most important concepts in the theory of Computation. In view of its significance, we discuss a number of issues in respect of TMs through the following remark:

Turing Machine is not just another computational model, which may be further extended by another still more powerful computational model. It is not only the most powerful computational model known so far but also is conjectured to be the ultimate computational model. In this regard, we state below the

**Turing Thesis:** *The power of any computational process is captured within the class of Turing Machines.*

It may be noted that Turing thesis is just a **conjecture and not a theorem, hence, Turing Thesis** can not be logically deduced from more elementary facts. However, the conjecture can be shown to be false, if a more powerful computational model is proposed that can recognize all the languages which are recognized by the TM model and also recognizes at least one more language that is not recognized by any TM. In view of the unsuccessful efforts made in this direction since 1936, when Turing suggested his model, at least at present, it seems to be unlikely to have a more powerful computational model than TM Model.

&lt;page_number&gt;124&lt;/page_number&gt;

---


## Page 57

Set theory, Computability and Complexity

# Check Your Progress-1

Q1 What is the meaning of the following symbols:

(i) Q
(ii) Σ
(iii) Γ
(iv) δ

Q2 Explain what is a Turing Machine?

Q3 How TM is different from Finite Automata?

---

## 3.3 NONDETERMINISTIC TURING MACHINE

Like nondeterministic finite automata, we can also imagine nondeterministic TM (NDTM). An NDTM is like the standard TM with the difference as described below.
In Standard TM, to each pair of the current state (except the halt state) and the symbol being scanned, there is a unique triplet comprising of the next state, unique action in terms of writing a symbol in the cell being scanned and the motion, if any, to the right or left. However, in the case NDTM, to each pair (q, s) with q as current state and s as symbol being scanned, there may be a finite set of the triplets { (q<sub>i</sub>, s<sub>i</sub>, m<sub>i</sub>) : i = 1,2,…… } of possible next moves. This set of triplets may be empty, i.e. for some particular (q,s) the TM may not have any next move. Or alternatively the set {(q<sub>i</sub>, s<sub>i</sub>, m<sub>i</sub>)} may have more than one triplet, meaning thereby that the NDTM in the state q and scanning symbols s, has the alternatives for next move to choose from the set {(q<sub>i</sub>, s<sub>i</sub>, m<sub>i</sub>)} of next moves.

It can be easily seen that standard TM is a special case of the NDTM in which for each (q,s) the set {(q<sub>i</sub>, s<sub>i</sub>, m<sub>i</sub>)} of next moves is a singleton set or empty.

In order to define formally the concept of Non-Deterministic TM (NDTM), and a configuration in NDTM etc, we assume that the tape is one-way infinite.

For the extensions of the standard TM, discussed so far, we did not state the full formal definition of each of the extension. We only discussed the definition only relative to the standard TM. Mainly we discussed configurations and partial move function δ for each of the extensions. However, in view of the significant though small, difference in the behaviour of an NDTMs, we provide below full formal definition of NDTM.

**Remark 1:**

An important point about the definition of NDTM needs to the highlighted. By the definition of δ which maps an element of (q, x) of Q x Γ to a set {(q<sub>i</sub>, x<sub>i</sub>, M<sub>i</sub>)} means that each element (q, x) of Q x Γ has the potential of leading to more than one configurations. In other words, there are various possible routes to a final configuration from one configuration. However, during one computation only one of these possible values (q<sub>i</sub>, x<sub>i</sub>, M<sub>i</sub>) will be associated with (q, x) through δ. But we can not tell in advance which one out of the ordered triples from the set {(q<sub>i</sub>, x<sub>i</sub>, M<sub>i</sub>)}.

This is why the adjective Non-Deterministic is used for this version of the T.M.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;125&lt;/page_number&gt;

---


## Page 58

Computability
and Complexity

**Remark 2:**

The set {(q<sub>i</sub>, x<sub>i</sub>, M<sub>i</sub>)} associated with (q, x) under δ, may be empty. This means there is no possible next move for (q, x), a situation that occurred even in the case of standard TM and other versions discussed so far. This is why δ was called a **partial function** from Q x Γ to Q x Γ x {L,R,N}.

**Remark 3:**

In the standard TM and the versions discussed before NDTM, we allowed δ as a partial function to Q x Γ x {L, R, N}. In other words, if a value under δ exists for (q, x) then the value has to be unique, i.e., can be determined. Therefore, the earlier versions are prefixed with the adjective *Deterministic*. The Non- Deterministic form of each of the earlier versions can be obtained by making suitable modifications in the corresponding definitions of δ etc on the lines of modifications suggested in the definition of NDTM from standard TM.

**Remark 4:**

Proper non-determinism means that at some stage, there are at least two next possible moves. Now, if we are engage two different persons or machines to work out further possible moves according to each of these two moves, the two can work independent of each other. **This means Non-Determination allows parallel computations.** This characteristic of Non-Determinism, also allows is further computations even if some of the sequences of moves may be locked as there may not be any next moves at some stages.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

**Definition:** An **Non-Deterministic Turing Machine** is a sextuple (Q, Σ, Γ, q<sub>0</sub>, h) where
Q: Set of States
Σ: Set of input symbols
Γ: Set of tape symbols
q<sub>0</sub>: The initial state
h: The halt state and
δ: Q x Γ → Power set of (Q x Γ x {L, R, N})

*The concept of a configuration is same as in the case of standard TM. But the concept of ‘yields in one step’ denoted by |<u>m</u> , has different meaning. Here one configuration may yield more than one configurations.*

*We explain these ideas through a suitable example, which also demonstrates the advantage of the Non- Deterministic Turing Machine over the standard Turing Machine. The advantage is in respect of the relative ease of construction of NDTM.*

**Remarks 5**

Before coming to the example, showing advantage of an NDTM in solving some problems; we need to understand properly the concept of acceptance of a language by an NDTM. First of all, let us recall below what is meant by acceptance of a language L by a standard TM M.

*A language L is accepted by a TM M if each string α ∈ L, is acceptable by M.*
Further a string α is acceptable M, if staring in the initial state q<sub>0</sub> of M, with α as input on the tape of M, if we are able to reach halt state in a finite number of moves,

&lt;page_number&gt;126&lt;/page_number&gt;

---


## Page 59

Set theory, Computability
and Complexity

A characteristic feature of the **standard TM**, in this case, is that if there is to be a sequence of moves from (q₀, α)to a final state, than that sequence might the unique.
However in the case of **Non-Deterministic machines**, the halt state may be reached through any one of various permissible sequences of moves. Therefore in this version a string α over the set of input symbols of an NDTM is acceptable by an NDTM M, if **by at least one but by any one** of the sequences of moves halt state is reached from (q₀, α). Now we discuss the example showing advantage of NDTM over standard TM.

**Example 1:**

Construct an NDTM which accepts the language { aⁿ bᵐ : n≥1, m ≥1}, i.e., the language of all strings over {a,b}, in which there is at least one a and one b and all a's precede all b's.

Solution: The diagrammatic representation of the required NDTM is as given below:

In the proposed NDTM, as the motion of the head is always to the Right except in the Halt state. Therefore, R is not mentioned in the labels in the diagram below:
<mermaid>
graph LR
    subgraph Diagram
        q0(q₀)
        q1(q₁)
        h(h)
    end

    q0 -->|a/a| q1
    q1 -->|b/b| h
    q1 -->|b/b| q0
</mermaid>

where the label i/j on an arc denotes that if symbol in the current cell is i then contents of the cell are to be replaced by j.
Formally the proposed NDTM may be defined as
M={ {q₀, q₁, h}, {a, b}, { a, b, #}, δ, q₀ , h }
Where δ is defined as follows:
δ (q₀, a)= {( q₀, a, R), (q₁, a, R)}
δ (q₀, b)= empty
δ (q₁, a)= empty
δ (q₁, b)= {(q₁, b, R), (h, b, N)}
If the machine has no next move, then it halts without accepting the string.

**Remarks 6:**

Though we have already mentioned earlier on a number occasions, yet, in view of the significance of non-determinism in designing TMs comparatively more easily, we again bring to notice that in the state q₀ on scanning symbol a, the TM may move in any one of the two next possible states viz to q₀ after moving the head to the right or to q₁ (after moving the head to the right). And, if the TM is implemented as a parallel computer then the computer can presume independently both branches initiated by (q₀,a,R) and (q₁,a,R)

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;127&lt;/page_number&gt;

---


## Page 60

Computability
and Complexity

# 3.4 UNDECIDABLE AND HALTING PROBLEMS

## UNDECIDABLE PROBLEM

A function g with domain D is said to be computable if there exists some Turing machine whose initial configuration is q0 w, i.e., the left-most symbol of the string w being scanned in state q0 and whose final configuration is q f g(w) for some final state qf , i.e., when the machine halts the only non-blank cells on the tape represent the function value g(w).

A function is said to be un-computable if no such machine exists. There may be a Turing machine that can compute f on part of its domain, but we call the function computable only if there is a Turing machine that computes the function on the whole of its domain.

For some problems, we are interested in simpler solution in terms of “yes” or “no”. We say that a problem is decidable if there exists a Turing machine that gives the correct answer for every statement in the domain of the problem.

A class of problems with two outputs “yes” or “no” is said to be decidable (solvable) if there exists some definite algorithm which always terminates (halts) with one of two outputs “yes” or “no”. Otherwise, the class of problems is said to be undecidable (unsolvable).

&lt;watermark&gt;INSTITUTE OF TECHNOLOGY UNIVERSITY&lt;/watermark&gt;

## THE HALTING PROBLEM

There are many problems which are not computable. But, we start with a problem which is important and that at the same time gives us a platform for developing later results. One such problem is the halting problem. Algorithms may contain loops that may be infinite or finite in length. The amount of work done in an algorithm usually depends on the data input. Algorithms may consist of various numbers of loops, nested or in sequence. Informally, the **Halting problem** can be put as:

**Given a Turing machine M and an input w to the machine M, determine if the machine M will eventually halt when it is given input w.**

Trial solution: Just run the machine M with the given input w.
*   If the machine M halts, we know the machine halts.
*   But if the machine doesn't halt in a reasonable amount of time, we cannot conclude that it won't halt. Maybe we didn't wait long enough.

What we need is an algorithm that can determine the correct answer for any M and w by performing some analysis on the machine's description and the input. But, it is shown by Alan Turing that no such algorithm exists.

&lt;page_number&gt;128&lt;/page_number&gt;

---


## Page 61

Set theory, Computability
and Complexity

# 3.5 COMPLEXITY

In the previous unit, we introduced you to the fact that there are a large number of problems which cannot be solved by algorithmic means and discussed a number of issues about such problems.

The advantage of such a study is our becoming aware of the fact that instead of attempting to write an algorithm for every problem that we are required to solve using a computer, we should first study the essential nature of the problem. In case the problem under consideration is not solvable by algorithmic means, we may adopt other computational techniques including use of heuristics, numerical and/or statistical techniques. Even out of problems, which though theoretically have algorithmic solutions, yet require such large amount of resources, that this type of problems are designated as *infeasible* for the purpose of computational solution. Out of the problems, which are *feasibly* solvable, there are problems each of which may have more than one algorithms to solve the problem. For us, it is desirable to know which one is better among the available ones. For example, we can use the algorithms viz, Bubble sort, Insertion sort, Heapsort and Quicksort, for sorting a list of numbers. Their designs are different but the outcome is the same for all, for a given list of numbers. As, there are more than one algorithms available to us to sort a list of numbers, it is natural for us to think of using the algorithm which solves a particular sorting problem, in some way better than the others. In context of practical disciplines like computer applications, an *efficient* solution is generally taken as a *better* solution. Efficiency of an algorithm can be considered in terms of the efficient use of computer resources, such as processor time and memory space used. In addition to the efficiency of execution of algorithms, other factors like time (taken by a team of software engineers and/or programmers) *required for developing algorithms* and *reliability* may also be taken into consideration as factors towards overall efficiency of an algorithm.

However, most of the time, in respect of efficiency of algorithms, we are only concerned with the time and space requirements of execution of algorithms.

In this unit, we will discuss the issue of efficiency of computation of an algorithm in terms of the *amount of time* used in its execution. On the basis of analysis of an algorithm, the amount of time that is estimated to be required in executing an algorithm, will be referred to as the **time complexity** of the algorithm. The time complexity of an algorithm is measured in terms of some (basic) **time unit** (not second or nano-second). Generally, time taken in executing one move of a TM, is taken as (basic) time unit for the purpose. or, alternatively, time taken in executing some elementary operation like addition, is taken as one unit. More complex operations like multiplication etc, are assumed to require an integral number of basic units. As mentioned earlier, given many algorithms (solutions) for solving a problem, we would like to choose the most efficient algorithm from amongst the available ones. For comparing efficiencies of algorithms, that solve a particular problem, time complexities of algorithms are considered as functions of the sizes of the problems (to be discussed). The *time complexity functions of the algorithms are compared in terms of their growth rates* (to be defined) as growth rates are considered important measures of comparative efficiencies.

&lt;watermark&gt;UNIVERSITY OF PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;129&lt;/page_number&gt;

---


## Page 62

Computability
and Complexity

The concept of the size of a problem, though a fundamental one, yet is difficult to define precisely. Generally, the size of a problem, is measured in terms of the size of the *input*. The concept of the size of an input of a problem may be explained informally through examples. In the case of multiplication of two nxn (squares) matrices, the size of the problem may be taken as n², i.e, the number of elements in each matrix to be multiplied. For problems involving polynomials, the degrees of the polynomials may be taken as measure of the sizes of the problems.

Also, we may have an intuitive idea about the term **growth rate** and its significance in the comparative study of algorithms that can be designed to solve problems. For the time being, in stead of attempting a formal definition, we illustrate the concept of *growth rate of time complexity function* of an algorithm and its significance through the following example.

Let us consider two algorithms to solve a problem P, having time-complexities respectively as f₁(n) = 1000n² and f₂(n) = 5n⁴, where size of the problem is assumed to be n. Then

f₁ (n) ≥ f₂ (n) for n ≤ 14 and
f₁ (n) ≤ f₂ (n) for n ≥ 15.

Also, the increase in the ratio (f₂ (n)/f₁ (n)) is faster than increase in n. Thus, informally, growth rate of f₂ (n) is more than the growth rate of f₁ (n). In one sense, the algorithm having time complexity f₂ (n) is *inferior* to the algorithm having time complexity f₁(n) as growth rate of f₂(n) is faster than that of f₁ (n).

For a problem, a solution with time complexity which can be expressed as a polynomial of the size of the problem, is considered to have an **efficient solution**. Unfortunately, not many problems that arise in practice, admit any efficient algorithms, as these problems can be solved, if at all, by only non-polynomial time algorithms. A problem which does not have any (known) polynomial time algorithm is called an **intractable problem**.

At this stage, it is important to be aware of the following relevant facts

(i) A **non-polynomial function need not always be exponential**: For example, the function f(n) = nlog₂ n is neither polynomial function nor exponential function of n, but, somewhere between the two but n^log_2(n) is a polynomial function

(ii) The term *solution* in its general form: need not be an algorithm. If by tossing a coin, we get the correct answer to each instance of a problem, then the process of tossing the coin and getting answers constitutes a solution. But, the process is not an algorithm. Similarly, we solve problems based on **heuristics**, i.e, good guesses which, generally but not necessarily always, lead to solutions. All such cases of solutions are not algorithms, or algorithmic solutions. To be more explicit, by an algorithmic solution A of a problem L (*considered as a language*) from a problem domain Σ*, we mean that among other conditions, the following are satisfied:

(a) A is a step-by-step method in which for each instance of the problem, there is a definite sequence of execution steps (*not involving any guesswork*).

(b) A *terminates* for each xεΣ*, irrespective of whether x εL or x ∉ L.

&lt;watermark&gt;SAITI UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;130&lt;/page_number&gt;

---


## Page 63

Set theory, Computability and Complexity

In this sense of algorithmic solution, only a **solution by a Deterministic TM** is called an **algorithm**. A solution by a **Non-Deterministic TM may not be an algorithm.**

(iii) However, for every NTM solution, there is a Deterministic TM (DTM) solution of a problem. Therefore, if there is an NTM solution of a problem, then there is an algorithmic solution of the problem. However, *the symmetry may end here*.

The *computational equivalence* of Deterministic and Non-Deterministic TMs does not state or guarantee any *equivalence in respect of requirement of resources* like time and space by the Deterministic and Non-Deterministic models of TM, for solving a (solvable) problem. To be more precise, if a problem is solvable in polynomial-time by a Non-Deterministic Turing Machine, then it is, of course, *guaranteed* that there is a deterministic TM that solves the problem, but *it is not guaranteed* that there exists a Deterministic TM that solves the problem *in polynomial time*. Rather, **this fact forms the basis for one of the deepest open questions of Mathematics, which is stated as ‘whether P = NP?’**(P and NP to be defined soon).

**The question put in simpler language means:** Is it possible to design a Deterministic TM to solve a problem in polynomial time, for which, a Non-Deterministic TM that solves the problem in polynomial time, has already been designed?

**We summarize the above discussion from the intractable problem’s definition onward.** Let us begin with definitions of the notions of P and NP.

P denotes the class of all problems, for each of which there is at least one known polynomial time Deterministic TM solving it.

NP denotes the class of all problems, for each of which, there is at least one known Non-Deterministic polynomial time solution. However, this solution may not be reducible to a polynomial time algorithm, i.e, to a polynomial time DTM.

We can define p and NP to be the classes of languages because problems from graph theory, combinatorics can often be formulated as language recognition problems. Consider a problem which requires an answer in form of “Yes” or “No” for each instance. Each instance of a problem can be encoded as a string and reformulate the problem as one of recognizing the language consisting of all the strings representing those instance of the problem whose answer is “Yes”.

With this logic P and NP classes of complexities can be defined as classes of languages:

**Definition**

P = { L | L can be decided or accepted by a DTM( Deterministic TM) in polynomial time}

NP = { L | L can be decided or accepted by a Nondeterministic TM in polynomial time}

NP is a set of decision problems ( with Yes or No answer) that can be solved by NDTM in polynomial time

Thus starting with two distinct classes of problems, viz, **tractable** problems and **intractable** problems, we introduced two classes of problems called **P and NP**. Some interesting relations known about these classes are:

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;131&lt;/page_number&gt;

---


## Page 64

Computability
and Complexity

(i) P = set of tractable problems
(ii) P ⊆ NP.

(The relation (ii) above simply follows from the fact that every Deterministic TM is a special case of a Non-Deterministic TM).

Check your Progress-2
Q1 What is Nondeterministic Turing Machine?
Q2 Define P and NP Complexity Classes.

## 3.6 SUMMARY

In this unit, after giving the informal idea of what a Turing machine is, the concept is formally defined and illustrated through an example. A Nondeterministic TM was introduced next and also explained how it is different from a standard TM. Besides TM and NDTM, P and NP classes of complexities were defined.

## 3.7 SOLUTIONS/ANSWERS

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

### Check Your Progress-1

Q1 What is the meaning of the following symbols:

(i) Q
(ii) Σ
(iii) Γ
(iv) δ

Ans1. (i) Q is the finite set of states,
(ii) Σ is the finite set of non-blank information symbols,
(iii) Γ is the set of tape symbols, including the blank symbol #,
(iv) δ is the **next-move** partial function from Q x Γ to Q x Γ x {L, R, N},
where ‘L’ denotes the tape Head moves to the left adjacent cell, ‘R’ denotes tape Head moves to the Right adjacent cell and ‘N’ denotes Head does not move, i.e., continues scanning the same cell.

Q2 Explain what is a Turing Machine?

Ans. 2: TM defines an abstract machine/mathematical model that consists of an infinite length tape divided into cells for storing input symbols and a head which scans and reads the input. If the TM reaches the final state, the input string is accepted, otherwise it is rejected. TMs are considered to be the most important formal models in the study of Computer Science.

Q3 How TM is different from Finite Automata?

Ans.3 The *Finite Automata* is used only as **accepting devices** for languages in the sense that the automata, when given an input string from a language, tells whether the string is acceptable or not. *The Turing Machines are designed to play at least the following three different roles:*

&lt;page_number&gt;132&lt;/page_number&gt;

---


## Page 65

Set theory, Computability
and Complexity

(i) As accepting devices for languages, similar to the role played by FAs.

(ii) As a computer of functions. In this role, a TM represents a particular function (say the SQUARE function which gives as output the square of the integer given as input). Initial input is treated as representing an argument of the function. And the (final) string on the tape when the TM enters the Halt State is treated as representative of the value obtained by an application of the function to the argument represented by the initial string.

(iii) As an enumerator of strings of a language that outputs the strings of a language, one at a time, in some systematic order, i.e, as a list.

**Check your Progress-2**

Q1 What is Nondeterministic Turing Machine?
Ans.1: In Standard TM, *to each* pair of the current state (except the halt state) and the symbol being scanned, *there is a unique* triplet comprising of *the next state*, *unique action* in terms of writing a symbol in the cell being scanned and *the motion*, if any, to the right or left. **However, in the case NDTM, to each pair** (q, s) with q as current state and s as symbol being scanned, *there may be a finite set of the triplets { (q<sub>i</sub>, s<sub>i</sub>, m<sub>i</sub>) : I=1,2,…… } of possible next moves.***

Q2 Define P and NP Complexity Classes.
**P denotes** the class of all problems, for each of which there is at least one known polynomial time Deterministic TM solving it.
**NP denotes** the class of all problems, for each of which, there is at least one known Non-Deterministic polynomial time solution. However, this solution may not be reducible to a polynomial time algorithm, i.e, to a polynomial time DTM.

We can define P and NP to be the classes of languages because problems from graph theory, combinatorics can often be formulated as language recognition problems. Consider a problem which requires an answer in form of “Yes” or “No” for each instance. Each instance of a problem can be encoded as a string and reformulate the problem as one of recognizing the language consisting of all the strings representing those instance of the problem whose answer is “Yes”.

With this logic P and NP classes of complexities can be defined as classes of languages:

Definition
P = { L | L can be decided or accepted by a DTM( Deterministic TM) in polynomial time}

NP = { L | L can be decided or accepted by a Nondeterministic TM in polynomial time}

NP is a set of decision problems ( with Yes or No answer) that can be solved by NDTM in polynomial time.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;133&lt;/page_number&gt;

---


## Page 66

&lt;img&gt;IGU logo&lt;/img&gt;
THE PEOPLE'S UNIVERSITY