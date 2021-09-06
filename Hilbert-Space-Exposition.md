---
abstract: |
    $\vspace{.1truein}$

    Hilbert spaces are vector spaces ubiquitous in many disciplines of
    mathematics and physics, and are of utility in a variety of areas,
    encompassing functional analysis, differential equations, Fourier
    analysis, and quantum mechanics. They provide a background for
    mathematical constructions defined on them. Hilbert spaces are often
    defined to be infinite-dimensional, though this is sometimes not the
    case.

    $\vspace{.1truein}$

    We will explore the properties intrinsic to Hilbert Spaces, some
    following from their definition as inner product spaces, and then study
    the properties of a special class of operators known as compact
    self-adjoint operators defined over a Hilbert Space and then we will
    move on to the Riesz Representation Theorem. We will connect the
    discussion of the Spectral Theorem and Riesz Representation Theorem to
    their respective quantum mechanical applications.

    $\vspace{.1truein}$
author:
- Pranav Vempati
date: |
     Department of Mathematics\
    University of California at Santa Cruz\
    Santa Cruz, CA 95064 USA\
    29 August 2021
title: Hilbert Spaces
---

\maketitle
Introduction {#introduction .unnumbered .unnumbered}
============

The familiar 3 dimensional Euclidean vector space, $\mathbb{R}^3$ is
sufficient for applications in 3 dimensions. However, mathematical and
physical theories may need more than 3 dimensions to work on, and early
forays into the nascent theory of functional analysis by the German
mathematician David Hilbert and the Hungarian mathematician Frigyes
Riesz around the turn of the 20th century necessitated an infinite
dimensional function space which was developed into the Hilbert Space
which is well known today.

$\vspace{.1truein}$

A Hilbert Space, roughly speaking, simply generalizes these familiar
properties of Euclidean space to any finite number, and even an infinite
number of dimensions. Physical theories and mathematical formulations
may then leverage this space to construct results that scale to an
arbitrary number of dimensions while leaving the central mathematical
thrust of the theory intact.

$\vspace{.1truein}$

A Hilbert Space is nothing more than an inner product space with an
additional property called completeness(which will be elaborated on
later).

$\vspace{.1truein}$

Definition and Properties
=========================

The below definition of a Hilbert Space reflects that of Kolmogorov and
Fomin(1961).

$\vspace{.1truein}$

\
$\vspace{.1truein}$

Equivalently, a Hilbert space can be defined as an inner product space
that is a complete normed space with respect to the metric induced by
its inner product.

$\vspace{.1truein}$

The criterion for completeness in this regard is the convergence of
every Cauchy sequence with points in the inner product space to a limit
that is in the same space. Note that in regards to the above definition,
Hilbert spaces can also be complex, i.e., they are defined over the
field of complex numbers, $\mathbb{C}$.

$\vspace{.1truein}$

**Example 1.1** Some notable examples of Hilbert spaces include
$\mathbb{C}$, the complex numbers, and $\mathbb{C}^N$.

$\vspace{.1truein}$

The function space $L^2(\mathbb{R})$, a vector space consisting of real
valued square integrable functions, is a Hilbert Space. In fact, it is
the sole $L^p$ space that is a Hilbert Space. $L^2(\mathbb{R})$ is
widely used in functional analysis owing to its property as a Hilbert
Space - the inner product on the Hilbert space $L^2(\mathbb{R})$ is
provided by $\langle f, g \rangle$ =
$\int_{-\infty}^{\infty} f(x) \overline g(x)dx$

$\vspace{.1truein}$

We now discuss some properties of Hilbert spaces, many of which are
inherited from the properties of inner product spaces. The parallelogram
law is satisfied by the norm introduced by the inner product in a
Hilbert Space. The important Cauchy-Schwarz inequality is now addressed.

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Theorem 1.1}(Cauchy-Schwarz Inequality)  \\
     For any two elements $x$ and $y$ of a Hilbert Space $H$, $| \langle x, y \rangle | \leq  \left\|x \right\| \left\|y \right\| $ with equality if and only if $x$ and $y$ are linearly dependent. 
     
\end{minipage}}
\hspace{0.1cm}
(Debnath and Mikusinski, *Introduction to Hilbert Spaces with
Applications*)

$\vspace{.1truein}$

