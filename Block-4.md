## Page 1

Block
# 4

## GRAPH THEORY

<table>
  <tr>
    <td>Unit 1<br>Basic Properties of Graphs</td>
    <td style="text-align: right;">199</td>
  </tr>
  <tr>
    <td>Unit 2<br>Connectedness</td>
    <td style="text-align: right;">221</td>
  </tr>
  <tr>
    <td>Unit 3<br>Eulerian and Hamiltonian Graphs</td>
    <td style="text-align: right;">243</td>
  </tr>
  <tr>
    <td>Unit 4<br>Graph Colourings</td>
    <td style="text-align: right;">263</td>
  </tr>
</table>

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 2

# BLOCK INTRODUCTION

## Block 4: Graph Theory

Suppose you want to drive from Delhi to Calcutta. There are several routes for making the trip. How would you find the shortest route? Or, suppose you try to colour a map of India in such a way that neighbouring states are assigned different colours. How will you conclude that only four colours are necessary to do so, without actually doing the colouring? These problems may seem very diverse at first sight but they can be expressed as problems involving arrangements of certain objects and relationships between them. To study the arrangements, we view these objects as points in a plane, and the relationships as lines joining them. The branch of mathematics that deals with arrangement problems in this manner is known as graph theory.

The theory of graphs has a definite starting place in a paper published back in 1736 by the Swiss mathematician Leonhard Euler (1707-1783). In this paper he solved a problem that was then known as the Konigsberg bridge problem by formulating it in terms of graph theory. This theory is now being fruitfully used for solving problems related to the manufacture of integrated circuits, routing problems in transport network, and other important areas of computer science. As you further study this block, we hope you will appreciate some of these applications.

The aim of this block is to introduce you to graph theory and its practical utility. We begin this in Unit 1. In particular we familiarize you with the basic terminology, on which the rest of the block is built.

In Unit 2 we introduce you to several special types of graphs. We also discuss 'trees, which were used in 1847 by Gustav Kirchhoff (1824-1887) to model and study the working of electrical circuits. Arthur Cayley (1821-1895) also used trees to count the distinct isomers of saturated hydrocarbons in 1857.

In Unit 3 we go on to present Euler's path-breaking work in graph theory. We also discuss an equally important idea here, that of a Hamiltonian cycle. This concept, named after Hamilton (1805-1865), was initially used by him in a mathematical puzzle. This very concept has now been used to tackle practical problems like the traveling salesperson problem, which we discuss in the unit.

In Unit 4 we discuss a famous problem in graph theory, that is, the ‘four-colour problem’. Francis Guthrie communicated this problemm to Augustus De Morgan in the 1850's through his brother. This was finally solved only in 1976 by Kenneth Appel and Wolfgang Haken, who presented a computer-aided proof of the four colour conjecture. In this unit we also discuss the characterization of planar graphs, which was given by Kasimir Kuratowski in 1930.

In a nutshell, the subject you are going to study is a very exciting one, both in its underlying mathematical structure and in its applications in present day science and technology. We hope you will enjoy studying this block.

&lt;watermark&gt;OPEN UNIVERSITY OF THE PEOPLE UNIVERSITY&lt;/watermark&gt;

---


## Page 3

# UNIT 1 BASIC PROPERTIES OF GRAPHS

## Structure

1.0 Introduction
1.1 Objectives
1.2 Graphs
1.3 Degree, Regularity and Isomorphism
1.4 Subgraphs
1.5 Summary
1.6 Solutions/Answers

## 1.0 INTRODUCTION

In our everyday life, we come across various problems requiring us to look at structures of objects and some family of subsets of those objects. For example, we may need to put up an electric network where different electrical gadgets are the objects, and they are to be connected by electric wires. The lengths of these wires may not be important, but it is important to know how the wires are connected. This means that it is important to know which gadgets are connected to the endpoints of the wires.

Another example is that of the public transport system in a city. Various places are the objects here, the bus routes are the connections, and we need to know the palaces connected to the railway station, say. Yet another problem could be that of establishing communication links between different centres.

All these problems can be represented pictorially with a set of dots called vertices and a set of edges connecting various pairs of dots. Such representations are called graphs. The solutions to the given problems can be obtained by analysing their graphs. Ideas given by various mathematicians to solve such problems gave birth to a branch of mathematics called **graph theory**.

In this unit we shall begin with defining a graph and study some of its basic properties. In Sec.1.2 and Sec.1.3 we have defined various types of graphs. Throughout the sections, these graphs and their properties are illustrated with the help of examples.

Next, Sec.1.4 is devoted to the study of subgraphs.

In the following units of this block you would notice how these simple basic ideas help us to solve many tough problems of day-to-day life. We can have graphs with vertices representing points in space, people, animal species, sports teams etc., and edges might represent roads, telephone lines, communication channels etc.

Before getting into the subject matter, let us take a look at the broad objectives of this unit.

## 1.1 OBJECTIVES

After studying this unit, you should be able to

*   identify different ways of representing a graph;
*   identify complete graphs, paths, cycles;

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;199&lt;/page_number&gt;

---


## Page 4

Graph Theory

*   obtain the complement of a graph;
*   write the degree sequence of a graph and obtain the number of edges of a graph using the degrees of vertices;
*   identify graphs isomorphic to a given graph;
*   obtain a sub graph of G induced by a subset of V(G);
*   draw a regular graph on p vertices having degree r, where p and r are integers with r < p, such that at least one of them is even.

# 1.2 GRAPHS

You must have used the term ‘graph’ while studying the calculus of real-valued functions of a real variable. It is a set of the form {(x, f(x)): x is in the domain of the function f}. Such a set helps us to analyse the function f. The graphs that we will define presently are a little different. Before giving a formal definition of a graph let us look at some simple examples.

**Example 1:** Take two points x₁, x₂ in the plane and join them by any line. This line may be a straight line or an arc. There are many ways of joining these points. In Fig.1 we have shown three different ways.
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig.1&lt;/img&gt;

*** Similarly in Examples 2 and 3 we have shown different ways of joining 4 points.

**Example 2:** Take four points x₁, x₂, x₃, x₄ in the plane. Join xᵢ to xᵢ₊₁ by a line for 1 ≤ i ≤ 3. Then join x₄ to x₁. In Fig.2 we have given two different ways of doing this.
&lt;img&gt;Fig.2&lt;/img&gt;

As far as our study in this block is concerned these drawings represent the same object.

***

**Example 3:** Take four points x₁, x₂, x₃, x₄ in the plane. Join x₁ to the three other points by lines.

&lt;page_number&gt;200&lt;/page_number&gt;

---


## Page 5

Basic Properties of Graphs

&lt;img&gt;Fig.3&lt;/img&gt;

Again in Fig.3 above, the three drawings represent the same object.

***

From the examples above, you may have observed the points are important as objects but their positions are not important. Similarly, it is important to know which pairs are joined to each other, but the lines or the curves joining them are not important.

In the diagrams above, each point is called a **vertex**, and the curve joining any pair is called an **edge**. So, for instance, in Example 1 we have two **vertices** (plural of ‘vertex’) x₁ and x₂, and one edge.

In this way, to each drawing corresponds two sets — one consisting of vertices, say V, and one of edges, say E.

Now, note that, to identify an edge, we need to know which vertices it joins. So, we denote an edge joining x₁ and x₂ by (x₁, x₂). So, any edge is given by a pair of points from V. Now, we are in a position to define the objects we wanted to.

**Definition :** An **undirected graph** G is a finite non-empty set V together with a set E consisting of pairs of points of V. The set V is called the **vertex set** of G, the set E is called the **edge set** of G. To show the relationship between V, E and G, we write G = (V(G), E(G)).

If |V|=p and|E| = q, then G is a **(p,q)-graph**.

Now, suppose the edges have a direction, then the edge going from a vertex x₁ to a vertex x₂ is not the same as the one going from x₂ to x₁. So, (x₁, x₂) ≠ (x₂, x₁). In this case, the edges are represented by **ordered** pairs, that is, elements of V×V, where V is the vertex set. This leads us to the following definition.

**Definition:** A **directed graph**, or **digraph**, G consists of a finite non-empty set V together with a subset E of the Cartesian product set V × V. We call V the **vertex set** of G and E the **edge set** of G, and we write G = (V(G), E(G)).

In Fig.4 we have shown directed as well as undirected graphs. **Note that**, in an undirected graph, if (u,v) is an edge, so is (v, u). So, the relation E(G) is a symmetric binary relation on V(G). However, in a digraph E(G) need not be symmetric.

Sometimes, it may happen that in a graph there is a **loop**, i.e., an edge joins a vertex to itself as in Fig.4 (c), where (u, u) shows a loop. It may also happen that there are two or more edges joining the same vertices, as in Fig.4 (c), where there are two edges joining y to x. Such edges are called parallel or multiple edges, and a graph with any

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;201&lt;/page_number&gt;

---


## Page 6

Graph Theory

parallel edges is called a **multigraph**.

&lt;img&gt;Fig. 4 (a) G with multiple edges between u and v, x and y.&lt;/img&gt; &lt;img&gt;Fig. 4 (b) G₁ with two parallel edges between u and v, x and y.&lt;/img&gt; &lt;img&gt;Fig. 4 (c) G₂ with two parallel edges between u and v, x and y.&lt;/img&gt;

(a) (b) (c)

Fig.4

Definition: An undirected graph without loops or parallel edges is called a **simple graph**.

Why don’t you try an exercise now ?

E1) There are four basic blood types: A,B, AB and O. Type O can donate to any of the four types. A and B can donate to AB as well as to their own types, but type AB can only donate to AB. Draw a graph that presents this information.

So far, we have seen several kinds of graphs. However, in this block, **we shall only discuss simple graphs**, and **shall just refer to them as graphs**. Also, whenever there is no confusion, **we shall write V and E in place of V(G) and E(G)**.

Now, let us introduce some terminology.

*   If e is an edge joining the vertices u and v of a graph G=(V,E), we will denote it as uv. In this case, u and v are called **adjacent vertices** (or **neighbours**), and are the **endpoints** of e. We also say that e is **incident** with u and v.
*   If distinct edges e₁ and e₂ of G have at least one vertex in common, then e₁ and e₂ are called **adjacent edges**.

For an example of these concepts, consider the graph G₁ of Fig.4. G₁ = (V, E), where V = {u, v, x, y} and E = {uv,ux,uy,vx,xy}. So, G₁ is a (4, 5)-graph. The only non-adjacent vertices of G₁ are v and y. The edges uv and vx are adjacent, since both are incident with the vertex v. The edges uv and xy are non-adjacent. Two other ways of representing the graph G₁ are shown in Fig.5. Thus, **there is no unique way of drawing a graph**; the relative placing of the points and curves have no special significance.

&lt;img&gt;Fig. 5 (a) Graph G₁ with vertices u, v, x, y and edges uv, ux, uy, vx, xy.&lt;/img&gt; &lt;img&gt;Fig. 5 (b) Graph G₁ with vertices u, v, x, y and edges uv, vx, xy.&lt;/img&gt;

Fig.5

Remark : Since a diagram of a graph, as in Figures 1-5, completely describe the graph, **we often refer to the diagram of a graph G as G itself**.

It is interesting to know that the structure of molecules can also be represented by graphs (see Fig.6). Various atoms are represented by the vertices and the structural

&lt;page_number&gt;202&lt;/page_number&gt;
&lt;watermark&gt;GOVERNMENT UNIVERSITY&lt;/watermark&gt;

---


## Page 7

Basic Properties of Graphs

bonds are represented by the edges. For example, butane as well as isobutane are both the hydrocarbons C₄H₁₀. But the manner in which the bonds are present between the carbon and hydrogen atoms makes the difference. In both the compounds each carbon atom is attached to four other atoms. Unlike isobutane, in butane there is no carbon atom which is attached to all the other carbon atoms.

&lt;img&gt;Butane structure diagram&lt;/img&gt;
Butane

&lt;img&gt;Isobutane structure diagram&lt;/img&gt;
Isobutane

Fig.6

You may now try some exercises.

E2) Take three vertices x, y, z and draw all possible (3,2)-graphs on these vertices.
E3) Write down the vertex set V and edge set E of each graph in Examples 1, 2and 3.

We now define some graphs which are used for data communication and parallel processing.

A) A complete graph is a graph in which any two vertices are adjacent, i.e., each vertex is joined to every other vertex by an edge. We denote the complete graph on n vertices by Kₙ.

In Fig.7, we have shown Kₙ for various n. K₁ is just a single vertex; K₂ consists of two vertices and an edge; K₃ is often called a triangle. The last two figures in Fig.7 show two ways of representing K₄.

&lt;img&gt;K1-K4 graphs&lt;/img&gt;
Fig.7

B) Star topology: Various computers, printers and plotters on a campus can be connected using a local area network. Some of these networks are based on graphs like the one given in Fig.8, called a star topology. In this graph n vertices are adjacent to one central vertex. This represents n devices connected to a central control device from which messages are sent to them.

&lt;img&gt;Star topology diagram&lt;/img&gt;
Fig.8 : Star topology

&lt;page_number&gt;203&lt;/page_number&gt;

---


## Page 8

Graph Theory

C) **Cycles:** A cycle C<sub>n</sub> is a graph on n vertices {x<sub>1</sub>, ..., x<sub>n</sub>} where E(C<sub>n</sub>) = {x<sub>i</sub>x<sub>i+1</sub>: 1 ≤ i ≤ n-1} ∪ {x<sub>n</sub>x<sub>1</sub>}. For instance, C<sub>16</sub> is shown in Fig.9.

&lt;img&gt;
A diagram showing a cycle C<sub>16</sub> with 16 vertices labeled x<sub>1</sub> to x<sub>16</sub>. The vertices are connected in a circular manner, forming a closed loop.
&lt;/img&gt;

Fig.9 : C<sub>16</sub>, a cycle on 16 vertices

You may now try the following exercise.

E4) How many edges do C<sub>n</sub> and K<sub>n</sub> have, n≥3?

We now take up some definitions related to certain algorithms.

**Definition:** Let G = (V, E) be a (p, q)-graph. By its complement $\overline{G}$, we mean the graph with V($\overline{G}$) = V(G) and E($\overline{G}$) = {xy : xy ∉ E(G), x, y ∈ V(G)}.

Note that $\overline{G}$ is a (p, $\overline{q}$)-graph, where $\overline{q}$ = (number of pairs of elements of V) - q.

Since in a set V with p elements, there can be C(p, 2) = $\frac{p(p-1)}{2}$ such pairs of elements, $\overline{q}$ = $\frac{p(p-1)}{2}$ - q.

**Remark:** The complement of $\overline{G}$ is G. Can you prove this ?

Let us consider some examples, Fig. 10 shows C<sub>5</sub> and its complement. Check whether $\overline{C}_5$ is also a cycle or not.

&lt;img&gt;
Two diagrams side-by-side. The left diagram shows a pentagon labeled x<sub>1</sub> through x<sub>5</sub>, forming a cycle. The right diagram shows a complete graph with five vertices (x<sub>1</sub> through x<sub>5</sub>) where all possible edges are present, except for those in the original pentagon.
&lt;/img&gt;

Fig.10

Two graphs G and H are **disjoint** if V(G) ∩ V(H) = φ

For another example, consider the graph shown in Fig.11 (a). Its complement breaks into two disjoint graphs. One is K<sub>3</sub> and the other is K<sub>4</sub> (see Fig.11 (b)).

&lt;page_number&gt;204&lt;/page_number&gt;

---


## Page 9

Basic Properties of Graphs

&lt;img&gt;A graph with 5 vertices connected by multiple edges.&lt;/img&gt;
(a)

&lt;img&gt;A graph with 3 vertices connected by 3 edges.&lt;/img&gt;
(b)

Fig.11

Consider the complements of all the graphs you have seen so far.
**Notice** that C₅ is a (5, 5) graph, and $\overline{C}_5$ has 5 edges. Also, in Fig.11, G is a (7, 12)-graph and $\overline{G}$ has 9 edges. Do you see any relation between the number of vertices of G and number of edges of $\overline{G}$? You may try the following exercises and look for the answer.

E5) Three graphs G₁, G₂ and G₃ are listed below
G₁ = ({u₁, u₂, u₃, u₄, u₅, u₆}, {u₁u₂, u₁u₅, u₁u₆, u₂u₃, u₂u₅, u₃u₄, u₄u₅})
G₂ = ({u₁,u₂, u₃, u₄,u₅}, {u₁u₂,u₁u₃, u₁u₄,u₁u₅, u₂u₄, u₂u₅, u₃u₄, u₃u₅})
G₃ = ({u₁, u₂, u₃, u₄, u₅, u₆}, {u₁u₂, u₁u₄, u₁u₅, u₂u₃, u₃u₄, u₃u₆, u₅u₆})
Find $\overline{G₁}$, $\overline{G₂}$ and $\overline{G₃}$.

E6) If G is a (p, q)-graph, then how many edges can $\overline{G}$ have?

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

So far we haven't really looked at the ways in which graphs are related to the real-life situations given in Sec.1.0. Let us consider some graphs that will help us see this connection.

## 1.3 DEGREE, REGULARITY AND ISOMORPHISM

You may recall that in the beginning we defined two vertices of a graph G to be adjacent if they are joined by an edge. Such vertices are also called **neighbours**. The set of all neighbours of a fixed vertex x of G is called the **neighbourhood set of x**, denoted by $N_G(x)$. Since our graphs are simple, there is a one-one correspondence between $N_G(x)$ and the set of all edges of G incident with the vertex x. Related to this set, we get the following number.

**Definition:** By the **degree** of a vertex x in G, we mean the number of edges incident with x. We denote the degree of x by $d_G(x)$.

By definition, $d_G(x) = |N_G(x)|$, where $|N_G(x)|$ denotes the number of elements of the set $N_G(x)$.

Since in a (p, q)-graph G the maximum number of edges incident with a vertex x canbe (p-1), we have
**0≤d_G(x)≤(p-1)** for every vertex x in G.

Whenever there is no possibility of confusion, we will simply write d(x) instead of $d_G(x)$.

&lt;page_number&gt;205&lt;/page_number&gt;

---


## Page 10

Graph Theory

Also a vertex x of a graph G is called an **even vertex** if d<sub>G</sub>(x) is even; otherwise it is called an **odd vertex**. A vertex with degree 0 is called an **isolated vertex**.

Now let us look at the following example.

**Example 4 :** Consider the graph G shown in Fig. 12. First consider the vertex x₁. Clearly, three edges are incident with it, so that d(x₁) = 3. Likewise you may observe that d(x₂) = 4, d(x₃) = 5, d(x₄) = 6 and d(x₅) = 7.

We can write these observations as d(xᵢ) = i + 2 for 1 ≤ i ≤ 5.

&lt;img&gt;Fig. 12 Graph G with vertices x₁ to x₅ and y₁ to y₁₅.&lt;/img&gt;

In the same way, we can write d(yⱼ) = 1 for 1 ≤ j ≤ 15.

You may now try the following exercises.

---

E7) Write down the degrees of all the vertices for the graphs given in Figures 5 to 9.

E8) If G is a (p, q)-graph and x is a vertex in G, show that the degree of x in $\overline{G}$ is p - 1 - d<sub>G</sub>(x).

---

**Note** that in Example 4
d(x₁) + d(x₂) + ... + d(x₅) + d(y₁) + ... + d(y₁₅)
= 40
= 2 × 20
= 2 × (number of edges in G)

Does a similar relationship hold for the graphs in Fig.5 to Fig.9 ? In fact, it should, because of the following theorem.

**Theorem 1 (Handshaking Theorem)** : If G is a (p, q)-graph with V(G) = {v₁, ..., v<sub>p</sub>}, and if d<sub>i</sub> = d<sub>G</sub>(v<sub>i</sub>), 1 ≤ i ≤ p, then $2q = \sum_{i=1}^{p} d_i$.
That is, **the sum of the degrees of the vertices of G is twice the number of edges.**

**Proof:** Consider the set S = {(x, e): x ∈ V(G), e ∈ E(G), x is an endpoint of e}. Choose a vertex v<sub>i</sub> ∈ V. This can be done in p ways. Now, since d<sub>i</sub> = d(v<sub>i</sub>), there are

&lt;page_number&gt;206&lt;/page_number&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 11

Basic Properties of Graphs

precisely d<sub>i</sub> edges incident with this vertex v<sub>i</sub>. These edges give d<sub>i</sub> elements of the set S. Adding over all the vertices of G, we get

$|S| = \sum_{i=1}^{p} d_i.$ (1)

Now choose an edge e in E(G). This can be done in q ways. This edge has precisely two endpoints, and they give two elements of S. Summing over every edge e ∈ E(G), we get

$|S| = 2q$ (2)

This is because every edge is counted twice, once for each vertex it contains. Equating (1) and (2) we get the required result.

The next result immediately follows from Theorem 1.

**Corollary 1:** The sum of the degrees of all the vertices of any graph is even.

You have already verified Theorem 1 for the graphs in Fig.5 to Fig.9. Now let us look at a useful application of Theorem 1.

So far, in the discussion, you must have noticed that for a simple (p, q)-graph G the edge set E(G) is a subset of the set of all subsets of size 2 of elements of V(G). This means q ≤ p(p-1)/2. But then you may wonder : is it always possible to go the other way round? That is, for any pair of positive integers (p, q) with q ≤ p(p-1)/2, is it always possible to find a (p, q)-graph?

Theorem 1 gives us a necessary condition on p and q under which a (p, q)-graph exists. It helps us to see that **there does not always exist a graph with vertices having given degrees.**

For instance, can we construct a graph on 12 vertices with 2 of them having degree 1, three having degree 3, and the remaining seven having degree 10? This is not possible. Why? If such a graph existed, the sum of the degrees of all its vertices would be 1+1+3+3+3+10+10+10+10+10+10=81, which is not even.
So, the condition of Theorem 1 would not be satisfied.

Theorem 1 can also be used to obtain another result which we discuss now. **Corollary 2:** Any graph can only have an even number of odd vertices.

**Proof:** Let G be a (p, q)-graph and let {x<sub>1</sub>, ..., x<sub>t</sub>} be the set of its odd vertices and {x<sub>t+1</sub>, ..., x<sub>p</sub>} be the set of its even vertices. Let d<sub>G</sub>(x<sub>i</sub>) = 2c<sub>i</sub>+1, 1≤ i ≤ t and d<sub>G</sub>(x<sub>i</sub>) = 2r<sub>i</sub>, t+1≤ i ≤ p.

Then Theorem 1 says that $2q = \sum_{1}^{p} d_G(X_i)$

⇒ $2q = \sum_{1}^{t} (2c_i + 1) + \sum_{t+1}^{p} (2r_i) = 2(c_1 + c_2 + ... + c_t) + t + 2(r_{t+1} + ... + r_p)$,

which shows that t is even.

What this result says is that **if a graph has any odd vertices**, then their number has to be even. So, for instance, we can’t have a graph with only 1 odd vertex. In some graphs, like K<sub>10</sub>, all the ten vertices are odd vertices. On the other hand, in K<sub>11</sub> all the vertices have degree 10, that is, none of the vertices are odd.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;207&lt;/page_number&gt;

---


## Page 12

Graph Theory

We now give the reason for the name given to Theorem 1.

**Corollary 3:** At any party, the number of people who shake the hands of an odd number of people is even.

You can see this from Theorem 1 if you consider a handshake between two hands as an edge between two adjacent vertices.

Let us now consider some numbers that help us judge the type of graph we are dealing with.

**Definitions:** If G = (V, E) is a (p, q)-graph, then
δ(G) = min{d_G(x): x ∈ V(G)} is called the **minimum vertex degree of G**, and
Δ(G) = max{d_G(x): x ∈ V(G)} is called the **maximum vertex degree of G**.
Clearly, δ(G) and Δ(G) are non-negative integers.

We can, in fact, re-number the vertices of V(G) as {v₁, ..., v_p} with dᵢ = d(vᵢ), 1 ≤ i ≤ p such that d₁ ≥ d₂ ≥ ... ≥ d_p, that is, place the vertices in decreasing order of their degrees. This is called the **degree sequence** of the graph G.

For instance, the degree sequence of the graph G in Fig. 11 is 7, 6, 5, 4, 3, 1, 1..., 1. &lt;watermark&gt;15 times&lt;/watermark&gt;

And now some exercises for you.

E9) Write down δ(G) and Δ(G) for all the graphs in Examples 1, 2, 3.

E10) For each of the number sequences given below, give an example of a graph having this as a degree sequence, if possible. Otherwise explain why such a graph does not exist.

(i) (3, 2, 2, 2, 1)
(ii) (3, 2, 2, 2, 1, 1)
(iii) (4, 3, 2, 1, 0)
(iv) (4, 4, 3, 3, 2, 2)
(v) (5, 5, 5, 4, 4, 3, 3)

E11) Let G be a (p, q)-graph, each of whose vertices has degree k or k+1. If G has m vertices of degree k and r vertices of degree k+1, then show that
m = (k+1)p - 2q.

Let us now consider graphs that have a constant degree sequence, that is, each of their vertices has the same degree. For example, the degree sequence of C₅ and its complement is 2, 2, 2, 2, 2, that is, it is a constant 2. Such graphs have a special status in graph theory, and we name them as follows.

**Definition:** A (p, q)-graph G is said to be **regular, with degree of regularity r**, if d_G(x) = r for every vertex x ∈ V(G). In this case we also say that G is an **r-regular graph**. Of course, 0 ≤ r ≤ (p - 1).

You have seen that K₃ is regular. What about Kₙ for n > 3? In fact, it is (n -1)-regular.

As you will see in the next unit, 3-regular graphs, called **cubic graphs**, are important. A well known example of a cubic graph is the **Petersen graph**. This is named after the Danish mathematician J.P.C. Petersen. He worked in several areas of pure and applied mathematics. Two representations of the Petersen graph are shown in Fig. 13. Note that it is a (10, 15)-graph.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;208&lt;/page_number&gt;

---


## Page 13

Basic Properties of Graphs

&lt;img&gt;Fig. 13&lt;/img&gt;

Let us now consider the following example of a regular graph.

**Example 5 (Hypercube Q<sub>n</sub>):** Let the vertex set consist of all n-tuples with entries 0,1 only. The edge set is given by
E(Q<sub>n</sub>) = { ab : a and b differ exactly at one coordinate}.
Here, by **a** we mean an n-tuple (a₁, … , a<sub>n</sub>), where a<sub>i</sub> = 0 or 1, for 1≤i≤n. In Fig.14, we show Q₂ and Q₃.

&lt;img&gt;Fig. 14: Julius Petersen (1839-1910)&lt;/img&gt;

&lt;img&gt;Fig. 15&lt;/img&gt;

Any vertex **a** is adjacent to precisely n other vertices. For example, (0,0, …,0) is adjacent to (1, 0, 0, …, 0), (0, 1, 0, 0, …0), … , (0, 0, …, 1). Hence, the hypercube Q<sub>n</sub> is n-regular. You should check that Q<sub>n</sub> has 2<sup>n</sup> vertices and n2<sup>n-1</sup> edges.

***&lt;watermark&gt;GIOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

You have seen some examples of regular graphs, and you can think of some more. You also know that if G is an r-regular graph on p vertices, then by Theorem 1, 2q = pr. So, pr is even. Therefore, at least one of p or r is even. Is the converse true ? That is, given a pair of integers p, r, 0 ≤ r ≤ (p – 1), where pr is even, can we always construct an r-regular graph on p vertices? This is true. The proof is by construction on the same lines as the examples we give below. We consider two cases — when r is even, and when r is odd.

**Example 6:** We construct a 4-regular graph G with 12 vertices. Let V(G)={x₁,…,x₁₂}. Place the vertices in a circular manner. Join x<sub>i</sub> to x<sub>i+1</sub> by an edge for every i, 1≤i≤11. Join x₁₂ to x₁ also by an edge. Now all the vertices have acquired degree 2. Now, join each x<sub>i</sub> to x<sub>i+2</sub> for every i = 1,…10. Finally, join x₁₁ to x₁ and x₁₂ to x₂, as in Fig.16. You can see that the resulting graph is 4-regular.

&lt;page_number&gt;209&lt;/page_number&gt;

---


## Page 14

Graph Theory

&lt;img&gt;Fig. 16&lt;/img&gt;

***

Example 7 : We shall construct a 5-regular graph on 12 vertices now. We first construct a graph on 12 vertices and with regularity (r-1), i.e., 5 - 1 = 4 — in fact, the graph constructed in Example 6.
Now join x<sub>i</sub> to x<sub>i+6</sub> for every i, 1 ≤ i ≤ 6.

We choose 6 because $\frac{p}{2} = 6$. Notice that the resulting graph is 5-regular (see Fig. 17).

&lt;img&gt;Fig. 17&lt;/img&gt;

***

The constructions above can be generalized to obtain a regular graph on p vertices with degree of regularity r, where at least one of p and r is even. In the following exercise, we give you an opportunity to do this.

E12) Construct a 5-regular graph on 10 vertices.

Often, when we look at two graphs, they appear different when they may essentially be the same. For instance, the complement of C<sub>5</sub> is essentially C<sub>5</sub>, though they don’t

