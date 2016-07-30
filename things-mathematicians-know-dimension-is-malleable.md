# Things mathematicians know but most people don't: dimension is malleable

One of my science pet peeves is when people say, "time is the fourth
dimension." It's like a fishy smell; when someone says it without a hint of
humor I usually end up convinced that they don't know what dimension is or how
it works. Considering that nobody really knows how time works either, the
statement is just utter nonsense. Even worse are those popular "science" videos
with titles like, "Imagining the Tenth Dimension" and, "Who lives in the
Eleventh Dimension?"

The biggest misunderstanding is in the word "the." That is, that time has no
choice but to be the fourth dimension. Why can't time be the first dimension?
Or the eleventh? What's so mystical and supernatural about the number four that
time has to go there?

In fact, the reality is that dimension is a mathematical construction designed
and redesigned as necessary to suit our needs in analyzing mathematical issues.
As a concept, dimension is *malleable*. And the easiest way to realize this is
to notice [how many different kinds of dimension there
are](http://en.wikipedia.org/wiki/Dimension_(mathematics_and_physics)#In_mathematics).

To name a few: the dimension of a vector space, the fractal dimension of a
curve, the dimension of a smooth manifold, the Hausdorff & Lebesgue dimensions
of a topological space, the Krull dimension of a commutative ring, the
Vapnik-Chervonenkis dimension of a hypothesis space (this one is particularly
important to me).

These all sound confusing and twisted, and they are almost completely unrelated
to each other, and few have anything to do with time or space. So why do we
call them all "dimension?" Because their job as concepts is to help us
taxonomize mathematical objects with respect to a notion of magnitude or
complexity. As a simplified example, we might be able to prove a theorem like:
"this computer program can learn to play any two-player game optimally, but
only if the 'game dimension' is not too large." Here dimension would describe
how complex the game is in a principled way.

![robot playing
chess](http://fc01.deviantart.net/fs19/i/2007/243/6/2/play_chess_with_robot_by_cuson.jpg)

On the other side of the coin, "dimensions" often just represent features of
some system. For example, you might represent an economic market in terms of
the price of tomatoes, diapers, whiskey, corn, and the unemployment rate. Then
one instance of the market requires five potentially independent numbers to
describe, and hence the space of all markets is a 5-dimensional space. We use
the word "space" mathematically to mean "collection." This has nothing to do
with physics. 

We can analyze the change of this market over time and, if we assume prices and
unemployment rates change continuously, it would trace out a one-dimensional
curve through a 5- or 6-dimensional space, depending on how you want to look at
things. But is anything about tomatoes or whiskey intrinsic to economics?
Certainly not. We could reorder, replace, or remove any of these dimensions if
it resulted in a better model. Indeed, the fashion of big data would lead us to
believe more dimensions are easier to learn from. The point is that the "true"
dimension of an economic market is whatever best suits our analytic needs.

A heavier example is an image: we can call the intensity of each pixel of an
image its own dimension, and then the space of all possible 100 by 100 pixel
images is a ten-thousand dimensional space! We can ask some very intriguing
questions like, what is the dimension of the space of naturally occurring
images, or of photographs of cats? Since very few images out of all possible
images are actually pictures of cats, we'd expect the dimension to be quite
small. In other words, the intensity of some pixels would tend to depend on the
intensity of neighboring pixels, and this would reduce the dimension. 

People do actually study this question. For example, the mathematical shape and
dimension of the space of 3 by 3 patches taken from natural images is known.
It's dimension is 2, and it's a shape known as the Klein Bottle. The Klein
bottle itself is a quirky thing: a two-dimensional surface whose inside is the
same as its outside, if you want o interpret it as having four spacial
dimensions. Here's the interpretation in terms of image patches.

![klein bottle model](http://jeremykun.files.wordpress.com/2013/10/klein-bottle-model.png)

Understanding this model leads to improved automated image classification,
detection, and generation. But it's not the *only* model of natural 3x3 image
patches.

Again, the central point here is that we humans invented the notion of
dimension and use it as a tool to shape our understanding of various ideas.
Spatial or time *interpretations* of dimension are prevalent because they're
extremely useful, but the truth is that dimension is what we make it. As with
the rest of mathematics, it only exists in our minds. 

So the next time someone tells you about "the" fourth dimension, tell them that
your fourth dimension is corn. 

*Jeremy Kun is the author of the blog [Math ∩ Programming](jeremykun.com). If
you found this article on dimension interesting, you might enjoy an
[application of the ideas to facial
recognition](http://jeremykun.com/2011/07/27/eigenfaces/).*

###### Things mathematicians know but most people don't
1. [There is more than one kind of infinity](http://j2kun.svbtle.com/things-mathematicians-know-more-than-one-infinity)
2. [Proofs are what's beautiful](http://j2kun.svbtle.com/things-mathematicians-know-proofs-are-beautiful)
3. [Dimension is Malleable](http://j2kun.svbtle.com/dimension-is-malleable)