As is known from study of inner product spaces, the triangle inequality
can be proven when assuming the Cauchy-Schwarz inequality on an inner
product space.

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Corollary 1.1}(Triangle Inequality)  \\
     For any $x \in H$, $y \in H$, 
     $\left\| x + y \right\|  \leq \left\|x \right\| + \left\|y \right\| $. This follows from the Cauchy-Schwarz inequality. 
     
\end{minipage}}
\hspace{0.1cm}
(Debnath and Mikusinski, *Introduction to Hilbert Spaces with
Applications*)

$\vspace{.1truein}$

*Proof*

Note that $\left\| x + y  \right\|^2$ =
$\left\| x \right\|^2  + 2\langle x, y \rangle + \left\| y \right\|^2$

by the Cauchy-Schwarz inequality, it follows that

$\left\| x + y  \right\|^2 \leq \left\| x \right\|^2  + 2 \left\|x \right\| \left\| y \right\| +  \left\| y \right\|^2$,

so,
$\left\| x + y  \right\|^2  \leq (\left\|x \right\|^2 + \left\|y \right\|)^2$

$\vspace{.1truein}$

The Pythagorean formula, stated for any two orthogonal vectors in an
inner product space, can be generalized to arbitrary finite dimension in
a Hilbert Space.

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Theorem 1.2}(Pythagorean Formula on Hilbert Spaces)  \\
       If {$x_{1} \ldots x_{n}$} is a set of orthogonal vectors in a Hilbert space, $H$, 
      $\left\|  \sum_{i=1}^{N} x_{i} \right\|^2$ = $\sum_{i=1}^{N} \left\| x_{i} \right\|^2$
        
\end{minipage}}
\hspace{0.1cm}
(Debnath and Mikusinski, *Introduction to Hilbert Spaces with
Applications*)

$\vspace{.1truein}$

An analogue of the Pythagorean Formula on infinite dimensional Hilbert
spaces is Parseval's Formula.

We will introduce the notion of a *seprable* Hilbert space. First, we
must describe a *complete orthonormal sequence*

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Definition 1.2}(Complete Orthonormal Sequence)  \\
      An complete orthonormal sequence on a Hilbert space $H$ is an orthonormal sequence such that for every $x \in H$, we have: 
      
      $\vspace{.1truein}$ 
      
      $x$ = $\sum_{i=1}^{\infty} \langle x, x_{i} \rangle x_{i}$.
      
\end{minipage}}
$\vspace{.1truein}$

\hspace{0.1cm}
(Debnath and Mikusinski, *Introduction to Hilbert Spaces with
Applications*)

$\vspace{.1truein}$

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Definition 1.3}(Separable Hilbert space)  \\
     A Hilbert space is called \textit{separable} if it contains a complete orthonormal sequence. Finite dimensional Hilbert spaces are considered separable.  
     
\end{minipage}}
\hspace{0.1cm}
(Debnath and Mikusinski, *Introduction to Hilbert Spaces with
Applications*)

$\vspace{.1truein}$

**Example 1.2**

$\vspace{.1truein}$

An example of a separable Hilbert space is $L^2[-\pi, \pi]$, the
function space of square integrable functions on -$\pi$ to $\pi$.
Another separable Hilbert space is $l^2$, the space of square summable
sequences.

$\vspace{.1truein}$

To see the utility of separable Hilbert spaces, consider the following
theorem

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Theorem 1.3}(Hilbert Space Isomorphism)  \\
      If $H$ is an infinite dimensional separable Hilbert Space, it is isomorphic to $l^2$. 
\end{minipage}}
\hspace{0.1cm}
(Debnath and Mikusinski, *Introduction to Hilbert Spaces with
Applications*)

$\vspace{.1truein}$

An isomorphism of Hillbert spaces is an equivalence relation over these
spaces.

$\vspace{.1truein}$

In view of the fact that complex infinite dimensional separable Hilbert
spaces are all isomorphic to $l^2$ and real infinite dimensional Hilbert
spaces are isomorphic to the real sequence space $l^2$, a remarkable
result follows - all complex infinite dimensional separable Hilbert
spaces can be regarded as the same space, and a result to the same
effect is true for all real infinite dimensional separable Hilbert
spaces.

$\vspace{.1truein}$

These intrinsic properties of Hilbert spaces, among others, lend
themselves to defining structures on them that in turn are amenable to
application in a physical context. These mathematical properties will
lead to the Spectral Theorem and the Riesz Representation Theorem, which
can be expressed as useful results formulated on Hilbert Spaces.