&lt;page_number&gt;210&lt;/page_number&gt;

---


## Page 15

Basic Properties of Graphs

look the same. To see why we say this, let us look at the two graphs in Fig.10. Now, consider the function f: V(C₅) →V (C̄₅) defined by
f(x₁) = x₁, f(x₂) = x₃, f(x₃) = x₅, f(x₄) = x₂, f(x₅) = x₄.
With this definition, note that whenever xᵢ xⱼ ∈ E(C₅), f(xᵢ)f(xⱼ)∈ E(C̄₅). In other words, xᵢ xⱼ is an edge of C₅ if and only if f(xᵢ)f(xⱼ) is an edge of C̄₅. In such a situation we say that f is an isomorphism between C₅ and C̄₅.

This leads us to the following definition.

**Definition :** Let G = (V(G), E(G)), H = (V(H), E(H)) be two graphs. By an **isomorphism** f from the graph G to the graph H, we mean a map f: V(G) → V(H)such that

(i) f is one-one and onto; and
(ii) x y ∈ E(G) if and only if f(x) f(y) ∈ E(H).

In this case we say that G and H are **isomorphic**. Otherwise they are called **non-isomorphic**.

Note that two graphs G and H are isomorphic **if and only if** there is a one-one correspondence between V(G) and V(H) that preserves adjacencies and non-adjacencies. In this case we say that the map f **preserves the structure of G**.

Let us consider one more example.

**Example 8 :** Consider the two graphs G and H shown in Fig.18.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;Graph G with vertices x₁, x₂, x₃, y₁, y₂, y₃, y₄ and edges connecting them.&lt;/img&gt;
G

&lt;img&gt;Graph H with vertices a, b, c, d, e, g, h and edges connecting them.&lt;/img&gt;
H

Fig.18

Define a map f : V(G) →V(H)as follows:
f(x₁) = a, f(x₂) = b, f(x₃) = c, f(y₁) = d, f(y₂) = e, f(y₃) = g,
f(y₄) = h. Observe that uv∈E(G) **if and only if** f(u)f(v) ∈ E(H).
The two graphs shown in Fig.18 are isomorphic under this correspondence.

***

As you can see, if G and H are isomorphic, many properties of a vertex in V(G) are shared by its image in V(H). For example, you can check that dg(u) = d_H(f(u)), for every u ∈ V(G).

Here's an exercise about isomorphic graphs.

E13) Show that the graphs G and H given in Fig.19 are isomorphic.

&lt;page_number&gt;211&lt;/page_number&gt;

---


## Page 16

Graph Theory

&lt;img&gt;G1 graph with two vertices connected by one edge.&lt;/img&gt;
G₁

&lt;img&gt;G graph with six vertices (u, v, w, x, y, z) forming a star-like structure.&lt;/img&gt;
G

&lt;img&gt;H graph with six vertices (l, m, n, o, p, q) forming a hexagonal structure.&lt;/img&gt;
H

Fig.19

As you have seen, in order to show that two graphs are isomorphic, it is enough to produce one isomorphism from one of them to the other. In some cases, as in Fig.20, it is clear that the 2 graphs are not isomorphic. However, if we are given two similar looking graphs, it is not easy to show that there **does not exist** any isomorphism between them. The six properties given below are of help in this matter. We shall state them, without proof.

&lt;img&gt;G2 graph with three vertices where the middle vertex has no edges.&lt;/img&gt;
G₂

Fig.20

**Theorem 3 :** Let f be an isomorphism from a graph G to a graph H. Then the following hold :

i) If G is a (p, q)-graph, then H is also a (p, q)-graph.

ii) The inverse map f⁻¹ is an isomorphism from the graph H to the graph G.

iii) If g is an isomorphism from the graph H to a graph K, then the composite map g ∘ f is an isomorphism from the graph G to the graph K.

iv) f induces a bijective map f ~ : E(G) → E(H), given by f ~ (x y) = f(x) f(y).

v) For every x ∈ V(G), a vertex y belongs to N_G(x) if and only if f(y) belongs to N_H(f(x)). (This means that d_G(x) = d_H(f(x)), for every x ∈ V(G).) Thus, the degree sequence of the graph G is the same as the degree sequence of the graph H.

vi) If G has a set of vertices {x₁, ..., xₙ} such that xₙ x₁ and xᵢ xᵢ₊₁ are in E(G) ∀i, 1 ≤ i ≤ (n -₁), then the vertices {f(x₁), ..., f(xₙ)} in V(H) are such that f(xₙ) f(x₁) as well as f(xᵢ) f(xᵢ₊₁) are in E(H) ∀i, 1 ≤ i ≤ (n-1). Thus, for every positive integer n ≥ 3, the number of copies of Cₙ in G is equal to the number copies of Cₙ in H.

Let us now consider the following examples where we have used these properties to show non-isomorphism of the two graphs.

**Example 9 :** Consider the two graphs shown in Fig.21. Both are (8, 8)-graphs and

&lt;watermark&gt;GOVERNMENT OF THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;G graph with eight vertices forming a cycle.&lt;/img&gt;
G

&lt;img&gt;H graph with eight vertices forming a cycle.&lt;/img&gt;
H

Fig.21

&lt;page_number&gt;212&lt;/page_number&gt;

---


## Page 17

Basic Properties of Graphs

have a copy of C<sub>6</sub> inside them. Are they isomorphic ? The degree sequence of the graph G is 4, 2, 2, 2, 2, 1, 1 and of the graph H is 3, 3, 2, 2, 2, 1, 1. This contradicts (v) of Theorem 3. Therefore, G and H are not isomorphic.

***

Example 10 : Consider the graphs G and H in Fig.22.
&lt;img&gt;Graph G with vertices x1, x2, x3, x4, x5, x6, x7, x8&lt;/img&gt;
&lt;img&gt;Graph H with vertices x1, x2, x3, x4, x5, x6, x7, x8&lt;/img&gt;
Fig.22

Both are (8, 12)-graphs and have a copy of C<sub>8</sub> inside them. Moreover, both have degree sequences 3, 3, 3, 3, 3, 3, 3, 3. They are still not isomorphic. This can be seen by observing that the graph G has no copy of a triangle inside it and the graph H has two triangles {x<sub>1</sub>, x<sub>2</sub>, x<sub>8</sub>} and {x<sub>4</sub>, x<sub>5</sub>, x<sub>6</sub>}, which contradicts (vi) of Theorem 3.

***

Example 11: Consider the graphs G and H shown in Fig. 23.
&lt;img&gt;Graph G with vertices x1, x2, x3, x4, x5, x6&lt;/img&gt;
&lt;img&gt;Graph H with vertices x1, x2, x3, x4, x5, x6&lt;/img&gt;
Fig.23

Both are (6, 6)-graphs having 3, 3, 2, 2, 1, 1 as their degree sequence. However, they are not isomorphic. In the graph G the two vertices x<sub>3</sub>, x<sub>5</sub> having degree 3 are adjacent. Under any isomorphism (if it exists) they should be mapped to two adjacent vertices of degree 3. We observe that in the graph H the two vertices of degree 3 are not adjacent.

***

Notice that the two graphs shown in Fig. 6, corresponding to butane and isobutane, are not isomorphic. Unlike isobutane, no carbon atom is attached to all the other carbon atoms of butane.

And now the following exercises for you to try.

E14) Draw at least 3 non-isomorphic graphs on four vertices.

E15) A graph G is said to be **self complementary** if it is isomorphic to its

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;213&lt;/page_number&gt;

---


## Page 18

Graph Theory

$\overline{G}$. Show that for a self complementary (p, q)-graph G, either p or (p – 1) is divisible by 4.

It is often the case that a graph under study is contained within some larger graph also being investigated. When we talk of an electric circuit, it is often described in terms of various sub-circuits. Transport in a country is always divided into various sections, for example, the railway transport in India is divided into Central Railway, Western Railway, ...etc. That is, whenever we study any system, it is important to study its subsystems. Likewise here in the next section we study subgraphs.

# 1.4 SUBGRAPHS

Let us start with considering the graph $G = (V(G), E(G))$ shown in Fig.24.

&lt;img&gt;Fig.24&lt;/img&gt;

What if we just take a part of this graph G? Would this be a graph? Yes, it would. For example, consider the following.

Let $V(G_1) = \{x_1, x_2, x_3, x_4\}$, $E(G_1) = \{x_i x_{i+1}: 1 \leq i \leq 3\} \cup \{x_4 x_1\}$.
Note that $G_1$ is **isomorphic** to $C_4$.
If $V(G_2) = \{x_8, x_9\}$, $E(G_2) = \{x_8 x_9\}$, then $G_2$ is **isomorphic** to $K_2$.
Also the graph $G_3$ is **isomorphic** to $C_7$, where
$V(G_3) = \{x_9, ..., x_{15}\}$, $E(G_3) = \{x_{15} x_9\} \cup \{x_i x_{i+1}: 9 \leq i \leq 14\}$

**Note** that all these graphs have one thing in common. Their vertex sets are subsets of $V(G)$ and edge sets are subsets of $E(G)$. In this sense, all these graphs are ‘portions’ of the graph G. Formally, we have the following definition.

**Definition :** Let $G = (V(G), E(G))$ be a graph. A **subgraph** H of the graph G is a graph, such that every vertex of H is a vertex of G, and every edge of H is an edge of G also, that is, $V(H) \subseteq V(G)$ and $E(H) \subseteq E(G)$.
Further, if H is a **subgraph** of a graph G, such that $V(H) = V(G)$ and $E(H) \subseteq E(G)$, that is, H and G have exactly the same vertex set, then H is called a **spanning subgraph** of G.

So, $G_1$, $G_2$ and $G_3$ given above are subgraphs of G given in Fig.23. However, the graph H, with $V(H) = V(G_3)$, $E(H) = E(G_3) \cup \{x_9 x_{12}\}$ is **not** a subgraph of the graph G, since the edge $x_9 x_{12}$ is not in $E(G)$.

&lt;page_number&gt;214&lt;/page_number&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 19

Basic Properties of Graphs

**Note**: You should write down the reasons why the following statements are true.

1) Every graph G is a subgraph of itself, i.e., **G is a subgraph of G**.
2) **For any v ∈ V(G), {v} is a subgraph of G.**

Now for an example of a spanning subgraph.

**Example 12:** Consider G = K₄ on four vertices x₁, x₂, x₃, x₄ as shown in Fig.25. From the figure you can see G₁, G₂, G₃ are subgraphs of G, with V(G₁)=V(G₂)=V(G₃)=V(G). So, G₁, G₂ and G₃ are spanning subgraphs of the graph G.

&lt;img&gt;Fig.25: Graph G with vertices x₁, x₂, x₃, x₄ and edges connecting them.&lt;/img&gt;
&lt;img&gt;Fig.25: Subgraph G₁ with vertices x₁, x₂, x₃, x₄ and edges connecting them.&lt;/img&gt;
&lt;img&gt;Fig.25: Subgraph G₂ with vertices x₁, x₂, x₃, x₄ and edges connecting them.&lt;/img&gt;
&lt;img&gt;Fig.25: Subgraph G₃ with vertices x₁, x₂, x₃, x₄ and edges connecting them.&lt;/img&gt;

***


&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

**Example 13:** Consider the Petersen graph G, with the vertex set {xᵢ : 1≤i≤5}∪{yⱼ : 1≤j≤5} shown in Fig.26. Consider the graph G₁, where V(G₁)={yⱼ : 1≤ j≤5}, E(G₁)={y₁y₃, y₃y₅, y₅y₂, y₂y₄}.

&lt;img&gt;Fig.26: The Petersen Graph with vertices x₁, x₂, x₃, x₄, x₅ and y₁, y₂, y₃, y₄, y₅ connected by edges.&lt;/img&gt;
&lt;img&gt;Fig.26: Subgraph G₁ with vertices y₁, y₂, y₃, y₄, y₅ and edges y₁y₃, y₃y₅, y₅y₂, y₂y₄.&lt;/img&gt;

&lt;page_number&gt;215&lt;/page_number&gt;

---


## Page 20

Graph Theory

Here every edge of G₁ is an edge in G. On the other hand, y₄ y₁ is an edge in G but not an edge in G₁. Thus, G₁ is a subgraph of G. So, is the graph G₂ shown in Fig.27. However, there is a difference in the two subgraphs. Though y₁ and y₄ lie in V(G₁), y₁y₄ is in E(G) but not in E(G₁). But, whenever two vertices of G₂ are joined by an edge in G, that edge belongs to E(G₂)

The property of the subgraph G₂ that we have just mentioned leads us to the following definition.

**Definition:** Let G be a graph and let S ⊆ V(G). By **the subgraph of the graph G, induced by the set S**, we mean the subgraph H with V(H)=S and the edge set consisting of those edges of G which are joining the vertices in S. That is,
E(H) = {x y : x ≠ y, x∈S, y∈S, x y∈E(G)}. We denote H by <S>G.

&lt;img&gt;
A diagram showing a pentagon labeled G₂ with vertices x₁, x₂, x₃, x₄, x₅.
Vertices y₁ and y₃ are inside the pentagon.
The edges connecting these points are:
- x₁ to x₂
- x₂ to x₃
- x₃ to x₄
- x₄ to x₅
- x₅ to x₁
- y₁ to y₃
- y₁ to x₁
- y₁ to x₂
- y₁ to x₃
- y₁ to x₄
- y₁ to x₅
- y₃ to x₁
- y₃ to x₂
- y₃ to x₃
- y₃ to x₄
- y₃ to x₅
&lt;/img&gt;

Fig.27

Note that two points of S are adjacent in <S>G if and only if they are adjacent in G.

For example, the subgraph G₂ in Example 13 is an induced subgraph of the graph G, induced by {x₁, x₂, x₃, x₄, x₅, y₁, y₃}, whereas the subgraph G₁ is not induced.

Note that for a vertex v ∈ V(G), by **G – v** we mean the subgraph <V(G) – {v}>G, which means a subgraph of G consisting of all points of G except v, and all edges of G except for the edges incident with v.
For a subset S of V(G), the subgraph <V(G) – S>G is often written as G–S.

We now illustrate various types of subgraphs, relating their minimum and maximum vertex degrees.

**Example 14:** Consider the graph G shown in Fig.28 (a). Observe that Fig.28 (b)

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;
A diagram showing a larger graph G with vertices v₁, v₂, v₃, v₄, v₅, v₆, v₇, v₈, v₉, v₁₀, v₁₁, v₁₂, and v₁₃.
The graph G has several edges connecting these vertices.
&lt;/img&gt;

(a)

&lt;img&gt;
A diagram showing a subgraph H₁ of G with vertices v₁, v₂, v₃, v₄, v₅, v₆, v₇.
The subgraph H₁ consists of a central vertex v₄ connected to six other vertices (v₁, v₂, v₃, v₅, v₆, v₇).
There are no edges between v₁, v₂, v₃, v₅, v₆, v₇.
&lt;/img&gt;

(b)

&lt;img&gt;
A diagram showing a subgraph H₂ of G with vertices v₁, v₂, v₃, v₄, v₅, v₆, v₇.
The subgraph H₂ consists of a central vertex v₄ connected to four other vertices (v₁, v₂, v₃, v₅, v₆, v₇).
There are no edges between v₁, v₂, v₃, v₅, v₆, v₇.
&lt;/img&gt;

(c)

&lt;page_number&gt;216&lt;/page_number&gt;

Fig. 28

---


## Page 21

Basic Properties of Graphs

&lt;img&gt;Fig. 28 (d) showing subgraph H3 with vertices v10, v11, v12, v9, v8, v7.&lt;/img&gt;
(d)

&lt;img&gt;Fig. 28 (e) showing vertex induced subgraph H2 with vertices v10, v11, v12, v9, v8, v7, v6, v5, v4.&lt;/img&gt;
(e)

**Fig.28 (contd.)**

shows a subgraph H₁, Fig.28 (c) gives a vertex induced subgraph H₂ with V(H₂) = V(H₁), Fig.28 (d) shows H₃ = G - v₄, and Fig.28 (e) gives the spanning subgraph H₄.

***

Now, a few exercises for you.

E16) Show that for a subgraph H of a graph G, Δ(H) ≤ Δ(G).

E17) Give an example of a subgraph H of a graph G with δ(G) < δ(H) and Δ(H) < Δ(G).

E18) Let G be a graph with n vertices and m edges, and let v be a vertex of G of degree k. How many vertices and edges does G - v have?

E19) Is every subgraph of a regular graph regular ? Give reasons for your answer.

&lt;watermark&gt;KATHIKA THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

We now end this unit by giving a summary of what we have covered here.

## 1.5 SUMMARY

1) A simple graph G consists of a finite non-empty set V of points together with a prescribed set E of 2 element subsets of V.

2) The complete graph Kₙ is a graph with n vertices such that every vertex is joined to every other vertex by an edge.

3) The path Pₙ is a graph on n vertices {x₁, x₂, ..., xₙ} in which any two consecutive edges are adjacent and where no edge and no vertex is repeated.

4) A cycle is a circuit in which the only repeated vertex is the first vertex, which is the same as the last vertex.

5) The complement of the (p, q)-graph G is a (p, q̄)-graph Ḡ where q = (number of pairs of elements of V) - q.

6) The number of edges incident with a vertex in a graph G gives the degree of the vertex. A graph having the same degree of all its vertices is regular.

&lt;page_number&gt;217&lt;/page_number&gt;

---


## Page 22

Graph Theory

7) In any graph the sum of the degrees of all its vertices is even.
8) There always exists an r-regular graph on p vertices, where p, r are non-negative integers and at least one of them is even.
9) For a graph G = (V(G), E(G)), a graph H = (V(H), E(H)) is a subgraph of G whenever V(H) ⊆ V(G) and E(H) ⊆ E(G).
10) A subgraph of a regular graph may or may not be regular.
11) A subgraph H of a graph G is a spanning subgraph of G if V(H) = V(G).
12) For any S ⊆ V(G), the subgraph of G induced by S is H=<S>G, where V(H)=S and E(H)={xy:x ≠ y, x∈S, y∈S, xy∈E(G)}.

# 1.6 SOLUTIONS / ANSWERS

E1)
<mermaid>
graph TD
    A --> O
    B --> O
    A -- AB --> O
    A -- AB --> B
    B -- AB --> A
</mermaid>
Fig.29

E2)
<mermaid>
graph TD
    subgraph Left Side
        X -- XZ --> Z
        X -- XY --> Y
    end
    subgraph Middle Side
        X -- XY --> Y
        Y -- YZ --> Z
    end
    subgraph Right Side
        X -- XZ --> Z
        Y -- YZ --> Z
    end
</mermaid>
Fig.30

E3) Example 1, V = {x₁, x₂}, E = {x₁x₂}
Example 2, V = {x₁, x₂, x₃, x₄} E = {x₁x₂, x₂x₃, x₃x₄, x₄x₁}
Example 3, V = {x₁, x₂, x₃, x₄}, E = {x₁x₂, x₁x₃, x₁x₄}

E4) Cₙ has n edges and Kₙ has $\frac{n(n-1)}{2}$ edges.

E5) E(Ḡ₁) = {u₁u₃, u₁u₄, u₂u₄, u₂u₆ u₃u₅, u₃u₆, u₄u₆, u₅u₆ }
E(Ḡ₂) = {u₂u₃, u₄u₅}
E(Ḡ₃) = {u₁u₃, u₁u₆, u₂u₄, u₂u₅, u₂u₆, u₃u₅, u₄u₅, u₄u₆ }

&lt;page_number&gt;218&lt;/page_number&gt;

---


## Page 23

Basic Properties of Graphs

E6) $\overline{G}$ can have $\frac{p(p-1)}{2} - q$ edges.

E7) For Fig.5, $d(x_i) = 4$, $1 \leq i \leq 5$, $d(y_i) = 2$, $1 \leq i \leq 7$.
For Fig.8, $d(x_i) = 2$, $1 \leq i \leq 5$.
Do the others similarly.

E8) $d_{\overline{G}}(x) = |N_{\overline{G}}(x)| = |\{y \in V(G): x \text{ } y \notin E(G)\}| = |V(G)| - 1 - |N_G(x)|$
$= p - 1 - d_G(x)$.

E9) (1) 1, 1 (2) 2, 2 (3) 1, 3

E10) ii) The graph has 3 vertices of odd degree, contradicting Corollary 1 of Theorem 1.
v) The sum of the degrees of all the vertices of a graph is odd, contradicting Corollary 1.
For the rest you can draw graphs whose degree sequence is the given one.

E11) $km + (k+1)r = 2q$ (Using Theorem 1) Also, $m + r = p$
Therefore,
$km + (k+1)(p-r) = 2q$
$E \Rightarrow m = (k+1)p - 2q$

E12) Here $p = 10$, $r = 5$. So $\frac{r-1}{2}$ is an integer. Take 10 vertices $\{x_1, x_2, ..., x_{10}\}$. Join $x_i$ to $x_{i+1}$ for $1 \leq i \leq 9$. Join $x_{10}$ to $x_1$. Now all the vertices have acquired degree $\frac{r-1}{2} = 2$. Join $x_i$ to $x_{i+2}$ for $i = 1, ..., 8$. Join $x_9$ to $x_1$ and $x_{10}$ to $x_2$. We now have a 4-regular graph. Here $\frac{P}{2} = n = 5$.
Thus, to obtain a 5-regular graph join $x_i$ to $x_{i+5}$ for $1 \leq i \leq 5$ (see Fig.31).

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig.31&lt;/img&gt;

E13) Consider the function
$\phi: V(G) \rightarrow V(H): \phi(u) = \ell, \phi(v) = m, \phi(w) = n, \phi(x) = p, \phi(y) = q, \phi(z) = r.$
You can check that $\phi$ is an isomorphism.

E14) If $p = 4$, then $q \leq C(4, 2) = 6$. So we want $(4, q)$-graphs, with $0 \leq q \leq 6$.
We are giving several in Fig. 32.

&lt;page_number&gt;219&lt;/page_number&gt;

---


## Page 24

Graph Theory

&lt;img&gt;Graphs with q = 0, 1, 2, 3, 4, 5, 6 vertices&lt;/img&gt;

Fig.32

E15) Suppose G is a (p, q)-graph. Then
E(G) ∪ E(Ḡ) = {the set of all pairs of vertices in V(G)}. Thus,
q + q̄ = p(p-1)/2.
If the graph G is self complementary, then q = q̄. Thus, p(p-1) = 2q + 2q̄ = 4q, that is 4 divides p(p-1). Since only one of p or (p-1) is even, this means either p or (p-1) is divisible by 4.

E16) Let x ∈ V(H) such that d_H(x) = Δ(H). Then, N_H(x) ⊆ N_G(x). Thus,
Δ(H) = |N_H(x)| ≤ |N_G(x)| ≤ Δ(G).

E17) δ(G) = 1 < 2 = δ(H)
Δ(H) = 2 < 3 = Δ(G)

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Graphs G and H with circles around them&lt;/img&gt;

Fig.33

E18) G-v will have (n - 1) vertices and m-k edges

E19) No, for example, any cycle is regular. However, if you remove one of its edges, you get a subgraph which is not regular.

&lt;page_number&gt;220&lt;/page_number&gt;

---


## Page 25

# UNIT 2 CONNECTEDNESS

## Structure

2.0 Introduction
2.1 Objectives
2.2 Connected Graphs
    2.2.1 Paths, Circuits and Cycles
    2.2.2 Components
    2.2.3 Connectivity
2.3 Bipartite Graphs
2.4 Trees
2.5 Summary
2.6 Solutions/Answers

## 2.0 INTRODUCTION

In the last unit you saw that graphs are often used to represent (that is, model) communication or transportation networks and several other systems such as representation of a molecule in a chemical compound. In a transportation network, it is necessary to know which destinations are connected by a direct route. For example, if air travel is abolished then the people without any seaport cannot go to any other country unless their neighbours provide the initial road passage through their territory. When we use a graph to model this situation, we need to see which vertices are connected. We also need to ensure that there is an edge between any two vertices. Such graphs are called connected graphs. In Sec.2.2 we will define connected graphs and we will show that any graph can be partitioned into connected graphs.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

In Sec.2.3, we will familiarise you with a type of graph which is useful in electronics and other areas. These graphs are called bipartite graphs. Such graphs are also very useful in studying neural networks.

In Sec. 2.4 we have considered another type of graph, a type, which also represents the chemical compounds butane and isobutane. We call such graphs trees. Here we will show that a tree has got several interesting properties, which are used in studying some real-life situations and various chemical compounds.

## 2.1 OBJECTIVES

After studying this unit, you should be able to

*   distinguish between walks, paths, circuits and cycles in a graph;
*   identify the components of various graphs;
*   define, and recognize, bipartite graphs, and trees.

## 2.2 CONNECTED GRAPHS

From Unit 1, you know that graphs model different real-life situations, especially situations involving routes — the vertices represent towns or junctions and each edge represents a road or some other form of communication link. This kind of a picture is very helpful in understanding connected graphs that we introduce in this section. To understand such graphs we need some definitions which describe ways of “going from

&lt;page_number&gt;221&lt;/page_number&gt;

---


## Page 26

Graph Theory

one vertex to another”. We shall first give these definitions in the following subsection.

## 2.2.1 Paths, Circuits and Cycles

Consider the graph in Fig.1. Imagine yourself walking along its edges, going from vertex to vertex.

&lt;img&gt;Fig.1&lt;/img&gt;

Suppose we want to start at the vertex x₁ and reach the vertex x₁₂. Is this possible? One possible way is to start from vertex x₁, walk along the edge x₁x₂, reach x₂, walk along the edge x₂x₃, reach x₃, walk along x₃x₄, reach x₄, and continue this till we reach x₁₂. Suppose we denote the edge joining xᵢ₋₁ and xᵢ as xᵢ₋₁xᵢ. Then we can describe this „walk“ in an alternating sequence of vertices and edges as x₁, x₁x₂, x₂, x₂x₃, x₃, x₃x₄, x₄x₅, x₅, x₅x₆, x₆, x₆x₉, x₉, x₉x₁₀, x₁₀, x₁₀x₁₁, x₁₁, x₁₁x₁₀, x₁₀, x₁₀x₁₃, x₁₃, x₁₃x₁₂, x₁₂. This is by no means the shortest way to reach x₁₂ from x₁. We could have gone from x₁ to x₅ directly. Moreover, we passed through the vertex x₁₀ twice. This is not necessary. So the walk above can be described as a leisurely walk. If we have more time at our disposal, we can trace and retrace more edges. For example, we could have gone from x₆ to x₉, and again back to x₆.

So what are we doing when choosing a walk? We are, in fact, choosing a sequence whose elements are vertices and edges, alternately. Let us formally define a walk.

**Definition:** A **walk** in a graph G is a finite sequence W = {v₀, e₁, v₁, e₂, … , eₖ, vₖ}, where v₀, v₁ ,..., vₖ are vertices of G and e₁, e₂,..., eₖ are edges joining the vertices vᵢ₋₁ and vᵢ; 1≤i≤k. (Note that all the vᵢs or eᵢs may not be distinct. There may be repetition.)

In this case we say that W is a **walk from v₀ to vₖ**, or W is a **v₀-vₖ walk**, or W is a **walk joining v₀ and vₖ**. The vertex v₀ is called the **initial vertex** and the vertex vₖ is called the **end vertex** of the walk W. The **number of edges contained in a walk**, i.e., k, is called the **length** of the walk W, and is denoted by ℓ(W). Since the vertices as well as the edges can be repeated, the length can very well be greater than the number of edges of the graph G.

**Note:** As you have seen, in a walk the vertices as well as edges can be repeated. So we cannot view this as a subgraph unless all the vertices as well as the edges in the walk are distinct.

Let’s consider an example.

**Example1**: Consider the graph on 5 vertices and 7 edges given in Fig.2. Find x₁-x₅ walks of length 8 and length 4, respectively.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;222&lt;/page_number&gt;

---


## Page 27

Connectedness

&lt;img&gt;Fig. 2&lt;/img&gt;

**Solution:** Consider the walk
W = {X₁, X₁ X₂, X₂, X₂ X₃, X₃, X₃ X₄, X₄, X₄ X₂, X₂, X₂ X₅, X₅, X₅ X₃, X₃, X₃ X₄, X₄, X₄ X₅, X₅}.
Then W is an x₁-x₅ walk of length 8.

Again, W' = {x₁, x₁x₂, x₂, x₂x₄, x₄, x₄x₃, x₃, x₃x₅, x₅} is an x₁-x₅ walk of length 4.

***

Why don't you try an exercise now?

E1) For the graph given in Fig.3, find a u-v walk of length 7.
&lt;img&gt;Fig.3&lt;/img&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

Since we are considering only simple graphs, we often write a walk W as {v₀, v₁, ..., vₖ}. While doing so, we assume that two consecutive vertices in the walk are joined by an edge in the graph, and that edge is included in the walk. For example, the x₁-x₁₂ walk corresponding to Fig.1 that we discussed can be written as
W = {x₁, x₂, x₃, x₄, x₅, x₆, x₉, x₁₀, x₁₁, x₁₀, x₁₃, x₁₂}.

