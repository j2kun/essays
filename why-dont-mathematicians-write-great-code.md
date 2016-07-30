# Why don't mathematicians write great code?

2014-08-25

In the [discussion](https://news.ycombinator.com/item?id=8054983) surrounding a
series of recent articles on the question of how mathematics relates to
programming (one of my favorite navel-gazing topics), the following question
was raised multiple times

> If mathematics is so closely related to programming, why don't professional
> (research) mathematicians produce great code? 

The answer is quite a simple one: they have no incentive to.

It's pretty ridiculous to claim that a mathematician, someone who typically
lives and breathes abstractions, could not learn to write well-organized and
thoughtful programs. To give a simple example, I once showed my advisor a
little bit about the HTML/CSS logical flow/style separation paradigm for
webpages, and he found it extremely natural and elegant. And the next thing he
said was along the lines of, "Of course, I would have no time to *really* learn
and practice this stuff." (And he says this as a relatively experienced
programmer)

That's the attitude of most researchers. Most programming tools are cool and
would be good to have expertise in, but it's not worth the investment. Mostly
that comes off as, "this is a waste of time," but what's keeping them from
writing great code is their career.

Mathematics and theoretical computer science researchers (and many other
researchers) are rewarded for one thing: publications. There is no structure in
place to reward building great software, and theoretical computer scientists in
particular are very aware of this. There have even been some informal proposals
to change that, because everyone understands how valuable good software
libraries are to progress in our fields.

But as it currently stands, the incentives for mathematicians reward one thing
and one thing only: publishing influential papers. There are *very* small
emphasis given to things like teaching, software, or administrative duties. But
the problem is that they don't *replace* publications. So spending work time on
things that are *not* publications takes away from time that could be spend on
papers. Everyone understands this about the job market. Say you have two
candidates of equally good work, but the first candidate has one more top-tier
paper and the second has contributed an equal amount of work to open source
software. Though I have never seen this happen first hand, every career panel I
have posed this question to has agreed the first candidate would be chosen with
high probability.

So when mathematicians or theoretical computer scientists *do* write code, they
have an incentive to get it working as quickly and cheaply as possible. They
need the results for their paper and, as long as it's correct, all filthy hacks
are fair game. This is most clearly illustrated by the relationship between
mathematicians and their primary paper-writing tool, the typesetting language
TeX. All mathematicians are proficient with it, but almost no mathematicians
actually *learn* TeX. Despite everyone knowing that TeX is a true programming
language (it has a compiler and a Turing-complete macro system), everyone
prefers to play guess-and-check with the compiler or find a workaround because
it's way faster than determining the root problem. 

With this in mind, it's hard to imagine your average mathematician having a
deep enough understanding of a general-purpose language to produce code that
software engineers would respect. So something like adequate testing, version
control, or documentation is that much more unlikely. Even if they do write
programs, most of it is exploratory, discarded once a proof is found achieving
the same result. Modern software engineering practices just don't apply.

For the majority of mathematicians, I claim this is mostly as it should be.
Building industry-strength tools is not the core purpose of academic research,
and much of mathematical research is not immediately (or ever) applicable to
software. And most large companies who want to utilize bleeding-edge research
for practical purposes form research teams. For example, Google does this, and
from what I've heard many of their researchers spend a lot of time working
with engineers to test and deploy new research. At places like Google (and
Yahoo, Microsoft, IBM, Toyota), researchers negotiate with their company
how their time is split between academic-style paper writing and
engineering pursuits, and there are researchers at both extremes. 

But even there, where coding is part of the goal, the best industry research
teams still hire based on publication history. I can only hypothesize why: a
great researcher can be taught programming practices trivially, so a strong
research history is more important. 