$\vspace{.1truein}$

The Spectral Theorem
====================

We will now see an application of Hilbert Spaces as a background for the
theory of self-adjoint operators defined on them, and study the
relationships between these self-adjoint operators and their underlying
Hilbert Space. To do so, we must formally introduce a few concepts in
order to build up to the Spectral Theorem.

$\vspace{.1truein}$

The following theorems, propositions, proofs, and definitions are
from(or derived from) Debnath and Mikusinski's *An Introduction to
Hilbert Spaces with Applications*. In the interest of brevity, inline
citations are omitted, however their existence is implied by the
preceding acknowledgement, unless an inline citation referencing another
source is present.

$\vspace{.1truein}$

We begin by introducing the notion of operators, bounded sequences,
bounded operators, and compact operators. $\vspace{.2truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Definition 2.1}(Bounded sequence)  \\
    Given a sequence ${a_n}$: \\
    
    If there exists a number $m$ such that $m \leq a_{n}$ for every $n$ the sequence is \textbf{bounded from below}. \\
    
    If there exists a number $M$  such that $a_{n} \leq M$ for every $n$ the sequence is \textbf{bounded from above}. \\

    A \textbf{bounded sequence} is a sequence bounded from below and above.  \\
 
    \end{minipage}}
(Dawkins)

$\vspace{.2truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Definition 2.2}(Bounded operator)  \\
     An operator $A$ is \textit{bounded} if there is a number $K$ such that $\left\| Ax \right\|$ $\leq$ $K\left\| x \right\|$
     for every $x$ in the domain of $A$. 
    \end{minipage}}
$\vspace{.1truein}$

With the definition of a bounded sequence at hand, we are ready to
define a *compact operator* on a Hilbert Space.

$\vspace{.1truein}$

$\vspace{.2truein}$

$\vspace{.1truein}$

**Example 2.1**

$\vspace{.1truein}$

An example of a compact operator is an integral operator on $L^2[a,b]$,
with a, b finite and $K$ continuous,

$\vspace{.1truein}$

$(Tx)(s)$ = $\int_{a}^{b} K(s,t)x(t) dt$

$\vspace{.1truein}$

The notions of *bounded* and *compact* operators can be related.
Specifically, the former is a superset of the latter.

$\vspace{.1truein}$

$\vspace{.2truein}$

*Proof* $\vspace{.1truein}$

We prove only the first statement in Proposition 2.1, namely that every
compact operator is bounded, and proceed by proof by contraposition. If
an operator $A$ is not bounded, then there exists a sequence ($x_{n}$)
such that $\left\| x \right\|$ = 1, for all $n \in \mathbb{N}$, and
$\left\| Ax_{n} \right\|$ $\rightarrow \infty$. The fact
$\left\| Ax_{n} \right\|$ $\rightarrow \infty$ implies $Ax_{n}$ does not
contain a convergent subsequence, so by definition $A$ is not a compact
operator either. As we have proved that not bounded implies not compact,
the contrapositive, the original proposition has been proved.

$\vspace{.1truein}$

Equipped with the definition of a bounded operator, the adjoint of an
operator can now be formalized.\

$\vspace{.1truein}$

Boundedness of the operator $A$ implies the following for the adjoint

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Theorem 2.1}  
     The adjoint, $A^*$, of a bounded operator $A$ is bounded. 
     
    \end{minipage}}
$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Definition 2.5}(Self-Adjoint operator)  \\
      If $A$ = $A^*$, $A$ is referred to as a self-adjoint operator. 
    \end{minipage}}
$\vspace{.1truein}$

Self-adjoint operators over a finite-dimensional complex vector space
and with respect to a certain basis can be represented as a Hermitian
matrix, that is, a matrix equal to its own conjugate transpose.

$\vspace{.1truein}$

