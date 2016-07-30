# Things mathematicians know but most people don't: there is more than one kind of infinity

2013-09-27

The depiction of mathematics in popular science often falls woefully short of
reality. Authors tend to prance around the "beauty" of numbers like e, π, and
the golden ratio φ, but in all honesty numbers are only one part of
mathematics, and they're not even the best part.

In a series of short vignettes, I want to take a quick dip into some
mind-bending ideas that mathematicians enjoy (and use as tools) on a daily
basis. Hopefully you can experience the same kind of joy I did when I first
learned about these topics, and with luck you just might be enticed enough to
dive deeper.

# There is more than one kind of infinity

This may come as a surprise to many of you. In primary and secondary school
very few teachers have a serious discussion about infinity, and how infinity
works. Is it a number? Does it obey usual laws of arithmetic? In most American
elementary and secondary schools, teachers won't give you a straight answer.

But here is perhaps a more basic question: is infinity unique? The first person
to seriously (mathematically) consider this question was the German
mathematician Georg Cantor. Around 1880, he presented his work showing that
there are in fact many kinds of infinity, and, despite being entirely correct,
it was rejected by his peers! Some rejected it based on philosophical or
religious objections, while others denied his work on mathematical grounds
despite being unable to find a flaw in his arguments. They called his ideas a
"disease," and "laughable," and Cantor himself was labeled a "corrupter of
youth." Many believe that this ridicule degraded Cantor's mental health, and
aided in his eventual institutionalization. 

As with most historical issues, mathematical hindsight is 20/20, and today
Cantor is deeply revered for his groundbreaking insight. The fact that there
are multiple kinds of infinity is often one of the first deep truths that a
student of mathematics learns. And some who go on to careers in mathematics do
all of their work entirely within subfields of math originating with Cantor.
The broadest name for this is "Set Theory".

So let's go ahead and see what all the fuss was about, and get at the heart of
the matter. 

## Owls and Hedgehogs and Elephants, oh, my!

Imagine you have a group of three observant owls.

![three
owls](http://cdn.abclocal.go.com/images/ktrk/cms_exf_2007/news/local/owls1.jpg)

You can think of the number 3 as being represented by these actual owls. But
you might also have a collection of three hedgehogs,

![three
hedgehogs](http://www.zooborns.com/.a/6a010535647bf3970b0168eae8b675970c-500wi)

and you could also say that the number 3 is represented by these hedgehogs.
Were you less familiar with numbers, you might be concerned that the number 3
as represented by hedgehogs might be different from the 3 as represented by
owls. But there is an obvious way to show they're the same kind of 3: you can
pair up each owl with a hedgehog. There are lots of ways to do this, and it
doesn't matter which we pick, but here's one possible way:

![hedge-jection](http://jeremykun.files.wordpress.com/2013/09/hedjection.png)

This "pairing up" has a formal name, it's called a *bijection*. The important
part is that each owl is paired with a distinct hedgehog, and each hedgehog
with a distinct owl. For example, if we had only two elephants,

![two elephants](http://hedweb.com/animimag/elephant-calfs.jpg)

Then we couldn't find a bijection between the three owls and the two elephants:
one owl would always be left out, and this tells us that 2 is not the same as
3. 

![sad owl has no elephant
friend](http://fc02.deviantart.net/fs71/f/2010/226/b/6/Sad_Owl_1_by_distasty.jpg)

Now this is all pretty simple and cute, but there's a very deep concept at work
here. We're saying that, rather than have a single universal concept for a
number, we have *many* kinds of definitions for numbers (i.e. we might use owls
or hedgehogs). We can show that some ideas are the same by giving relationships
(a bijection, in this case) between the separate concepts, and that some ideas
are different by asserting no relationship of the desired form can exist.

But what does it have to do with infinity? Well we can extend this method for
describing numbers to an infinite collection of objects. So let's imagine we
have an infinite parade of turtles. That's right, this time it's really
[turtles all the way
down](http://en.wikipedia.org/wiki/Turtles_all_the_way_down):

![infinitely many
turtles](http://jeremykun.files.wordpress.com/2013/09/turtles.png)

In a very straightforward way, we can ask how many turtles there are and call
whatever concept that is "infinity," or ∞.  We're not really saying we know
what it is, but we're giving it a name.

Now we do something crazy. It's Cinco de Mayo in the land of turtles today, so
we can choose to put sombreros on some of the turtles. Maybe the first and
third turtles get sombreros, but the second doesn't, and we keep going.

![some turtles have
sombreros](http://jeremykun.files.wordpress.com/2013/09/turtles-with-sombreros.png)

But we have to be careful here: it's important that we consider *everyone* in
the turtle parade for the possibility of getting a sombrero. That is, we might
need an infinite number of sombreros if, say, every other turtle gets one. We
also have the option of choosing that nobody gets sombreros. It's all fair
here.

Now we can take the **collection of all ways to pick who gets sombreros and who
doesn't**, and ask how big that collection is. 

"What's the problem?" you might protest, "It's just infinity again, the same as
the number of turtles in the parade." And this is where things get interesting.
The deep truth, and what Cantor was ridiculed for discovering, is that this
kind of infinity is actually *bigger!* Outrage! Heresy! Excommunication! But
it's the truth.

Let's call this collection **Sombrero Choices**, and we'll call the turtle
parade **Turtles**. When we say the infinity represented by the size of
**Sombrero Choices** is bigger than the infinity represented by the size of
**Turtles,** what we're really saying is that there is no bijection between
**Turtles** and **Sombrero Choices**. That is, there is no way to pair up
turtles with ways to choose sombreros without leaving anyone out, as we did
with the owls and the hedgehogs.

So we're saying that the infinity represented by **Turtles** is a *different*
kind of infinity than that represented by **Sombrero Choices**, and it's not
hard to see that the latter should be considered "bigger."

How could one hope to prove such a thing? Well, the proof would be difficult to
understand in terms of turtles and sombreros, and requires a relatively deep
concept called "diagonalization." If you're genuinely interested in a proper
treatment, you should check out [the more detailed
post](http://jeremykun.com/2011/07/09/set-theory-a-primer/) on my blog [Math ∩
Programming](http://jeremykun.com/). There is also a comment thread there for
questions and discussion.

###### Things mathematicians know but most people don't
1. [There is more than one kind of infinity](http://j2kun.svbtle.com/things-mathematicians-know-more-than-one-infinity)
2. [Proofs are what's beautiful](http://j2kun.svbtle.com/things-mathematicians-know-proofs-are-beautiful)
3. [Dimension is Malleable](http://j2kun.svbtle.com/dimension-is-malleable)