Let us now consider some particular kinds of walks, that we use in studying computer science.

**Definitions :**

1) A walk W is called a **path** if all its vertices are distinct, and hence, all its edges are distinct.

2) A u-v walk is **closed** if u = v, and **open** if u ≠ v.

3) A walk in which all the edges are distinct and the only repeated vertex is the first vertex, this being the same as the last vertex, is called a **cycle**. (Remember, we had introduced you to cycles in Unit 1.)

Let us consider an example.

**Example 2 :** In the graph in Fig.4, find the following:

i) a closed walk which is not a cycle;
ii) a walk which is not a path;
iii) a cycle.

**Solution:** i) There are several closed walks in it which are not cycles. For instance, W = {x₅, x₆, x₇, x₈, x₅, x₁₁, x₁₂, x₁₃, x₁₄, x₁₅, x₁₁, x₅} is a closed walk. Since the edge x₅ x₁₁ is repeated, it is not a cycle.

&lt;page_number&gt;223&lt;/page_number&gt;

---


## Page 28

Graph Theory

&lt;img&gt;Fig. 4 graph with vertices x1 to x15 and edges connecting them.&lt;/img&gt;

ii) W₀ = {x₅, x₆, x₇, x₈, x₅, x₉, x₁₀, x₅} is a walk. Here the vertex x₅ is repeated three times. Thus, this is not a path.

iii) W₁ = {x₅, x₆, x₇, x₈, x₅} is a cycle. So is W₂ = {x₁₁, x₁₂, x₁₃, x₁₄, x₁₅, x₁₁}.

*** Try these exercises now.

E2) If all edges are distinct, then all vertices are distinct. True or false ? Why ?

E3) Let G = (V, E) be a graph, where V = {t, u, v, w, x, y, z} and E = {tu, tv, tw, ux, vw, vy, uz, wx, wz, xy, xz}. In G, find
i) a u-v walk that is not a path,
ii) a (u-u) walk that is not a cycle,
iii) a (u-u) cycle of minimum length.

E4) Let G be a graph such that δ(G) ≥ k . Use the principle of induction to show that G has a path of length k starting at any given vertex.
(Recall that δ(G) = min {d_G(x) : x ∈ V(G)}.)

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

Now, we know that a walk need not be a path. However, we shall now prove that in any u-v walk, we can always find a path from u to v.

**Theorem 1:** If W is a u-v walk joining two distinct vertices u and v, then there is a path joining u and v contained in the walk.

**Proof:** We will prove this using the principle of mathematical induction on the length of the walk."

Let P(k) denote the statement ,,If W is a u-v walk of length k, then there exists a path joining u and v contained in W.

If k = 1, then P(1) is true since every walk of length 1 is a path.

Now, let us assume that the statement P(k-1) is true. In other words, we assume that given any x-y walk of length ≤ k-1, there exists a path joining x and y contained in the walk. Then we want to show that the statement P(k) is true.

So, consider the u-v walk W = {u = u₀, e₁, u₁, ..., eₖ, uₖ = v} of length k.
If W is already a path, we are done. Otherwise, there is at least one vertex which is repeated. Suppose j is the smallest integer such that the vertex uⱼ is repeated. Then

&lt;page_number&gt;224&lt;/page_number&gt;

---


## Page 29

there is an integer t > j such that u<sub>j</sub> = u<sub>t</sub>. Now consider the walk W<sub>1</sub> obtained by removing the part {e<sub>j+1</sub>, ..., e<sub>t</sub>} in W, that is,
W<sub>1</sub> = {u = u<sub>0</sub>, e<sub>1</sub>, ..., u<sub>j</sub> = u<sub>t</sub>, e<sub>t+1</sub>, ...e<sub>k</sub>, u<sub>k</sub> = v}. Clearly, W<sub>1</sub> is a u-v walk contained in the walk W, and its length is k-t+j<k, since j < t. Hence, by induction, we can get a path P joining u and v contained in W<sub>1</sub>. Since P is contained in W<sub>1</sub> and W<sub>1</sub> is contained in W, the path P is contained in the walk W.
So, the result is true for any walk of length k, i.e., P(k) is true.

Therefore, by induction, P(n) is true for all n. Hence the result.

**Note** that the theorem above does not say that there is a walk joining any two vertices in a graph. In fact, in many practical situations it is very important to know which vertices in a graph can be joined by a walk, **and hence** by a path. For instance, in the graph in Fig.5, there is no a-x walk. Hence there is no path from a to x.

Try an exercise now.

E5) Consider the walk {x<sub>3</sub>, x<sub>5</sub>, x<sub>2</sub>, x<sub>4</sub>, x<sub>3</sub>, x<sub>2</sub>, x<sub>1</sub>} in the graph given in Fig.2. Obtain two distinct x<sub>3</sub>-x<sub>1</sub> paths contained in this walk.

While studying networks, we often need to know whether two vertices in a graph are joined by a walk or not. This leads us to the definition of a connected graph, which we will introduce now.

## 2.2.2 Components

As you have noticed, almost all the graphs we have discussed so far have been „in one piece“. Some, like the one in Fig.5, are not. We can formalise this difference by introducing the concept of connectedness.

**Definition:** A graph G = (V, E) is called **connected** if for any two vertices u, v ∈ V, there exists a u-v walk in G. If G is not connected, then it is called **disconnected**.

This means that in a connected graph any two distinct vertices are joined by a path (by Theorem 1). For instance, K<sub>n</sub> is connected ∀n ≥1.However, a **null graph**, i.e., a graph whose edge set is empty, is totally disconnected (see Fig.6).

Here are some related exercises for you.

E6) Can a graph with one vertex be connected? Give reasons for your answer.

E7) Which of the graphs given in Fig.7 are connected?

&lt;img&gt;Fig.5&lt;/img&gt;

&lt;img&gt;Fig.6 : A null graph&lt;/img&gt;

&lt;img&gt;Fig.7&lt;/img&gt;

E8) “If a graph G is connected, then all its subgraphs are connected.” Prove or disprove this statement.

While solving E8, you would have realised that subgraphs of connected graphs need not be connected. Similarly, some subgraphs of disconnected graphs are connected. Let us discuss such subgraphs now.

&lt;page_number&gt;225&lt;/page_number&gt;

---


## Page 30

Graph Theory

**Definition:** Let G = (V, E) be a graph. A subgraph H of G is called a **component** of G if H is connected and it is not a subgraph of any other connected subgraph of G. Thus, a component of G is, in a sense, a „maximal“ connected subgraph of G.

The number of components of G is denoted by c(G). For instance, the graph in Fig.5 has two components, the graph in Fig.6 has 6 components, and the graph in Fig.1 has one component.

Let us consider another example.

**Example 3:** Find all the components of the graph G given in Fig.8.
&lt;img&gt;Fig.8&lt;/img&gt;
Fig.8

**Solution:** G has three components, given in Figures 9 (a), (b) and (c).
&lt;img&gt;Fig.9&lt;/img&gt;
Fig.9
* * *

You can now try this exercise.

---

E9) Consider the graph G given by Fig. 10. Find
(i) all the connected subgraphs of G;
(ii) all the components of G. Are they disjoint? Give reasons for your answer.
&lt;img&gt;Fig.10&lt;/img&gt;
Fig.10

---

Consider all the graphs you have seen so far in this unit. In each case, it can be written as a disjoint union of its components. This phenomenon generalizes to any graph, as you will see in the following theorem, which we shall only state.

**Theorem 2:** Every graph can be partitioned into its components.

&lt;page_number&gt;226&lt;/page_number&gt;

---


## Page 31

Connectedness

You may ask how this result can be of help. Knowing the number of components, for instance, helps us to find a bound for the number of edges of a graph. Here is a result about this, again without proof.

**Theorem 3:** If G is a graph with n vertices and k components, then G can have at least n-k edges, and at most $\frac{1}{2} (n-k)(n-k+1)$ edges.

A very useful result that immediately follows from this is :

**Corollary 1:** If G is a connected (n, m)-graph, then $n-1 \leq m \leq \frac{1}{2} n(n-1)$.

Try some exercises now.

E10) Give an example of a graph with
i) 4 components, each of which is complete;
ii) 3 components, where no two components are isomorphic.

E11) Can a graph have more components than vertices ? Give reasons for your answer.

&lt;watermark&gt;UNIVERSITY OF THE PEOPLE&lt;/watermark&gt;

Another approach used in the study of connected graphs is to ask „how connected“ a connected graph is. One possible interpretation of this question is to ask how many edges or vertices must be removed from the graph in order to disconnect it. We shall discuss this in the next subsection.

## 2.2.3 Connectivity

Let us now consider a graph showing an electric circuit (see Fig.11). This graph is connected. Suppose we cut the wire connecting d and e in the electric circuit. This means that in the graph showing the circuit, we are actually removing the edge de. When we cut the wire, the circuit becomes disconnected. Correspondingly, the removal of the edge de in the graph makes the graph disconnected.

Removing the edge de does not mean that we remove the vertices d and e.

&lt;img&gt;Fig.11&lt;/img&gt;

We just saw a situation in which the removal of one edge disconnects the graph. This lead us to the following definition.

**Definition:** An edge e of a connected graph G is called a **bridge** in G if the removal of e disconnects G. When we remove an edge e from the graph G, we denote the resulting graph by **G-e**.

Not every edge is a bridge. For instance, if we remove the edge ab in Fig. 11, the resulting graph is not disconnected. This also holds for the graph given in Fig. 12, which represents the roads connecting the main towns in a state.

&lt;page_number&gt;227&lt;/page_number&gt;

---


## Page 32

Graph Theory

&lt;img&gt;Fig. 12&lt;/img&gt;

In this case no edge is a bridge since there always exist alternative connections.

Here are some related exercises for you.

E12) Find the bridges in each of the graphs in Fig.13.
&lt;img&gt;Fig. 13 (a)&lt;/img&gt; &lt;img&gt;Fig. 13 (b)&lt;/img&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E.13) How many bridges do C_n and K_n have, where n≥3 ?

Let us consider the graph given in Fig.11 again. This graph is connected. Here, if we remove the edge de, then the resulting graph gets disconnected, the number of components becoming 2. On the other hand, if we remove the edge dc, then the graph does not get disconnected. Note that the edge dc belongs to the cycle {a, b, c, d, a}, but the edge de does not belong to any such cycle. The cycle seems to provide an alternative connection between the vertices c and d.

In fact, it follows from the definition of a bridge that **an edge e of a graph G is a bridge if and only if e does not belong to any cycle of G.**

While doing E13, you have obtained many graphs which do not have a bridge. To disconnect such a graph we need to remove more than one edge. Therefore, given a graph, it is natural to ask how many edges need to be removed before it gets disconnected. This leads us to the following definition.

**Definition:** The **edge-connectivity**, λ(G), of a connected graph G is the least number of edges that need to be removed for G to become disconnected.

For example, the edge-connectivity of any graph with a bridge is 1. Let us consider another kind of example.

**Example 4:** Find the edge-connectivity of the graph G given in Fig.14.
&lt;img&gt;Fig. 14&lt;/img&gt;

**Solution:** First note that this graph does not have any bridges. Therefore its edge-connectivity is more than 1. Now, if we remove the edges xz, zy, then the graph gets

&lt;page_number&gt;228&lt;/page_number&gt;

---


## Page 33

Connectedness

disconnected. Similarly, there are other sets of two edges, namely, {xv, vu}and {uw, wy}, the removal of which disconnects G. Therefore, the edge connectivity of G is 2.
***

**Note : In the context of computer networks, the edge-connectivity of a graph representing such a network gives the number of link failures that can be tolerated before the network becomes disconnected.**

Why don't you try some exercises now?

E14) Find the edge-connectivity of C<sub>n</sub> and K<sub>n</sub> for n≥3.

E15) Find λ (G), where G is the Petersen graph.

Let us now look at a particular type of set of edges of a connected graph.

**Definition : A cutset of a connected graph G is a set S of edges with the following properties:**

i) the removal of all the edges in S disconnects G;
ii) the removal of any proper subset of S will not disconnect G.

For example, consider the graph given in Fig.15

&lt;img&gt;Fig.15&lt;/img&gt;

The set {uw, ux, vx} and {uw, wx, xz} are cutsets for this graph. However, the set {uw, wx, xz, yz} is not a cutset since this set has a subset {uw, wx, xz}, the removal of which disconnects G.

**Note : 1) Two cutsets of a graph need not have the same number of edges. For example, the sets {uw, ux, vx} and {wy, xz} are both cutsets of the graph in Fig.15.**

2) The edge-connectivity of a graph G is the size of the smallest cutset of G.

Try this exercise now.

E16) Which of the following sets of edges are cutsets of the graph given in Fig.16, and what is the edge-connectivity of the graph ?
i) {su, sv},
ii) {uv, wx, yz},
iii) {ux, vx, wx, yz},
iv) {yt},
v) {wx, xz, yz},
vi) {uw, wx, wy}

&lt;img&gt;Fig.16&lt;/img&gt;

We can also think of connectivity in terms of the minimum number of vertices which need to be removed in order to disconnect a graph. Remember that, when we remove an edge, we do not remove its end vertices. However, **when we remove a**
&lt;page_number&gt;229&lt;/page_number&gt;

---


## Page 34

Graph Theory

vertex, then any edge incident with that vertex also gets removed.

Analogous to the notion of a bridge, we define a cut-vertex.

**Definition :** A **cut-vertex** of a connected graph G is a vertex v of G such that G–v is disconnected.

For instance, in Fig. 11, both d and e are cut-vertices.

Now we can define vertex-connectivity and a vertex-cutset on similar lines as we have done for edges. Why don’t you try it for yourself (see E 17)?

E17) Define vertex-connectivity and vertex-cutset of a graph.
E18) Find the vertex-connectivity and a vertex-cutset for the graph given in Fig. 16.

Once again, if a graph represents a computer network, then its **vertex connectivity** gives the number of node failures that the network can tolerate.

We shall now introduce you to another type of graph which underlies many computer, and other, applications.

## 2.3 BIPARTITE GRAPHS

In this section we shall define bipartite graphs and explain their importance through various problems. Let us first start with the following problem.

Four persons x₁, x₂, x₃ and x₄ are available to fill five jobs y₁, y₂, y₃, y₄ and y₅. x₁ is qualified for the jobs y₁ and y₂; x₂ is qualified for the jobs y₁ and y₃; x₃ is qualified for the job y₄; and x₄ is qualified for the jobs y₂, y₃ and y₅. The assignment problem is concerned with the following questions:

i) Can each person be assigned to a single job for which she is qualified?
ii) If so, how should the assignment be made?
iii) If assigning to a single job is not possible, at most how many jobs should be assigned to each person ?

The problem of the kind stated above is known as an assignment problem. To solve this problem it is convenient to consider the following graph-theoretic model of the situation (see Fig. 17).

&lt;watermark&gt;GOVERNMENT UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;
A diagram showing four vertices labeled x₁, x₂, x₃, and x₄ on the left side, and five vertices labeled y₁, y₂, y₃, y₄, and y₅ on the right side. There are multiple edges connecting each xᵢ to each yⱼ, indicating that each person is qualified for all jobs.
&lt;/img&gt;

Fig. 17

The graph G, representing the problem, has an edge joining xᵢ and yⱼ if xᵢ is qualified for the job yⱼ. Then the problem of assigning people to jobs for which they are

&lt;page_number&gt;230&lt;/page_number&gt;

---


## Page 35

Connectedness

qualified is equivalent to the problem of selecting a subset of the set of edges such that each x will be connected to exactly one y by one of these edges.

Now, if you look at the graph given in Fig. 17, you will see that the set of its vertices can be divided into two disjoint subsets such that no two vertices in a subset are adjacent. Let us formally define such graphs.

**Definition:** A graph G is said to be **bipartite** if V(G) = X ∪ Y, where X and Y are non-empty sets such that X ∩ Y = φ and every edge in E(G) has one end vertex in the set X and the other end vertex in the set Y. The sets X and Y form a **partition** of the set V(G), and we often say that X ∪ Y is a **bipartition** of the graph G. We also denote such a graph by **G(X,Y)**.

An alternative way of thinking of a bipartite graph is in terms of colouring its vertices with two colours, say red and blue — a graph is bipartite if we can colour each vertex red or blue in such a way that every edge has a red end and a blue end.

Bipartite graphs are useful in studying various real-life problems, including neural networks. One model that emulates the essential working of the network using graph theory is given in Fig. 18. As you can see, this is a bipartite graph, so that the properties of bipartite graphs are useful for studying this model.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig.18&lt;/img&gt;

Let us consider some other examples of bipartite graphs.

**Example 5:** Show that C₆ is bipartite and K₃ is not bipartite.

**Solution:** In Fig. 19 we show C₆. Since V(C₆) can be partitioned into {a, c, e} and {b, d, f}, C₆ is bipartite.

In K₃ each vertex is adjacent to every other vertex. Therefore, no bipartition is possible.

***

Note that in a bipartite graph G(X,Y), it is not necessary that each vertex of X is joined to each vertex of Y. For instance, in C₆ in Fig. 19, a is not joined to d. This leads us to the following definition.

**Definition:** A **complete bipartite graph** is a bipartite graph G(X,Y) in which each x ∈ X is joined to every y ∈ Y, i.e., G is also a complete graph. If |X| = r and |Y| = s, we denote G(X,Y) by **Kᵣₛ**. In Fig. 20 we have shown a few of these graphs.

&lt;img&gt;Fig.19 : C₆ is bipartite&lt;/img&gt;
&lt;page_number&gt;231&lt;/page_number&gt;

---


## Page 36

Graph Theory

&lt;img&gt;K1,5 graph&lt;/img&gt;
K₁₅

&lt;img&gt;K3,4 graph&lt;/img&gt;
K₃₄

&lt;img&gt;K3,3 graph&lt;/img&gt;
K₃₃

Fig 20 : Some complete bipartite graphs

Now, given a bipartite graph, you may wonder if the bipartition is unique. The following example will give you an answer to this question.

**Example 5:** Find two different bipartitions of the graph given in Fig.21.

&lt;img&gt;Fig.21 graph&lt;/img&gt;
Fig.21

**Solution:** The vertex set is {x₁, x₂, y₁, y₂, y₃, z₁, z₂}.
One way of partitioning this can be by taking X = {x₁, x₂, z₂}, Y = {z₁, y₁, y₂, y₃}.
Another way can be X₁ = {x₁, x₂, y₃}, Y₁ = {z₂, z₁, y₁, y₂}.
Both these partitions make G bipartite.
***
Note that the graph in Fig.21 is not connected. Had it been connected it would not have been possible to find more than one bipartition of G. In fact, we have the following theorem.

**Theorem 4:** A connected bipartite graph has a unique bipartition.

We shall now state a theorem, which gives a characterisation for bipartite graphs.

**Theorem 5:** A graph G is bipartite if and only if G does not contain any cycle of odd length as a subgraph.

This result is very useful. For instance, using it we know that **Cₙ is not bipartite whenever n is odd.**

You can try some exercises now.

E19) Check whether the hypercube Q₃ and the star graphs are bipartite.

E20) For which values of m and n is Kₘ,ₙ regular ?

E21) i) Is the subgraph of a bipartite graph bipartite ?
ii) Is the complement of a bipartite graph bipartite ?
Give reasons for your answers.

E22) Show that if G₁, ..., Gₙ are bipartite, then ⋃ᵢ₌₁ⁿ Gᵢ is bipartite.

&lt;watermark&gt;GOVERNMENT OF THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;232&lt;/page_number&gt;

---


## Page 37

Connectedness

Let us now go back to the assignment problem. In that problem we are interested in finding those special subgraphs of the associated bipartite graph which give a solution to the problem. We have defined such subgraphs below.

**Definition:** A **matching** in a bipartite graph G is a set of edges such that no two edges have a common end vertex. In other words, a matching in G (X,Y) defines a one-to-one correspondence between the vertices in a subset of X and the vertices in a subset of Y.

For example, Fig.22 shows a bipartite graph and one of its matchings. Can you find any other matching? We leave this as an exercise for you to check (see E 23 ).

&lt;img&gt;
(a)
A bipartite graph with four vertices on the left side labeled 1, 2, 3, 4 and four vertices on the right side labeled A, B, C, D.
Edges connect:
1-A, 1-B, 1-C, 1-D
2-A, 2-B, 2-C, 2-D
3-A, 3-B, 3-C, 3-D
4-A, 4-B, 4-C, 4-D
&lt;/img&gt;

(b)
A matching in G showing:
1-A
2-B
3-D
&lt;/img&gt;

Fig.22 : a) G is bipartite; b) A matching in G

Related to the concept of matching, we have another concept.

**Definition:** A matching of X into Y is called a **complete matching** of X and Y if there is an edge incident with every vertex in X. In other words, a matching is complete if a one-to-one correspondence is defined between all the vertices in X and the vertices in a subset of Y.

Is the matching given in Fig.22 (b) a complete matching? No, because in this matching, the vertex 4 is not included.

In graph-theoretic terminology, the **assignment problem** can be stated in the following way: if G = G (X, Y) is a bipartite graph, when does there exist a complete matching from X to Y in G? So, for a given bipartite graph, we want to know whether there is a complete matching of the set of vertices in X into the set of vertices in Y. The following theorem gives a **necessary and sufficient condition** for the existence of such a matching. As before we shall only state the theorem, omitting the proof.

**Theorem 6:** Let G = G (X, Y) be a bipartite graph. A complete matching of X into Y exists in G if and only if |A| ≤ |R(A)| for every subset A of X, where |A| denotes the number of elements in A (also called cardinality of A) and R(A) denotes the set of vertices in Y that are adjacent to the vertices in A.

Let us apply this theorem to the assignment problem in the following example.

**Example 6**: Verify the conditions of Theorem 6 for the assignment problem given at the beginning of this section (see Fig.17).

**Solution**: To check the theorem we have to consider all subsets of the vertex set X = {x₁,x₂,x₃,x₄}, their cardinality, the corresponding sets R(A), and their cardinality. Table 1 gives a list of all the possibilities.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;233&lt;/page_number&gt;

---


## Page 38

Graph Theory

Table 1

<table>
<thead>
<tr>
<th>A</th>
<th>|A|</th>
<th>R(A)</th>
<th>|R(A)|</th>
</tr>
</thead>
<tbody>
<tr>
<td>∅</td>
<td>0</td>
<td>∅</td>
<td>0</td>
</tr>
<tr>
<td>{x₁}</td>
<td>1</td>
<td>{y₁,y₂}</td>
<td>2</td>
</tr>
<tr>
<td>{x₂}</td>
<td>1</td>
<td>{y₂,y₃}</td>
<td>2</td>
</tr>
<tr>
<td>{x₃}</td>
<td>1</td>
<td>{y₄}</td>
<td>1</td>
</tr>
<tr>
<td>{x₄}</td>
<td>1</td>
<td>{y₂,y₃,y₅}</td>
<td>3</td>
</tr>
<tr>
<td>{x₁,x₂}</td>
<td>2</td>
<td>{y₁,y₂,y₃}</td>
<td>2</td>
</tr>
<tr>
<td>{x₂,x₃}</td>
<td>2</td>
<td>{y₁,y₃,y₄}</td>
<td>2</td>
</tr>
<tr>
<td>{x₃,x₄}</td>
<td>2</td>
<td>{y₂,y₃,y₄,y₅}</td>
<td>4</td>
</tr>
<tr>
<td>{x₁,x₄}</td>
<td>2</td>
<td>{y₁,y₂,y₃,y₅}</td>
<td>4</td>
</tr>
<tr>
<td>{x₂,x₄}</td>
<td>2</td>
<td>{y₁,y₂,y₃,y₄}</td>
<td>4</td>
</tr>
<tr>
<td>{x₁,x₃}</td>
<td>2</td>
<td>{y₁,y₂,y₄}</td>
<td>3</td>
</tr>
<tr>
<td>{x₁,x₂,x₃}</td>
<td>3</td>
<td>{y₁,y₂,y₃,y₄}</td>
<td>4</td>
</tr>
<tr>
<td>{x₂,x₃,x₄}</td>
<td>3</td>
<td>{y₁,y₂,y₃,y₄,y₅}</td>
<td>5</td>
</tr>
<tr>
<td>{x₁,x₃,x₄}</td>
<td>3</td>
<td>{y₁,y₂,y₃,y₄}</td>
<td>4</td>
</tr>
<tr>
<td>{x₁,x₂,x₄}</td>
<td>3</td>
<td>{y₁,y₂,y₃,y₅}</td>
<td>4</td>
</tr>
<tr>
<td>{x₁,x₂,x₃,x₄}</td>
<td>4</td>
<td>{y₁,y₂,y₃,y₄,y₅}</td>
<td>5</td>
</tr>
</tbody>
</table>

It shows that the condition |A|≤|R(A)| is satisfied for all subsets A of X. Hence the condition of Theorem 6 is satisfied. This shows that there exists a complete matching from X into Y for the assignment problem. Therefore, the assignment problem is solved.

***
You can now try an exercise.
***
E 23) For the bipartite graph given in Fig.22, find a matching, apart from the given one. Does the graph have a complete matching ? Give reasons for your answer.
***
Let us now see another type of graph which has come into prominence because of its applications to electrical networks.
***
## 2.4 TREES
***
We are all familiar with the idea of a family tree. The concept of a tree in graph theory first arose in connection with work of a mathematician G. Kirchhoff on electric networks in the 1840s, and with the work of another mathematician Cayley on the enumeration of chemical molecules in the 1870s. More recently, trees are used in many areas, ranging from linguistics to computing. For instance, trees are used to study the following problems:
* How should items in a list be stored so that an item can be easily located ?
* How should a set of characters be efficiently coded by bit strings ?

So, let us begin our study of trees by considering the following graphs.

&lt;img&gt;G&lt;/img&gt; &lt;img&gt;H&lt;/img&gt;
&lt;page_number&gt;234&lt;/page_number&gt;
Fig.23

---


## Page 39

Connectedness

Can you find any difference in their structures ? You might have noticed that G is disconnected, and has no cycles. On the other hand, H is connected and has no cycles. From the following definition you will see that H is an example of a tree.

**Definition :** A **tree** is a connected graph with no cycles. A **forest** is a graph, each of whose components is a tree.

Fig.24 shows a graph with four components, each of which is a tree. Hence, the graph is a forest.

&lt;img&gt;Fig.24&lt;/img&gt;

A tree has several defining properties which we shall list in the following theorem.

**Theorem 7 :** Let G be a graph with n vertices. Then the following statements are equivalent.

i) G is a tree.
ii) G has no cycles and has (n – 1) edges.
iii) G is connected and has (n – 1) edges.
iv) G is connected and every edge is a bridge.
v) Any two vertices of G are connected by exactly one path.

**Proof :** If n = 1, all the five results are trivial. We shall, therefore, assume that n ≥ 2. Now, from your study of mathematical logic you know that if we prove (i) ⇒(ii), (ii) ⇒(iii), (iii) ⇒(iv), (iv) ⇒ (v) and (v) ⇒ (i), then all the statements will be proved to be equivalent. So, let us prove the implications one by one.

(i) ⇒ (ii) : By definition, G does not have any cycles. We shall show that G has (n – 1) edges, by induction.
If n = 2, then the number of edges is 1. Therefore, the result is true for n = 2.
So, now let us assume that every tree on p vertices has (p – 1) edges for any positive integer p such that 2 ≤ p < n. Then we have to show that every tree on n vertices has (n – 1) edges.
Now suppose we remove any edge. Since G has no cycles, the removal of any edge disconnects G into two graphs G₁ and G₂, such that G₁ and G₂ are connected and have no cycles. Therefore, G₁ and G₂ are trees and each has less than n vertices.
Let n₁ and n₂ be the vertices in G₁ and G₂. Then n₁ + n₂ = n.
Since n₁ and n₂ are less than n, by our induction assumption, the number of edges in G₁ and G₂ are n₁ – 1 and n₂ – 1, respectively. Therefore, the total number of edges in both the graphs is n₁ + n₂ – 2 = n – 2. These edges, together with the edge which is removed, will give the total total number of edges in the original graph. Therefore, the total total number of edges in G is n – 1.

Thus, we have shown that every tree on n vertices has n – 1 edges. By induction, this is true for all n.

(ii) ⇒ (iii) : Suppose that G is disconnected. Let c(G) = t > 1. Let G₁,G₂,…,Gₜ be the components of G such that the number of vertices in each Gᵢ is pᵢ for i = 1,2,…,t, and the number of edges in each Gᵢ is qᵢ, for i = 1,2,…,t. Then p = p₁ + p₂ + … + pₜ, q = q₁+…+qₜ.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;235&lt;/page_number&gt;

---


## Page 40

Graph Theory

Now, since every G<sub>i</sub> is connected and without cycles, G<sub>i</sub> is a tree for i = 1,2,...,t.
Therefore, by what we have shown while proving (i) ⇒ (ii), q<sub>i</sub> = p<sub>i</sub> - 1 ≤ i ≤ t. Then
p - 1 = q = q<sub>1</sub> + ... + q<sub>t</sub> = p - t.
That is, t = 1, which contradicts our assumption that t > 1. Therefore, G is connected.