A special class of self-adjoint operators on Hilbert Spaces have special
properties given by the Spectral Theorem. Furthermore, we require the
operators to be compact, that is, in an informal sense, to map between
finite subsets of one vector space to relatively compact subsets of
another vector space.

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Theorem 2.2}(Spectral Theorem for compact self-adjoint operators)  \\
        Let $A$ be a compact, self-adjoint operator on an infinite-dimensional Hilbert Space $H$. Then $H$ has a complete orthonormal basis consisting of the eigenvectors of $A$. Additionally, for every $x \in H$, we have: \\
        $Ax$ = $\sum^{\infty}_{n = 1} $ $\lambda_{n}\langle x, v_{n} \rangle v_{n}$, \\
        where $Av_{n}$ = $\lambda_{n}v_{n}$, that is, $v_n$ is an eigenvector of $A$ with eigenvalue $\lambda_{n}$. 
    \end{minipage}}
$\vspace{.1truein}$

Note that this extends a known result from linear algebra to infinite
dimensions, enabled by the underlying infinite dimensional Hilbert
space.

$\vspace{.1truein}$

We can further extend this result to a corollary with regards to
projections. Recall that a projection $P$ is an idempotent, such that
$P^2 = P$.

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Corollary 2.1}  
       If $A$ is a compact, self-adjoint operator over a Hilbert Space $H$, then \\ 
       $A$ = $\sum^{\infty}_{n = 1} \lambda_{n} P_{n}$
    \end{minipage}}
$\vspace{.1truein}$

*Proof*

Take ${v1, v2, v3, ...}$ as our orthonormal basis of eigenvectors with
respective eigenvalues $\lambda_{1}, \lambda_{2}, \lambda_{3}, ...$ .
$P_{n}$ is the projection operator onto the one dimensional subspace
spanned by $v_{n}$. Note that as $P_{n}x$ =
$\langle x, v_{n} \rangle v_{n}$. In light of this observation, the
equation associated with the Spectral Theorem(Theorem 2.2) can be
written as $Ax$ = $\sum^{\infty}_{n = 1} \lambda_{n} P_{n} x$.

$\vspace{.2truein}$

This is a powerful result, implying that an operator so constructed over
a Hilbert space can be diagonalized.

$\vspace{.2truein}$

The utility of self-adjoint operators in quantum mechanics lies in the
fact that observables such as position and momentum can be defined as
self-adjoint operators over a Hilbert Space. The eigenvalues of a
self-adjoint operator over a Hilbert space are real, and eigenvectors
associated with distinct eigenvalues are orthogonal, thus enabling
interpretable results for a measurement made on an observable.
Additionally, mixed states in quantum mechanics can be represented as
self-adjoint operators over a Hilbert Space, and by the spectral theorem
discussed earlier, can be diagonialized. This directly implies that any
mixed state can be written as a finite combination of orthogonal pure
states, a major result in quantum theory. These properties motivate
physicists to formulate quantum mechanical observables as self-adjoint
operators over a complex Hilbert space.

$\vspace{.2truein}$

The Riesz Representation Theorem and Bra-Ket Notation
=====================================================

$\vspace{.1truein}$

The Riesz representation theorem, developed by the Hungarian
mathematician Frigyes Riesz(1880-1956) relates a real or complex Hilbert
space to its continuous dual, and we will primarily discuss the complex
Hilbert space.

$\vspace{.1truein}$

The Riesz representation theorem is fundamental to quantum mechanics as
it forms the rigorous mathematical foundation for Paul Dirac's bra-ket
notation, in widespread use in the field.

$\vspace{.1truein}$

The Riesz representation theorem states that in an inner product space,
linear functionals can be regarded as inner products. Recall the notion
of an inner product space in multiple dimensions that is complete with
respect to the metric induced by the norm coincides with that of a
Hilbert Space.

$\vspace{.1truein}$

\fbox{\begin{minipage}{40em}
    \textbf{Theorem 3.1}(Riesz Representation Theorem)  \\
   
    On an inner product space $(V, \langle . , . \rangle)$, any linear functional $\phi:   V -> $F has the form $(\phi, x)$ = $\langle z, x \rangle$ for a unique $z$ = $z_{\phi}$ $\in$ $V$. 
    
\end{minipage}}
$\vspace{.1truein}$

(Costin)

$\vspace{.1truein}$

The Riesz Representation theorem induces an isometric isomorphism to the
dual space if the underlying field is the real numbers, and the
isomorphism is antilinear if the underlying field is the complex
numbers. Equipped with the theorem, we can provide a construction for
the dual space of a complex Hilbert space, $H^*$.\
$\forall h \in H$, define $\mu_{h}$: $H \rightarrow \mathbb{C}$ by

$\vspace{.1truein}$

