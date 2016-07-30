# Programming is not math, huhng is not math, huh?

2014-06-18

You're right, programming isn't math. But when someone says this, chances are
it's a programmer misunderstanding mathematics.

I often hear the refrain that programmers don't need to know any math to be
proficient and have perfectly respectable careers. And generally I agree. I
happen to think that programming only becomes fun when you incorporate
mathematical ideas, and I happen to write [a blog about the many ways to do
that](http://jeremykun.com), but that doesn't stop me from realizing that the
vast majority of programmers completely ignore mathematics because they don't
absolutely need it. 

So when Sarah Mei argues in her article ["Programming is not
Math"](http://www.sarahmei.com/blog/2014/07/15/programming-is-not-math/) that
math skills should not be considered the only indicator of a would-be
programmer's potential, I wholeheartedly agree. I've never heard anyone make
that argument, but I'm much younger than she is. Having faith in Mei's vast
life experience, I'll assume it was this way everywhere when she was writing
Fortran in school, and it seems plausible that the attitude lingers at the most
prestigious universities today.

But then she goes on to write about mathematics. As much as I respect her
experience and viewpoints, her article misses the title's claim by a long shot.
It's clear to me that it's because she doesn't understand the mathematics part
of her argument. Here's the best bit:

> Specifically, learning to program is more like learning a new language than
> it is like doing math problems. And the experience of programming today, in
> industry, is more about language than it is about math.

This is the core of her misunderstanding: being good at math is not about being
good at "doing math problems" (from the context of her article it's clear that
she equates this with computation, e.g. computing Riemann sums). And the
experience of programming in your particular corner of industry is not
representative of what programming is about. The reality of the
mathematics/programming relationship is more like this:

 1. Mathematics is primarily about conjecture, proof, and building theories, not
    doing slews of computations.
 2. Learning to do mathematics is much more like learning language than learning
    to program is like learning language.
 3. Large amounts of effort are spent on tedious tasks in industry for no reason
    other than that we haven't figured out how to automate them yet. And novel
    automations of tedious tasks involve interesting mathematics by rule, not
    exception. 
 4. That doesn't change how crucially reliant every programmer (and every
    company) is on the mathematical applications to programming that allow them to
    do their work.

# Mathematics is closer to language

Item 2 is probably why Mei isn't able to find any research on the similarities
between math and programming. There is a ton of research relating mathematics
to language learning. For an extended bibliography with a nice narrative, see
Keith Devlin's book [The Math
Gene](http://www.amazon.com/The-Math-Gene-Mathematical-Thinking/dp/0465016197).

One big reason that mathematics is much more like language than programming, is
that doing mathematics involves resolving ambiguities. In programming you have
a compiler/interpreter that just *dictates* how an ambiguity resolves. But in
mathematics, as in real language, you have to resolve them yourself based on
context. This happens both in the modeling side of mathematics and in the
hard-core theory side. Contrary to the most common internet wisdom, almost no
working mathematicians do math from a purely axiomatic standpoint. The
potential for ambiguities arises in trying to communicate a proof from one
person to another in an elegant and easy-to-understand way. Note the focus on
communicating. This is essentially the content of a first course in proofs,
which, by the way, is usually titled something like "A transition to advanced
mathematics." The reason that this never shows up when you're computing Riemann
sums is because in that context you're playing the role of the computer and not
the mathematician. It's like getting the part of a spear carrier in a play and
claiming, "acting is just about standing around looking fierce!" It's a small,
albeit important, part of a *much* larger picture.

Having studied all three subjects, I'd argue that mathematics falls *between*
language and programming on the hierarchy of rigor.

 - Human language
 - Mathematics
 - Programming

and the hierarchy of abstraction is the exact reverse, with programming being
the most concrete and language being the most abstract. Perhaps this is why
people consider mathematics a bridge between human language and programming.
Because it allows you to express more formal ideas in a more concrete language,
without making you worry about such specific hardware details like whether your
integers are capped at 32 bits or 64. Indeed, if you think that the core of
programming is expressing abstract ideas in a concrete language, then this
makes a lot of sense.

This is precisely why learning mathematics is "better" at helping you learn the
kind of abstract thinking you want for programming than language. Because
mathematics is closer to programming on the hierarchy. It helps even more that
mathematics and programming readily share topics. You teach graph coloring for
register allocation, linear algebra and vector calculus for graphics,
combinatorics for algorithms. It's not because you need to know graph coloring
or how to count subsets of permutations, but because it shows the process of
reasoning about an idea do you can understand the best way to organize your
code. If you want to connect language to programming you almost always have to
do so through mathematics (direct modeling of sentence structure via
programming is a well-tried and unwieldy method for most linguistic
applications).

# Big-O is "pretty much meaningless"

Another issue I have with Mei's article is on her claim that "big-O" is
meaningless in the real world. More specifically, she says it only matters what
the runtime of an algorithm is on "your data." 

Let's get the obvious thing out of the way. I can name many ways in which a
result in improving the worst-case asymptotic complexity of an algorithm has
literally changed the world. Perhaps the biggest is the [fast Fourier
transform](http://jeremykun.com/2012/07/18/the-fast-fourier-transform/). So if
you're applying to work at a company like Google, which deservingly gets credit
for changing the world, it makes total sense for interviewees to be familiar
with the kind of mathematical content that has changed the world in the
past. Maybe it's a mistake for smaller companies to emulate Google, but you
can't blame them for wanting to hire people who would do well at Google.

But at a deeper level I don't believe Mei's argument. Her example is this.

> An algorithm that is O(n**2) for arbitrary data may actually be constant time
> (meaning O(1)) on your particular data, and thus faster than an algorithm
> that is O(n log n) no matter what data you give it.

First, the chance is absolutely negligible that you will come across a
nontrivial problem where the runtime of a standard algorithm meets the worst
case on "your" data, but when you use a generally-considered worse algorithm it
does much better. Second, there is a very rich mathematical theory of,
"algorithms that run extremely fast and return correct answers to queries with
high probability." So again, you can turn to mathematics where the expectations
are quantifiable rather than arbitrary and guessed.

But more deeply, **nobody in industry has any clue** what it is that
characterizes "real world data" that allows you to make worst-case guarantees.
They have a fuzzy idea (real social networks are usually sparse, etc.), but
little in the way of a comprehensive understanding. This is a huge topic, but
it's a topic of **active research**, which is uncoincidentally filled to the
brim with mathematics. The takeaway is that even if you have an algorithm that
*seems* to run quickly on "your" data, "seems" is the best you'll be able to
say without answering big open research questions.  You won't be able to
guarantee anything, which means you'll be stuck telling your manager that
you're introducing more points of failure into the system, and you risk being
paged in the middle of the night because the company has expanded to China and
their data happens to break your algorithm on average.

But you're a smart engineer, so what do you do? You run your clever algorithm
and track how long it takes; if it takes too long, you abort and do the
standard O(n log n) solution instead. Problem solved. But wait! You needed to
know the difference between your algorithm's worst case complexity and the
baseline complexity, and you had to determine how long to wait before aborting. 

The fact is, you can't function without knowing the baselines, and asymptotic
runtime (big-O) is the gold standard for comparing algorithms. Certainly you
can mix things up as appropriate, as the fictional engineer in our story did,
but if you're going to do a more detailed analysis you have to have a reference
frame. At a company where a one-in-a-million error happens a hundred times a
day, mathematical guarantees are (literally) what help you sleep at night. Not
every programmer deals with these questions regularly (which is why I don't
think math is necessary to be a programmer), but if you want to be a *great*
programmer you had better bet you'll need it. Companies like Google and Amazon
and Microsoft face these problems, aspire to greatness, and want to hire great
programmers. And great programmers can discuss the balance issues of various
algorithms.

But Sarah Mei is right, there might be some interesting ways to model
algorithms running better on "your" data than the worst case (and if I were
interviewing someone I would gladly entertain such a discussion), but I can say
with relative certainty that even an above-average math-phobic interviewee is
not going to have any new and deep insights there. And even if one does, one
needs to be able to answer the question of how this relates to what is already
known about the problem. Without that how can you know your solution is better?

# A "minor specialization"

Now my biggest beef is with her conclusive dismissal of mathematics.

> If a small and shrinking set of programming applications require math, so
> much so that we cordon you off into your own language to do it, then it’s
> pretty clear that heavy math is, these days, a minor specialization.

Oh please. You can't possible think that every mathematician who programs does
so in Fortran or Haskell. I'm a counterexample: I'm proficient in C, C++, Java,
Python, Javascript, HTML and CSS. I have only really dabbled in Haskell and
Racket and other functional languages (I like them a lot, but I just get more
done in Python).

But what's worse is that I have so many programming applications of mathematics
that I don't know what to do with them all. It's like they're sprouting from my
ears! 

Let's take the examples of what Mei thinks are purely unmathematical uses of
programming: "ease of use, connectivity, and interface." I'm assuming she means
the human-computer interaction version of these questions. So this is like, how
to organize a website to make it easy for users to find information and
streamline their workflow. I'd question whether anyone in the industry can
really be said to be "solving" these problems rather than just continually
debating which solution they arbitrarily think is best. In fact, I'm more
inclined to argue that companies change their interface to entice users to pay
for updates more than to make things easier to use (I'm looking at you,
Microsoft Word).

In any case, it's clear that Mei is biased toward one very specific kind of
programming, which does have mathematical aspects (see below). But moreover,
she blurs the distinction between an application of mathematics to programming
and what she finds herself and her colleagues actively doing in her work. Let
me counter with my own, more quantifiable examples of the mind-bogglingly
widespread applications of mathematics to industry, both passive and active.

**Optimization:** the big Kahuna of mathematical applications to the real
world. Literally every industrial company relies on state of the art
optimization techniques to optimize their factories, shipping lines, material
usage, product design. And I'm not even talking about the software industry
here. I'm talking about Chevron, Walmart, Goldman Sachs. Every single Fortune
500 company applies more "heavy" math on a daily basis than could be taught in
four years of undergraduate education. They don't care about ease of use, they
care about getting that extra 0.05% profit margin. And as every mathematician
knows, there is a huge theory of optimization that ranges from linear
programming to functional analysis to weird biology-inspired metaheuristics. 

**Signal processing:** No electric device or wireless communication system
would exist without signal processing. The entire computer industry relies on
digital signal processing techniques and algorithms proliferated via
mathematics. Literally every time you type a key on your keyboard, you're
relying on applications of mathematics to programming. Sure, you don't need to
know how to build a car to drive it, but signal processing techniques extend to
other areas of programming, such as graphics, data mining, and optimization,
and a large portion of the software industry is disguised as the hardware
industry because they use languages like VHDL instead of Ruby. They *really*
need to know this topic, and it's not fair to forget them. That being said,
let's not forget all the engineers who do signal processing in Matlab. Our list
just keeps getting bigger and bigger, huh?

**Statistics:** Every company needs to manage their risk and finances via
statistics, and every application of mathematics and statistics to risk and
finance is done via programming. Whether you use SAS, JMP, R, or just Excel,
it's all programming and all requires mathematical understanding. This is not
even to mention all of the statistical modeling (via programming) that goes on
in a non-financial setting. For example, in Obama's presidential campaign and
in sports forecasting. Even as I write this, NPR is reporting on the Malaysia
flight that was shot down in Ukraine, and how technicians are using
"mathematics and algorithms" to pinpoint the location of the crash.

**Machine Learning:** A hot topic these days, but for a long time engineers
have been trying to answer the question, "what does it mean for a computer to
learn?" Surprise, surprise, the generally accepted answer these days came from
mathematicians. The theory of
[PAC-learning](http://jeremykun.com/2014/01/02/probably-approximately-correct-a-formal-theory-of-learning/),
and more generally its relationship to the many widely-used machine learning
techniques, paved the way for things like boosting and the study of statistical
query algorithms. Figuring out smart ad serving? Try [bandit-learning
techniques](http://jeremykun.com/2013/10/28/optimism-in-the-face-of-uncertainty-the-ucb1-algorithm/).
It's mathematics all the way down.

**Graphics/Layout:** You want ease of use in human computer interaction? You
want graphics. You want special effects in movies? You need linear algebra,
dynamical systems, lots of calculus, and lots of graphics programming. You want
video games? Data structures, computational geometry, and twice as much
graphics as you thought you'd ever need. You want a dynamic, adaptive,
tile-based layout on your website? Get ready for packing heuristics, because
that stuff is NP-hard! Information trees, word clouds, rankings, all of these
layout concepts have rich mathematical underpinnings. 

You see, Mei's fundamental misconception is that the kind of applications that
we haven't yet automated and modularized constitutes what programming is all
about. We don't know how to automate the translation of obscure and ambiguous
business rules to code. We don't know how to automate the translation from a
picture you drew of what you want your website to look like to
industry-strength CSS. We don't know how to automate the organization of our
code so as to allow us to easily add new features while maintaining backwards
compatibility. So of course most of what goes on in the programming industry is
on that side of the fence. And before we had compilers we spent all our time
tracking memory locations and allocating registers by hand, too, but that's no
more the heart and soul of programming than implementing business rules.

And by analogy, most of writing is not literature but fact reporting and budget
paperback romance novels, but we teach students via Twain and Wilde. And most
cooking is reheating frozen food, not farm-to-table fine cuisine, so should a
culinary student study McDonald's?

But if you wanted to genuinely *improve* on any of these things, if you wanted
to figure out how to automate the translation of drawn sketches to good HTML
and CSS, you can count on there being some real mathematical meat for you to
tenderize. I hope you try, because without mathematics we programmers are going
to have an extremely hard time making real progress in our field.