(iii) ⇒ (iv) : Suppose there is an edge which is not a bridge. Then the removal of that
edge will result in a graph with n vertices and (n-2) edges. This is not possible when
G is connected, by Corollary 1 to Theorem 3. Therefore, every edge is a bridge.

(iv) ⇒ (v) : Since T is connected, each pair of vertices is connected by at least one
path. If a given pair of vertices is connected by two paths, then they form a cycle,
which contradicts the fact that every edge is a bridge. Therefore, there is a unique path
joining any two vertices.

(v) ⇒ (i) : We are assuming that any two vertices are connected by a unique path. So,
the graph G is connected. Now, suppose G contains a cycle C = {x<sub>0</sub>,x<sub>1</sub>,...,x<sub>n</sub>=x<sub>0</sub>}.
Then we can find two distinct paths P<sub>1</sub> = {x<sub>0</sub>,x<sub>1</sub>} and P<sub>2</sub> = {x<sub>0</sub>,x<sub>n-1</sub>,...,x<sub>2</sub>,x<sub>1</sub>}
connecting the vertices x<sub>0</sub> and x<sub>1</sub>, which contradicts our assumption. Therefore, G
does not contain any cycle, and hence, is a tree.

Why don’t you try some exercises now ?

E24) For which values of m and n is K<sub>m,n</sub> a tree ?
E25) Which of the following graphs are trees, and why ?

&lt;img&gt;Graph (a)&lt;/img&gt;
(a)

&lt;img&gt;Graph (b)&lt;/img&gt;
(b)

&lt;img&gt;Graph (c)&lt;/img&gt;
(c)

&lt;img&gt;Graph (d)&lt;/img&gt;
(d)

Fig.25

The theorem above tells us that a tree has got several nice properties which a general
graph does not have. In fact, the importance of trees in graph theory is that every
connected graph contains a tree which has all the vertices of the original graph, as you
will now see.

Let us consider a connected graph G. Consider a cycle in it and remove one of its
edges such that the resulting graph stays connected. We repeat this procedure with one
of the remaining cycles, continuing until there are no cycles left. The graph which
remains is a connected subgraph of G which does not have any cycle. Therefore, it is a
tree. Note that this tree has all the vertices of G. Such a graph is called a spanning tree,
as you will realize from the following definition.

**Definition** : A **spanning tree** for a graph G is a subgraph of G which contains all the
vertices of G and is a tree.

This concept is useful for finding, for example, the minimum number of roads to be
kept open to maintain connections in a given transport network.

Now, the question is whether every graph has a spanning tree. The following theorem,
the proof of which is omitted, tells us about this.

**Theorem 7** : A graph G is connected **if and only if** it has a spanning tree.

&lt;page_number&gt;236&lt;/page_number&gt;

---


## Page 41

Connectedness

The theorem above tells us that in a graph with k components, each component will have a spanning tree. Because of this result and because of the special structure of trees, in trying to prove a general result in graph theory, it is sometimes convenient to try to prove the corresponding result for a tree. The general result would, then, follow.

**Note : A spanning tree is not unique.** For instance, Fig. 26 shows a connected graph G and two of its spanning trees, T₁ and T₂.

&lt;img&gt;Fig. 26 - Graph G and its spanning trees T₁ and T₂&lt;/img&gt;

You can try some exercises now.

E26) Draw three spanning trees of the following graph.
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig. 27 - Graph with vertices A, B, C, D, E&lt;/img&gt;

E27) Is a tree a bipartite graph ? Give reasons for your answer.

Spanning trees are important in data networking, particularly in multicasting over Internet Protocol (IP) networks. To send data from a source computer to multiple receiving computers, each of which is a subnetwork, data could be sent separately to each computer. This type of networking, called unicasting, is inefficient, since many copies of the same data are transmitted over the network. To make the transmission of data to multiple receiving computers more efficient, IP multicasting is used. With IP multicasting, a computer sends a single copy of data over the network, and as data reaches intermediate routers the data are forwarded to one or more other routers so that ultimately all receiving computers in their various subnetworks receive these data.

For data to reach receiving computers as quickly as possible, there should be no loops (which in graph theory terminology are circuits or cycles) in the path that data take through the network. That is, once data have reached a particular router, data should never return to this router. To avoid loops, the multicast routers use network algorithms to construct a spanning tree in the graph that has the multicast source, the routers, and the subnetworks containing receiving computers as vertices, with edges representing the links between computers and/or routers.

So far we have seen three types of graphs : connected graphs, bipartite graphs and trees. You will see several other types of graphs in the following units. Let us now summarise what we have covered in this unit.

&lt;page_number&gt;237&lt;/page_number&gt;

---


## Page 42

Graph Theory

# 2.5 SUMMARY

In this unit we have discussed the following points.

1) The definition and use of the terms ‘walk’, ‘path’ and ‘cycle’ in a graph. We have also proved and used the fact that in every u-v walk there is a u-v path.
2) Properties of connected graphs, how to find components of a graph, the effect of removal of a vertex or an edge on the number c(G) of the components of a graph G.
3) The application of the fact that if G is a (p,q)-graph with k components, then p − k ≤ q ≤ 1/2(p − k)(p − k + 1).
4) The definition and properties of bipartite graphs, and a characterisation of such graphs in terms of not containing odd cycles.
5) What a matching is, and when a complete matching exists.
6) Explanation of trees and spanning trees, particularly the importance of such graphs among the class of all connected graphs.
7) The proof and application of the statement that a graph G with n vertices is a tree iff it has no cycles and has (n−1) edges iff it is connected and has (n−1) edges.

&lt;watermark&gt;UNIVERSITY OF THE PEOPLE'S&lt;/watermark&gt;

# 2.6 SOLUTIONS/ANSWERS

E1) {u, uv, ux, x, xy, y, yv, v, vb, b, bu, u, uv, v} is a walk of length 7. This is not the only one. Think of some others too.

E2) False. For instance, in a cycle all the edges are distinct, not all the vertices.

E3) i) It is easy to find examples if you draw the walk. One example is {u,x,w,z,y,x,w,v}. There are other examples.

ii) W = {u,v,y,z,w,x,z,u} is a walk in which the vertex z is repeated. Therefore, W is not a cycle.

iii) W₀ = {u,t,w,x,u} is a cycle such that all other cycles have length greater than l(W₀).

E4) We use induction on k. If k = 1, then every vertex has at least one neighbour. Thus, there exists a path of length 1 starting at any vertex. Now, by induction, assume that in every graph H with δ(H) ≥ (k−1), there is a path of length (k−1) starting at any given vertex.

Let G be a path with δ(G) ≥ k (>1). Let x₀ be any vertex in G. Choose any edge e₁ incident on x₀. Consider G−e₁. Removal of one edge reduces only the degree of its end vertices by one. Thus, δ(G − e₁) ≥ (k − 1). Thus, by induction, there is a path {x₁,e₂,...,eₖ,xₖ} of length (k−1) in G₁. Moreover, since the degree of xₖ₋₁ is at least k, we can choose xₖ different from x₀,x₁,...,xₖ₋₂. Also {x₀,e₁,x₁,e₂,...,xₖ} is a path of length k in G starting from x₀. Therefore, there exists a path of length k starting at any vertex in G.

&lt;page_number&gt;238&lt;/page_number&gt;

---


## Page 43

Connectedness

Since this is true for all k, the result follows.

E5) {x₃, x₅, x₂, x₁} and {x₃, x₂, x₁}.

E6) It is connected. Because if it is disconnected then there exists two distinct vertices which are not joined by a path, which is not possible since the graph does not have two distinct vertices.

E7) (a) and (b) are connected, (c) is disconnected.

E8) The statement is false. For example, consider the graph K₃ given in Fig.28(a). The subgraph of this graph obtained by deleting the edges v₁v₃ and v₂v₃, given in Fig.28(b), is not connected.

&lt;img&gt;Fig.28&lt;/img&gt;

E9) i) The graphs having single vertices a,b,c,d,e,f, and the graphs having the following vertices and edges

i) V = {a,b}, E = {ab}
ii) V = {a,c}, E = {ac}
iii) V = {c,d}, E = {cd}
iv) V = {c,f}, E = {cf}
v) V = {d,c,a}, E = {dc,ca}
vi) V = {b,a,c}, E = {ba,ac}
vii) V = {a,b,c,d}, E = {ab,ac,cd}

ii) Two components are the graph formed by the vertices a,b,c and d, and the graph formed by the vertices e and f. They are disjoint, for if they have a vertex in common the two component graphs would be connected.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E10) An example each is given below. You can think of many others.

&lt;img&gt;Fig.29 : K₃ ∪ K₄ ∪ K₁ ∪ K₅&lt;/img&gt;

&lt;img&gt;Fig.30&lt;/img&gt;

E11) No, since each component must contain at least one vertex.

&lt;page_number&gt;239&lt;/page_number&gt;

---


## Page 44

Graph Theory

E12) In (a) there is only one bridge given by bc. In (b) there are several bridges, e.g., u₁u₃, u₃u₆, u₅u₆.

E13) None.

E14) λ(Cₙ) = 2, λ(Kₙ) = n - 1.

E15) λ(G) = 3.

E16) The sets given in (i), (iii), (iv) and (vi) are cutsets. The set given in (ii) is not a cutset, since its removal does not disconnect the graph; the set given in (v) is also not a cutset, since we can disconnect the graph by removing just xz and yz.

E17) The **vertex-connectivity** of a connected graph G is the smallest number of vertices whose removal disconnects G.

A **vertex-cutset** of a connected graph G is a set H of vertices with the following properties :

i) the removal of all vertices in H disconnects G;
ii) the removal of any proper subset of H will not disconnect G.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E18) The vertex-connectivity is 1, and the vertex-cutset is {w}.

E19) Q₃ does not contain any odd cycle. Therefore, by Theorem 5, it is bipartite. The star network with n+1 vertices is K₁,n, and hence, is bipartite.

E20) Only for m=n, is Kₘ,ₙ regular.

E21) i) Yes. Let G be a bipartite graph, with a bipartition X ∪ Y. Let H be a subgraph of G. If V(H) is disjoint from either X or Y, then E(H) = φ. And then, any partition of V(H) into two subsets will serve as a bipartition. In the other situation, (V(H) ∩ X) ∪ (V(H) ∩ Y) is a bipartition of V(H).

ii) No, e.g., the complement of G given in Fig.21 contains C₇. So, by Theorem 5, G is not bipartite.

E22) Let Gᵢ, 1 ≤ i ≤ n, be bipartite graphs with the bipartitions V(Gᵢ) = Xᵢ ∪ Yᵢ, respectively. Let G = ⋃ᵢ₌₁ⁿ Gᵢ. Then E(G) is the disjoint union ⋃ᵢ₌₁ⁿ E(Gᵢ). V(G) = A ∪ B, where A = ⋃ᵢ₌₁ⁿ Xᵢ and B = ⋃ᵢ₌₁ⁿ Yᵢ, is a bipartition of V(G). This can be seen as follows : Let e be an edge in E(G). Since E(G) is a disjoint union of E(G₁),...,E(Gₙ), the edge e belongs to only one of them. Without loss of generality, suppose e ∈ E(Gᵣ). Since Gᵣ is bipartite with a bipartition Xᵣ ∪ Yᵣ, this means e has one end vertex in Xᵣ and the other in Yᵣ, that is, e has one end vertex in A and the other in B. Thus, G is bipartite with a bipartition A ∪ B.

E23) Fig.31 gives another matching, which is in fact a complete matching.

&lt;page_number&gt;240&lt;/page_number&gt;

---


## Page 45

Connectedness

&lt;img&gt;A line with four points labeled 1, 2, 3, 4 connected to A, B, C, D respectively.&lt;/img&gt;

Fig.31

E24) For m=1, n ≥1 or n =1 and m ≥1 only. For m ≥ 2, n ≥ 2, K<sub>m,n</sub> will contain a cycle.

E25) The ones in (a) and (c) are trees by Condition (iii), Theorem 7. The one in (b) is not, for the same reason. The one in (d) is not because it contains C<sub>5</sub>.

E26) &lt;img&gt;Three graphs. The first graph has two vertical lines, each ending in a point, which are then connected by a horizontal line to another point. The second graph has a vertical line ending in a point, which is then connected to a horizontal line that connects to another point. The third graph has a vertical line ending in a point, which is then connected to a horizontal line that connects to another point, which is then connected to a third point.&lt;/img&gt;
Fig.32

E27) Yes. Since a tree does not have any cycles, by Theorem 5 it is a bipartite graph.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;241&lt;/page_number&gt;

---


## Page 46

&lt;img&gt;IGU logo&lt;/img&gt;
THE PEOPLE'S UNIVERSITY

---


## Page 47

# UNIT 3 EULERIAN AND HAMILTONIAN GRAPHS

## Structure

3.0 Introduction
3.1 Objectives
3.2 Eulerian Graphs
3.3 Hamiltonian Graphs
3.4 Travelling Salesperson Problem
3.5 Summary
3.6 Solutions / Answers

## 3.0 INTRODUCTION

Suppose you go to a new city as a salesperson. You would naturally like to familiarise yourself with all the important routes. One way to do this is to buy a map of the city and go around the city. If you do this without proper planning, you may pass through some of the streets more than once. To avoid this, you would need to sit down and plan your route. The most efficient route would involve traversing every street in it only once. But is it possible to find such a route?

This question is so natural that you may not be surprised to know that a similar question was raised more than 250 years ago. Königsberg was a city in what was known as Prussia those days. The Pregel river flowed through this city forming two islands (see B and C in Fig.1).

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig. 1: A schematic diagram of Königsberg&lt;/img&gt;

The two islands and the rest of the city were connected to each other by seven bridges. Some of the citizens used to amuse themselves with the following question: Is it possible to go around the city using each bridge exactly once?

In 1736, the great Swiss mathematician Leonhard Euler (pronounced as ‘oiler’) answered this question by converting this into a problem in graph theory. We will see this problem in Section 3.2 (Sec.3.2 in brief), while discussing graphs named after Euler.

There is one more question similar to the Königsberg problem in recreational mathematics — which figures can be drawn without lifting the pen from the paper and without going over any of the lines twice? This question is also answered in Sec.3.2. A mathematical puzzle invented by Hamilton involves finding a cycle containing all the vertices of a certain graph. Motivated by this, we will discuss conditions for a

&lt;img&gt;Fig. 2: Leonhard Euler (1707-1783)&lt;/img&gt;

&lt;page_number&gt;243&lt;/page_number&gt;

---


## Page 48

Graph Theory

graph to contain a cycle containing all the vertices of the graph. Such as graph is called a Hamiltonian graph, in honour of Hamilton. In Sec. 3.3 we will give some necessary and sufficient conditions for a graph to be Hamiltonian.

Finally, in Sec.3.4 we discuss a related question, the travelling salesperson problem.

## 3.1 OBJECTIVES

After studying this unit, you should be able to

*   check whether a given graph is Eulerian or not;
*   check whether a given graph satisfies certain necessary conditions for a Hamiltonian graph;
*   check whether a given graph satisfies certain sufficient conditions for a Hamiltonian graph;
*   apply the 1-exchange algorithm to reduce the weight of a Hamiltonian cycle.

## 3.2 EULERIAN GRAPHS

As we mentioned in the introduction, Euler solved the Königsberg problem by converting it into a problem in graph theory. He represented each land area by a vertex and each bridge by an edge (see Fig.3(a)).

&lt;watermark&gt;YOU&lt;/watermark&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;Fig. 3&lt;/img&gt;

You might have noticed that the graph in Fig.3(a) is a **multigraph**. Here A and C are connected by two edges; So are C and D. Let us break up one of the edges connecting C and D by adding a new vertex E. Similarly, break up one of the edges joining A and C by adding a new vertex F. Then, we get the simple graph in Fig.3 (b). If we can find a way of going around the graph in Fig.3(b) using each edge only once, then we can do so in the graph in Fig.3 (a) also, and vice-versa. This process of subdividing the edges can be carried out for any multigraph.

To understand the problem, let us introduce some terms first.

**Definitions :**

i ) A **trail** is a walk in which no edge is repeated.
ii) A **circuit** is a trail whose starting vertex and end vertex are the same.
iii) A trail which is not a circuit is sometimes called an **open trail**.
iv) A circuit (resp. trail) in a graph G containing all the edges of G, is called an **Eulerian circuit** (resp. **Eulerian trail**).
v) A **graph is Eulerian** if it contains an Eulerian circuit.

So, we can rephrase the Königsberg bridge problem in the following way:
**Is the graph in Fig. 3(b) Eulerian?**

&lt;page_number&gt;244&lt;/page_number&gt;

---


## Page 49

Eulerian and Hamiltonian Graphs

Before going further, we give a clarification of our definition of Eulerian graphs in the form of a remark.

**Remark:** You may have noticed that we made connectedness a part of the definition of Eulerian graphs. This is to avoid examples like the one given in Fig. 4. Here the graph has a circuit which contains all the edges of the graph. However, there is no edge through which we can reach the isolated vertex. Unless there is a very special reason, we will not bother about a place to which there is no access! So, such isolated vertices are of no interest to us. By making connectedness a part of the definition, such situations can be avoided.

Now, let us consider some examples of Eulerian graphs. The simplest class of example is a cycle, for example, C<sub>6</sub> in Fig. 5(a). We can get another example by adding a cycle of length 3 to the graph in Fig. 5(a) at v<sub>1</sub> (see Fig. 5(b)).

&lt;img&gt;Fig.4&lt;/img&gt;
Fig.4

&lt;img&gt;Fig. 5a&lt;/img&gt; &lt;img&gt;Fig. 5b&lt;/img&gt; &lt;img&gt;Fig. 5c&lt;/img&gt;
(a) (b)
(c)
Fig. 5

This is also Eulerian because we can start at the vertex v<sub>1</sub>, traverse the inner triangle, come back to v<sub>1</sub> and traverse the outer cycle. We get yet another Eulerian graph by incorporating a cycle of length 6 at v<sub>1</sub> to Fig. 5 (a) (see Fig. 5(c)).

Now you may like to verify whether you have understood the definition of an Eulerian circuit by attempting the following exercise.

E1) Prove that the graph given in Fig.5(c) is Eulerian by producing an Eulerian circuit in it.

E2) What is the difference between an Eulerian graph and an Eulerian circuit?

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

You probably found E1 easy. In a simple example like this, you can easily prove that a graph is Eulerian by producing an Eulerian circuit by trial and error. This may not be possible in more complicated cases. It is **impossible** to prove that a graph is **not** Eulerian by trial and error — we may miss some clever way of tracing an Eulerian circuit. So, we need a necessary and sufficient condition for a graph to be Eulerian. The condition should also be easy to apply. The next theorem gives such a condition. Euler’s proof of the necessary part of the theorem appeared in *Solutio problematis geometriam situs pertinentis* (The solution of a Problem relating to the Geometry of Position). Hierholzer proved the sufficiency part.

**Theorem 1:** A connected graph G is Eulerian **if and only if** the degree of each of its vertices is even.

**Proof:** We shall first assume that the graph G is Eulerian and prove that all its vertices have even degree. So, let T be an Eulerian circuit in G. Every time the circuit passes through a vertex, it uses two edges, one to reach the vertex v and one to leave it. What about the vertex v from which we start tracing the circuit? The edge with which we

&lt;page_number&gt;245&lt;/page_number&gt;

---


## Page 50

Graph Theory

start the circuit is paired with the edge with which we end the circuit. Apart from this, every time we pass through v in the intermediate stages, we will use two edges incident at the vertex as before. Also, we traverse each edge only once. So, all the vertices of the graph have even degree.

To prove the converse, consider a connected graph in which each vertex has even degree. We will now prove that G contains an Eulerian circuit, by induction on the number of edges in G.

Suppose that the number of edges is 0. Since we have assumed that the graph is connected, it consists of a single isolated point. Since the edge set is empty the statement that there is an Eulerian circuit containing all the edges is vacuously true.

Next, assume that all the graphs with fewer edges than G contain an Eulerian circuit. All the vertices of G have even degree and G has no vertex of degree 0 (isolated vertex) since it is connected. So, all the vertices have degree at least 2. We can start from an arbitrary point u = u₀ and trace a circuit C as follows:

We choose any edge u₀u₁ incident at u₀. Since u₁ has degree at least two, there is another edge incident at u₁, say u₁u₂. We go on tracing a circuit like this, always making sure that we enter and leave any vertex by different edges. During the course of tracing C, we may pass through u₀ several times. The process ends when we reach u₀ and find that there is no unused edge to leave u₀. If the circuit we have obtained contains all the edges, we are done. Otherwise, we remove this circuit from G and call the resulting (possibly disconnected) graph H. All the vertices in each of the components of H have even degree and all the components have fewer edges than G.

&lt;watermark&gt;SIT UNIVERSITY&lt;/watermark&gt;
Note that, by connectedness of G, each component of H must contain a point of C.

So all the components are Eulerian. We now get an Eulerian circuit in G as follows: We start from any vertex v on the circuit C and traverse the edges of C till we come to a vertex that lies on one of the components of H. We then traverse the Eulerian circuit in that component, eventually returning to the circuit C. We continue along C in this fashion, taking Eulerian circuits of components of H as we come to them, finally returning to the vertex v we started with. We would have used each of the edges only once, that is, we have obtained an Eulerian circuit.

Hence, by induction, the result is true for all graphs satisfying the condition of the converse.

Let us now see if we can solve the Königsberg bridge problem using Theorem 1.

**Example 1:** Check whether the Königsbergians can go round the city using each bridge only once.

**Solution:** You may recall that we have reduced the Königsberg bridge problem to finding an Eulerian circuit in Fig.3(b). According to the necessary part of the theorem, if a graph has an Eulerian circuit, it has no edges of odd degree. But, as you can see, all the vertices, except E and F, have odd degree. So, this graph does not have an Eulerian circuit. So, the Königsbergians cannot go around the city using each vertex only once.

* * *

Now, here are some exercises to test your understanding.

E3) After Euler proved his theorem, much water has flown under the bridges in Königsberg. In 1875, an extra bridge was built in Königsberg, joining the land areas A and D (see Fig.6). Is it possible now for the Königsbergians to go round the city, using each bridge only once?

&lt;page_number&gt;246&lt;/page_number&gt;

---


## Page 51

Eulerian and Hamiltonian Graphs

D
C
B
A

&lt;img&gt;Fig. 6&lt;/img&gt;

E4) By writing the degree sequences of the following graphs, check whether they are Eulerian. For the graphs that are Eulerian, write down an Eulerian circuit.

&lt;img&gt;G1&lt;/img&gt;
G₁
Fig.7

&lt;img&gt;G2&lt;/img&gt;
G₂

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E5) a) For which values of n is Kₙ Eulerian?

b) For which values of n and m is Kₙ,ₘ Eulerian?

E6) Check whether Q₃ and Q₄ are Eulerian.

E7) Show that, in a connected Eulerian graph, an Eulerian circuit can be traced starting from any vertex.

Suppose now that the people of Königsberg will be happy if they can go around the city, still using all the bridges only once, but they do not mind ending their tour at a point different from their starting point. Is this possible? Let us now examine this question. We will convert this to a problem in graph theory. But, before that, we need a definition that will be helpful in formulating our problem.

**Definition:** A graph G is **edge traceable** if G contains an open trail that contains all the edges of G.

For instance, the graph in Fig.8. is edge traceable because it contains the open trail {v₅, v₁, v₂, v₅, v₄, v₃, v₂, v₄}. This contains all the seven edges of the graph and the end vertices are distinct.

In view of the definition of an edge traceable graph, citizens of Königsberg will have to check whether the graph in Fig.3(b) is edge traceable. As an immediate consequence of Theorem 1, we get the following characterisation of edge traceable graphs.

&lt;page_number&gt;247&lt;/page_number&gt;

---


## Page 52

&lt;img&gt;Fig.8&lt;/img&gt;
**Theorem 2:** A connected graph G with two or more vertices is edge traceable if and only if it has exactly two vertices of odd degree.

**Proof:** Suppose G is an edge traceable graph. Then, there is an open trail T containing all the edges of G. Suppose x and y are the first and the last vertices of T. We now add a new vertex a and join this to x and y. Let us call the new graph we obtain $G'$. This is illustrated for a particular case in Fig.9 below:

&lt;img&gt;Fig.9&lt;/img&gt;

In the graph $G'$ we get an Eulerian circuit as follows:
We start at a, trace the edge ax, trace the open trail T, and trace the edge ya, So, by Theorem 1 all the edges of $G'$ have even degree. Except for x and y, the degrees of all the vertices are unaffected by the addition of the edges ax and ay. So, all of them must have even degree, considered as vertices in G. In the case of vertices x and y, their degrees have become even after the edges ax and ay are added, i.e., after their degrees are increased by one. So, before the addition of the edges, their degrees must have been odd.

**Conversely,** suppose that exactly two vertices x and y have odd degree. Then, by adding a new vertex a and two new edges ax and ay, the degrees of all the vertices become even. So, we can find an Eulerian circuit starting at a. Let this Eulerian circuit be $\{v_0 = a, v_1, \ldots, v_n = a\}$. Since x and y are the only vertices to which a is adjacent, either $v_1 = x$ or $v_{n-1} = x$. If $v_1 = x$, we must have $v_{n-1} = y$ and $\{v_1 = x, v_2, \ldots, v_{n-1} = y\}$ is an open Eulerian trail. Similarly, if $v_1 = y$, we must have $v_{n-1} = x$, and $\{v_1 = y, v_2, \ldots, v_{n-1} = x\}$ is an open Eulerian trail. Hence, the theorem is proved.

&lt;watermark&gt;INSTITUTE OF TECHNOLOGY&lt;/watermark&gt;

Let us now look at the question that motivated us to prove the theorem above.
**Example 2:** Check whether it is possible for the Königsbergians to go around the city, still using each bridge only once, but ending the trip at a point different from the starting point (see Fig.3 (b)).

**Solution:** Referring to Fig.3(b), as we observed before, all the vertices except E and F have odd degree, i.e., there are four vertices of odd degree. So, it is not possible for Königsbergians to tour the city using each bridge only once, even if they are allowed to start and end the tour at two different points.

* * *

Here are some related exercises for you to try.

E8) Consider the situation after the addition of a new bridge in 1875 (see Fig.6). Is it possible to tour the city using each bridge only once, if starting and ending the tour at two different points is permitted?

E9) By writing down the degree sequence, find out which of the following graphs are edge traceable.

&lt;page_number&gt;248&lt;/page_number&gt;

---


## Page 53

Eulerian and Hamiltonian Graphs

&lt;img&gt;A cube-like structure with vertices labeled v1, v2, v3, v4, v5, v6.&lt;/img&gt;
(a)

&lt;img&gt;A hexagon-like structure with vertices labeled v1, v2, v3, v4, v5, v6.&lt;/img&gt;
(b)

Fig. 10

We considered one more problem that we mentioned in the introduction to this unit. This asks for a method for determining whether a given figure can be drawn without lifting the pencil from the paper and without going over any of the lines twice. There is such a method, which we shall now illustrate.

**Example 3:** Check whether the graph in Fig.11(a) can be drawn without lifting the pencil from the paper and without going over any of the lines twice.

**Solution:** The method involves 4 steps.

**Step 1:** (Add vertices at the junctions where two or more lines meet, and at the ends of line segments.) In Fig.11 (a) there are three such junctions A, B and C. So, add vertices at A, B and C to get the multigraph with a loop in Fig.11 (b). Note that the curve joining A and B in Fig.11 (a) is replaced by a straight edge in Fig.11 (b). Similarly, the curve joining A and C is represented by the edge AC.

**Step 2:** (If there are no loops, go to Step 3. If there are loops, eliminate the loops by adding two vertices of degree two.) If we add two vertices D and E of degree 2 to the earlier loop at A, we get the figure in Fig.11(c).

**Step 3:** (If there are no multiple edges go to Step 4. Otherwise, eliminate the multiple edges by adding vertices of degree 2.) In Fig.11(c), B and C are connected by two edges. We eliminate one of the multiple edges by adding a vertex F to it.

**Step 4:** (Count the number of edges of odd degree in the resulting graph. If there are two vertices of odd degree, the graph is edge traceable. If there is no vertex of odd degree, the graph is Eulerian . So, the graph can be drawn without lifting pen from paper. Therefore, the figure we started with can be traced without lifting pen from paper.) As you can see from Fig.11(d) there are exactly two edges, B and C, of odd degree. So, the figure can be traced without lifting the pencil from the paper.

&lt;watermark&gt;UNIVERSITY OF THE PEOPLE&lt;/watermark&gt;

&lt;img&gt;A figure resembling a pot or vase with a loop.&lt;/img&gt;
Fig.11(a)

&lt;img&gt;A triangle with a loop at its base.&lt;/img&gt;
Fig.11(b)

&lt;img&gt;A triangle with a loop at its base, and another loop connecting two points outside the triangle.&lt;/img&gt;
Fig.11(c)

&lt;img&gt;A triangle with a loop at its base, and another loop connecting two points outside the triangle, with a vertex F added between them.&lt;/img&gt;
Fig.11(d)

