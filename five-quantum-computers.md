# The world will never need more than five quantum computers

2014-06-24

I have been gradually making my way through Scott Aaronson's wonderful book,
"Quantum Computing Since Democritus." The book is chock-full of deep insights
phrased in just-technical-enough language (the kind which I want to relay to
the world through an [internet
megaphone](http://jeremykun.com/2014/06/12/three-years-old-and-an-idea-for-a-podcast/)).
Scott really has learned how to apply the good and bad attitudes of the past to
the problems of today. 

For example, did you know that originally computers had so many problems with
errors that many people argued fault-tolerant computers would never exist? This
was before the transistor, of course, but it was believed that the external
world would always have such an adverse interference with the physical machine
that one could not reliably use the outputs. John von Neumann proved to the
contrary that even with the error-prone hardware of the time it was possible to
design perfect fault-tolerance into a machine. But his accomplishment was
largely forgotten after the transistor was invented and shown to be so reliable
as not to need any extra error-correction scaffolding. 

But the idea that computers would never be error-tolerant enough was probably
the origin of the famous slew of quotes that [the world would never need more
than five
computers](http://en.wikipedia.org/wiki/Thomas_J._Watson#Famous_misquote). It's
not so ridiculous a proposition in that context, since the world also only has
need for around five particle accelerators. Scott notices the parallel for
quantum computers, the worry that the outside world would interfere with the
computations so as to render them useless, and discusses the existence of
quantum fault-tolerance in the same vein as von Neumann's theorem.

Nevertheless, the question of whether the world will ever need more than five
quantum computers (assuming they're feasible to scale) is still a poignant one.
It's not because of error, but because of what kinds of problems quantum
computers are believed to be better at than classical computers. 

You see, it's widely known that quantum computers *aren't* more powerful than
classical computers in the sense that they can compute things that classical
computer cannot. The real question is one of efficiency, and by efficiency I
mean the difference between polynomial time and worse-than-polynomial time and
the problem scales. The truth is we only know of a few key problems that we
know quantum computers can solve efficiently, and that we don't know for sure
that classical computers can't.

One example is factoring integers. We know that quantum computers can factor
integers quickly, but we don't know for sure that classical computers cannot.
In fact, many researchers believe that, because of recent advances in computer
science and cryptography, we *will* find a polynomial-time algorithm for
factoring integers relatively soon.

The question is, who really needs to factor integers on a regular basis? The
only answer I can come up with is number theorists (trying to prove theorems)
and the government (trying to break encryption). But these days [people are
moving away from factoring-based
encryption](http://rjlipton.wordpress.com/2013/03/02/cryptography-is-dead/). So
who's left to care?

There are, admittedly, other ways that quantum computers can speed up things,
but it's not as drastic as the mainstream media would have one believe. For
example, the best known speedup for solving NP-complete problems, which
includes most scheduling, packing, and routing problems (an efficient algorithm
for this would revolutionize the world), is on the order of a square-root. That
is, it reduces the time from an exponential to a
square-root-of-an-exponential, which is still egregiously slow. 

This is not to downplay the importance of quantum computing. It's a
multifaceted subject providing a vast trove of interesting problems, answers,
and discussions. It excites me that one day I might actually contribute some
small fact to nudge forward human knowledge about quantum computing. But the
set of useful problems we know how to solve efficiently with quantum computers
is just so minuscule. In order to convince me that quantum computers may
someday become commonplace, one would need to present a problem that quantum
computers can solve with applications on the scale of Facebook. It needs to be
something that potentially every human could have use for. And while I am not
an expert in quantum computing, if such a problem and solution existed I'd
probably have heard of it by now (it would be trumpeted along with factoring
and the hidden subgroup problem as triumphs of the model).

So unless there are extreme revolutions in theoretical computer science, which
is certainly possible, it seems safe to reuse that infamous quote here: the
world will never have need for more than five quantum computers.
