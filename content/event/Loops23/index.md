---
title: A common divisor graph for skew braces

event: LOOPS'23
event_url: https://www.ilariacolazzo.info/gryb2023/

location: Będlewo, Poland
#address:
#  street: 450 Serra Mall
#  city: Stanford
#  region: CA
#  postcode: '94305'
#  country: United States

summary: LOOPS'23

abstract: 'In the combinatorial study of solutions to the Yang--Baxter equation (YBE), recently 
introduced rings-theoretical objects play a fundamental role: skew braces.
A skew brace is a set with two group operations 
$+$ and $\circ$ satisfying a compatibility condition.
In a skew brace $(A,+,\circ)$,
the group $(A,\circ)$ acts on $(A,+)$ by automorphism
via the so-called $\lambda$-map, $\lambda\colon (A,\circ)\to\Aut(A,+)$.
This action is involved in the (universal) construction of
the set-theoretic solutions to the YBE
provided by skew braces.
Furthermore, the $\lambda$-action deeply influences the structure of a finite skew brace,
as e.g. ideals are $\lambda$-invariant 
normal subgroups (for both group structures).
Motivated by similar ideas in representation theory
of finite groups (see \cite{MR2397031})
and by the work of 
of Bertram, Herzog, and Mann \cite{MR1099007}, 
we study a \emph{common divisor graph}:
% associated with a finite skew brace $A$:
the simple undirected graph whose vertices are the non-trivial $\lambda$-orbits 
and two vertices are adjacent if their sizes are not coprime. 
We provide some examples and prove
that it has at most two connected components
and that, in the connected case, its diameter
is at most four.
The main result is a complete classification of finite skew braces
with a one-vertex graph.
In particular, we have the following enumeration.
\begin{theorem}
    There are only three non-isomorphic finite skew braces
    with an abelian additive group and one-vertex graph.
\end{theorem}

\begin{thm}
    The number of non-isomorphic skew braces of size $2^md$ (with $d$ odd)
    whose graph has only one vertex is
    $ma(d)$ if $m\leq3$ and $2a(d)$ if $m\geq4$,
    where $a(d)$ is the number of isomorphism classes
    of abelian groups of order $d$.
\end{thm}

\begin{thebibliography}{37}

\bibitem{MR2397031} M.L. Lewis, \emph{An overview of graphs associated with character degrees and conjugacy class sizes in finite groups}, The Rocky Mountain Journal of Mathematics 38 (175-211), 2008.

\bibitem{MR1099007} E.A. Bertram, M. Herzog, Marcel, A. Mann, \emph{On a graph related to conjugacy classes of groups}, The Bulletin of the London Mathematical Society 6 (569-575), 1990.

\end{thebibliography}'

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2023-06-30'
#date_end: '2023-06-20'
all_day: true

# Schedule page publish date (NOT talk date).
#publishDate: '2017-01-01T00:00:00Z'

authors:
  - admin

tags: []

# Is this a featured talk? (true/false)
featured: false

image:
  caption: ''
  focal_point: Right

#links:
#  - icon: twitter
#    icon_pack: fab
#    name: Follow
#    url: https://twitter.com/georgecushen
url_event: 'https://www.impan.pl/en/activities/banach-center/conferences/23-loops'
#url_poster: 'gryb2023_poster.pdf'
url_slides: 'Slidesloops23.pdf'
#url_video: 'https://youtube.com'

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
#projects:
#  - example
---