* * *

If you go through the example above carefully, you may realize that there is a much easier method for deciding whether a figure can be drawn without lifting the pencil form the paper and without going over any of the lines twice. In analogy with graphs, let us call the number of lines that meet in a junction, the degree of the junction for convenience. Note that, only those junctions where more than two lines meet can give rise to vertices of odd degree. All the other vertices that we added are of even degree. In view of this observation, we have the following result.

**Theorem 3:** A figure can be drawn without lifting the pencil from the paper and without going over any of the lines twice **if and only if** the number of junctions whose degree is odd, and at least 3, is either 2 or 0.

&lt;page_number&gt;249&lt;/page_number&gt;

---


## Page 54

Graph Theory

Here is an opportunity for you to apply the method described above.

E10) Which of the following figures can be drawn without lifting pen from paper and without covering any line segment more than once? (Note that the end points of the vertical line in G₁ are vertices of degree 1.)

&lt;img&gt;G₁&lt;/img&gt;
G₁

&lt;img&gt;G₂&lt;/img&gt;
G₂

&lt;img&gt;G₃&lt;/img&gt;
G₃

Fig.12

E11) Construct, if possible, Eulerian graphs with the following number of vertices and edges. When it is not possible, explain why you think so.

<table>
<thead>
<tr>
<th></th>
<th>a</th>
<th>b</th>
<th>c</th>
</tr>
</thead>
<tbody>
<tr>
<td>Number of vertices</td>
<td>5</td>
<td>6</td>
<td>7</td>
</tr>
<tr>
<td>Number of edges</td>
<td>10</td>
<td>10</td>
<td>6</td>
</tr>
</tbody>
</table>

So far, we have seen that if all the vertices of a graph have even degree, it is Eulerian. However, there are situations where we know that a graph is Eulerian, but we still may not be able to find an Eulerian circuit in it. There is an algorithm due to Fleury that gives a method of finding an Eulerian circuit in an Eulerian graph.

In this section we were interested in finding circuits in which all the edges of the graph occur exactly once. In the next section we are interested in finding cycles in which all the vertices occur exactly once.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

## 3.3 HAMILTONIAN GRAPHS

Suppose a transport company operates bus services between 10 different places. There are places with no direct bus service between them, but there is always a route between any two places that go through the other places. In this situation, the company wants to offer a round trip that passes through each of the cities exactly once. Is this possible?

Let us formulate this question as a problem in graph theory. Let us represent the places by vertices. Two vertices are adjacent if a direct bus connects the corresponding places. Since it is possible to go from each place to another, the graph we get is a connected graph. So, the transport company’s problem is :
**Is there a cycle in the graph in which each vertex occurs precisely once?**

A similar question was a basis of the mathematical game described by William Rowan Hamilton. He called this game ‘Traveller’s Dodecahedron’, and also ‘A Voyage Round the World’. In this two-player game, we take a regular dodecahedron, each of its 20 vertices representing a city of the world. One player inserts a pin in a vertex.

&lt;img&gt;Fig. 13: Hamilton (1805-1865)&lt;/img&gt;

&lt;page_number&gt;250&lt;/page_number&gt;

---


## Page 55

Eulerian and Hamiltonian Graphs

The other player is supposed to find a ‘world tour’ starting from this vertex, touching the remaining 19 cities once and returning to the starting vertex. This amounts to finding a cycle covering all the vertices of the regular dodecahedron. Fig.14 gives such a cycle.

&lt;img&gt;Fig.14&lt;/img&gt;

Such a cycle is, aptly, named after Hamilton.

**Definition :** A cycle C in a graph G is called a **Hamiltonian cycle** if it contains all the vertices of G. A graph is called **Hamiltonian** if it contains a Hamiltonian cycle. A graph is called **non-Hamiltonian** if it is not Hamiltonian.

Can you think of examples of Hamiltonian graphs other than the one given in Fig.14? For instance, is any cycle a Hamiltonian graph? Is any graph obtained by adding edges to a Hamiltonian graph also Hamiltonian? The answer to both these questions is ‘yes’. For example, the graphs in Fig.15 are Hamiltonian.

&lt;img&gt;Fig.15 (a)&lt;/img&gt; &lt;img&gt;Fig.15 (b)&lt;/img&gt; &lt;img&gt;Fig.15 (c)&lt;/img&gt;
(a) (b) (c)

Are there any non-Hamiltonian graphs? Trees are obvious examples of non-Hamiltonian graphs. Since they don’t have any cycles, they cannot have a cycle containing all the vertices!

Note that, by definition, a Hamiltonian graph contains a cycle containing all the vertices. So, a Hamiltonian graph cannot have cut vertices or pendant vertices. (Recall that a **pendant vertex** is a vertex of degree 1.) This gives a simple method for constructing examples of non-Hamiltonian graphs. For example, the graph in Fig.16 is non-Hamiltonian because it has a cut vertex, namely, the vertex common to both the triangles.

Here are some exercises to help you test your understanding of the discussion above.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E12) Construct a non-Hamiltonian graph on 5 vertices.

E13) i) Is a Hamiltonian graph Eulerian ?

&lt;img&gt;Fig.16&lt;/img&gt;
Fig.16

&lt;page_number&gt;251&lt;/page_number&gt;

---


## Page 56

Graph Theory

ii) Is an Eulerian graph Hamiltonian ?
Give reasons for your answers.

E14) Check whether the hypercube Q₃ is Hamiltonian.
***

We have used the existence of a cut vertex to prove that the graph in Fig. 16 is not Hamiltonian. However, this does not give us a foolproof method of identifying non-Hamiltonian graphs. For example, Kₘ,ₙ, m, n ≥ 2, has no cut vertices or pendant vertices, and it is not Hamiltonian when m + n is odd, as we shall now show.

**Example 4:** Show that Kₘ,ₙ is not Hamiltonian when m + n is odd.

**Solution:** Since Kₘ,ₙ is bipartite, it does not have cycles of odd length. On the other hand, it has an odd number of vertices. So, a Hamiltonian cycle in this graph, if it exists, must be of odd length. Therefore, Kₘ,ₙ is not Hamiltonian when m + n is odd.

* * *

From the previous example it is clear that to identify non-Hamiltonian graphs we need some conditions which do not depend on the existence of a cut vertex or pendant vertex. The following theorem gives necessary condition for a graph to be Hamiltonian. We will omit the proof of this theorem in this course.

Recall that c(G) denotes the number of components of G.

**Theorem 4:** If G is a Hamiltonian graph, then for every proper subset S of V(G), we must have c(G − S) ≤ |S|.

Let us now look at an example to illustrate the use of Theorem 4.

**Example 5:** Show that Kₘ,ₙ is not Hamiltonian if m < n.

**Solution:** Recall that the vertex set of Kₘ,ₙ can be partitioned into two disjoint subsets X and Y of cardinality m and n, respectively, in such a way that no two edges in the same subset are adjacent and every vertex in X is adjacent to every vertex in Y. Let us take X to be the set S in Theorem 4. So, |S| = m in this case. If we delete all the vertices in X, the graph becomes totally disconnected. So, there are n components in G − S, one corresponding to each vertex of Y. So, c(G−S) = n > m = |S| in this case. Therefore, by Theorem 4, Kₘ,ₙ is non-Hamiltonian.

***Remark:** If the condition given in Theorem 4 is not satisfied, the graph is non-Hamiltonian. However, if the condition is satisfied, it does not mean that the graph is Hamiltonian. For example, consider the Petersen graph in Fig. 17. You can check that for each subset S of V(G), c(G − S) ≤ |S|. But G is non-Hamiltonian (which is not easy to check!).*

&lt;watermark&gt;SCHOOL OF THEORETICAL UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;Fig.17&lt;/img&gt;

Now for some exercises to check your understanding of Theorem 4.

&lt;page_number&gt;252&lt;/page_number&gt;

---


## Page 57

Eulerian and Hamiltonian Graphs

E15) Show that the following graph is non-Hamiltonian.
(Hint: Find a set S ⊂ V(G) such that c(G - S) > |S|.)

&lt;img&gt;Fig. 18&lt;/img&gt;

E16) Check whether the following graphs are Hamiltonian.

&lt;img&gt;Fig. 19&lt;/img&gt;

So far, we have seen some necessary conditions for a graph to be Hamiltonian. They are helpful if we want to show that a given graph is non-Hamiltonian. They are of no use if we want to show that a given graph is Hamiltonian. We need some sufficient conditions for this purpose. Since we are looking for a cycle covering all the vertices, it is reasonable to expect success whenever, at every vertex, there are enough choices of edges. This is confirmed by the following theorems. Theorem 5 was proved by Gabriel Dirac in 1952. This was generalized to Theorem 6 by Oystein Ore in 1960.

**Theorem 5 (Dirac's criterion)** : If G is a simple graph on p vertices, p ≥ 3, and if $\delta(G) \geq \frac{p}{2}$, then G is Hamiltonian.

$\delta(G) = \min\{\text{deg}_G(x) \mid x \in V(G)\}$

**Theorem 6 (Ore's criterion)** : Let G be a simple graph on p vertices, p ≥ 3, satisfying the condition that d(u) + d(v) ≥ p for any two non-adjacent vertices u and v in G. Then G is Hamiltonian.

Can you see that Dirac's theorem follows from Ore's theorem? This is because if $\delta(G) \geq \frac{p}{2}$, then for **any** two vertices u and v, we have
d(u) + d(v) ≥ 2δ(G) ≥ p.

So, the conditions of Ore's theorem are satisfied whenever the conditions of Dirac's Theorem are satisfied. So, if we prove Ore's criterion, we will have also proved Dirac's criterion.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;253&lt;/page_number&gt;

---


## Page 58

Graph Theory

**Proof of Theorem 6 :** We shall prove this result by **contradiction.** Suppose the theorem is false. Then, there are non-Hamiltonian graphs with p vertices satisfying Ore's criterion. So, the following set is non-empty:

F = {G | |V(G)| = p, G is non-Hamiltonian and satisfies Ore's condition}
Choose a graph in F with the maximum number of edges among all such graphs.
(Such a graph must exist, because there are only finitely many graphs in F.) Let us denote this graph by G<sub>M</sub>.

As G<sub>M</sub> is non-Hamiltonian, it cannot be complete. So, there are two vertices, call them u and v, which are not adjacent. So, adding the edge e = uv to G<sub>M</sub>, we get a new graph G'<sub>M</sub>. The number of vertices in G'<sub>M</sub> is still p because we haven't removed any vertex. Since we haven't removed any edge, the degrees of each of the vertices has not decreased. So, Ore's condition holds for any two vertices in G'<sub>M</sub> also. But then, G'<sub>M</sub> must be Hamiltonian. If it is not, it will be in F. This is not possible because |E(G'<sub>M</sub>)| = |E(G<sub>M</sub>)| + 1, and G<sub>M</sub> was chosen to be a graph in F with the maximum possible edges.

Now, since G'<sub>M</sub> is Hamiltonian, we can choose a Hamiltonian cycle C in G'<sub>M</sub>. Since G is non-Hamiltonian, the edge uv must lie on C. (Why?) Removing this edge, we get a path in G containing all the vertices. Let

P = {u = u<sub>1</sub>, u<sub>2</sub>, ..., u<sub>p</sub> = v} be this path. Define S = {u<sub>j</sub> : uu<sub>j+1</sub> ∈ E(G<sub>M</sub>)}, T = {u<sub>j</sub> : u<sub>j</sub>v ∈ E(G<sub>M</sub>)}.

Clearly, u<sub>p</sub> = v ∉ S ∪ T. (Why?) Hence, |S ∪ T| < p. Now, if possible, suppose S ∩ T ≠ φ. Then, let u<sub>r</sub>∈S ∩ T. {u<sub>1</sub>,..., u<sub>r</sub>, u<sub>p</sub>, u<sub>p-1</sub>,...,u<sub>r+1</sub>, u<sub>1</sub>} is a Hamiltonian cycle in the graph G (see Fig.20). This contradicts the assumption that G is non-Hamiltonian.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig. 20&lt;/img&gt;

Hence, S ∩ T = φ, that is, |S ∩ T| = 0.
But then, p ≤ d<sub>G<sub>M</sub></sub>(u) + d<sub>G<sub>M</sub></sub>(v) = |S| + |T| = |S ∪ T| < p, i.e., p < p.
This is a contradiction. Thus, our assumption that the theorem is false, is wrong. In other words, every graph G on p ≥ 3 vertices, satisfying Ore's condition, is Hamiltonian.

**Remark:** Note that Theorem 5 and Theorem 6 are sufficient conditions. They are not at all necessary. For example, C<sub>n</sub>, n > 4, is always Hamiltonian, but C<sub>n</sub> is a 2-regular graph, and therefore, d(u) + d(v) = 4 always.

Here is an example to illustrate the use of the theorems.

**Example 6 :** To which of the graphs in Fig.21 does Dirac's criterion apply? To which does Ore's criterion apply?

&lt;page_number&gt;254&lt;/page_number&gt;

---


## Page 59

Eulerian and Hamiltonian Graphs

&lt;img&gt;Graph (a)&lt;/img&gt;
(a)

&lt;img&gt;Graph (b)&lt;/img&gt;
(b)

Fig.21

**Solution:** For the graph in Fig.21(a), p = 6 and d(v) = 3 for each vertex v. So, δ(G) = 3. Thus, Dirac's criterion is satisfied for this graph.

For the graph in Fig.21(b), p = 5, but d(x) = 2. So, Dirac's criterion is not satisfied by this graph. However, d(u) + d(v) ≥ 5 for all pairs of non-adjacent vertices u and v (in fact, for all pairs u and v). So, Ore's criterion applies in this case.

* * *

Try the following exercise now to test your understanding of the example above.

---

E17) To which of the following graphs does Ore's criterion apply? To which of these does Dirac's criterion apply?

&lt;img&gt;Graph (a)&lt;/img&gt;
(a)

&lt;img&gt;Graph (b)&lt;/img&gt;
(b)

&lt;img&gt;Graph (c)&lt;/img&gt;
(c)

&lt;img&gt;Graph (d)&lt;/img&gt;
(d)

Fig.22

---

So far, we have seen a few necessary conditions and some sufficient conditions for a graph to be Hamiltonian. Are there any conditions that are both necessary and sufficient for a graph to be Hamiltonian? So far no such conditions have been found.

Now, we have come to the end of our discussion on the problem stated in the beginning of the section. In the next section we consider a related, but slightly different problem where we assume that any two places are directly connected by a bus route. We are interested in finding a way of going around all the places, visiting each place only once, and doing so in the shortest possible time.

---

## 3.4 TRAVELLING SALESPERSON PROBLEM

A travelling salesperson wants to visit a number of towns and return to her base. The travelling time between any two towns is known. How should she plan her journey so that she spends as short a time as possible but visits each town precisely once? This is known as the **travelling salesperson problem**. Here, one assumes that a direct route connects any two towns without passing through any of the other towns on the list. If we try to represent the towns by vertices and the direct route by edges, then we simply get a complete graph. How should we represent the time required to go from one town to the other? This question leads to the concept of a weighted graph.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;255&lt;/page_number&gt;

---


## Page 60

Graph Theory

**Definition:** A **weighted graph** is a pair (G, f), where G is a graph and f is a real-valued function on the set E(G).

In simple language, we associate some real number f(e) with each edge e of the graph G. In the case of the travelling salesperson problem, f(e) is simply the time required to travel from one end vertex of e to the other end vertex.

Related to this we have another definition.

**Definition:** Let W be a walk in a weighted graph G. By the **weight of the walk W**, we mean the sum of the weights of all the edges in W.

So, our traveller's problem reduces to finding a Hamiltonian cycle of minimum weight in a weighted complete graph. One possible approach is to find a Hamiltonian cycle first and then search for edges having smaller weight and modify the cycle using them. The modifications can be made as below:

Let C = {v₁, ..., vₚ, v₁} be a Hamiltonian cycle in a weighted **complete graph**. For a fixed i, first check whether there is a j such that
f(vᵢvⱼ) + f(vᵢ₊₁vⱼ₊₁) < f(vᵢvᵢ₊₁) + f(vⱼvⱼ₊₁).
If this inequality holds, then replace the cycle C by
Cᵢⱼ = {v₁, ..., vᵢ, vⱼ, vⱼ₋₁, ..., vᵢ₊₁, vⱼ₊₁, vⱼ₊₂, ..., vₚ, v₁}.
In Fig.23, we have shown this diagrammatically.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig. 23 (a)&lt;/img&gt; &lt;img&gt;Fig. 23 (b)&lt;/img&gt;
Fig.23

The algorithm for reducing the weight of the cycle is called the **1-exchange heuristic**, and was proposed by Lin and Kernighan.

Clearly, the weight of the cycle Cᵢⱼ is strictly less than that of the cycle C. After performing a sequence of such modifications, one is left with a cycle whose weight cannot be reduced further by this process. Of course, **there is no guarantee that the resulting cycle will have the least possible weight**. There may be other cycles with lower weight. But it will often be fairly good. In fact, finding the minimum weight cycle is an NP-hard problem (ref. the course MCS-031.)

Let us consider an example of how the 1-exchange heuristic is applied.

**Example 7:** Consider the copy of a weighted K₆ given in Fig.24. Starting with the cycle {L, M, N, O, P, T, L}, modify it to a cycle of lesser weight. The number on the edge e indicates the weight f(e) assigned to it.

**Solution:** You can check that f(LO) + f(MP) = 80 < f(LM) + f(OP) = 107.
So, we modify the cycle to {L, O, N, M, P, T, L}(see Fig.25(a)).
Now, f(MT) + f(PL) = 121 < f(MP) + f(TL) = 138 (see Fig.25(b)).
So, again we modify the cycle to {L, O, N, M, T, P, L}.
Again, f(OP) + f(NL) = 86 < f(ON) + f(PL) = 87 (see Fig.25(c)).
Hence, modify the cycle to {L, O, P, T, M, N, L} (see Fig.25 (d)).
You can check that we can't decrease the weight of the cycle in the graph further.

&lt;page_number&gt;256&lt;/page_number&gt;

---


## Page 61

Eulerian and Hamiltonian Graphs

&lt;img&gt;Fig. 24 - A weighted graph with vertices L, T, P, O, N, M.&lt;/img&gt;

Fig. 24

&lt;img&gt;Fig. 25 - Four subgraphs (a), (b), (c), (d) showing cycles with weights.&lt;/img&gt;
(a)
(b)
(c)
(d)

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

Hence, by this method we have reduced a cycle of weight 237 to a cycle of weight 192.

* * *

Here is a related exercise for you to try !

E18) Start with the cycle {v₁, v₂, v₃, v₄, v₅, v₁} in the following weighted copy of K₅. Carry out the reduction step once to get a cycle of lesser weight.

&lt;img&gt;Fig. 26 - A weighted graph with vertices v₁, v₂, v₃, v₄, v₅.&lt;/img&gt;
Fig. 26

We have now reached the end of our unit. Let us briefly summarise what we have studied in this unit.

&lt;page_number&gt;257&lt;/page_number&gt;

---


## Page 62

Graph Theory

# 3.5 SUMMARY

In this unit we defined the following terms:

i) Eulerian circuit: A circuit in a graph is called Eulerian if each edge of the graph occurs exactly once in the circuit.

ii) Eulerian graph: A connected graph is Eulerian if it contains an Eulerian circuit.

iii) Open trail: A trail is open if the initial and end vertices of the trail are distinct.

iv) Edge traceable graphs: A connected graph is edge traceable if it has an open trail.

v) Hamiltonian cycle: A cycle is Hamiltonian if each vertex of the graph occurs exactly once in the cycle.

vi) Hamiltonian graphs: A graph is called Hamiltonian if it contains a Hamiltonian cycle.

We also discussed the following points in the unit.

1) The proof and application of the statement : A connected graph is Eulerian iff the degree of each of its vertices is even.

2) The proof and use of the statement : A connected graph with two or more vertices is edge traceable iff it has exactly two vertices of odd degree.

3) The application of an algorithm for checking if a figure can be drawn without lifting pen from paper and without going over any of the lines twice.

4) The application of the fact that if G is Hamiltonian, then c(G−S)≤|S| ∀ S ⊆ V(G).
We also gave an example to show that this condition is not sufficient.

5) The application of the Dirac and Ore criteria for a graph to be Hamiltonian.
According to these criteria, for a simple graph G on p vertices, p≥3,
i) if δ(G)≥$\frac{p}{2}$, G is Hamiltonian (Dirac)
ii) if d(u)+d(v)≥p for any two non-adjacent vertices u and v of G, then G is Hamiltonian (Ore).

6) The travelling salesperson problem, namely, applying the 1-exchange heuristic to obtain a Hamiltonian cycle of smaller weight than that of a given cycle in a complete weighted graph.

# 3.6 SOLUTIONS/ANSWERS

E1) Here is an Eulerian circuit:
{V₁, V₂, V₃, V₄, V₅, V₆, V₁, V₇, V₈, V₄, V₁₀, V₉, V₁}
Of course, there are many different Eulerian circuits in the graph, and you may have come up with a different one.

&lt;watermark&gt;© THE UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;258&lt;/page_number&gt;

---


## Page 63

Eulerian and Hamiltonian Graphs

E2) The graph G is the pair (V(G), E(G)), and the circuit is a finite sequence consisting of elements of V and E alternately such that every element of E exists once in this sequence.

E3) The situation will be as in Fig.27. After the addition of the new edge, both the vertices A and D have become even degree vertices. However, B and C still have odd degree. So, it is still not possible for the Königsbergians to go around the city using each bridge exactly once.

&lt;img&gt;Fig.27&lt;/img&gt;

E4) The degree sequence of G₁ is {8, 4, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2}. All the vertices are even, and hence the graph is Eulerian. You can check that the following gives an Eulerian circuit in it.
{X₁, X₂, X₃, X₄, X₁, X₅, X₆, X₃, X₇, X₈, X₁, X₉, X₁₀, X₁₁, X₁, X₁₂, X₁₃, X₁₄, X₁₅, X₁}.
The degree sequence of G₂ is {8, 4, 4, 4, 4, 4, 4, 2, 2, 2, 2}. Since all the degrees are even, it is Eulerian. An Eulerian circuit in G₂ is
{X₁, X₂, X₃, X₄, X₅, X₁, X₃, X₅, X₂, X₄, X₁, X₆, X₇, X₈, X₁, X₉, X₇, X₁₀, X₁}.

E5)
a) Kₙ is an (n – 1)-regular graph. So, it is Eulerian when n – 1 is even, i.e., n is odd.
b) Kₙ,ₘ has n vertices of degree m – 1 and m vertices of degree n – 1. So, it is Eulerian when n, m are odd.

E6) In Q₃, every vertex has degree 3, and hence it is a non-Eulerian graph. On the other hand, all the vertices of Q₄, have degree 4. Hence, Q₄ is Eulerian.

E7) Suppose G is an Eulerian graph and {v₀, v₁, …, vₙ = v₀} is an Eulerian circuit in it. Let x = vᵢ be any vertex in G. Then, the following is an Eulerian trail starting and ending at x:
{x = vᵢ, vᵢ₊₁, …, vₙ = v₀, v₁, …, vᵢ₋₁}

E8) Refer to Fig.27. After the construction of the new bridge all the vertices except B and C are even, i.e., there are two vertices of odd degree. So, it is possible to go round the city using each bridge only once, starting and ending the trip at two different points.

E9)
a) Let us write down the degree sequence of the graph. It is {4, 4, 4, 3, 3, 3, 3, 3, 3, 3}. It has eight vertices of odd degree. So, the graph in Fig.10(a) is not edge traceable.
b) The degree sequence of the graph in Fig.10(b) is {4, 3, 3, 2, 2, 2}. So, it has exactly two vertices of odd degree. So, the graph is edge traceable.

E10) Since G₁ has exactly two vertices of odd degree, it can be drawn without lifting pen from paper and without going over any of the vertices twice. Since G₂ has 6 vertices of odd degree (degree 3), it cannot be traced without lifting pen from paper. Since G₃ has precisely two vertices of odd degree, this can also be traced without lifting pen from paper.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;259&lt;/page_number&gt;

---


## Page 64

Graph Theory

E11) The solutions for (a) and (b) are given below.

&lt;img&gt;Figure 28a&lt;/img&gt;
(a)

&lt;img&gt;Figure 28b&lt;/img&gt;
(b)

Fig.28

c) Recall that any Eulerian graph is connected. Here, the number of vertices is one more than the number of edges. So, such a graph is a tree, and therefore, does not contain any cycle. Thus, there is no Eulerian graph with the given number of vertices and edges.

E12) For example, consider the graph in Fig.29. This is non-Hamiltonian because the vertex x is a cut vertex.

&lt;img&gt;Figure 29&lt;/img&gt;
Fig.29

E13) i) See Fig.30. This has a Hamiltonian cycle {v₁, v₂, v₃, v₄, v₅, v₆, v₁}. But, it is not Eulerian because the vertices v₂ and v₅ have odd degrees.

ii) The graph given in Fig.29 is Eulerian because all its vertices have even degree. As, we have seen already, it is not Hamiltonian.

&lt;img&gt;Figure 30&lt;/img&gt;
Fig.30

E14) A Hamiltonian cycle in Q₃ is {000, 100, 110, 010, 011, 111, 101, 001, 000}.

E15) If you remove the vertices marked x, y and z in Fig.31, you will get four connected components, namely, one inner triangle and three isolated outer vertices.

&lt;img&gt;Figure 31&lt;/img&gt;
Fig.31

Hence, by Theorem 4, the given graph is non-Hamiltonian.

E16) A Hamiltonian cycle in the graph G₁ is {x₇, x₃, x₄, x₂, x₆, x₅, x₁, x₇}. The following cycle in the graph G₂ is Hamiltonian : {x₁₂, x₁₄, x₈, x₉, x₁₀, x₁₁, x₁₃, x₇, x₆, x₅, x₄, x₃, x₂, x₁, x₁₂}.

E17) a) This is a 4-regular graph. So, δ(G) = 4. Here p = 6, and therefore, the condition δ(G) ≥ $\frac{p}{2}$ is satisfied. So, Dirac's criterion (and therefore, Ore's criterion) applies here.

&lt;page_number&gt;260&lt;/page_number&gt;

---


## Page 65

Eulerian and Hamiltonian
Graphs

b) Here p = 7. The vertices v<sub>6</sub> and v<sub>7</sub> have degree 3 < $\frac{7}{2}$. Therefore,
Dirac's criterion does not apply. However, the only pairs of non-adjacent vertices in this graph are (v<sub>6</sub>, v<sub>4</sub>), (v<sub>6</sub>, v<sub>5</sub>), (v<sub>6</sub>, v<sub>3</sub>), (v<sub>7</sub>, v<sub>4</sub>), (v<sub>7</sub>, v<sub>5</sub>), (v<sub>7</sub>, v<sub>1</sub>).
Ore's condition is satisfied for these pairs of vertices. So, this graph is Hamiltonian.

c) Here p = 8 and the graph is 4-regular. So, Dirac's criterion is satisfied.

d) Here p = 8, but the vertices v<sub>8</sub> and v<sub>4</sub> have degree 3 which is less than $\frac{p}{2}$ = 4. So, Dirac's criterion is not satisfied. The only pairs of non-adjacent vertices are (v<sub>7</sub>, v<sub>3</sub>), (v<sub>7</sub>, v<sub>4</sub>), (v<sub>7</sub>, v<sub>5</sub>), (v<sub>7</sub>, v<sub>6</sub>), (v<sub>8</sub>, v<sub>2</sub>), (v<sub>8</sub>, v<sub>3</sub>), (v<sub>8</sub>, v<sub>4</sub>), (v<sub>8</sub>, v<sub>5</sub>). You can check that Ore's criterion is satisfied for these pairs of vertices.

E18) Notice that
f(v<sub>1</sub> v<sub>2</sub>) + f(v<sub>4</sub> v<sub>5</sub>) = 51 + 78 = 129
f(v<sub>1</sub> v<sub>4</sub>) + f(v<sub>2</sub> v<sub>5</sub>) = 5 + 36 = 41

We can modify the given cycle to get the following cycle of smaller weight:
{v<sub>1</sub>, v<sub>4</sub>, v<sub>3</sub>, v<sub>2</sub>, v<sub>5</sub>, v<sub>1</sub>}.