$\mu_{h}(f)$ = $\langle f, h \rangle$, $f \in H$. We have the following
properties on the dual space:\
1) $\mu_{h}$ $\in H^*$ for each h $\in$ H, and further, we have norm
preservation, namely the fact that $\left\| u_{h} \right\|$ =
$\left\| h \right\|$ $\vspace{.1truein}$

2\) For every $\mu \in H^*$, there exists a unique $h \in H$ such that
$\mu = \mu_{h}$.

$\vspace{.1truein}$

3\) If $L$: $H \rightarrow H^*$, given by $L(h)$ = $\mu_{h}$, $L$ is an
antilinear isometric bijection between $H$ and $H^*$. This is a property
unique to complex Hilbert spaces.

$\vspace{.1truein}$

$\mu_{\alpha g + \beta h}$ = $\bar \alpha \mu_{g} + \bar \beta \mu_{h}$,
where we have complex conjugation on $\alpha$ and $\beta$. (Heil)

$\vspace{.2truein}$

In quantum mechanics, the space of states is represented by column or
*ket* vectors on a complex Hilbert Space, denoted as $| v \rangle$ while
the linear functionals are represented by bras, denoted as
$\langle  f |$. A ket vector is sometimes referred to in quantum
mechanical parlance as a *wavefunction*. A wavefunction in quantum
mechanics has the interpretation that its squared absolute value yields
a real number quantifying the probability of that particle being in a
particular place at a particular time.

$\vspace{.2truein}$

The bra-ket notation, introduced by Paul Dirac, provides a concise means
of expressing quantum mechanical calculations on these row and column
vector analogues. The notation is given a firm mathematical footing by
identification with the Riesz Representation Theorem. The linear
functionals(bras) pairing with the ket vectors from the underlying
Hilbert Space gives the interpretation of an inner product on this
space, and this pairing is justified by the Riesz Representation Theorem
- hence, we have: $\langle f | v \rangle$ $\in \mathbb{C}$, with the
resultant element produced by this inner product lying in the field of
complex numbers the underlying Hilbert space is defined over,
$\mathbb{C}$. The Riesz Representation theorem also yields the
interpretation of the linear functional, namely the bra, \"acting\" on
the ket to yield an element of the underlying field. Note that the
object of the following discussion on bra-ket notation is expository in
that it is an introduction to the notation and some of its basic
properties, yet is not meant to be an exhaustive overview of the
subject, which would lie beyond the scope of this paper on Hilbert
Spaces.

$\vspace{.1truein}$

The properties of bras and ket vectors follow from those of linear
functionals and vectors, respectively. We will explore each separately,
then discuss the properties of the inner product when bringing a bra and
ket together. For brevity, I will preface the following by noting that
this exposition follows that of Robert Littlejohn's Physics 221A(UC
Berkeley) Notes.

$\vspace{.1truein}$

**Properties of kets**:

$\vspace{.1truein}$

Let $\mathcal{E}$ denote a complex vector space, finite or infinite
dimensional, associated with some physical system, which we will later
see becomes a complex Hilbert Space when a suitable inner product is
defined on it.

Note that a ket commutes under multiplication with an element of the
field of complex numbers, $\mathbb{C}$:

$\vspace{.2truein}$

$\hspace{.2truein}$ $c | \psi \rangle$ = $| \psi \rangle c$.

$\vspace{.2truein}$

**Properties of bras**:

$\vspace{.1truein}$

If the kets can be regarded as wavefunctions of the form $\psi(x)$, the
bras correspond to the complex conjugate of these wavefunctions,
$\psi^*(x)$.

To obtain the perspective more frequently employed by quantum
physicists, however, we can invoke the Riesz representation theorem and
regard the bra as a linear functional, an element of the dual space and
naturally dual to ket vector, and hence an element of the space
$\mathcal{E}^*$. This gives rise to the intuitive understanding of bras
as dual to kets, i.e. bras can be understood as row vectors and kets as
column vectors. Hence, a bra is defined as

$\vspace{.1truein}$

$\hspace{.1truein}$ $\langle \alpha |: V \rightarrow C$

$\vspace{.1truein}$

sending a ket vector from the underlying Hilbert Space to a complex
number. The mapping implied by a bra is constrained to be linear. That
is, the mapping is of the form:

$\vspace{.1truein}$

