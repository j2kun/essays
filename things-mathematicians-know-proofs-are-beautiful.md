# Things mathematicians know but most people don't: proofs are what's beautiful

2013-09-30

The depiction of mathematics in popular science often falls woefully short of
reality. Authors tend to prance around the "beauty" of numbers like e, π, and
the golden ratio φ, but in all honesty numbers are only one part of
mathematics, and they're not even the best part.

In a series of short vignettes, I want to take a quick dip into some
mind-bending ideas that mathematicians enjoy (and use as tools) on a daily
basis. Hopefully you can experience the same kind of joy I did when I first
learned about these topics, and with luck you just might be enticed enough to
dive deeper.

# The beauty of mathematics lies in proofs

While there are many different styles of doing mathematics (I plan to write a
separate article about this soon), one thing that all mathematicians agree on
is the value of a good proof. It's weird to think of proofs as having an
aesthetic quality, but they do. Good proofs glean insight into why something is
true, and they often involve new techniques that can be used to prove other
things. And most of all, good proofs are *beautiful.* When mathematicians talk
about "the beauty of π", they don't mean that the number itself is beautiful.
It's just a number and is no more or less beautiful than 2π or -π or 1/π. What
*is* beautiful is how π relates to so many other things in mathematics, and
these relationships are established by interesting proofs. 

And much like the career of an artist is in the compositions he or she creates,
proofs are the brushstrokes of mathematics. No idea is interesting unless there
are proofs of theorems that show it is interesting. We are simply not happy
with a true fact, as a physicist might be if he accidentally stumbled upon some
physical law that was empirically accurate. No, a mathematician would need to
*prove* that the law is consistent and follows logically from natural
assumptions. Without a proof, "laws" are just words in the wind.

I want to show you the aesthetics of a proof with two simple examples, and I
assure you that you can understand them without any mathematical knowledge.
While it might not be immediately obvious how to solve the problems, the proofs
are so simple and obvious a seven-year-old could understand them. Indeed, this
is a big part of the beauty of these particular problems.

## Tournaments

The first problem is nice because, as my colleague Maxwell mentioned, you can
explain it over a dinner table without any paper or a pencil. It's simply a
shift in perspective that makes an initially opaque question crystal clear.

Suppose you have a tournament of 16 people playing table tennis. The tournament
is single-elimination, so the winner of a game goes on while the loser does
not. The question is: how many games are played in total? 

In the first round, there are eight games, and eight winners. In the second
round, there are four games and four winners. In the third round, two games and
two winners, and in the last round there is one game and one winner. With some
elbow grease or a calculator, you could figure out that 15 games are played in
total. Sweet.

But in this tournament we got lucky because everyone played a game in every
round. Nobody had to sit out because we got lucky with the initial number of
players. Now what if there were 1,000 players? How many games would be played
then?

The same analysis of counting how many games there are in each round becomes
much more difficult, because you have to keep track of how many players are
sitting out in each round. If I tried for a moment to write out the
calculations on paper, I'd quickly fill up the page with illegible chicken
scratch. I might even get an answer at the end: 999 games. That's a bit weird:
it's just the number of players minus one, which was true when there were 16
players, too. I'd have to check and double check that I didn't make any
mistakes, but even if my counting was sound I don't really understand *why* I
got this answer, nor am I sure that it will work if I change the starting
number of players. All in all, I have little more insight into the problem than
when I started. Might there be a better way?

Indeed, here comes the beautiful proof. We just notice that every player loses
exactly one game, except for the winner of the whole tournament. So if we want
to count the number of games, we can just count the number of losers, which is
obviously 999. And this idea will not change if the number of players changes.
Sha-zam!

![math medal](http://jeremykun.files.wordpress.com/2013/09/math-medal.jpg)

If you've read [the previous post in this
series](http://j2kun.svbtle.com/things-mathematicians-know-more-than-one-infinity),
you might recognize this as a bijection between the set of games played and the
set of losers. Indeed, coming up with clever bijections is a standard
mathematical tool used to count things. And so we have a beautiful solution to
this initially difficult-sounding problem, and a new method of proof we can try
to use on any other counting problem we might be faced with.

I've told this proof to mathematicians and English majors and kids alike, and
it seems to have a widespread aesthetic appeal. And at the same time, it's not
even immediately clear to non-mathematicians that this is mathematics at all!
It doesn't involve derivatives or polynomials or fractions or the other things
most people assume mathematics is limited to.

## Triangles inside Rectangles

Here's an even simpler example, which is often cited as the simplest example of
a beautiful proof. Say you have a triangle sitting inside a rectangle like
this:

![triangle in a
rectangle](http://jeremykun.files.wordpress.com/2011/06/triangle1.png)

How much space do you think this triangle takes up within the rectangle? Maybe
1/3? Maybe 1/2? Maybe a little less than 2/3? You can guess and measure all you
want, but how can you be entirely sure that you're right?

Well here comes the inspired proof: we can simply draw a line:

![triangle proof](http://jeremykun.files.wordpress.com/2011/06/triangle2.png)

Explaining this is trivial. The triangle takes up exactly half of the rectangle
because it does so on both sides of the line. We know it takes up half on both
sides of the line because of the symmetry of each piece. It is completely
obvious, but we can say it in words: rotating something (the piece of the
triangle) preserves its area, and the part of the rectangle to the left of the
line is just the piece of the triangle and the piece after rotating it 180
degrees.

Here the deep tool we're using is symmetry: drawing new lines help us decompose
complicated shapes into easy-to-manage pieces, and using nice rotations and
reflections we can reason about the pieces.

The beauty in both the tournament proof and the triangle proof lies in
simplicity, cleverness, and the discovery of a deep new tool. If we wanted to
ask new questions about different kinds of tournaments (say double-elimination)
or different kinds of triangles (say, if the peak is shifted left outside the
rectangle), we can use these new techniques to attack them. If we're lucky, we
can come up with a more general proof that applies to *all* tournament problems
(or triangle problems) that we could encounter. This is called a classification
theorem, and finding such a proof is a monumental accomplishment.

Want to see some more beautiful proofs? I made [a
gallery](http://jeremykun.com/proof-gallery/) of some of my favorites over the
years on my blog [Math ∩ Programming](http://jeremykun.com). One that is
particularly good for the non-mathematical crowd is the one about [tiling a
chessboard with
dominoes](http://jeremykun.com/2011/06/26/tiling-a-chessboard/). A more
advanced elegant geometry proof involves spontaneously [turning circles into
cones](http://jeremykun.com/2011/07/13/three-circles-and-collinear-centers-of-dilation/).
There is also a great picture proof about [the number of ways to choose 2
things from a collection of n
things](http://jeremykun.com/2011/10/02/n-choose-2/). Enjoy!

###### Things mathematicians know but most people don't
1. [There is more than one kind of infinity](http://j2kun.svbtle.com/things-mathematicians-know-more-than-one-infinity)
2. [Proofs are what's beautiful](http://j2kun.svbtle.com/things-mathematicians-know-proofs-are-beautiful)
3. [Dimension is Malleable](http://j2kun.svbtle.com/dimension-is-malleable)