<mermaid>
graph LR
    subgraph Original Cycle
        A[v<sub>1</sub>] -- v<sub>2</sub> --> B[v<sub>3</sub>] -- v<sub>4</sub> --> C[v<sub>5</sub>] -- v<sub>1</sub> --> A
    end
    subgraph Modified Cycle
        D[v<sub>1</sub>] -- v<sub>4</sub> --> E[v<sub>3</sub>] -- v<sub>2</sub> --> F[v<sub>5</sub>] -- v<sub>1</sub> --> D
    end
    A --- B
    B --- C
    C --- D
    D --- E
    E --- F
    F --- A
    style A fill:none,stroke:none
    style B fill:none,stroke:none
    style C fill:none,stroke:none
    style D fill:none,stroke:none
    style E fill:none,stroke:none
    style F fill:none,stroke:none
    linkStyle 0 stroke-width:0px;
    linkStyle 1 stroke-width:0px;
    linkStyle 2 stroke-width:0px;
    linkStyle 3 stroke-width:0px;
    linkStyle 4 stroke-width:0px;
    linkStyle 5 stroke-width:0px;
    linkStyle 6 stroke-width:0px;
    linkStyle 7 stroke-width:0px;
    linkStyle 8 stroke-width:0px;
    linkStyle 9 stroke-width:0px;
    linkStyle 10 stroke-width:0px;
    linkStyle 11 stroke-width:0px;
    linkStyle 12 stroke-width:0px;
    linkStyle 13 stroke-width:0px;
    linkStyle 14 stroke-width:0px;
    linkStyle 15 stroke-width:0px;
    linkStyle 16 stroke-width:0px;
    linkStyle 17 stroke-width:0px;
    linkStyle 18 stroke-width:0px;
    linkStyle 19 stroke-width:0px;
    linkStyle 20 stroke-width:0px;
    linkStyle 21 stroke-width:0px;
    linkStyle 22 stroke-width:0px;
    linkStyle 23 stroke-width:0px;
    linkStyle 24 stroke-width:0px;
    linkStyle 25 stroke-width:0px;
    linkStyle 26 stroke-width:0px;
    linkStyle 27 stroke-width:0px;
    linkStyle 28 stroke-width:0px;
    linkStyle 29 stroke-width:0px;
    linkStyle 30 stroke-width:0px;
    linkStyle 31 stroke-width:0px;
    linkStyle 32 stroke-width:0px;
    linkStyle 33 stroke-width:0px;
    linkStyle 34 stroke-width:0px;
    linkStyle 35 stroke-width:0px;
    linkStyle 36 stroke-width:0px;
    linkStyle 37 stroke-width:0px;
    linkStyle 38 stroke-width:0px;
    linkStyle 39 stroke-width:0px;
    linkStyle 40 stroke-width:0px;
    linkStyle 41 stroke-width:0px;
    linkStyle 42 stroke-width:0px;
    linkStyle 43 stroke-width:0px;
    linkStyle 44 stroke-width:0px;
    linkStyle 45 stroke-width:0px;
    linkStyle 46 stroke-width:0px;
    linkStyle 47 stroke-width:0px;
    linkStyle 48 stroke-width:0px;
    linkStyle 49 stroke-width:0px;
    linkStyle 50 stroke-width:0px;
    linkStyle 51 stroke-width:0px;
    linkStyle 52 stroke-width:0px;
    linkStyle 53 stroke-width:0px;
    linkStyle 54 stroke-width:0px;
    linkStyle 55 stroke-width:0px;
    linkStyle 56 stroke-width:0px;
    linkStyle 57 stroke-width:0px;
    linkStyle 58 stroke-width:0px;
    linkStyle 59 stroke-width:0px;
    linkStyle 60 stroke-width:0px;
    linkStyle 61 stroke-width:0px;
    linkStyle 62 stroke-width:0px;
    linkStyle 63 stroke-width:0px;
    linkStyle 64 stroke-width:0px;
    linkStyle 65 stroke-width:0px;
    linkStyle 66 stroke-width:0px;
    linkStyle 67 stroke-width:0px;
    linkStyle 68 stroke-width:0px;
    linkStyle 69 stroke-width:0px;
    linkStyle 70 stroke-width:0px;
    linkStyle 71 stroke-width:0px;
    linkStyle 72 stroke-width:0px;
    linkStyle 73 stroke-width:0px;
    linkStyle 74 stroke-width:0px;
    linkStyle 75 stroke-width:0px;
    linkStyle 76 stroke-width:0px;
    linkStyle 77 stroke-width:0px;
    linkStyle 78 stroke-width:0px;
    linkStyle 79 stroke-width:0px;
    linkStyle 80 stroke-width:0px;
    linkStyle 81 stroke-width:0px;
    linkStyle 82 stroke-width:0px;
    linkStyle 83 stroke-width:0px;
    linkStyle 84 stroke-width:0px;
    linkStyle 85 stroke-width:0px;
    linkStyle 86 stroke-width:0px;
    linkStyle 87 stroke-width:0px;
    linkStyle 88 stroke-width:0px;
    linkStyle 89 stroke-width:0px;
    linkStyle 90 stroke-width:0px;
    linkStyle 91 stroke-width:0px;
    linkStyle 92 stroke-width:0px;
    linkStyle 93 stroke-width:0px;
    linkStyle 94 stroke-width:0px;
    linkStyle 95 stroke-width:0px;
    linkStyle 96 stroke-width:0px;
    linkStyle 97 stroke-width:0px;
    linkStyle 98 stroke-width:0px;
    linkStyle 99 stroke-width:0px;
    linkStyle 100 stroke-width:0px;
    linkStyle 101 stroke-width:0px;
    linkStyle 102 stroke-width:0px;
    linkStyle 103 stroke-width:0px;
    linkStyle 104 stroke-width:0px;
    linkStyle 105 stroke-width:0px;
    linkStyle 106 stroke-width:0px;
    linkStyle 107 stroke-width:0px;
    linkStyle 108 stroke-width:0px;
    linkStyle 109 stroke-width:0px;
    linkStyle 110 stroke-width:0px;
    linkStyle 111 stroke-width:0px;
    linkStyle 112 stroke-width:0px;
    linkStyle 113 stroke-width:0px;
    linkStyle 114 stroke-width:0px;
    linkStyle 115 stroke-width:0px;
    linkStyle 116 stroke-width:0px;
    linkStyle 117 stroke-width:0px;
    linkStyle 118 stroke-width:0px;
    linkStyle 119 stroke-width:0px;
    linkStyle 120 stroke-width:0px;
    linkStyle 121 stroke-width:0px;
    linkStyle 122 stroke-width:0px;
    linkStyle 123 stroke-width:0px;
    linkStyle 124 stroke-width:0px;
    linkStyle 125 stroke-width:0px;
    linkStyle 126 stroke-width:0px;
    linkStyle 127 stroke-width:0px;
    linkStyle 128 stroke-width:0px;
    linkStyle 129 stroke-width:0px;
    linkStyle 130 stroke-width:0px;
    linkStyle 131 stroke-width:0px;
    linkStyle 132 stroke-width:0px;
    linkStyle 133 stroke-width:0px;
    linkStyle 134 stroke-width:0px;
    linkStyle 135 stroke-width:0px;
    linkStyle 136 stroke-width:0px;
    linkStyle 137 stroke-width:0px;
    linkStyle 138 stroke-width:0px;
    linkStyle 139 stroke-width:0px;
    linkStyle 140 stroke-width:0px;
    linkStyle 141 stroke-width:0px;
    linkStyle 142 stroke-width:0px;
    linkStyle 143 stroke-width:0px;
    linkStyle 144 stroke-width:0px;
    linkStyle 145 stroke-width:0px;
    linkStyle 146 stroke-width:0px;
    linkStyle 147 stroke-width:0px;
    linkStyle 148 stroke-width:0px;
    linkStyle 149 stroke-width:0px;
    linkStyle 150 stroke-width:0px;
    linkStyle 151 stroke-width:0px;
    linkStyle 152 stroke-width:0px;
    linkStyle 153 stroke-width:0px;
    linkStyle 154 stroke-width:0px;
    linkStyle 155 stroke-width:0px;
    linkStyle 156 stroke-width:0px;
    linkStyle 157 stroke-width:0px;
    linkStyle 158 stroke-width:0px;
    linkStyle 159 stroke-width:0px;
    linkStyle 160 stroke-width:0px;
    linkStyle 161 stroke-width:0px;
    linkStyle 162 stroke-width:0px;
    linkStyle 163 stroke-width:0px;
    linkStyle 164 stroke-width:0px;
    linkStyle 165 stroke-width:0px;
    linkStyle 166 stroke-width:0px;
    linkStyle 167 stroke-width:0px;
    linkStyle 168 stroke-width:0px;
    linkStyle 169 stroke-width:0px;
    linkStyle 170 stroke-width:0px;
    linkStyle 171 stroke-width:0px;
    linkStyle 172 stroke-width:0px;
    linkStyle 173 stroke-width:0px;
    linkStyle 174 stroke-width:0px;
    linkStyle 175 stroke-width:0px;
    linkStyle 176 stroke-width:0px;
    linkStyle 177 stroke-width:0px;
    linkStyle 178 stroke-width:0px;
    linkStyle 179 stroke-width:0px;
    linkStyle 180 stroke-width:0px;
    linkStyle 181 stroke-width:0px;
    linkStyle 182 stroke-width:0px;
    linkStyle 183 stroke-width:0px;
    linkStyle 184 stroke-width:0px;
    linkStyle 185 stroke-width:0px;
    linkStyle 186 stroke-width:0px;
    linkStyle 187 stroke-width:0px;
    linkStyle 188 stroke-width:0px;
    linkStyle 189 stroke-width:0px;
    linkStyle 190 stroke-width:0px;
    linkStyle 191 stroke-width:0px;
    linkStyle 192 stroke-width:0px;
    linkStyle 193 stroke-width:0px;
    linkStyle 194 stroke-width:0px;
    linkStyle 195 stroke-width:0px;
    linkStyle 196 stroke-width:0px;
    linkStyle 197 stroke-width:0px;
    linkStyle 198 stroke-width:0px;
    linkStyle 199 stroke-width:0px;
    linkStyle 200 stroke-width:0px;
    linkStyle 201 stroke-width:0px;
    linkStyle 202 stroke-width:0px;
    linkStyle 203 stroke-width:0px;
    linkStyle 204 stroke-width:0px;
    linkStyle 205 stroke-width:0px;
    linkStyle 206 stroke-width:0px;
    linkStyle 207 stroke-width:0px;
    linkStyle 208 stroke-width:0px;
    linkStyle 209 stroke-width:0px;
    linkStyle 210 stroke-width:0px;
    linkStyle 211 stroke-width:0px;
    linkStyle 212 stroke-width:0px;
    linkStyle 213 stroke-width:0px;
    linkStyle 214 stroke-width:0px;
    linkStyle 215 stroke-width:0px;
    linkStyle 216 stroke-width:0px;
    linkStyle 217 stroke-width:0px;
    linkStyle 218 stroke-width:0px;
    linkStyle 219 stroke-width:0px;
    linkStyle 220 stroke-width:0px;
    linkStyle 221 stroke-width:0px;
    linkStyle 222 stroke-width:0px;
    linkStyle 223 stroke-width:0px;
    linkStyle 224 stroke-width:0px;
    linkStyle 225 stroke-width:0px;
    linkStyle 226 stroke-width:0px;
    linkStyle 227 stroke-width:0px;
    linkStyle 228 stroke-width:0px;
    linkStyle 229 stroke-width:0px;
    linkStyle 230 stroke-width:0px;
    linkStyle 231 stroke-width:0px;
    linkStyle 232 stroke-width:0px;
    linkStyle 233 stroke-width:0px;
    linkStyle 234 stroke-width:0px;
    linkStyle 235 stroke-width:0px;
    linkStyle 236 stroke-width:0px;
    linkStyle 237 stroke-width:0px;
    linkStyle 238 stroke-width:0px;
    linkStyle 239 stroke-width:0px;
    linkStyle 240 stroke-width:0px;
    linkStyle 241 stroke-width:0px;
    linkStyle 242 stroke-width:0px;
    linkStyle 243 stroke-width:0px;
    linkStyle 244 stroke-width:0px;
    linkStyle 245 stroke-width:0px;
    linkStyle 246 stroke-width:0px;
    linkStyle 247 stroke-width:0px;
    linkStyle 248 stroke-width:0px;
    linkStyle 249 stroke-width:0px;
    linkStyle 250 stroke-width:0px;
    linkStyle 251 stroke-width:0px;
    linkStyle 252 stroke-width:0px;
    linkStyle 253 stroke-width:0px;
    linkStyle 254 stroke-width:0px;
    linkStyle 255 stroke-width:0px;
    linkStyle 256 stroke-width:0px;
    linkStyle 257 stroke-width:0px;
    linkStyle 258 stroke-width:0px;
    linkStyle 259 stroke-width:0px;
    linkStyle 260 stroke-width:0px;
    linkStyle 261 stroke-width:0px;
    linkStyle 262 stroke-width:0px;
    linkStyle 263 stroke-width:0px;
    linkStyle 264 stroke-width:0px;
    linkStyle 265 stroke-width:0px;
    linkStyle 266 stroke-width:0px;
    linkStyle 267 stroke-width:0px;
    linkStyle 268 stroke-width:0px;
    linkStyle 269 stroke-width:0px;
    linkStyle 270 stroke-width:0px;
    linkStyle 271 stroke-width:0px;
    linkStyle 272 stroke-width:0px;
    linkStyle 273 stroke-width:0px;
    linkStyle 274 stroke-width:0px;
    linkStyle 275 stroke-width:0px;
    linkStyle 276 stroke-width:0px;
    linkStyle 277 stroke-width:0px;
    linkStyle 278 stroke-width:0px;
    linkStyle 279 stroke-width:0px;
    linkStyle 280 stroke-width:0px;
    linkStyle 281 stroke-width:0px;
    linkStyle 282 stroke-width:0px;
    linkStyle 283 stroke-width:0px;
    linkStyle 284 stroke-width:0px;
    linkStyle 285 stroke-width:0px;
    linkStyle 286 stroke-width:0px;
    linkStyle 287 stroke-width:0px;
    linkStyle 288 stroke-width:0px;
    linkStyle 289 stroke-width:0px;
    linkStyle 290 stroke-width:0px;
    linkStyle 291 stroke-width:0px;
    linkStyle 292 stroke-width:0px;
    linkStyle 293 stroke-width:0px;
    linkStyle 294 stroke-width:0px;
    linkStyle 295 stroke-width:0px;
    linkStyle 296 stroke-width:0px;
    linkStyle 297 stroke-width:0px;
    linkStyle 298 stroke-width:0px;
    linkStyle 299 stroke-width:0px;
    linkStyle 300 stroke-width:0px;
    linkStyle 301 stroke-width:0px;
    linkStyle 302 stroke-width:0px;
    linkStyle 303 stroke-width:0px;
    linkStyle 304 stroke-width:0px;
    linkStyle 305 stroke-width:0px;
    linkStyle 306 stroke-width:0px;
    linkStyle 307 stroke-width:0px;
    linkStyle 308 stroke-width:0px;
    linkStyle 309 stroke-width:0px;
    linkStyle 310 stroke-width:0px;
    linkStyle 311 stroke-width:0px;
    linkStyle 312 stroke-width:0px;
    linkStyle 313 stroke-width:0px;
    linkStyle 314 stroke-width:0px;
    linkStyle 315 stroke-width:0px;
    linkStyle 316 stroke-width:0px;
    linkStyle 317 stroke-width:0px;
    linkStyle 318 stroke-width:0px;
    linkStyle 319 stroke-width:0px;
    linkStyle 320 stroke-width:0px;
    linkStyle 321 stroke-width:0px;
    linkStyle 322 stroke-width:0px;
    linkStyle 323 stroke-width:0px;
    linkStyle 324 stroke-width:0px;
    linkStyle 325 stroke-width:0px;
    linkStyle 326 stroke-width:0px;
    linkStyle 327 stroke-width:0px;
    linkStyle 328 stroke-width:0px;
    linkStyle 329 stroke-width:0px;
    linkStyle 330 stroke-width:0px;
    linkStyle 331 stroke-width:0px;
    linkStyle 332 stroke-width:0px;
    linkStyle 333 stroke-width:0px;
    linkStyle 334 stroke-width:0px;
    linkStyle 335 stroke-width:0px;
    linkStyle 336 stroke-width:0px;
    linkStyle 337 stroke-width:0px;
    linkStyle 338 stroke-width:0px;
    linkStyle 339 stroke-width:0px;
    linkStyle 340 stroke-width:0px;
    linkStyle 341 stroke-width:0px;
    linkStyle 342 stroke-width:0px;
    linkStyle 343 stroke-width:0px;
    linkStyle 344 stroke-width:0px;
    linkStyle 345 stroke-width:0px;
    linkStyle 346 stroke-width:0px;
    linkStyle 347 stroke-width:0px;
    linkStyle 348 stroke-width:0px;
    linkStyle 349 stroke-width:0px;
    linkStyle 350 stroke-width:0px;
    linkStyle 351 stroke-width:0px;
    linkStyle 352 stroke-width:0px;
    linkStyle 353 stroke-width:0px;
    linkStyle 354 stroke-width:0px;
    linkStyle 355 stroke-width:0px;
    linkStyle 356 stroke-width:0px;
    linkStyle 357 stroke-width:0px;
    linkStyle 358 stroke-width:0px;
    linkStyle 359 stroke-width:0px;
    linkStyle 360 stroke-width:0px;
    linkStyle 361 stroke-width:0px;
    linkStyle 362 stroke-width:0px;
    linkStyle 363 stroke-width:0px;
    linkStyle 364 stroke-width:0px;
    linkStyle 365 stroke-width:0px;
    linkStyle 366 stroke-width:0px;
    linkStyle 367 stroke-width:0px;
    linkStyle 368 stroke-width:0px;
    linkStyle 369 stroke-width:0px;
    linkStyle 370 stroke-width:0px;
    linkStyle 371 stroke-width:0px;
    linkStyle 372 stroke-width:0px;
    linkStyle 373 stroke-width:0px;
    linkStyle 374 stroke-width:0px;
    linkStyle 375 stroke-width:0px;
    linkStyle 376 stroke-width:0px;
    linkStyle 377 stroke-width:0px;
    linkStyle 378 stroke-width:0px;
    linkStyle 379 stroke-width:0px;
    linkStyle 380 stroke-width:0px;
    linkStyle 381 stroke-width:0px;
    linkStyle 382 stroke-width:0px;
    linkStyle 383 stroke-width:0px;
    linkStyle 384 stroke-width:0px;
    linkStyle 385 stroke-width:0px;
    linkStyle 386 stroke-width:0px;
    linkStyle 387 stroke-width:0px;
    linkStyle 388 stroke-width:0px;
    linkStyle 389 stroke-width:0px;
    linkStyle 390 stroke-width:0px;
    linkStyle 391 stroke-width:0px;
    linkStyle 392 stroke-width:0px;
    linkStyle 393 stroke-width:0px;
    linkStyle 394 stroke-width:0px;
    linkStyle 395 stroke-width:0px;
    linkStyle 396 stroke-width:0px;
    linkStyle 397 stroke-width:0px;
    linkStyle 398 stroke-width:0px;
    linkStyle 399 stroke-width:0px;
    linkStyle 400 stroke-width:0px;
    linkStyle 401 stroke-width:0px;
    linkStyle 402 stroke-width:0px;
    linkStyle 403 stroke-width:0px;
    linkStyle 404 stroke-width:0px;
    linkStyle 405 stroke-width:0px;
    linkStyle 406 stroke-width:0px;
    linkStyle 407 stroke-width:0px;
    linkStyle 408 stroke-width:0px;
    linkStyle 409 stroke-width:0px;
    linkStyle 410 stroke-width:0px;
    linkStyle 411 stroke-width:0px;
    linkStyle 412 stroke-width:0px;
    linkStyle 413 stroke-width:0px;
    linkStyle 414 stroke-width:0px;
    linkStyle 415 stroke-width:0px;
    linkStyle 416 stroke-width:0px;
    linkStyle 417 stroke-width:0px;
    linkStyle 418 stroke-width:0px;
    linkStyle 419 stroke-width:0px;
    linkStyle 420 stroke-width:0px;
    linkStyle 421 stroke-width:0px;
    linkStyle 422 stroke-width:0px;
    linkStyle 423 stroke-width:0px;
    linkStyle 424 stroke-width:0px;
    linkStyle 425 stroke-width:0px;
    linkStyle 426 stroke-width:0px;
    linkStyle 427 stroke-width:0px;
    linkStyle 428 stroke-width:0px;
    linkStyle 429 stroke-width:0px;
    linkStyle 430 stroke-width:0px;
    linkStyle 431 stroke-width:0px;
    linkStyle 432 stroke-width:0px;
    linkStyle 433 stroke-width:0px;
    linkStyle 434 stroke-width:0px;
    linkStyle 435 stroke-width:0px;
    linkStyle 436 stroke-width:0px;
    linkStyle 437 stroke-width:0px;
    linkStyle 438 stroke-width:0px;
    linkStyle 439 stroke-width:0px;
    linkStyle 440 stroke-width:0px;
    linkStyle 441 stroke-width:0px;
    linkStyle 442 stroke-width:0px;
    linkStyle 443 stroke-width:0px;
    linkStyle 444 stroke-width:0px;
    linkStyle 445 stroke-width:0px;
    linkStyle 446 stroke-width:0px;
    linkStyle 447 stroke-width:0px;
    linkStyle 448 stroke-width:0px;
    linkStyle 449 stroke-width:0px;
    linkStyle 450 stroke-width:0px;
    linkStyle 451 stroke-width:0px;
    linkStyle 452 stroke-width:0px;
    linkStyle 453 stroke-width:0px;
    linkStyle 454 stroke-width:0px;
    linkStyle 455 stroke-width:0px;
    linkStyle 456 stroke-width:0px;
    linkStyle 457 stroke-width:0px;
    linkStyle 458 stroke-width:0px;
    linkStyle 459 stroke-width:0px;
    linkStyle 460 stroke-width:0px;
    linkStyle 461 stroke-width:0px;
    linkStyle 462 stroke-width:0px;
    linkStyle 463 stroke-width:0px;
    linkStyle 464 stroke-width:0px;
    linkStyle 465 stroke-width:0px;
    linkStyle 466 stroke-width:0px;
    linkStyle 467 stroke-width:0px;
    linkStyle 468 stroke-width:0px;
    linkStyle 469 stroke-width:0px;
    linkStyle 470 stroke-width:0px;
    linkStyle 471 stroke-width:0px;
    linkStyle 472 stroke-width:0px;
    linkStyle 473 stroke-width:0px;
    linkStyle 474 stroke-width:0px;
    linkStyle 475 stroke-width:0px;
    linkStyle 476 stroke-width:0px;
    linkStyle 477 stroke-width:0px;
    linkStyle 478 stroke-width:0px;
    linkStyle 479 stroke-width:0px;
    linkStyle 480 stroke-width:0px;
    linkStyle 481 stroke-width:0px;
    linkStyle 482 stroke-width:0px;
    linkStyle 483 stroke-width:0px;
    linkStyle 484 stroke-width:0px;
    linkStyle 485 stroke-width:0px;
    linkStyle 486 stroke-width:0px;
    linkStyle 487 stroke-width:0px;
    linkStyle 488 stroke-width:0px;
    linkStyle 489 stroke-width:0px;
    linkStyle 490 stroke-width:0px;
    linkStyle 491 stroke-width:0px;
    linkStyle 492 stroke-width:0px;
    linkStyle 493 stroke-width:0px;
    linkStyle 494 stroke-width:0px;
    linkStyle 495 stroke-width:0px;
    linkStyle 496 stroke-width:0px;
    linkStyle 497 stroke-width:0px;
    linkStyle 498 stroke-width:0px;
    linkStyle 499 stroke-width:0px;
    linkStyle 500 stroke-width:0px;
    linkStyle 501 stroke-width:0px;
    linkStyle 502 stroke-width:0px;
    linkStyle 503 stroke-width:0px;
    linkStyle 504 stroke-width:0px;
    linkStyle 505 stroke-width:0px;
    linkStyle 506 stroke-width:0px;
    linkStyle 507 stroke-width:0px;
    linkStyle 508 stroke-width:0px;
    linkStyle 509 stroke-width:0px;
    linkStyle 510 stroke-width:0px;
    linkStyle 511 stroke-width:0px;
    linkStyle 512 stroke-width:0px;
    linkStyle 513 stroke-width:0px;
    linkStyle 514 stroke-width:0px;
    linkStyle 515 stroke-width:0px;
    linkStyle 516 stroke-width:0px;
    linkStyle 517 stroke-width:0px;
    linkStyle 518 stroke-width:0px;
    linkStyle 519 stroke-width:0px;
    linkStyle 520 stroke-width:0px;
    linkStyle 521 stroke-width:0px;
    linkStyle 522 stroke-width:0px;
    linkStyle 523 stroke-width:0px;
    linkStyle 524 stroke-width:0px;
    linkStyle 525 stroke-width:0px;
    linkStyle 526 stroke-width:0px;
    linkStyle 527 stroke-width:0px;
    linkStyle 528 stroke-width:0px;
    linkStyle 529 stroke-width:0px;
    linkStyle 530 stroke-width:0px;
    linkStyle 531 stroke-width:0px;
    linkStyle 532 stroke-width:0px;
    linkStyle 533 stroke-width:0px;
    linkStyle 534 stroke-width:0px;
    linkStyle 535 stroke-width:0px;
    linkStyle 536 stroke-width:0px;
    linkStyle 537 stroke-width:0px;
    linkStyle 538 stroke-width:0px;
    linkStyle 539 stroke-width:0px;
    linkStyle 540 stroke-width:0px;
    linkStyle 541 stroke-width:0px;
    linkStyle 542 stroke-width:0px;
    linkStyle 543 stroke-width:0px;
    linkStyle 544 stroke-width:0px;
    linkStyle 545 stroke-width:0px;
    linkStyle 546 stroke-width:0px;
    linkStyle 547 stroke-width:0px;
    linkStyle 548 stroke-width:0px;
    linkStyle 549 stroke-width:0px;
    linkStyle 550 stroke-width:0px;
    linkStyle 551 stroke-width:0px;
    linkStyle 552 stroke-width:0px;
    linkStyle 553 stroke-width:0px;
    linkStyle 554 stroke-width:0px;
    linkStyle 555 stroke-width:0px;
    linkStyle 556 stroke-width:0px;
    linkStyle 557 stroke-width:0px;
    linkStyle 558 stroke-width:0px;
    linkStyle 559 stroke-width:0px;
    linkStyle 560 stroke-width:0px;
    linkStyle 561 stroke-width:0px;
    linkStyle 562 stroke-width:0px;
    linkStyle 563 stroke-width:0px;
    linkStyle 564 stroke-width:0px;
    linkStyle 565 stroke-width:0px;
    linkStyle 566 stroke-width:0px;
    linkStyle 567 stroke-width:0px;
    linkStyle 568 stroke-width:0px;
    linkStyle 569 stroke-width:0px;
    linkStyle 570 stroke-width:0px;
    linkStyle 571 stroke-width:0px;
    linkStyle 572 stroke-width:0px;
    linkStyle 573 stroke-width:0px;
    linkStyle 574 stroke-width:0px;
    linkStyle 575 stroke-width:0px;
    linkStyle 576 stroke-width:0px;
    linkStyle 577 stroke-width:0px;
    linkStyle 578 stroke-width:0px;
    linkStyle 579 stroke-width:0px;
    linkStyle 580 stroke-width:0px;
    linkStyle 581 stroke-width:0px;
    linkStyle 582 stroke-width:0px;
    linkStyle 583 stroke-width:0px;
    linkStyle 584 stroke-width:0px;
    linkStyle 585 stroke-width:0px;
    linkStyle 586 stroke-width:0px;
    linkStyle 587 stroke-width:0px;
    linkStyle 588 stroke-width:0px;
    linkStyle 589 stroke-width:0px;
    linkStyle 590 stroke-width:0px;
    linkStyle 591 stroke-width:0px;
    linkStyle 592 stroke-width:0px;
    linkStyle 593 stroke-width:0px;
    linkStyle 594 stroke-width:0px;
    linkStyle 595 stroke-width:0px;
    linkStyle 596 stroke-width:0px;
    linkStyle 597 stroke-width:0px;
    linkStyle 598 stroke-width:0px;
    linkStyle 599 stroke-width:0px;
    linkStyle 600 stroke-width:0px;
    linkStyle 601 stroke-width:0px;
    linkStyle 602 stroke-width:0px;
    linkStyle 603 stroke-width:0px;
    linkStyle 604 stroke-width:0px;
    linkStyle 605 stroke-width:0px;
    linkStyle 606 stroke-width:0px;
    linkStyle 607 stroke-width:0px;
    linkStyle 608 stroke-width:0px;
    linkStyle 609 stroke-width:0px;
    linkStyle 610 stroke-width:0px;
    linkStyle 611 stroke-width:0px;
    linkStyle 612 stroke-width:0px;
    linkStyle 613 stroke-width:0px;
    linkStyle 614 stroke-width:0px;
    linkStyle 615 stroke-width:0px;
    linkStyle 616 stroke-width:0px;
    linkStyle 617 stroke-width:0px;
    linkStyle 618 stroke-width:0px;
    linkStyle 619 stroke-width:0px;
    linkStyle 620 stroke-width:0px;
    linkStyle 621 stroke-width:0px;
    linkStyle 622 stroke-width:0px;
    linkStyle 623 stroke-width:0px;
    linkStyle 624 stroke-width:0px;
    linkStyle 625 stroke-width:0px;
    linkStyle 626 stroke-width:0px;
    linkStyle 627 stroke-width:0px;
    linkStyle 628 stroke-width:0px;
    linkStyle 629 stroke-width:0px;
    linkStyle 630 stroke-width:0px;
    linkStyle 631 stroke-width:0px;
    linkStyle 632 stroke-width:0px;
    linkStyle 633 stroke-width:0px;
    linkStyle 634 stroke-width:0px;
    linkStyle 635 stroke-width:0px;
    linkStyle 636 stroke-width:0px;
    linkStyle 637 stroke-width:0px;
    linkStyle 638 stroke-width:0px;
    linkStyle 639 stroke-width:0px;
    linkStyle 640 stroke-width:0px;
    linkStyle 641 stroke-width:0px;
    linkStyle 642 stroke-width:0px;
    linkStyle 643 stroke-width:0px;
    linkStyle 644 stroke-width:0px;
    linkStyle 645 stroke-width:0px;
    linkStyle 646 stroke-width:0px;
    linkStyle 647 stroke-width:0px;
    linkStyle 648 stroke-width:0px;
    linkStyle 649 stroke-width:0px;
    linkStyle 650 stroke-width:0px;
    linkStyle 651 stroke-width:0px;
    linkStyle 652 stroke-width:0px;
    linkStyle 653 stroke-width:0px;
    linkStyle 654 stroke-width:0px;
    linkStyle 655 stroke-width:0px;
    linkStyle 656 stroke-width:0px;
    linkStyle 657 stroke-width:0px;
    linkStyle 658 stroke-width:0px;
    linkStyle 659 stroke-width:0px;
    linkStyle 660 stroke-width:0px;
    linkStyle 661 stroke-width:0px;
    linkStyle 662 stroke-width:0px;
    linkStyle 663 stroke-width:0px;
    linkStyle 664 stroke-width:0px;
    linkStyle 665 stroke-width:0px;
    linkStyle 666 stroke-width:0px;
    linkStyle 667 stroke-width:0px;
    linkStyle 668 stroke-width:0px;
    linkStyle 669 stroke-width:0px;
    linkStyle 670 stroke-width:0px;
    linkStyle 671 stroke-width:0px;
    linkStyle 672 stroke-width:0px;
    linkStyle 673 stroke-width:0px;
    linkStyle 674 stroke-width:0px;
    linkStyle 675 stroke-width:0px;
    linkStyle 676 stroke-width:0px;
    linkStyle 677 stroke-width:0px;
    linkStyle 678 stroke-width:0px;
    linkStyle 679 stroke-width:0px;
    linkStyle 680 stroke-width:0px;
    linkStyle 681 stroke-width:0px;
    linkStyle 682 stroke-width:0px;
    linkStyle 683 stroke-width:0px;
    linkStyle 684 stroke-width:0px;
    linkStyle 685 stroke-width:0px;
    linkStyle 686 stroke-width:0px;
    linkStyle 687 stroke-width:0px;
    linkStyle 688 stroke-width:0px;
    linkStyle 689 stroke-width:0px;
    linkStyle 690 stroke-width:0px;
    linkStyle 691 stroke-width:0px;
    linkStyle 692 stroke-width:0px;
    linkStyle 693 stroke-width:0px;
    linkStyle 694 stroke-width:0px;
    linkStyle 695 stroke-width:0px;
    linkStyle 696 stroke-width:0px;
    linkStyle 697 stroke-width:0px;
    linkStyle 698 stroke-width:0px;
    linkStyle 699 stroke-width:0px;
    linkStyle 700 stroke-width:0px;
    linkStyle 701 stroke-width:0px;
    linkStyle 702 stroke-width:0px;
    linkStyle 703 stroke-width:0px;
    linkStyle 704 stroke-width:0px;
    linkStyle 705 stroke-width:0px;
    linkStyle 706 stroke-width:0px;
    linkStyle 707 stroke-width:0px;
    linkStyle 708 stroke-width:0px;
    linkStyle 709 stroke-width:0px;
    linkStyle 710 stroke-width:0px;
    linkStyle 711 stroke-width:0px;
    linkStyle 712 stroke-width:0px;
    linkStyle 713 stroke-width:0px;
    linkStyle 714 stroke-width:0px;
    linkStyle 715 stroke-width:0px;
    linkStyle 716 stroke-width:0px;
    linkStyle 717 stroke-width:0px;
    linkStyle 718 stroke-width:0px;
    linkStyle 719 stroke-width:0px;
    linkStyle 720 stroke-width:0px;
    linkStyle 721 stroke-width:0px;
    linkStyle 722 stroke-width:0px;
    linkStyle 723 stroke-width:0px;
    linkStyle 724 stroke-width:0px;
    linkStyle 725 stroke-width:0px;
    linkStyle 726 stroke-width:0px;
    linkStyle 727 stroke-width:0px;
    linkStyle 728 stroke-width:0px;
    linkStyle 729 stroke-width:0px;
    linkStyle 730 stroke-width:0px;
    linkStyle 731 stroke-width:0px;
    linkStyle 732 stroke-width:0px;
    linkStyle 733 stroke-width:0px;
    linkStyle 734 stroke-width:0px;
    linkStyle 735 stroke-width:0px;
    linkStyle 736 stroke-width:0px;
    linkStyle 737 stroke-width:0px;
    linkStyle 738 stroke-width:0px;
    linkStyle 739 stroke-width:0px;
    linkStyle 740 stroke-width:0px;
    linkStyle 741 stroke-width:0px;
    linkStyle 742 stroke-width:0px;
    linkStyle 743 stroke-width:0px;
    linkStyle 744 stroke-width:0px;
    linkStyle 745 stroke-width:0px;
    linkStyle 746 stroke-width:0px;
    linkStyle 747 stroke-width:0px;
    linkStyle 748 stroke-width:0px;
    linkStyle 749 stroke-width:0px;
    linkStyle 750 stroke-width:0px;
    linkStyle 751 stroke-width:0px;
    linkStyle 752 stroke-width:0px;
    linkStyle 753 stroke-width:0px;
    linkStyle 754 stroke-width:0px;
    linkStyle 755 stroke-width:0px;
    linkStyle 756 stroke-width:0px;
    linkStyle 757 stroke-width:0px;
    linkStyle 758 stroke-width:0px;
    linkStyle 759 stroke-width:0px;
    linkStyle 760 stroke-width:0px;
    linkStyle 761 stroke-width:0px;
    linkStyle 762 stroke-width:0px;
    linkStyle 763 stroke-width:0px;
    linkStyle 764 stroke-width:0px;
    linkStyle 765 stroke-width:0px;
    linkStyle 766 stroke-width:0px;
    linkStyle 767 stroke-width:0px;
    linkStyle 768 stroke-width:0px;
    linkStyle 769 stroke-width:0px;
    linkStyle 770 stroke-width:0px;
    linkStyle 771 stroke-width:0px;
    linkStyle 772 stroke-width:0px;
    linkStyle 773 stroke-width:0px;
    linkStyle 774 stroke-width:0px;
    linkStyle 775 stroke-width:0px;
    linkStyle 776 stroke-width:0px;
    linkStyle 777 stroke-width:0px;
    linkStyle 778 stroke-width:0px;
    linkStyle 779 stroke-width:0px;
    linkStyle 780 stroke-width:0px;
    linkStyle 781 stroke-width:0px;
    linkStyle 782 stroke-width:0px;
    linkStyle 783 stroke-width:0px;
    linkStyle 784 stroke-width:0px;
    linkStyle 785 stroke-width:0px;
    linkStyle 786 stroke-width:0px;
    linkStyle 787 stroke-width:0px;
    linkStyle 788 stroke-width:0px;
    linkStyle 789 stroke-width:0px;
    linkStyle 790 stroke-width:0px;
    linkStyle 791 stroke-width:0px;
    linkStyle 792 stroke-width:0px;
    linkStyle 793 stroke-width:0px;
    linkStyle 794 stroke-width:0px;
    linkStyle 795 stroke-width:0px;
    linkStyle 796 stroke-width:0px;
    linkStyle 797 stroke-width:0px;
    linkStyle 798 stroke-width:0px;
    linkStyle 799 stroke-width:0px;
    linkStyle 800 stroke-width:0px;
    linkStyle 801 stroke-width:0px;
    linkStyle 802 stroke-width:0px;
    linkStyle 803 stroke-width:0px;
    linkStyle 804 stroke-width:0px;
    linkStyle 805 stroke-width:0px;
    linkStyle 806 stroke-width:0px;
    linkStyle 807 stroke-width:0px;
    linkStyle 808 stroke-width:0px;
    linkStyle 809 stroke-width:0px;
    linkStyle 810 stroke-width:0px;
    linkStyle 811 stroke-width:0px;
    linkStyle 812 stroke-width:0px;
    linkStyle 813 stroke-width:0px;
    linkStyle 814 stroke-width:0px;
    linkStyle 815 stroke-width:0px;
    linkStyle 816 stroke-width:0px;
    linkStyle 817 stroke-width:0px;
    linkStyle 818 stroke-width:0px;
    linkStyle 819 stroke-width:0px;
    linkStyle 820 stroke-width:0px;
    linkStyle 821 stroke-width:0px;
    linkStyle 822 stroke-width:0px;
    linkStyle 823 stroke-width:0px;
    linkStyle 824 stroke-width:0px;
    linkStyle 825 stroke-width:0px;
    linkStyle 826 stroke-width:0px;
    linkStyle 827 stroke-width:0px;
    linkStyle 828 stroke-width:0px;
    linkStyle 829 stroke-width:0px;
    linkStyle 830 stroke-width:0px;
    linkStyle 831 stroke-width:0px;
    linkStyle 832 stroke-width:0px;
    linkStyle 833 stroke-width:0px;
    linkStyle 834 stroke-width:0px;
    linkStyle 835 stroke-width:0px;
    linkStyle 836 stroke-width:0px;
    linkStyle 837 stroke-width:0px;
    linkStyle 838 stroke-width:0px;
    linkStyle 839 stroke-width:0px;
    linkStyle 840 stroke-width:0px;
    linkStyle 841 stroke-width:0px;
    linkStyle 842 stroke-width:0px;
    linkStyle 843 stroke-width:0px;
    linkStyle 844 stroke-width:0px;
    linkStyle 845 stroke-width:0px;
    linkStyle 846 stroke-width:0px;
    linkStyle 847 stroke-width:0px;
    linkStyle 848 stroke-width:0px;
    linkStyle 849 stroke-width:0px;
    linkStyle 850 stroke-width:0px;
    linkStyle 851 stroke-width:0px;
    linkStyle 852 stroke-width:0px;
    linkStyle 853 stroke-width:0px;
    linkStyle 854 stroke-width:0px;
    linkStyle 855 stroke-width:0px;
    linkStyle 856 stroke-width:0px;
    linkStyle 857 stroke-width:0px;
    linkStyle 858 stroke-width:0px;
    linkStyle 859 stroke-width:0px;
    linkStyle 860 stroke-width:0px;
    linkStyle 861 stroke-width:0px;
    linkStyle 862 stroke-width:0px;
    linkStyle 863 stroke-width:0px;
    linkStyle 864 stroke-width:0px;
    linkStyle 865 stroke-width:0px;
    linkStyle 866 stroke-width:0px;
    linkStyle 867 stroke-width:0px;
    linkStyle 868 stroke-width:0px;
    linkStyle 869 stroke-width:0px;
    linkStyle 870 stroke-width:0px;
    linkStyle 871 stroke-width:0px;
    linkStyle 872 stroke-width:0px;
    linkStyle 873 stroke-width:0px;
    linkStyle 874 stroke-width:0px;
    linkStyle 875 stroke-width:0px;
    linkStyle 876 stroke-width:0px;
    linkStyle 877 stroke-width:0px;
    linkStyle 878 stroke-width:0px;
    linkStyle 879 stroke-width:0px;
    linkStyle 880 stroke-width:0px;
    linkStyle 881 stroke-width:0px;
    linkStyle 882 stroke-width:0px;
    linkStyle 883 stroke-width:0px;
    linkStyle 884 stroke-width:0px;
    linkStyle 8