$\hspace{.1truein}$
$\langle \alpha | (c_{1} | \psi_{1} \rangle + c_{2} | \psi_{1} \rangle )$
=
$c_{1} \langle \alpha | (| \psi_{1} \rangle) + c_{2} \langle \alpha | (| \psi_{2} \rangle)$

$\vspace{.1truein}$

Let us confirm that the mapping provided by a bra satisfies the
properties of a homomorphism:

$\vspace{.1truein}$

$\hspace{.1truein}$ Given $c \in \mathbb{C}$,
$(c \langle \alpha |)(| \phi \rangle )$ =
$c\langle \alpha| (| \phi \rangle)$

$\vspace{.1truein}$

and,

$\vspace{.1truein}$

$\hspace{.1truein}$ $(\langle a_{1} | +  \langle a_{2} |)$
($| \psi \rangle$) = $\langle a_{1} | ( | \psi \rangle)$ +
$\langle a_{2} | ( | \psi \rangle)$

$\vspace{.1truein}$

We have confirmed, by a procedure similar to Definition 3.6 on the
lecture notes, that the dual space of the Hilbert Space underlying the
bra-ket formulation of quantum mechanics is $Hom(V,\mathbb{C})$

$\vspace{.1truein}$

By the fact that a finite dimensional vector space has the same
dimension as its dual, we know that $dim(V)$ = $dim(V*)$.

$\vspace{.1truein}$

On a slightly tangential note, the outer product between two kets,
$| \psi \rangle$ and $| \phi \rangle$ can be defined by
$| \psi \rangle \langle \phi |$.

$\vspace{.1truein}$

Equipped with the above detailed discussion of bras and kets, we are now
ready to discuss the inner product on $V$ induced by a pairing of a ket
vector with the corresponding bra from the dual space.

$\vspace{.1truein}$

Assume there exists on $\mathcal{E}$ a scalar(inner) product
$g: \mathcal{E} \times  \mathcal{E} \rightarrow \mathbb{C}$. $g$ can be
regarded as a function that consumes two ket vectors and produces a
complex number, i.e.

$\vspace{.1truein}$

$\hspace{4cm}$ $g(|\psi \rangle, |\phi \rangle)$ $\in \mathbb{C}$

$\vspace{.1truein}$

We follow the physics convention in that we take the mapping provided by
$g$ to be linear in its second operand and antilinear in the first, that
is -

$\hspace{1cm}$
$g(| \psi \rangle, c_{1} | \phi_{1} \rangle + c_{2} | \phi_{2} \rangle )$
= $c_{1} g(| \psi \rangle, | \phi_{1} \rangle)$ +
$c_{2} g(| \psi \rangle, | \phi_{2} \rangle)$

$\vspace{.1truein}$

$\hspace{1cm} g c_{1} | \psi_{1} \rangle + c_{2} | \psi_{2} \rangle, | \phi \rangle)$
= $c_{1}^* g(| \psi_{1} \rangle, | \phi \rangle)$ +
$c_{2}^* g(| \psi_{2} \rangle, | \phi \rangle)$

$\vspace{.1truein}$

where $\psi$ and $\phi$ reprise their role as ket vectors. As it is
constructed on the field of complex complex numbers, $g$ is symmetric,
or more precisely in this context, a *Hermitian* map. Therefore,

$\vspace{.1truein}$

$\hspace{4cm}$ $g(| \psi \rangle,  | \phi \rangle)$ =
$g(| \phi \rangle,  | \psi \rangle)^*$

$\vspace{.1truein}$

$g$ is a positive-definite map. Explicitly, $\forall | \phi \rangle$,
$| \phi \rangle$ being a ket, the mapping $g$ is characterized by

$\vspace{.1truein}$

$\hspace{4cm}  g(| \phi \rangle , | \phi \rangle) \geq 0$

$\vspace{.1truein}$

With this mapping only equalling zero when the ket $| \phi \rangle$ is
zero.

Given the inner product, we can define a *dual correspondence*, here
denoted as CR, from $\mathcal{E} \rightarrow \mathcal{E}^*$. This dual
correspondence, CR, converts ket vectors to bras , which in a physical
context can be equivalently viewed as taking the complex conjugate of
the wavefunction encoded by the ket vector.

The dual correspondence takes a ket to a bra, that is:

$\vspace{.1truein}$

$\hspace{4cm}$ CR: $| \psi \rangle \rightarrow \langle \psi |$

