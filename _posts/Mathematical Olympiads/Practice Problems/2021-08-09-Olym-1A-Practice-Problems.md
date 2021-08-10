---
layout: article
title: Olym 1A | Olymplex
date: 2021-08-16 12:00:00 -0400
mathjax: true
permalink: /mathematical-olympiads/algebra/olym-1a/practice-problems/
---
<h1>Olym 1A. Equations and Formulae <br> <ssup> - Practice Problems </ssup></h1>
<p><a href="https://ramaniumx.github.io/phantom-jekyll-theme/">Olymplex</a> > <a href="https://ramaniumx.github.io/phantom-jekyll-theme/mathematical-olympiads/">Mathematical Olympiads</a> > <a href="https://ramaniumx.github.io/phantom-jekyll-theme/mathematical-olympiads/algebra/">Algebra</a> > <a href="https://ramaniumx.github.io/phantom-jekyll-theme/mathematical-olympiads/algebra/olym-1a/">Olym 1A</a> > <a href="https://ramaniumx.github.io/phantom-jekyll-theme/mathematical-olympiads/algebra/olym-1a/practice-problems/">Practice Problems</a><p>
The 62nd International Mathematical Olympiad (namely the IMO) was held remotely on July 21-22, 2021. As a former IMO participant, I thought it would be fun (and somehow educational) to have former Korean IMO participants attempting this year's IMO problems and livestream it, and we did that at Twitch (unfortunately we didn't record it, but you can look at some clips!).<br>
Our livestreaming team consisted of six people who participated in one (or two) of IMO 2018, 2019, and 2020. Here, I am going to share the solutions that we came up with, along with some additional notes on each problem.<br>
<h2>Problem 1. Easy cards </h2>
<bluebox>Let $n \geqslant 100$ be an integer. Ivan writes the numbers $n, n+1, \ldots, 2n$ each on different cards. He then shuffles these $n+1$ cards, and divides them into two piles. Prove that at least one of the piles contains two cards such that the sum of their numbers is a perfect square. </bluebox>
<b>Solution. </b> 
It suffices to prove that there are three integers $n \le a<b<c \le 2n$ such that $a+b, b+c, c+a$ are perfect squares.<br>
To accomplish this, we will set $a = 2i^2 - 4i, b= 2i^2+1, c= 2i^2+4i$ for some integer $i$. Then it follows that $a+b = (2i-1)^2, a+c=(2i)^2, b+c=(2i+1)^2,$ so we only need<br>
$$2i^2-4i \ge n ,2i^2+4i \le 2n \iff (i-1)^2 \ge \frac{n}{2}+1 , (i+1)^2 \le n+1$$<br>
for some integer $i$. This is equivalent to $\lfloor \sqrt{n+1} \rfloor - \lceil \sqrt{\frac{n}{2}+1} \rceil \ge 2$, which can be verified easily.<br>
<h2>Problem 2. New n-var ineq</h2><br>
<bluebox>Show that the inequality<br>
$$\sum\_{i=1}^{n} \sum\_{j=1}^{n} \sqrt{ \lvert x_i - x_j \rvert} \le \sum\_{i=1}^{n} \sum\_{j=1}^{n} \sqrt{\lvert x_i + x_j \rvert}$$
holds for all reals $x_1, x_2, \cdots, x_n.$ </bluebox>