---


## Page 66

&lt;img&gt;IGU logo&lt;/img&gt;
THE PEOPLE'S UNIVERSITY

---


## Page 67

# UNIT 4 GRAPH COLOURINGS

## Structure

4.0 Introduction
4.1 Objectives
4.2 Vertex Colouring
4.3 Edge Colouring
4.4 Planar Graphs
4.5 Map Colouring Problem
4.6 Summary
4.7 Solutions/Answers

## 4.0 INTRODUCTION

You must have seen political maps of India with different states coloured differently to distinguish between them. Have you ever wondered what the minimum number of colours required to colour the map is for any two states with a common boundary to have two different colours? This problem of finding the minimum number of colours needed to colour a given map is called the map colouring problem.

We can formulate the problem in terms of graph theory. We can construct a graph in such a way that each state of India corresponds to a vertex of India and two states are adjacent if and only if the corresponding vertices are adjacent. So, we have to colour the vertices of the graph in such a way that any pair of adjacent vertices have different colours. In the map colouring problem, we ask for the minimum number of colours needed to carry out such a colouring.

Note that the construction mentioned above leads to a special class of graphs called planar graphs. If we are interested in the map colouring problem alone, it is enough to restrict ourselves to such graphs. However, the general vertex colouring problem, which asks for the minimum number of colours needed to colour the vertices of a given graph, not necessarily planar, is interesting in itself. So, we start our unit by discussing this problem in Sec. 4.2.

Analogous to the colouring of vertices, is the colouring of edges. In Sec. 4.3, we have a brief discussion on edge colourings. This includes the definition of edge colouring, some examples of edge colouring and statements of some of the well known results in this field.

In Sec. 4.4, as a preparation for our study of the map colouring problem, we study planar graphs. In this section, we will prove some basic results about planar graphs. We will also prove a characterization of planar graphs due to Kuratowski.

In Sec. 4.5, we study the map colouring problem. We give a brief history of the four colour theorem, which says that any map can be coloured with four colours. However, the proof of this theorem is beyond the scope of this course.

## 4.1 OBJECTIVES

After studying this unit, you should be able to

*   compute the vertex chromatic number of some simple graphs;

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;263&lt;/page_number&gt;

---


## Page 68

Graph Theory

*   compute the edge chromatic number for some simple graphs;
*   in simple cases verify whether a given graph is planar or not using Kuratowski’s theorem;
*   explain the map colouring problem and relate it to the study of planar graphs.

# 4.2 VERTEX COLOURING

In this section, we start our study of colourings by considering the graph in Fig. 1. We have given a colouring of K₃ using three colours, namely, red (r), green (g) and blue (b).

&lt;img&gt;Fig.1&lt;/img&gt;

Why have we used three colours? It is because we want the adjacent vertices to have different colours. In K₃, any two vertices are adjacent. So we need to colour each of the vertices with different colours. Keep this example in mind when you read the definition given below.

&lt;watermark&gt;'χ' is the Greek letter 'chi'.&lt;/watermark&gt;

**Definition:** A **vertex colouring** of a graph G is an assignment of colours to vertices of G in such a way that no two adjacent vertices have the same colour. A graph is called **k-vertex colourable** if it has a vertex colouring of k colours. The **minimum number of colours required to colour a graph G** is called the **vertex chromatic number of G**, usually denoted as **χ(G)**.

We will say that a graph is **k-chromatic** (or **k-colourable**) if it has chromatic number k.

In Fig. 1, we were able to use the names of the colours, red, green and blue, because we needed only three colours. Suppose we need, say, 20 colours, can we still use the names to refer to the colours? We may not remember the names of so many colours, and could call them Colour 1, Colour 2, etc. This will do just as well, because the names of the colours are not important as long as you can distinguish between the different colours. In the diagrams, we will denote the colours as [1], [2]....

Let us now look at some examples.

**Example 1:** Colour the graphs in Fig. 2 with the minimum possible number of colours. Also, find the chromatic numbers of the graphs.

&lt;img&gt;Fig. 2 : Some examples of colouring&lt;/img&gt;

**Solution:** In Fig. 2(a), K₁ has just one vertex. Let us colour this with [1]. So, one colour is clearly the minimum required for colouring this graph. Hence, its chromatic number is 1.

&lt;page_number&gt;264&lt;/page_number&gt;

---


## Page 69

Graph Colourings

In Fig. 2(b), K₂ has two adjacent vertices. We assign [1] to the vertex v₁ and [2] to the vertex v₂. Thus, we have a 2-colouring. Is there a 1-colouring? No! The two vertices are adjacent and so we need at least two colours. In other words, the chromatic number X(K₂) = 2.

In Fig. 2(c), we have three vertices and we can colour them with three different colours. But, can we also have a two-colouring? Notice that, v₁ and v₃ are not adjacent. So, we can colour them with the same colour, say, [1]. v₂ is adjacent to both v₁ and v₃. So, we cannot assign [1] to this. Let us assign [2] to v₂. So, we have a 2-colouring. As we cannot have a 1-colouring, this graph has chromatic number 2.

In Fig. 2(d), we have K₅. In this any two vertices are adjacent, so we need as many colours as there are vertices, that is, we need five colours. So K₅ has chromatic number 5.

*** χ(Kₙ) = n ∀n ≥1 because any pair of vertices are adjacent in Kₙ.

**Remark:** In the example above, we saw that the chromatic number of K₁ is 1. More generally, **a graph consists of isolated vertices, if and only if its chromatic number is 1.**

**Example 2:** Find the chromatic number of a bipartite graph with a non-empty edge set.

**Solution:** From Unit 2, you may recall that a graph G is bipartite if the vertex set of G can be partitioned into two **non-empty** disjoint subsets A and B Such that any two vertices in a given set are non-adjacent. We get a 2-colouring of G by assigning [1] to all the vertices in A and [2] to all the vertices in B. (This is illustrated in a particular case in Fig. 3.) Further, note that, since A and B are non-empty and since the edge set of G is non-empty, at least one vertex in A is adjacent to a vertex in B and these two vertices must have different colours. So, we cannot manage with less than two colours. So, X(G) = 2 if G is a bipartite graph with a non-empty edge set.

*** &lt;img&gt;Fig.3&lt;/img&gt;

**Remark:** We saw, in Example 2, that the chromatic number of a bipartite graph with non-empty edge set is 2. The converse is also true. Given a graph G and a 2-colouring of G, we can partition the edge set of G into two non-empty sets A and B defined as follows:
A = { v ∈ V(G) | v is assigned the colour [1] }
B = { v ∈ V(G) | v is assigned the colour [2] }
By the definition of colouring, no two vertices in A are adjacent, and similarly for B. Since A and B are disjoint, G is bipartite, by definition.

Here are some exercises to test your understanding of the examples above.

E1) What is the chromatic number of
i) a tree with at least two vertices?
ii) an even cycle C₂n, n ≥ 2?
iii) an odd cycle C₂n+1, n ≥ 1?

Now, if a graph is k-colourable, are all its subgraphs k-colourable? Let us see. Let G be a k-colourable graph and H be its subgraph. We assign to each vertex of H the same colour that we assigned to it, considered as a vertex of G. If two vertices are non-adjacent in G, they are non-adjacent in H, and therefore this gives a colouring of H. In other words, X(H) ≤ k = X(G) for every subgraph H of G. We can also recast this statement in the following form. **If a graph G has a subgraph H with chromatic number k, the chromatic number of G must be at least k. This fact**

&lt;page_number&gt;265&lt;/page_number&gt;

---


## Page 70

Graph Theory helps us in finding the chromatic number of a graph sometimes. We illustrate this in the next example.

**Example 3:** Find the chromatic number of the Grötzsch graph (see Fig 4(a).)

&lt;img&gt;Without colouring (a)&lt;/img&gt;
Without colouring
(a)

&lt;img&gt;With 4-colouring (b)&lt;/img&gt;
With 4-colouring
(b)

Fig. 4 : The Grötzsch graph

**Solution:** Fig.4(b) gives a 4-colouring of this graph. Can this graph have a 3-colouring? Let us see. Since the outer 5-cycle is an odd cycle, it needs three colours. So, we need at least three colours. Let us suppose the colours of x₁,...,x₅ are as shown in Fig.4(b). Since y₁ is adjacent to x₂ and x₅, we have to give it a colour different from 2 and 3. So, we assign 1 to it. Similarly, the colours of y₄ and y₅ must be 2 and 3, respectively. Since the vertex z is adjacent to vertices to which the colours 1, 2 and 3 have been allotted, we have to use a fourth colour for this vertex. So, this graph is not 3-colourable. Therefore, this has chromatic number 4.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

In the examples and exercises above, we saw that if a graph G has a subgraph H with chromatic number X(H) = n, then X(G) ≥ n. In particular, if a graph G has a subgraph H which is isomorphic to Kₙ (such a subgraph H is known as a **clique of size n**), the chromatic number of G is at least n.

However, **the converse is not true**, i.e., if a graph has chromatic number ≥ n, it need not have a clique of size n. The Petersen graph provides a counter-example for this. Its chromatic number is 3 (see E2). Convince yourself (you need not prove it) that it does not contain a clique of size 3, i.e., a subgraph isomorphic to K₃.

More generally, in 1955, Mycielski proved that, for any integer k, there exists a k-chromatic graph without triangles. The proof of this result is beyond the scope of this course. However, it is not difficult to prove the much weaker result that if the chromatic number of a connected graph is greater than 2, it contains an odd cycle. We leave this as an exercise for you (see E3), along with some more exercises, to test your understanding of the material we have covered so far.

E2) Find a 3-colouring of the graph in Fig.5, and its chromatic number.

&lt;img&gt;Fig.5&lt;/img&gt;
Fig.5

&lt;page_number&gt;266&lt;/page_number&gt;

---


## Page 71

Graph Colourings

E3) Show that the chromatic number of the Petersen graph, given in Fig. 6, is 3.
Also check that it does not contain K₃.

&lt;img&gt;Fig.6 : The Petersen graph&lt;/img&gt;

E4) Show that if X (G) ≥ 3 for a graph G, it contains an odd cycle

E5) Find the chromatic number of the following graph.

&lt;img&gt;Fig. 7&lt;/img&gt;

E6) Construct a graph with chromatic number 5.

&lt;watermark&gt;INDIAN UNIVERSITY THE PEOPLE'S&lt;/watermark&gt;

Recall that, we have shown that any 2-colourable graph is bipartite. How was this done? We had put all the vertices having the same colour in a single set. There were two colours and so we got two subsets. They were disjoint because no vertex can be assigned two colours.

We are going to extend these ideas to n-colourable graphs. We do this through the concept of colour classes, which we now define.

**Definition:** For a k-colouring of a graph G, consider the set Cᵢ = { x ∈ V(G) | x is assigned the colour [i] }, for 1 ≤ i ≤ k.
Clearly, Cᵢ ∩ Cⱼ = ∅, for every i ≠ j, and V(G) = C₁ ∪ ... ∪ Cₖ.
In particular, if X (G) = n, each of the n colours is assigned to at least one vertex. (Why?) So none of these subsets is empty. Therefore, we get a partition of the vertex set V(G) into n mutually disjoint non-empty subsets. The subsets C₁,..., Cₙ are called **the colour classes** of G given by the n-colouring.

The colour classes can be defined for any colouring of a graph G, not just for a χ (G)-colouring.

For example, the colour classes of a 2-colourable graph give a bipartition of the vertex set of the graph, making it bipartite.

Let us now look at some examples of colour classes.

**Example 4:** Find the colour classes in the two different colourings of the graph given in Fig.8.

&lt;page_number&gt;267&lt;/page_number&gt;

---


## Page 72

Graph Theory

&lt;img&gt;Fig. 8&lt;/img&gt;

**Solution :** The colour classes given by the colouring in Fig. 9(a) are C₁ = {x₁}, C₂ = {x₄, x₆, x₈, x₁₀, x₁₅, x₁₆}, C₃ = {x₃, x₁₂, x₁₃, x₁₄} and C₄ = {x₂, x₅, x₇, x₉, x₁₁}. Check that C₁ = {x₇, x₉, x₁₁, x₁₅}, C₂ = {x₁, x₅, x₈, x₁₂, x₁₄}, C₃ = {x₄, x₁₀, x₁₆}, C₄ = {x₂, x₆}, and C₅ = {x₃, x₁₃} are the colour classes corresponding to the colouring in Fig. 9(b).

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig. 9 (a)&lt;/img&gt;
&lt;img&gt;Fig. 9 (b) F&lt;/img&gt;

*** Try some exercises to test your understanding of the example above.

E7) Check whether ‘xRy iff x and y lie in the same colour class’ defines an equivalence relation on the vertices of a graph G.
E8) Colour the following graph in two different ways, and give the colour classes in each case.

&lt;page_number&gt;268&lt;/page_number&gt;

---


## Page 73

Graph Colourings

&lt;img&gt;A graph with 7 vertices (x1, x2, x3, x4, x5, x6, x7) connected by edges.&lt;/img&gt;
Fig. 10

We have seen that any colouring of a graph gives rise to colour classes. You know that, if x, y are two vertices in a colour class C_i, then xy ∉ E(G). So, **each colour class consists of mutually non-adjacent vertices**. We now give a name to those subsets of the vertex set of a graph with this property.

**Definition:** A subset S of the vertex set V(G) of a graph G, is said to be an **independent set** if any two vertices in S are non-adjacent. An independent set is called **maximal** if it is not contained in any other independent set. The number of vertices in a largest independent set of G, is called the **independence number** of the graph G, and is denoted by α(G).

So, for example, each colour class is an independent set, and, in fact, a maximal independent set. However, all independent sets are not dependent on a particular colouring.

**Example 5 :** Find three different maximal independent sets in the graph given in Fig. 11.
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;A graph with 8 vertices (v1, v2, v3, v4, v5, v6, v7, v8) connected by edges.&lt;/img&gt;
Fig. 11

**Solution :** The graph has the following maximal independent sets :
{v8, v5}, {v5, v1, v2, v3, v7}, {v1, v2, v3, v4, v6, v7}
Let us check this.

Firstly, {v8, v5} is a maximal independent set because all the other vertices are adjacent to one of these two vertices. So, if any more vertices are added, the resulting set will no longer be an independent set.

In the same way, you can check that the other two sets are also maximal independent sets.

*** &lt;page_number&gt;269&lt;/page_number&gt;

---


## Page 74

Graph Theory

Now test your understanding of independent sets by trying the following exercises.

E9) Find an independent set of cardinality 4 in the graph given below:

&lt;img&gt;Fig. 12&lt;/img&gt;

E10) Find α(G) for the graphs given in Fig.8 and Fig. 10.

If we can colour the vertices of a graph, can we colour the edges of a graph? Is it interesting, or useful, to do so? In the next chapter, we will answer these questions.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

# 4.3 EDGE COLOURING

In this section, we consider the problem of colouring the edges of a graph in such a way that no two edges with a common vertex receive the same colour. We will not prove any of the important results in this subject although we will state some of them. The purpose of this section is to give a brief introduction to edge colouring. We begin by defining edge colouring.

**Definition:** A k-edge colouring of a graph G is an assignment of k colours to the edges of G in such a way that no two edges incident with the same vertex have the same colour. A graph is **k-edge colourable** if it has a k-edge colouring. The **minimum number** of colours required to colour the edges of a graph is called the **edge chromatic number of G**, usually denoted by χ'(G).

Let us now look at some examples of edge colouring. The easiest case is the edge colouring of those graphs which have edge chromatic number 1.

**Example 6 :** Find all the graphs that have edge chromatic number 1.

**Solution:** Suppose a graph G has edge chromatic number 1. Since the edge chromatic number is one, the graph is 1-edge colourable, and no two edges share an end vertex, that is, the graph must be the union of some isolated vertices and some components consisting of two vertices and an edge (see Fig.13). Conversely, a graph which is the union of isolated vertices and components having two vertices each has edge chromatic number 1.

&lt;img&gt;Fig.13&lt;/img&gt;

***

**Example 7 :** Colour the edges of the graphs K₃, K₄, K₅.

&lt;page_number&gt;270&lt;/page_number&gt;

---


## Page 75

Graph Colourings

**Solution :** The colouring of K₃, K₄, K₅ is given in Fig. 14. Here no two adjacent edges have received the same colour. In all the cases, we have used the least possible colours.

&lt;img&gt;Fig. 14 - K₃ edge colouring&lt;/img&gt;
&lt;img&gt;Fig. 14 - K₄ edge colouring&lt;/img&gt;
&lt;img&gt;Fig. 14 - K₅ edge colouring&lt;/img&gt;

***

**Example 8 :** Give an edge colouring of the Petersen graph.

**Solution:** Fig. 15 gives a 4-edge colouring of the Petersen graph.

&lt;img&gt;Fig. 15 - Petersen graph edge colouring&lt;/img&gt;

Again no two adjacent edges have received the same colour. You can quickly check that three colours will not be enough. So χ'(G) = 4.

***

**Example 9:** Give edge colourings of all the trees on 5 vertices.

**Solution :** In Fig.16, we have presented all types of possibilities, with colourings.

&lt;img&gt;Fig. 16 - Tree on 5 vertices edge colourings&lt;/img&gt;

Again we have used the least possible number of colours.

***

**Example 10:** Find the edge-chromatic number of Cₙ.

