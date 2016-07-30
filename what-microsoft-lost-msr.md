# What Microsoft lost when it closed MSR Silicon Valley

2014-09-22

Since I started thinking about my own job opportunities, I have always heard
and considered Microsoft as the best place for research in industry. Other
companies are also considered pretty excellent, but Microsoft tends to make the
top of the list in terms of who they hire and how they make it easy for great
people to do great work. 

For example, when Yahoo closed their New York research lab two years ago,
Microsoft offered every fired researcher a job, and even opened a new lab in
New York so they didn't have to move! And though I haven't verified this, from
what I've heard Microsoft has never (before now) fired a researcher. They vet
their candidates and hire people they intend to keep for the long haul.
Microsoft puts people in charge of the research labs who understand that the
primary goal is to further the state of the art. And they have a strong track
record of doing just that.

So shock and awe that Microsoft would close MSR Silicon Valley (and fire dozens
of fantastic researchers overnight) is the only reasonable response. They fired
almost everyone, offering to retain only a couple of the very highest caliber
researchers provided they're willing to move. But make no mistake, we're
talking about giants among people who are still extremely tall, here, so to
kick anyone out is literally to say, "We don't want Microsoft to be associated
with awesome breakthroughs and innovations in computer science."

I'm familiar with the theory folks, and if I can convince you that
*theoretical* work is important, then certainly the applied researchers are
doing similarly impactful work. So let me give a quick, and by the nature of a
short article *totally* underappreciative, overview of the work done by theory
folks at MSR.

Let's start with Leslie Lamport. Since the early 70's Lamport has had a steady
stream of impressive algorithms and impossibility results in distributed
systems. His seminal paper on the ["bakery
algorithm"](http://research.microsoft.com/en-us/um/people/lamport/pubs/bakery.pdf)
gave a beautifully simple solution to the "semaphore problem" of multiple
processors corrupting shared memory, which improved over prior solutions by
adding fault tolerance and priority access. Things only get better from there.
Lamport invented [consensus
protocols](http://en.wikipedia.org/wiki/Paxos_(computer_science)) and the Paxos
algorithm, invented [Byzantine fault
tolerance](http://en.wikipedia.org/wiki/Byzantine_fault_tolerance), [logical
clocks] (http://en.wikipedia.org/wiki/Lamport_timestamps), and fantastically
impossible-sounding ways to [maintain global
state](http://en.wikipedia.org/wiki/Snapshot_algorithm) in a distributed system
that doesn't have global communication capabilities.

Leslie Lamport's research has **changed the way we think about distributed
computing** many times in his career, and at the ripe age of 73, he's still
going strong. For a better overview of his research than I can give here, see
[this blog post](http://brooker.co.za/blog/2014/03/30/lamport-pub.html).

Lamport may seem impressive (and he is!) but revolutionizing computer science
is par for the course at Microsoft Research SV. [Cynthia
Dwork](http://en.wikipedia.org/wiki/Cynthia_Dwork) has changed the discussion
around privacy, inventing a new way to make statistical information public
without compromising the identity of any individual in a database. She has
spearheaded the entire subfield of cryptography, known as [differential
privacy](http://en.wikipedia.org/wiki/Differential_privacy). This is not even
to mention all of her other impressive contributions to cryptography, including
the first [lattice-based
cryptosystem](http://en.wikipedia.org/wiki/Lattice-based_cryptography) paving
the way for [fully homomorphic
encryption](http://en.wikipedia.org/wiki/Homomorphic_encryption), and the ideas
that formed the basis of cryptocurrencies. Dwork's work on privacy is a
reaction to contemporary incidents of de-anonymization of medical and internet
data, so to imagine that these researchers are living in some abstract world
devoid of application is a fantasy. Dwork's work influences Microsoft's
products (and everyone else's) by changing the way we think about privacy.

And then there are people like Omer Reingold, who furthered the study of
space-efficient algorithms by solving a long-standing open problem about
undirected graph connectivity. He also changed the way we think about
randomness through his work on expander graphs, which has permeated science all
the way to [discussions](http://www.scottaaronson.com/blog/?p=1823) about the
physics and philosophy of consciousness. As if that weren't enough, Reingold
has made countless other contributions to cryptography and fault tolerance, and
he's just getting started! With so much impressive work under his belt, this is
what he had to say about his colleagues at MSR:

> In a place with no borders between research areas, I was free to follow my
> intellectual curiosity with colleagues I wouldn’t normally have the great
> fortune of working with. My non-theory colleagues have left me a much more
> complete computer scientist than I ever been. My theory colleagues left me in
> absolute awe! Being surrounded by the creativity and brilliance of a unique
> collection of young scientists was such a rush. I am confident that they will
> make many departments and research groups much better in the following months
> and years. My only regret is every free minute I didn’t spend learning from
> these wonderful colleagues and friends.

His [blog
post](http://windowsontheory.org/2014/09/19/farewell-microsoft-research-silicon-valley-lab/)
containing that quote is showered with comments by powerhouses of research all
lamenting the loss of the hub of innovation and science. 

There are just too many accomplished people to do justice to them all, but the
point is that Microsoft stands to lose more than just world-class researchers.
They stand to lose (and to some degree already lost) their image among
academics. Serious academic work needs stability, time, and collaboration, and
can't happen with only two out of the three. Important researchers are already
questioning the security of industry lab jobs.

[![williams-tweet.png](https://svbtleusercontent.com/kwseiqyamhzrfg_small.png)](https://svbtleusercontent.com/kwseiqyamhzrfg.png)

And this seems to be a trend across industry: big company gets a new CEO and
downsizes research. The interesting thing is that Microsoft could have
maintained face and stability by giving researchers a year's notice, enough
time to secure academic positions (which are notoriously slow to materialize).
Was the cost of keeping a relatively small research lab for one year really
worth the dent to their image? 

If the trend continues and industry research is no longer an obvious goal for
young researchers, and when the few good university slots fill up, where will
they go? And by they I mean *we,* because I will soon be forced to decide for
myself. Will we work abroad (I'm certainly considering that option), and weaken
the country's relative level of innovation? Politicians don't seem to like
that, but they won't increase science funding to compensate. Will we switch
careers, go into finance and potentially cause another economic meltdown? Or
waste our collective skill and talent designing iPhone games or CRUD apps? Or
worst of all go work for the NSA and undermine modern security? 

I can think of a few worthwhile endeavors specific to my interests (read: not
evil or selfish, and also with a reasonable salary), but I know a lot of PhD
students don't have such clear backups they can be enthusiastic about. They
would be much more likely to fall for the salary of Goldman Sachs or the
stability of the NSA instead of navigating the new frontiers of computer
science. Skeptics might say that's just how the market works, but chances are
that skeptic's job wouldn't exist if it weren't for the pioneers of computer
science. Innovation breeds better opportunities for everyone. Behind Snapchat
and Google are Fourier analysis and distributed networks. Behind Amazon is a
century of combinatorial optimization. Behind every banking and finance firm is
a mountain of cryptography keeping their secrets and clients safe.

Theory informs practice by mapping out what can and can't be done, and industry
labs have some of the best track records of producing great research. So when
Microsoft sends a message implying they don't care, they risk deterring talent,
but we all risk losing the fruits of the work great researchers might have done
at a hub like MSR Silicon Valley.
