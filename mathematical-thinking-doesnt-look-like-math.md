# Mathematical thinking doesn't look anything like mathematics
2013-12-03

I like to think a lot about mathematics education, and I often read articles
about the woes of standards and testing and bad curricula. But there's one huge
problem with all the talking heads and the purported panaceas. 

It's that nobody is giving a good description of what mathematical thinking
skills *are*.

Oh, sure, people will throw around vague and fancy words like "critical
thinking" and "quantitative reasoning" and "mathematical modeling." But as
every mathematician knows it's the content of a definition that counts. When
you get down to the details about what these fancy terms really mean, almost
every article or standard or curriculum I've ever read falls flat on its face
and reverts to the same old crappy word problems and standards we have learned
to hate so passionately. I could give a huge list of specific writers, pundits,
and state standards that fail in this way, but it would distract us from the
real question:

## What the hell does it mean for a skill to be mathematical?

What makes a thought or thought process "mathematical," and which of those
skills are valuable for students to learn? Obviously not every student will
become a mathematician or even work in STEM, so there has to be a gradient from
useful to not useful. Finding a bona-fide criterion to distinguish between the
two seems extremely hard, but we can at least start by pointing out examples of
what kinds of thinking are mathematical and what kinds are not.

The surprising truth is that those skills that are most predominantly
mathematical actually look *nothing like* mathematics! I want to illustrate
this in two ways. The first is to point to the writing of a prolific
mathematician (theoretical computer scientist) Scott Aaronson, and his article,
[Twenty Reasons to Believe Oswald Acted
Alone](http://www.scottaaronson.com/blog/?p=1596). In this article Aaronson
gives a list of reasons why all of the conspiracy theories about the
assassination of John F. Kennedy are probably wrong. Interestingly, these
reasons have significant overlap with the [thought process Aaronson uses to
approach mathematical research](http://www.scottaaronson.com/blog/?p=304) when
the claims appear to be too good to be true. But for the reader not actively
involved in mathematical research, it's easier to see the logic at work on a
universally understood topic: whether the government is involved in a
conspiracy.

The entire article is worth reading, but let me point out some of his arguments
that are obviously mathematical.

>  The shooting of Oswald by Jack Ruby created the perfect conditions for
>  conspiracy theorizing to fester.  Conditioned on that happening, it would be
>  astonishing if a conspiracy industry hadn’t arisen, with its hundreds of
>  books and labyrinthine arguments, even under the assumption that Oswald and
>  Ruby both really acted alone.

Why is this mathematical? There are no numbers, equations, or geometric
transformations at work here. Because of some keywords like "conditioned," you
might think there's some high-level probability theory happening behind the
scenes. Maybe Aaronson scratched out a few computations on the back of a napkin
and exclaimed, "By Jove, it's simply Bayes Theorem!" But no, that didn't
happen. And you don't need to know any probability theory to follow (or even
come up with) this argument.

That is, if we want to teach mathematics with the goal of teaching critical
thinking skills, then it makes much more sense to have students apply basic
probabilistic arguments to things like the JFK assassination than to have them
memorize how to solve problems about randomly drawing socks out of a drawer.

The point is that the *thinking skills* aren't about getting answers right or
even getting an answer at all (we have computers to crunch the numbers for us,
after all). The point is to give concrete, logical, high level reasons why
something is true or false. Compare this to factoring polynomials, graphing
parabolas, and computing derivatives, and you start to wonder what skills our
current education system could possibly be developing, considering how much
time we devote to these tasks and how tangential they are to critical thinking.

Here's another example:

> Almost all JFK conspiracy theories must be false, simply because they’re
> mutually inconsistent.  Once you realize that, and start judging the
> competing conspiracy theories by the standards you’d have to judge them by if
> *at most one could be true,* enlightenment may dawn as you find there’s
> nothing in the way of just rejecting all of them.

This is clearly mathematical, because one of the most fundamental mathematical
arguments is to suppose two claims are true, and deduce something impossible.
The conclusion is then that both claims can't be true, and at least one is
false. This is one form of a *proof by contradiction*. And indeed, if we want
to teach proof techniques for people who aren't going to go on to do
mathematics, this example shows that we need not appeal to algebra or calculus.

One more:

> If the conspiracy is so powerful, why didn’t it do something more impressive
> than just assassinate JFK? Why didn’t it rig the election to prevent JFK from
> becoming President in the first place?  (In math, very often the way you
> discover a bug in your argument is by realizing that the argument gives you
> more than you originally intended—vastly, implausibly more.  Yet every
> pro-conspiracy argument I’ve read seems to suffer from the same problem.  For
> example, after successfully killing JFK, did the conspiracy simply disband?
> Or did it go on to mastermind other assassinations?  If it didn’t, why not?
> Isn’t pulling the puppet-strings of the world sort of an ongoing proposition?
> What, if any, are the limits to this conspiracy’s power?)

This thought is one held dear by many theoretical computer scientists, because
we are specifically interested in the computational power of various kinds of
mathematical models. But once again the deep mathematical idea is trivial to
understand. 

There are a couple of other mathematical bits in Aaronson's article, but the
point is to show that mathematical thinking comes in way more forms than
educators will tell you. And so my question to these educators is this: if
critical thinking is a primary goal of mathematics education, is this the kind
of critical thinking you're talking about? Or is it a different kind of
critical thinking? These are the questions that need to be answered before we
even start thinking about a curriculum. 

In my mind this is in fact the kind of critical thinking we're after in
education, and all that stuff about polynomials and geometry and calculus is
supposed to be a means to that end. It still doesn't give me a definition of
critical thinking, but it does provide a *list* of examples of critical
thinking. I expand this list in my lengthy [critique of the Common Core
Mathematical
Standard](http://jeremykun.com/2013/11/04/deconstructing-the-common-core-mathematical-standard/)
on my blog Math ∩ Programming.

But this is only half of mathematics education. We don't just care about
critical thinking skills but also in what I call *problem formalization* or
what others would call *mathematical modeling*. The reason I don't call it
mathematical modeling is because that conjures images of physics and finance
and a whole lot of other very specific applications of mathematics to the
outside world. 

Problem formalization in my intended fashion is much broader. For example, it
includes figuring out how to deal with the question, "is infinity a number?"
That is, it focuses heavily on understanding what the heck is even being asked
in a precise way. It can include many aspects people ascribe to mathematical
modeling: clarifying or rejecting assumptions, describing things by equations,
relating things back to the real-world picture. But it need not have any or all
of these things. 

To say it another way, problem formalization is about taking a question and
making it precise, perhaps with existing or newly invented mathematics. The
kinds of critical thinking skills we described with Scott Aaronson's musings on
JFK are, for the mathematician, a guide to figuring out how to do appropriate
problem formalization (and, perhaps to a greater extent, sketching the
formalization of a proof). Indeed, any tool you would use to address a question
of truth with proof is already mathematics, and if we're concerned about
innovation and global competitiveness, teaching our students to generate their
own mathematical ideas is much more important than having them memorize
dictated ideas, even if the two coincide. 

For an extended example of problem formalization, and evidence that mathematics
can be taught this way, read my post [on teaching graph
theory](http://jeremykun.com/2011/06/26/teaching-mathematics-graph-theory/)
(which is commonly thought of as an advanced mathematical subject) to high
school freshman. Most of the content of this article doesn't look like
mathematics at all to somebody who isn't substantially familiar with
mathematics, and the real mathematical heart of the whole thing is not even the
part that does look like mathematics.

I could use this discussion to propose a curriculum, one split up into tracks
for Reasoning and Problem Formalization. I think educators should consider such
an approach very seriously, but the true purpose of this article is to
emphasize that **educators must deeply understand their goals when
designing curricula and standards.** Because as it stands the means are not
even in the same ballpark as the stated ends.

While the problems facing education in the US can be described as nothing other
than gargantuan, making sure we understand what makes stuff "mathematical" is
something we can easily solve by giving mathematics teachers more training
before they enter the classroom and more resources for training during their
careers, by allowing more time outside the classroom to hone curricula, and by
giving higher wages and respect to attract excellent teachers. 

While one could make this argument for any subject and at any level of
education, it's clear to me that most of these fixes aren't already in place
for mathematics because our society doesn't understand why we have mathematics
at all, or what it contributes to our education and life after school. It's
not to promote innovation in engineering and science or to train
mathematicians (though it may help a great deal). It's simply to learn
certain kinds of principled thinking skills, and this can be in the context
of analyzing John F. Kennedy's assassination or doing puzzles about
bridges, and it often requires no "mathematics" as most people know it.

I'm not suggesting we remove all algebra or geometry from education, just that
we think harder (and think mathematically) about the purpose of mathematics in
education. Until we understand what that is and design education around it,
sports programs will continue receive more funding, textbooks will continue to
be awful, and students will continue to find mathematics boring and stupid.