**Solution:** As in the case of vertex colouring, if n is even, the edge chromatic number is 2. We can colour the edges alternately with the two colours. If n is odd, the edge chromatic number is 3. We have illustrated this in the case of C₄ and C₅ in Fig.17.

&lt;img&gt;Fig. 17 - C₄ and C₅ edge colourings&lt;/img&gt;

***

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;271&lt;/page_number&gt;

---


## Page 76

Graph Theory

If G is a graph and v ∈ V(G) such that d<sub>G</sub>(v) = Δ(G), then all the edges incident on v must receive different colours. Hence, any edge colouring of G will need at least Δ(G) colours, that is, Δ(G) ≤ χ'(G).

Regarding an upper bound for χ'(G), in 1964 Vizing proved the following result.

**Theorem 1:** For any graph G, χ'(G) ≤ Δ(G) + 1.

So, for any graph G, Δ(G) ≤ χ'(G) ≤ Δ(G) + 1.

Therefore, there are only two possibilities for the edge chromatic number of a graph G, either Δ(G) or Δ(G) + 1. We now present some of the results known in this direction, without proof.

1) The **edge chromatic number** of K<sub>n</sub> is n, if n is odd (≠ 1) and n - 1 if n is even. Recall that, K<sub>n</sub> is (n - 1)-regular. So Δ(K<sub>n</sub>) = n - 1.

2) For a **bipartite graph** G, χ'(G) = Δ(G) (proved by König in 1916).

Here are some related exercises now.

E11) What is the edge chromatic number of K<sub>m,n</sub> ?

E12) Consider the tree T given in Fig. 18. Give an explicit Δ(T)-edge colouring of T.

&lt;img&gt;Fig.18&lt;/img&gt;

In the introduction, we mentioned that the map colouring problem can be reduced to finding the minimum number of colours needed to colour a special class of graphs called planar graphs. In the next section, we define planar graphs and prove some basic results that will be useful in the study of the map colouring problem.

## 4.4 PLANAR GRAPHS

In transistor radios and television sets, you must have seen printed circuit boards. These boards have slots for various components and these slots are connected to each other. The connection between these slots must be made in such a way that no two connections cross each other. Given an electronic circuit, is it always possible to design a printed circuit board corresponding to it?

This can be formulated as a problem in graph theory. We replace the electronic components by vertices and the connections between them by edges. If the resulting graph can be drawn in such a way that no two of the edges cross each other except at the vertices, then we can design a printed circuit board for the given circuit. Let's start by seeing what such graphs are called.

&lt;page_number&gt;272&lt;/page_number&gt;

---


## Page 77

Graph Colourings

**Definition:** A graph G is called **planar** if it can be drawn on a plane in such a way that no two edges cross each other at any point except possibly at a common end vertex. Such a drawing is called a **plane drawing**.

To see some examples of planar graphs, consider Fig. 19. In this figure, we have given the five regular solids called platonic solids. In the second row, we have given the corresponding planar graphs. In each of these graphs, the vertices correspond to the vertices of the associated solid and the edges correspond to the edges of the solid.

&lt;img&gt;Fig. 19: Regular solids and the corresponding planar graphs&lt;/img&gt;

Next, we introduce the concept of a region. Look at the tetrahedron in Fig. 19 (a). It has four faces. The planar graph corresponding to it is given in Fig. 19(A). It divides the plane into four faces, or regions, which we have numbered from 1 to 4 in the figure. Similarly, the graph of the cube, given in Fig. 19(B) divides the plane into six regions.

In all the cases above, it is very clear what the different regions are. But, look at the graph in Fig. 20. Into how many regions does it divide the plane? Two or three? Do the points x and y lie in the same region or in different regions? To avoid such confusion we need to define the concept of a region carefully. Here is the definition.

**Definition:** Given a plane drawing of a planar graph G, by a **region** (or **face**) of G, we mean a maximal portion of the plane for which any two points a, b in it can be joined by a curve which lies completely in that portion of the plane.

If R is a region of a planar graph G, by the **boundary of R** we mean all those points x in the plane corresponding to the vertices and edges of G having the property that x can be joined to any point in that region by a simple curve all of whose points, except x, are in that region.

There is always one unbounded region of G, and it is called the **exterior region** of G. Any other region is called an **interior region**.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig. 20: x and y are just points in the plane, they are not vertices.&lt;/img&gt;
&lt;page_number&gt;273&lt;/page_number&gt;

---


## Page 78

Graph Theory

Let us go back to Fig. 20 again. Armed with this definition, we can answer the question we raised. As you can see in Fig. 21, the points x and y can be joined by a curve that does not cross any of the edges. So, there are only two regions, the region inside the triangle and the region outside it. Both the points lie in the exterior region of the triangle.

&lt;img&gt;Fig.21&lt;/img&gt;

Let us now look at an example to understand these concepts better.

**Example 11:** Find the number of regions in the graphs given in Fig.22.

&lt;img&gt;Fig. 22 (a)&lt;/img&gt; &lt;img&gt;Fig. 22 (b)&lt;/img&gt;
(a) (b)

**Solution:** The graph in Fig. 22 (a) has 8 regions, 7 interior and 1 exterior region. In the graph in Fig. 22(b), there are 3 regions.

*** Now, try the following exercises.

E13) Find the number of regions in a tree, a cycle and K₄.
E14) Is a subgraph of a planar graph planar ? Why ?

Now, given a planar (p,q)-graph, is there any relationship between the number of regions, r, and p,q ? Let us calculate the quantity p – q + r for all the planar graphs in Fig. 13 and for the graph in Fig. 16(b), to see if we can find an answer to this.

&lt;watermark&gt;© THE UNIVERSITY&lt;/watermark&gt;

<table>
<thead>
<tr>
<th>Graph</th>
<th>P</th>
<th>q</th>
<th>r</th>
<th>p – q + r</th>
</tr>
</thead>
<tbody>
<tr>
<td>Fig. 16(b)</td>
<td>6</td>
<td>7</td>
<td>3</td>
<td>2</td>
</tr>
<tr>
<td>Tetrahedron</td>
<td>4</td>
<td>6</td>
<td>4</td>
<td>2</td>
</tr>
<tr>
<td>Cube</td>
<td>8</td>
<td>12</td>
<td>6</td>
<td>2</td>
</tr>
<tr>
<td>Octahedron</td>
<td>6</td>
<td>12</td>
<td>8</td>
<td>2</td>
</tr>
<tr>
<td>Dodecahedron</td>
<td>20</td>
<td>30</td>
<td>12</td>
<td>2</td>
</tr>
<tr>
<td>Icosahedron</td>
<td>12</td>
<td>24</td>
<td>18</td>
<td>2</td>
</tr>
</tbody>
</table>

As you can see, p – q + r is 2 for all these planar graphs. In fact, the following theorem, proved by Euler in 1736, shows that this is true for all such graphs.

**Theorem 2 (Euler’s formula):** If G is a connected planar (p,q)-graph, then the number r of the regions of G is given by r = q – p + 2.

**Proof:** We apply induction on q, the number of edges of G, to show that p – q + r = 2.
If q = 0, then G just consists of 1 isolated vertex since it is connected. Hence, r = 1 and the formula holds.

Now, assume that the formula holds for any plane drawing of a (p,t)-graph for every t ≤ (q – 1), and suppose G is a (p, q)-graph.

If G is a tree, then p = q + 1 and r = 1, so that the formula holds.

&lt;page_number&gt;274&lt;/page_number&gt;

---


## Page 79

Graph Colourings

If G is not a tree, then it contains a cycle. Let e be an edge of G that lies on a cycle of G, and consider the subgraph G – e of G. When we remove this edge e on the cycle, we are joining two regions to make one region out of them (e.g., if we remove e in Fig.23(a), the earlier regions 1 and 2 join to become one region in Fig.23(b).) So, G – e has p vertices, (q – 1) edges and (r – 1) regions.

&lt;img&gt;Fig. 23a&lt;/img&gt;
(a)

&lt;img&gt;Fig. 23b&lt;/img&gt;
(b)

**Fig. 23**

Now, by the induction assumption, Euler’s formula holds for G – e. So, the number of regions = number of edges – number of vertices + 2.
i.e., r – 1 = (q – 1) – p + 2.
⇒ r = q – p + 2.

Hence, by induction, the result is true for any connected planar graph.

**Remark :** Since r = p – q + 2, where p and q are fixed once we fix a graph, the number of regions in a plane drawing of a planar graph is independent of the plane drawing.

The result we have just proved does not immediately help us to tell whether a graph is planar or not. However, we derive a necessary condition for planarity from it that is very useful. It tells us intuitively, that a planar graph can’t have ‘too many’ edges. Recall that a graph on p vertices can have up to $\frac{p(p-1)}{2}$ edges. In the case of planar graphs, there is a much better bound. We give this bound in the next theorem.

**Theorem 3:** If G is a planar (p, q)-graph, with p ≥ 3, then q ≤ 3p – 6. Further, if G is also bipartite, we have q ≤ 2p – 4.

**Proof :** For p = 3, the result is clearly true. So, we assume p ≥ 4. Let G have r regions. For each region R of G, the number of edges lying on its boundary is at least 3. So, if S is the sum of the number of edges of each region, then S ≥ 3r. Also, every edge of G is counted once or twice while obtaining S. So S ≤ 2q. Thus, 3r ≤ 2q. Using Euler’s formula, we obtain 3(q – p + 2) ≤ 2q, which gives us q ≤ 3p – 6.

Now, if G is also bipartite, it will not contain any 3-cycle. Therefore, a region will be bounded by at least 4 edges, so that S ≥ 4r. Then, as argued above, we get q ≤ 2p – 4.

Let us see how this result helps us to check whether a graph is planar or not.

**Example 12:** Show that K₅ is not planar.

**Solution:** Suppose K₅ is planar. Then the number of edges and vertices in K₅ satisfy the relation q ≤ 3p – 6 given in Theorem 3. K₅ has 5 vertices and 10 edges, so 10 ≤ 3 × 5 – 6, i.e. 10 ≤ 9, a contradiction. Thus, K₅ is non-planar.

Try the next exercise to check your understanding of Theorem 3.

E15) Show that K₃,₃ is non-planar. Hence, show that given 3 houses, each having 3 outlets for electricity, gas and water, respectively, it is not possible to

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

&lt;page_number&gt;275&lt;/page_number&gt;

---


## Page 80

Graph Theory

connect each of these utilities to each of the houses without the lines or mains crossing.

We have already seen that K<sub>5</sub> and K<sub>3,3</sub> are not planar. To prove this we used either of two necessary conditions. However, these conditions are not sufficient. For example, in the Grötzsch graph (see Fig.4), p = 11, q = 20 and 20 ≤ 33 – 6 = 27. So, the condition in Theorem 3 is satisfied. But, as we shall show later, the Grötzsch graph is not planar.

So, the question is whether there is a necessary and sufficient condition for a graph to be planar. In 1930, K. Kuratowski, a Polish mathematician, proved a necessary and sufficient condition for a graph to be planar. We will state this theorem and illustrate its application through an example. To understand the statement, let us first consider Fig. 24 below.

&lt;img&gt;Fig. 24 : Subdivision of a graph&lt;/img&gt;

In this figure, we have started with K<sub>4</sub> and inserted vertices of degree 2 in some of the existing edges. For example, in Fig. 24(b), we have inserted a vertex a on the edge uv. In effect, this replaces the edge uv with two new edges va and au. We have made similar changes in the graphs in Fig. 24(b), Fig. 24(c), Fig. 24(d) and Fig. 24(e). In this way we have got subdivisions of the graph in Fig. 24(a), as you shall now see.

**Definition:** A graph G′ is a **subdivision** of a graph G if it can be obtained by adding one or more vertices of degree 2 on the existing edges of G. In other words, we ‘subdivide’ some of the existing edges.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig.25&lt;/img&gt;

**Note**: If a graph is planar, all its subdivisions are planar. If a graph G is non-planar, any subdivision of G is also non-planar. So, if a graph contains a non-planar subgraph or a subgraph which is a subdivision of a non-planar graph, it is non-planar. For example, the graph in Fig. 25 is non-planar since it contains as a subgraph a subdivision of K<sub>5</sub> (shown by dotted lines), which is a non-planar graph.

In proving the non-planarity of the graph in Fig. 25, is it just a coincidence that we found that it had a subdivision of K<sub>5</sub> as a subgraph? Here’s an exercise about this.

E16) Check whether the graph given in Fig.26
i) is planar;
ii) has a subdivision of K<sub>5</sub>.
&lt;img&gt;Fig.26&lt;/img&gt;

&lt;page_number&gt;276&lt;/page_number&gt;

---


## Page 81

Graph Colourings

From E16 you see that non-planar graphs do not necessarily contain a subdivision of K₅. However, Kuratowski's theorem (stated below) says that a non-planar graph has to contain a subgraph which is a subdivision of K₅ or K₃,₃. So, we need to restrict our search for non-planar subgraphs (or their subdivisions) to only these two graphs.

**Theorem 4 (Kuratowski) :** A graph G is non-planar if and only if it contains a subdivision of K₅ or K₃,₃ as a subgraph.

We will not present the proof of this statement here. But, we shall look at an example to see how this theorem can be used to prove non-planarity.

**Example 13:** Show that the Grötzsch graph (see Fig. 4) is non-planar.

**Solution:** From Kuratowski's theorem we know that we have to look for a subgraph which is a subdivision of K₅ or K₄. But, in this case, which of these two should we look for? Note that a subdivision of a graph does not affect the degree of any of the vertices of a graph; it only introduces new vertices of degree 2.

So, if our graph contains a subdivision of K₅, it will contain at least 5 vertices of degree 4. If it contains a subdivision of K₃,₃ it will have at least six vertices of degree 3.

Let us first check if our graph contains a subdivision of K₃,₃. Since it contains only five vertices of degree 3, namely, y₁, y₂, y₃, y₄ and y₅, it cannot contain a subdivision of K₃,₃.

So, let us check if it contains a subdivision of K₅. K₅ contains 5 vertices of degree 4. In the Grötzsch graph also there are 5 vertices of degree 4, namely x₁, x₂, x₃, x₄ and x₅. Let us remove the middle vertex, labelled as z. We get the graph given in Fig. 27(a).

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Grötzsch graph with labels x₁, x₂, x₃, x₄, x₅ and y₁, y₂, y₃, y₄, y₅.&lt;/img&gt;
&lt;img&gt;Grötzsch graph after removing the middle vertex z, showing vertices x₁, x₂, x₃, x₄, x₅.&lt;/img&gt;

Fig. 27 : Non-planarity of the Grötzsch graph.

As you can see, it can be obtained from K₅ in Fig. 27(b) by adding degree two vertices to x₁x₃, x₁x₄, x₂x₄, x₂x₅, x₃x₅ and x₁x₅. So, it is non-planar.

***

Now, an exercise for you to try!

E17) Show that the Petersen graph (in Fig.5) is non-planar.
(Hint : Consider the graph obtained by removing the two horizontal edges.)

In the next section we will discuss the map colouring problem. We will show that this can be reduced to a colouring of planar maps.

&lt;page_number&gt;277&lt;/page_number&gt;

---


## Page 82

Graph Theory

# 4.5 MAP COLOURING PROBLEM

The four colour problem asks whether any map of a part of the world can be coloured with 4 colours. We begin this section with a brief discussion of the history of the four colour problem. We then show how to construct a planar graph corresponding to a given map in such a way that colouring the graph is equivalent to colouring the map. So, if we can prove that any planar map can be coloured with four colours, we would have proved that any map can be coloured with four colours. In 1976, the American mathematicians, Kenneth Appel and Wolfgang Haken, proved that four colours are enough to colour planar graphs. They used nearly 1200 hours of computer time on some of the fastest computers available at that time to prove this by doing a case-by-case analysis. This gives an idea about the complexity of the proof, which we will not be giving in this course.

Now, for some background about this problem. In 1852, Francis Guthrie communicated the four colour problem to De Morgan through his brother Fredrick Guthrie, who was a student at the University College, London at that time. It appeared in print for the first time when Cayley published a paper on this problem in the Royal Geographical Society in 1879. In this paper, he outlines where the difficulties lie in this problem. In the same year, A.B. Kempe published a proof of the theorem in the American Journal of Mathematics. However, in 1890, P.J. Heawood pointed out a mistake in Kempe's proof. He also showed that the proof can be modified to show that five colours are enough to colour any map. Since then many mathematicians, G.D. Birkhoff, Veblen, Ore, Franklin among others, contributed to the solution of the problem. Appel and Haken finally solved the problem in 1976.

We now show how to construct a planar graph corresponding to a given map in such a way that colouring the vertices of the graph is equivalent to colouring the map.

Consider the map given in Fig. 28(a) below. There are 10 regions in the map, A, B, C, D, E, F, G, H, I and J, including the exterior region. In this map we add a vertex corresponding to each region of the map (see Fig.28(b)). Note that we have added a vertex corresponding to the exterior region, namely, J.

&lt;watermark&gt;GOVERNMENT UNIVERSITY&lt;/watermark&gt;

&lt;img&gt;
A diagram showing a map with regions A, B, C, D, E, F, G, H, I, and J.
&lt;/img&gt;
(b)

&lt;img&gt;
A diagram showing a planar graph corresponding to the map in Fig. 28(a).
Vertices: A, B, C, D, E, F, G, H, I, J.
Edges: A-a, B-b, C-c, D-d, E-e, F-f, G-g, H-h, I-i, J-j.
&lt;/img&gt;

Fig. 28

We join two vertices if the corresponding regions have an edge in common. For example, we have connected a and c because they have a common boundary (see Fig. 29 below). We have not connected the vertices a and e because they do not have a common boundary. We do not connect two vertices if the corresponding regions share only a point and not a boundary. For example, we have not connected c and g by an edge for this reason.

As you can see, we get a planar graph, and colouring this graph is equivalent to colouring the map. (We assume that the exterior region of the map is coloured with a single colour.) So, the four colour problem can be stated as follows:

&lt;page_number&gt;278&lt;/page_number&gt;

---


## Page 83

Graph Colourings

&lt;img&gt;Fig.29&lt;/img&gt;

**Is it possible to colour any planar graph with four colours?**

The following theorem answers this question.

**Theorem 5 (Appel-Haken) :** Any planar graph can be coloured with four colours.

As we mentioned in the introduction we will not be proving this theorem.

Now, the question is whether we can get a better result. Can we colour a map with three colours always? No! For example, K₄ is planar, being the graph corresponding to a tetrahedron, and it cannot be coloured with three colours. So, we cannot improve the result in Theorem 5.

Why don't you try an exercise now ?

&lt;watermark&gt;IGNOU&lt;/watermark&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

E18) Show that χ(K₅) = 5. Does this contradict Theorem 5 ? Give reasons for your answer.

E19) Check whether there exists a non-planar graph with vertex chromatic number i) 1, ii) 2, iii) 3.

On doing E18, you will have realised that the result in Theorem 5 would not hold true for non-planar graphs.

We have now reached the end of this unit. Let us briefly summarise what we have learnt so far.

## 4.6 SUMMARY

In this unit we discussed the following concepts along with several examples and exercises.
i) **Vertex colouring of a graph:** A vertex colouring of a graph is an assignment of colours to its vertices in such a way that no two adjacent vertices receive the same colouring.

ii) **Vertex chromatic number of graph:** The chromatic number of a graph is the minimum number of colours required to colour the graph.

iii) **A colour class of a colouring:** For each colour of a colouring, the set of all vertices that are coloured with that colour is the colour class of that colour.

&lt;page_number&gt;279&lt;/page_number&gt;

---


## Page 84

Graph Theory

iv) **Independent set:** A subset of the vertex set is independent if any two vertices in the set are non-adjacent.

v) **Edge colouring of a graph:** An edge colouring of a graph is an assignment of colours to its edges in such a way that no two edges with a common vertex are given the same colour.

vi) **Edge chromatic number of a graph:** The edge chromatic number of a graph is the minimum number of colours needed to colour the edges of graph.

vii) **Planar graph:** A graph is planar if there is a plane drawing in which no two edges cross each other, except at vertices.

viii) **Subdivision of a graph:** A graph G₂ is a subdivision of another graph G₁ if it can be obtained from G₁ by inserting vertices of degree two in the existing edges.

In the process we also studied the following matters.

1) χ(Kₙ) = n; andχ(G) = 2 iff G is a bipartite graph with E(G) ≠ φ.

2) If G has a subgraph isomorphic to Kₙ, then χ(G) ≥ n. But the converse is not true. However, if χ(G) ≥ 3, then G contains an odd cycle.

3) For a graph G, the colour classes corresponding to each of the χ(G) colours give maximal independent sets of V(G).

4) Vizing’s bound for the edge chromatic number of a graph, namely,
   Δ (G) ≤ χ’ (G) ≤ Δ (G) + 1.

5) Euler’s formula for planar graphs, which states that Number of vertices – Number of edges + Number of regions = 2, for any planar graph.

6) If G is a planar (p, q)-graph, with p ≥ 3, then q ≤ 3p – 6. Further, if G is also bipartite, we have q ≤ 2p – 4.

7) Kuratowski’s characterization of planar graphs, which says that a graph is planar if and only if it does not contain a subdivision of K₃,₃ or K₅.

8) The four colour theorem (without proof), which says that any planar graph can be coloured with four colours.

&lt;watermark&gt;GOVERNMENT OF INDIA UNIVERSITY&lt;/watermark&gt;

## 4.7 SOLUTIONS/ANSWERS

E1)
i) Trees do not contain cycles as subgraphs, and therefore, in particular, they are bipartite. Since a tree is connected and we have assumed it has at least two vertices, it has chromatic number 2.

ii) Even cycles do not contain odd cycles as subgraphs. So, they are bipartite. Therefore, they have chromatic number 2.

iii) The chromatic number of an odd cycle is 3. Since it is not bipartite, its chromatic number is at least 3. We get a 3-colouring of C₂n+₁ as follows:Let { v₁, v₂,……,v₂n+₁ }be the vertex set of C₂n+₁.

&lt;page_number&gt;280&lt;/page_number&gt;

---


## Page 85

Graph Colourings

We assign [1] to all the vertices in the set {v<sub>i</sub> ∈ V(C<sub>2n+1</sub>) | i odd, 1 ≤ i ≤ 2n}, and [2] to all the vertices in the set {v<sub>i</sub> | i even, 2 ≤ i ≤ 2n}.
Now, v<sub>2n+1</sub> is adjacent to both v<sub>1</sub> and v<sub>2n</sub>. So, we cannot assign [1] or [2] to this vertex. Therefore, we assign the colour [3] to v<sub>2n+1</sub>.

E2) A three-colouring of the Petersen graph is given below.

&lt;img&gt;Fig. 30&lt;/img&gt;

Further, the Petersen graph contains a 5-cycle which has chromatic number three. So, the Petersen graph has chromatic number three.

E3) Since it has chromatic number greater than 2, it cannot be bipartite. So, it must contain an odd cycle.

E4) A 3-colouring of the graph is given in Fig.31. Also, it has cycles of length 5 as subgraphs, and we have already seen that cycles of odd length have chromatic number 3. Therefore, the chromatic number of this graph is 3.

&lt;img&gt;Fig. 31&lt;/img&gt;

E5) In the graph in Fig. 7, the graph induced by v<sub>4</sub>, v<sub>5</sub>, v<sub>6</sub>, v<sub>7</sub> is K<sub>4</sub>. So, it has a clique of size 4 and therefore we need at least 4 colours. We get a 4-colouring by assigning [1] to v<sub>1</sub>, [2] to v<sub>2</sub>, [3] to v<sub>3</sub>, [2] to v<sub>4</sub> [3] to v<sub>5</sub>, [1] to v<sub>6</sub> and [4] to v<sub>7</sub>. So, the chromatic number is 4.

E6) The figure given in Fig. 32 is 5-chromatic. It contains a clique of size 5, namely, the subgraph induced by the vertices w<sub>1</sub>, w<sub>2</sub>, w<sub>3</sub>, w<sub>4</sub>, w<sub>5</sub>. So, we need at least 5 colours. We first give a 5-colouring to the subgraph isomorphic to

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;page_number&gt;281&lt;/page_number&gt;

---


## Page 86

Graph Theory

K₅ by assigning 1 to wᵢ, 1 ≤ i ≤ 5. Next, we assign 2 to v₁, 3 to v₂, 1 to v₃, 2 to v₄, and 1 to v₅.

&lt;img&gt;Fig. 32&lt;/img&gt;

E7) Firstly, every vertex lies in some colour class.
Next, (x,x)∈R ∀ x∈V(G).
Then, (x,y)∈R ⇔ (y, x)∈R, x, y∈V(G).
Finally, you can see that (x,y)∈R and(y, z)∈R ⇒ (x, z)∈R, x, y, z∈V(G).

E8) Two different colourings are given in Fig. 33.

&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig. 33 (a)&lt;/img&gt;
&lt;img&gt;Fig. 33 (b)&lt;/img&gt;

The colour classes for the colouring in Fig. 33(a) are {x₁}, {x₂}, {x₇}, {x₃, x₅}, {x₄, x₆}. The colour classes for the colouring in Fig. 33(b) are {x₁}, {x₂}, {x₃}, {x₄, x₇} and {x₅, x₆}.

E9) {v₁, v₂, v₄, v₆}

E10) For the graph in Fig.8, you can see that {x₁₃, x₁₄, x₃, x₅, x₇, x₉, x₁₁} is an independent set and any other set has ≤ 7 elements. Thus α(G) = 7.

For the graph in Fig.10, note that for every vertex xᵢ, there are precisely two vertices in G not adjacent to xᵢ. But those two are adjacent. Hence, α(G) = 2.

E11) Since Kₘ,ₙ is a bipartite graph, by König's result,
χ'(Kₘ,ₙ) = Δ(Kₘ,ₙ) = min(m,n).

E12) The required Δ(T)-colouring is given in Fig. 34. You must remember that it is not unique.

&lt;page_number&gt;282&lt;/page_number&gt;

---


## Page 87

Graph Colourings

&lt;img&gt;Fig.34&lt;/img&gt;

E13) For a tree, the number of regions is 1; for a cycle it is 2; for K₄ it is 4 (see Fig.35).

E14) Yes. This is because, if G can be drawn without its edges crossing each other, this would also hold for any subgraph of G, as its edge set is a subset of the edge set of G.

E15) Since K₃,₃ is bipartite, we can apply Theorem 5. Here p = 6 and q = 9. But, 2p - 4 = 10 > 9 = q. So, K₃,₃ is not planar.
The situation given is modelled by K₃,₃. Since K₃,₃ is non-planar, some of its edges will cross each other. Therefore, the corresponding lines or mains of the utility will cross.

E16) If you consider the vertex sets {x₁, x₃, x₄} and {x₂, x₅, x₆}, you will see that K₃,₃ is a subgraph of this graph. Thus, the graph is non-planar. You can also check that it is not a subdivision of K₅.

E17) The graph obtained by deleting the two horizontal edges is shown in Fig. 36(a). We have redrawn Fig. 36(a) in Fig. 36(b) so that you can clearly see that it is a subdivision of K₃,₃.

&lt;img&gt;Fig.35&lt;/img&gt;
&lt;watermark&gt;THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;
&lt;img&gt;Fig. 36&lt;/img&gt;

E18) Since K₅ is non-planar, there is no contradiction. Use the arguments given in Sec.4.2 to show χ(K₅) = 5.

E19) χ(G) = 1 iff G consists of isolated vertices. In this case, there is no question of non-planarity.
χ(K₃,₃) = 2.
χ(G) = 3, where G is the Petersen graph.

&lt;page_number&gt;283&lt;/page_number&gt;

---


## Page 88

NOTE

&lt;watermark&gt;IGNOU THE PEOPLE'S UNIVERSITY&lt;/watermark&gt;

---


## Page 89

MPDD/IGNOU/P.O. 1H /AUGUST, 2023

# MCS-212
## Discrete Mathematics

&lt;img&gt;ignou logo&lt;/img&gt;
THE PEOPLE'S UNIVERSITY

Indira Gandhi National Open University
School of Computer and Information Sciences (SOCIS)

# MCS-2212
# Discrete Mathematics

Direct Proof: Modus Tollens

(premise 1)
(premise 2)
Material implication
(conjunction)
(distribution)
Disjunctive syllogism
Simplification

&lt;img&gt;Mathematical equations and diagrams including:
- Unweighted Edge
- Weighted Edge
- Undirected Graph
- Directed Graph
- Diagrams showing AND gates with labels AB, B+C, BC
- A diagram labeled "parts" and "non-parts" with logical expressions like p ∧ q ≥ p, p ∧ q ≥ q, q ≥ p → q, q ≥ q → p, p ∨ q ≥ p ∨ q, pq ∨ r ≥ p ∨ r, pq ∨ pr ≥ pq ∨ pr
- The traditional Chomsky hierarchy with languages and automata:
    - recursively-enumerable language
    - Turing machine
    - context-sensitive language
    - linear-bounded automaton
    - context-free language
    - push-down automaton
    -
    - regular finite-state automaton
&lt;/img&gt;

ISBN : 978-93-5568-943-6