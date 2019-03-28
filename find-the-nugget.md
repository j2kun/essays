# Find the nugget

DATE

Math has a lot of information in it. How does one remember it all?

Some folks use systems of flashcards, as Michael Nielsen detailed recently.
I've tried that, and it never really worked for me. For example, I tried that
to memorize concepts in statistics (power vs. sensitivity, Type I, II errors),
but it never sticks.

LINK TO MICHAEL NIELSENS POST

Another tried and true approach is to use the concept to do something else.
There's a joke in academia that students don't learn algebra until they take
calculus. This approach has often worked for me, but it has to be the right
kind of application. One that actually requires you to exercise your knowledge
of the dependent subject. You won't learn linear regression well by using a
black-box library, but you might by implementing a weighted variant, or proving
it fails to model a particular distribution of data.

But even with an application, you need to actively work to synthesize your
knowledge. Even if I designed a statistical experiment, I need to deliberate on
what power and sensitivity are in that context, and connect it to my lizard
brain's undersatnding, or I'll mix them up again in a week. The technique that
has worked for me is compression. I think most professional mathematicians
actively do this, whether they explain it or not.

You see, mathematicians are lazy. It's a trait shared with programmers, but a
different sort of flavor. The primary goal of mathematics is for humans to gain
insights about mathematical objects and patterns. The laziness is oriented
around human understanding and communication, whereas software laziness is
often oriented around reducing toil—those repetitive, time intensive tasks that
should be automated.

LINK TO DEFINITION OF TOIL

Mathematical compression is different, and closer to how programmers might
internalize hard-won wisdom about design or operations. I often hear (and
repeat) the phrase, "Prefer composition over inheritance," which summarizes a
morass of pitfalls in short-sighted uses of object orientation. Or such gems as
"Test behaviors, not functions," and "Double it or cut it by half." These
nuggets of wisdom can be expanded on demand, ideally with references to
examples, postmortems, and other documents with details that we can't remember
offhand. And we shouldn't remember them! A four-word maxim is easy to recall,
and it's how we synthesize solutions across disparate areas of software.

ADD LINKS TO PAGES EXPLAINING QUOTES: SID MEIER CIVILIZATION

For mathematical objects I often construct (or receive) a similarly short
nugget that encapsulates the core property of an idea. The details, including
statements of theorems, proofs, and examples, are either referenced or
re-derived as needed.

Here's a recent example from an interaction I had on Twitter (where it's very
easy to nerd snipe me).

"What's the smallest possible entry of the Perron eigenvector of a graph?"

My nugget: Perron eigenvector measures the probability of a random walk landing
on each node. Small entry -> low probability. What sorts of graphs have some
node in it that would be hard to reach if you walked randomly through the
graph? A clique with a long tail seems good.

My guess: n/2 clique with n/2 tail.

Actual: ...

Compare this to what an uninitiated person would do to try to answer this
question. Go to Wikipedia, and the Wikipedia page is a mess of notation and
"this is the same as that" references, but with no mention of a random walk at
all.

LINK TO WIKIPEDIA

Mathematicians prefer compression over memorization. If a complex proof can be
condensed into a single picture, we rejoice. If a small representative example
captures all the difficulties of the general proof, we are happy to omit the
general proof entirely! A good nugget allows you to reproduce the details on
demand without any particularly strong memory of the details themselves.

This mentality has led to published papers that are incorrect; both small
falsehoods and fatal flaws show up regularly because authors omit details.

LINK TO EXAMPLES OF FALSE THEOREMS PUBLISHED, MAYBE LES LAMPORT ESSAY?

Blashpemous! Gauss would disown his children for bringing such shame on the
family name. More realistically, this should be thought of as mathematicians
leaning into their failure budget. Mathematics is a freight train lumbering
through time.  Vagabonds may hitch a ride, but if their ideas are incorrect
they will eventually be caught, corrected, refined, or fall off and be
forgotten. It's not critical that a piece of mathematics be perfect at first
publication. Human understanding can be refined and corrected in retrospect
with little permanent damage. We're not aiming for five nines.

LINK TO GAUSS TELLING HIS KIDS NOT TO BE MATHEMATICIANS

LINK TO CONCEPT OF NINES

Better yet, the pattern of compressing and re-deriving math as needed serves as
a continual check against the claims of published math. Mathematicians might
often argue that the process of re-deriving math is part of the learning
process. They are right to a point. Math is not a spectator sport, and working
out the details yourself is a great way to come up with your own nuggets. On
the other hand, this attitude can also be used by authors (myself included) to
justify the wrong kind of laziness: not doing due diligence, skipping details
because it's cumbersome to typeset, or leaving out extra conditions needed to
make a claim true.

Finding the nugget of a mathematical idea is the best way to remember it long
term. In my experience, there's no limit to how many nuggets you can retain. I
haven't done complex analysis in almost ten years—and I was hardly any good at
it!—but I still remember nuggets about making path integrals easy by going off
the real line. I can't remember the names of any theorems, but I remember the
concept and use of a winding number: it turns integrals into counting problems.

So if you're learning a mathematical topic, and it's important enough that you
want to remember it long term, try to find the nugget, and accept that you will
forget the rest.
