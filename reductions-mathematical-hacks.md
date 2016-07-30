# Reductions are the Mathematical Equivalent of Hacks

2014-05-05

Though I don't remember who said it, I once heard a prominent CS researcher say
the following:

> Reductions are the lifeblood of theoretical computer science.

He was totally right. For those readers who don't know, a reduction is a
systematic way to transform instances of one problem into instances of another,
so that solutions to the latter translate back to solutions to the former.

Here's a simple example. Say you want to generate a zero or a one at random,
such you're equally likely to get either outcome. You can reduce this problem
to the problem of generating a zero or a one with some biased probability
(that's not *completely* biased).

In other words, you can simulate a fair coin with a biased coin. How do you do
it? You just flip your biased coin twice. If the outcome is "heads then tails,"
you call the outcome of the fair coin "heads." If the outcome is "tails then
heads" you call the outcome of the fair coin "tails." In any other event (TT or
HH), you try again. This works because if you know you flipped one heads and
one tails, then you're just as likely to get the heads first as you are to get
the tails first. If your coin is biased with probability p, these two events
both happen with probability p(1-p).

Even more fascinating is that you can go the other way too! Given a fair coin,
[you can simulate coins with any bias you
want!](http://jeremykun.com/2014/02/12/simulating-a-biased-coin-with-a-fair-coin/)
This is a quantifiable way to say, "biased coins and unbiased coins are
computationally equivalent." Theoretical computer science is just bursting with
these cool proofs, and they are the mathematical equivalent of a really neat
"hack."

Why do I call it a hack? The word is primarily used for bad but effective
solutions to programming problems (avoiding bugs without fixing their root
cause and such). But another use of the word is to successfully use a thing for
a purpose against or beyond its original intention. Like exploiting a buffer
overflow to get access to sensitive data or [using building lights to play
Tetris](http://hacks.mit.edu/Hacks/by_year/2012/tetris/), hacks have a certain
unexpectedness about them. And most of all hacks are slick.

Reductions come in many colors, the most common of which in computer science is
the *NP-hardness* reduction. This is a reduction from a specific kind of
problem (believed to be hard) to another problem while keeping the size
"small," by some measure. And the reason it's important is because if you show
a problem is NP-hard (has a reduction from a known NP-hard problem), then you
are including it in a class of problems that are believed to have no efficient
solution. So in this case a reduction is one way to measure the difficulty of a
problem you're studying.

One really fun example is that the rule-sets of [most classic Nintendo games
are NP-hard](http://arxiv.org/abs/1203.1895). That is, you can design a level
of Donkey Kong Country (or Super Mario Brothers, or Pokemon Red) so that
getting to the end of the level would require one to solve a certain kind of
logic problem. So if you could write a program to beat any Donkey Kong level
(or even tell if there is a way to beat it), you could solve these hard logic
problems. 

The key part of the reduction is that, given *any* such logic problem, you can
design a level that does this. That is, there is an algorithm that transforms
descriptions of these logic problems into Donkey Kong levels in an efficient
manner. The levels are quite boring, to be sure, but that's not the point. The
point is that Donkey Kong is being used to encode arbitrary logic, and that's a
sweet hack if I've ever see one.

If you enjoy the hacker mindset, and you want to get more into mathematics, you
should seriously try reading about this stuff. You have to wade through a
little bit of big-O notation and know that a Turing machine is roughly the same
thing as a computer, but the ideas you unlock are really fun to think about.
Here's an [article I wrote about P vs
NP](http://jeremykun.com/2012/02/23/p-vs-np-a-primer-and-a-proof-written-in-racket/),
actually implementing one of the famous reduction proofs in code.

Even better, once you understand a few basic NP-hardness reductions, you can
already start contributing to open research problems! For example, nobody knows
if the problem of factoring integers is NP-hard. So if you could find a way to
encode logic in a factoring problem the same way you can for a Donkey Kong
level, you'd be pretty famous. On the easier side, it just so happens that
potentially NP-hard problems show up a lot in research. Two of my current
research projects are about problems which I suspect to be NP-hard, but for
which I have no proof. And once you prove they're NP-hard then you can
start asking the obvious follow-ups: can I find good *approximate*
solutions? How much easier do I need to make the problem before it becomes
easy? The list goes on, giving more and more open questions and, the best
part, more opportunities for great hacks.