$\vspace{.1truein}$

The dual correspondence, CR, can be regarded as the operation of
Hermitian conjugation. Explicitly, we have that:

$\vspace{.1truein}$

$\hspace{4cm}$ $\langle \psi |$ = $(| \psi \rangle)^\dagger$

$\vspace{.1truein}$

Provided $\mathcal{E}$ is finite dimensonal, the mapping induced by the
dual correspondence, CR, is bijective. That is, $\vspace{.1truein}$

$\hspace{4cm}$ $\langle \psi |$ $\in \mathcal{E}^*$, $\exists$
$| \phi \rangle$ $\in$ $\mathcal{E}$ s.t. $\langle \psi |$ =
$(| \phi \rangle)^\dagger$

$\vspace{.1truein}$

This concludes our discussion of some of the fundamentals of the bra-ket
notation and its relation to Hilbert spaces and their duals.

Conclusion
==========

$\vspace{.1truein}$

Hilbert spaces are both intriguing mathematical objects in their own
right and of tremendous utility to fields ranging from engineering to
physics. We have explored the basic properties of Hilbert Spaces, some
courtesy of their being inner product spaces, and noted the
benefits(especially in regards to simplicity of classification of
spaces) separability confers on infinite dimensional Hilbert spaces. We
also reviewed the properties of self-adjoint operators on Hilbert spaces
and the powerful result of the Spectral Theorem for compact self-adjoint
operators.

$\vspace{.1truein}$

An overview of the Riesz representation theorem and the construction of
the dual space was presented and it was related to the justification for
the bra-ket notation. Finally, we reviewed some of the fundamentals of
bra-ket notation, which, in turn, elucidated the nature of and
operations on Hilbert spaces and their duals in a physical context.

$\vspace{.1truein}$

Their formulation in the late 19th century by Hilbert allowed quantum
mechanics to develop on the rich mathematical framework afforded by
Hilbert spaces in the 1920s. As we have shown, the bra-ket notation is
no mere expediency, and is justified by Frigyes Riesz's formulation of
the Riesz Representation theorem. A historical anecdote relates that
even David Hilbert himself was surprised that the Hilbert space and the
theory built on it found such fundamental applications in quantum and
atomic physics.

$\vspace{.1truein}$

Hilbert Spaces have found use outside of pure mathematics and
mathematical physics. The computer scientist Risi Kondor in 2003 at
Columbia University formulated a theory of Hilbert space methods in
machine learning. The theoretical result justifying the optimality of
the ReLU activation function in deep neural networks is rooted in an
important statistical result known as the representer theorem, which in
turn leverages the structure of Reproducing Kernel Hilbert Spaces.

$\vspace{.1truein}$

\pagebreak
\bib{kolmogorov}{book}{
  title={Elements of the Theory of Functions and Functional Analysis},
  author={Andrey Kolmogorov and Sergei Fomin},
  date={1961}
}
\bib{hilbert}{book}{
  title={An Introduction to Hilbert Spaces with Applications},
  author={Lokenath Debnath and Piotr Mikusinski },
  date={2005}
}
\bib{web}{webpage}{
  title={The Riesz Representation Theorem},
  author={Rodica Costin},
  url={https://people.math.osu.edu/costin.10/5101/Orthog20p10-11.pdf},
}
\bib{lamar}{webpage}{
  title={More on Sequences},
  author={Paul Dawkins},
  url={https://tutorial.math.lamar.edu/classes/calcii/moresequences.asp}
}
\bib{gtech}{webpage}{
  title={The Dual of a Hilbert Space},
  author={Christopher Heil},
  url={https://people.math.gatech.edu/~heil/6338/summer08/section5a.pdf}
}
\bib{spectral}{webpage}{
  title={The importance of being Spectral},
  author={Alessandro Bisio},
  url={"https://quantum-journal.org/views/qv-2019-07-09-15/}
}
\bib{berkeley}{webpage}{
  title={The Mathematical Formalism of Quantum Mechanics},
  author={Robert Littlejohn},
  url={http://bohr.physics.berkeley.edu/classes/221/0708/notes/hilbert.pdf}
}
\bib{ML}{webpage}{
  title={A Short Introduction to Hilbert Space Methods in Machine Learning},
  author={Risi Kondor},
  url={http://www.cs.columbia.edu/~risi/notes/tutorial6772.pdf}
}