<b>Solution. </b> We will prove the problem with strong induction on $n$. The base cases in which $n \le 2$ are trivial.<br>
<greenbox><i>Lemma. </i> For any real $x \neq 0$ and $0 < \epsilon < 2\|x\|,$ we have <br>
$$ \sqrt{\lvert x-\epsilon/2 \rvert}+\sqrt{\lvert x+\epsilon/2 \rvert} < 2\sqrt{\lvert x \rvert}. $$</greenbox> <br>
<i>Proof. </i> This directly follows from Jensen as both $\sqrt{x}$ and $\sqrt{-x}$ are concave on their domains. $\square$<br>
Note that the left-hand side remains constant under translation of the variables ($x_j \leftarrow x_j + \frac{C}{2}$), so it is sufficient to consider the case where the right-hand side is minimized under translation.<br>
Accordingly, let $f(C):= \sum_{i, j} \sqrt{|x_i + x_j + C|}.$ Then $f(C)$ is continuous on $\mathbb{R}$ and bounded below; thus $f$ attains a minimum. <br>
Let $f(C)$ be that minimum, and suppose $x_i+x_j+C \neq 0$ for every indices $1 \le i, j \le n.$ <br>
By the lemma, for all sufficiently small $\epsilon$ we have<br>
$$ \sum\_{i, j} \sqrt{\lvert x_i + x_j + C + \epsilon \rvert} + \sum\_{i, j} \sqrt{\lvert x_i + x_j + C - \epsilon \rvert} < \sum\_{i, j} 2\sqrt{\lvert x_i+x_j+C \rvert}, $$<br>
so $\min \\{f(C-\epsilon), f(C+\epsilon)\\} < f(C).$ This contradicts the minimality of $f(C).$ Hence there are indices $i, j$ such that $x_i+x_j+C=0.$<br>
Now by the translation $x_j \leftarrow x_j + \frac{C}{2}$ we have $x_i+x_j=0$ for some $i, j.$ WLOG assume $i=j=n$ or $i=n-1, j=n,$ then the inequality reduces to the following two inequalities, which holds by the induction hypothesis.<br>
$$ \sum\_{i=1}^{n-1} \sum\_{j=1}^{n-1} \sqrt{ \lvert x_i - x_j \rvert} \le \sum\_{i=1}^{n-1} \sum\_{j=1}^{n-1} \sqrt{\lvert x_i + x_j \rvert} $$<br>
$$ \sum\_{i=1}^{n-2} \sum\_{j=1}^{n-2} \sqrt{ \lvert x_i - x_j \rvert} \le \sum\_{i=1}^{n-2} \sum\_{j=1}^{n-2} \sqrt{\lvert x_i + x_j \rvert} $$<br>
Note that equality holds iff the $x_i$s are symmetric with respect to the origin, i.e. the multiset $\\{x_1, x_2, \cdots, x_n \\}$ can be partitioned into groups of size at most two so that each group has sum $0.$<br>
## Problem 3. Classical Triangle Geo<br>
<bluebox>Let $D$ be an interior point of the acute triangle $ABC$ with $AB > AC$ so that $\angle DAB = \angle CAD.$ The point $E$ on the segment $AC$ satisfies $\angle ADE =\angle BCD,$ the point $F$ on the segment $AB$ satisfies $\angle FDA =\angle DBC,$ and the point $X$ on the line $AC$ satisfies $BX = CX.$ Let $O_1$ and $O_2$ be the circumcenters of the triangles $ADC$ and $EXD,$ respectively. Prove that the lines $BC, EF,$ and $O_1O_2$ are concurrent. </bluebox><br>
<b>Solution. </b><br>
<i>Step 1. </i> Let $D'$ denote the isogonal conjugate of $D$ with respect to $\triangle ABC.$ Then the given angle condition implies<br>
$$ \angle FDB' = \angle DBC = \angle FDD', $$<br>
so $(BFDD'),(DD'CE)$ are cyclic. Hence by PoP,<br>
$$ AF\times AB= AD\times AD'= AE\times AC, $$<br>
we obtain that $(BCEF)$ is also cyclic.<br>
Now we recall a well-known lemma used in several IMO/ISLs:<br>
<greenbox><i>Lemma.</i> Let $ABCD$ be a quadrilateral and $X$ be a point in its interior so that $\angle AXB+\angle CXD = \pi$. Then $X$ has an isogonal conjugate with respect to $ABCD$.</greenbox><br>
<i>Step 2.</i> By the above lemma, it follows that $D$ and $D'$ are isogonal conjugates with respect to $\square BCEF$. Hence<br>
$$ \angle BDF = \angle BD'F = \pi - \angle CD'E = \angle D'EC + \angle D'CD = \angle DEF + \angle DBC, $$<br>
which implies that $\odot(DEF)$ and $\odot(DBC)$ are tangent to each other. By the radical axis theorem on $\odot(AEF), \odot(DEF), \odot(DBC)$, the point $T := BC \cap EF$ satisfies $TD^2 = TB \times TC$.<br>
<i>Step 3.</i> Let $P$ be the intersection of $\odot(AEF)$ and $\odot(ABC)$. Then $\triangle PBC \sim \triangle PFE$ by the Miquel point property, and<br>
$$ \angle PBX=\angle XBC -\angle PBC=\angle ACB -\angle PFE = \angle AFE- \angle PFE =\angle AFP =\angle XEP. $$<br>
Hence $(XPEB)$ are cyclic.<br>
<i>Step 4.</i> Let $PB$ and $AC$ intersect at $I$ and let $\odot(XDE)$ and $\odot(ADC)$ meet again at $G$. Then by PoP<br>
$$ XI\times IE=PI\times IB =AI\times IC, $$<br>
so $I$ lies on the radical axis of $\odot(XDE)$ and $\odot(ADC)$ which is $DG.$ Hence by PoP again, we have<br>
$$ BI\times IP=AI\times IC =DI\times IG $$<br>
so $(BDPG)$ are cyclic.<br>
<i>Step 5.</i>
To finish, consider the inversion centered at $T$ with radius $TD$. By _Step 2_ we have $TD^2 =TB\times TC=TP\times TA$, and thus $G = \odot(ADC) \cap \odot(BDP)$ is fixed under this inversion (as the two circles swap to each other). Hence $TG=TD$, and $T$ lies on the perpendicular bisector of $DG$, which is $O_1 O_2.$ This concludes the proof.<br>
