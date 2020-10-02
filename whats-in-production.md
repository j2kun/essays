# What is Actually Used?

2020-10-01

Everyone wants their work to be useful.
Being useful to others is a fundamental need of the human soul.
That often manifests as the need to _feel_ useful to others,
even if it is fulfilled only superficially.
Or worse,
one tries to accommodate pressure
to make their work seem useful
in ways that it isn't,
or to groups for whom it isn't,
because those ways of being useful are considered "better"
by someone in a position of power.
These manifestations are ultimately harmful.

This has implications for mathematics,
when we ask the question,
"What parts of mathematics have useful applications?"
(The mature version of "When are we ever going to use this?")
But first I want to talk about software,
and a simpler question, namely,
"What is in production right now?"

These days I write datacenter optimization software.
I collaborate on cross-cutting initiatives
with dozens of project managers and engineers daily.
In three years at my organization,
I've noticed a curious trend,
which I am certain is not special to my organization.
The trend is that
_almost everyone is misinformed_
about what features are in production,
and what features are useful and what are not.
They end up misleading me (and others),
and causing confusion that slows progress.

They do this often because they feel pressure.
There is not enough time to do all that needs doing.
If I'm not your manager,
you can say something is done to get me off your back.
They also seem to do this because
they don't want to acknowledge that past work was useless.
It's hurtful to say someone's work was better left undone.
I've seen multiple senior engineers leave
after it was clear the impact of their big project was worse than doing nothing.

One system I worked on
was part of a costly monthly business process.
Each month, new features were turned on and tested (not by me).
My component had a feature,
I'll call it Feature P.
In discussions with the owners of the end-to-end system,
I was told multiple times that Feature P
was turned on in production and had been for months.
Confusion followed, and I later
I checked the configuration files myself and saw
that the feature had never been turned on.
I later found out that the owners didn't want the feature.

This sort of event occurs
across my professional bubble.
I've heard all of the following unconditional claims that I later confirmed false:

- A dashboard currently works and is checked daily.
- A bug fix has been deployed to production.
- A system considers a particular input.
- An approach was tried and deemed to be unusable.
- A word has a commonly agreed definition.

In the end,
I fall back on ["trust, but verify."](https://en.wikipedia.org/wiki/Trust,_but_verify)

Another example that stands out to me
regards a machine learning system I annulled.
This particular system aimed to detect anomalies
in another system I worked on.
I was given a prototype,
and was told it was very important to productionize it.
The system had no baseline or labeled data,
which was a red flag,
but I started working on it anyway because of how important
I was told it was.
A teammate and I spent two quarters on it.
At the end, we determined the system
produced a 30% false positive rate and a 30% false negative rate (hundreds of alerts).
This is abysmal.
Then I dug in and found 2-3 bugs
by studying major _false negatives,_
spent about a week fixing them,
and eliminated the underlying problems
that spurred the original suggestion to do anomaly detection.
In the end, I removed the anomaly detector.

This experience is relevant,
because over a year later
a higher-up manager called out this project
as a great success in applying machine learning in our org.
This manager had presumably only seen
the original engineer's presentation on their prototype,
and had no idea it was actually a waste of 1+ engineer-years.
The manager probably also wanted
to make the effort feel valued, and inspire people.
Though it comes from a good heart,
it was counterproductive.
It's only by acknowledging, studying,
and remembering failure
that we can learn from it.
The first step is knowing what succeeded and what didn't
after the fanfare of the first release.

There's an adage whose eponym I can't remember, like,
"If a biologist finds news coverage of biology
full of factual errors,
then why would they trust
news coverage of unfamiliar topics, like economics?"
If I can't trust people in my insular organization
to tell me what's in production,
how can I trust mathematicians
to tell me what mathematics is used in production?
How can I trust them to be honest about success and failure?

I've been thinking about this a lot recently.
As a graduate student,
I was often led astray by research papers and books that
described a particular concept as unquestionably useful in the real world,
only to find it was not used at all,
or it was not as useful as claimed.
It also doesn't help that "application"
can mean very different things to different people.
To a normal person, it means that you can
use it to solve a problem humans have in the real world,
or apply it to creative pursuits.
To many in math, it means applicable to solve other,
purely theoretical problems.
Too often it really means, "look, citations!"
Perhaps we need a different word for
"widely applicable,
but only to writing yet more research papers."
Maybe academics would feel better if they had a Latin phrase
like "applicable _in contemplatio_,"
versus "applicable _in res_."

This bothers me when theory meets practice,
because every theory paper
within spitting distance of applications
reads like the manager praising the failed anomaly detector.
Everything is described as profoundly useful.
Doubtlessly this is intended to draw in PhD students,
funding from grants requiring such lip service,
and worst of all, funding for startups.
But real knowledge about a method's practical merits
is crucial when planning what to build.

Though I have experienced this dozens of times on smaller scales, here are three examples of math topics which,
in my experience, have fallen short of their advertising,
though the last one is a juicy "so far."

The first is [semidefinite programming (SDP)](https://en.wikipedia.org/wiki/Semidefinite_programming).
I read a ton about SDP in graduate school.
It's a strict generalization of linear programming (which _is_ widely applicable)
allowing some special nonlinear constraints,
but is still efficiently solvable.
The major theoretical breakthrough is a better [approximation
algorithm for the max-cut problem](https://en.wikipedia.org/wiki/Maximum_cut#Approximation_algorithms).[^maxcut]
There are plenty of famous researchers
[singing the praises](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-251j-introduction-to-mathematical-programming-fall-2009/readings/MIT6_251JF09_SDP.pdf)
of SDP.

> Semidefinite programming (SDP) is the most exciting development in
> mathematical programming in the 1990’s. SDP has applications in such diverse
> fields as traditional convex constrained optimization, control theory, and
> combinatorial optimization. Because SDP is solvable via interior point
> methods, most of these applications can usually be solved very efficiently in
> practice as well as in theory.

However, in a conversation with a few experts in applied optimization,
it seems there are few (if any) known application domains
where SDP is better than alternatives.
One expert told me that
he hasn't heard of a single realistic application,
and that everyone who claims to do SDP in practice
"secretly linearizes" behind the scenes.[^linearize]
Other experts could at best point me
to a few research papers about robotics controllers,
but those in the robotics limelight today
seem to be completely ignoring SDP
in favor of ML and RL-based approaches.

A second example is [topological data analysis (TDA)](https://en.wikipedia.org/wiki/Topological_data_analysis).
I spent a year studying this as a graduate student,
and I was bolstered by the fact
that a real software company, [Ayasdi](https://www.ayasdi.com/),
headlined it as their secret sauce.
I even called them about an internship.
Ayasdi was founded by [Gunnar Carlsson](https://en.wikipedia.org/wiki/Gunnar_Carlsson),
who ran a research group at Stanford on TDA.
I studied their flagship TDA algorithm,
"persistent homology,"
which purportedly allows you to say tantalizing things like,
"The manifold underlying financial data is topologically a Klein bottle!!"

I implemented it and applied it to a bunch of datasets.
It provided no information.
I studied their papers
that purportedly showed persistence homology vanquishing real problems.
Ultimately, I realized that
these TDA techniques are not very useful.
Most of the "success" was that,
after some feature engineering,
and dubious squinting at the TDA output,
you fall back on standard mathematical
and statistical modeling.
The degree to which TDA enables one
to come up with a better model is unclear.
And without validation, the claims about TDA are circular.
This [Ayasdi article about Trump](https://www.ayasdi.com/the-secret-of-his-success-how-topological-data-analysis-provides-a-glimpse-into-what-may-be-powering-the-trump-engine/) demonstrates this.
And anyway,
the "TDA" in that article is clustering principal components.
Old moves, new name.

Despite their claims that TDA has
"taken the data science world by storm,"
it seems that TDA is just one step of a pipeline
that uses a lot of standard techniques.
Ayasdi's [featured white paper](https://www.ayasdi.com/wp-content/uploads/2020/08/ALM-and-Liquidity-Final.pdf)
is full of technobabble that reinforces this,
and adds more red flags,
such as claims
(which occur throughout Ayasdi's literature)
that TDA computes all possible model features
and all model transformations at once.
Some of their other [materials](https://www.ayasdi.com/resources/from-5-to-13-redefining-the-positions-in-basketball/)
confirm that step one is still feature engineering,
the sauce is clustering,
and the topological algorithms in the literature (persistence, zig-zags, etc.)
are either not exposed, or (my hunch) not used.

The claims about
"eliminating the need for feature engineering"
are particularly triggering.
See, clustering is a horrendously underspecified problem space.
The world is full of clustering algorithms,
and you can often pick a clustering algorithm that gives you
the output you want.
In other words, clustering is model selection,
whether you acknowledge it or not.
Shai Ben-David has some excellent papers on this topic,
with [this survey](https://arxiv.org/abs/1805.08838) being (as I understand it)
his last paper before "giving up" because he decided it's hopeless
for practitioners to take model selection seriously.
Sloppy clustering was the same problem
plaguing the anomaly detection system I described earlier,
so my practical experience agrees.

A third example is [SAT](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem) solvers.
For those who don't know, a SAT solver is a black box
for determining whether a boolean formula can be satisfied
by some assignment of variables to truth values.
If you listen to researchers on this one,
you might think that every hard problem in computer science
falls before the might of the SAT hammer.
Donald Knuth even writes,

> The SAT problem is evidently a killer app, because
> it is key to the solution of so many other problems.

After hearing about how Marijn Heule
[wants to solve the Collatz Conjecture](https://www.quantamagazine.org/can-computers-solve-the-collatz-conjecture-20200826/)
using SAT solvers, I was reminded anew of
the wide claims of SAT's applicability,
and now that I am more skeptical of such claims I posted
[a twitter thread](https://twitter.com/jeremyjkun/status/1303057920419004416)
asking for examples.
It elicited a large response.

I had always heard SAT solvers are actively used
in the design of circuits, and I believe it.
That thread convinced me there is a wider variety of problems
that SAT solvers are used for than I thought,
and they also informed me of a generalization to SAT called
Satisfiability Modulo Theories (SMT),
that is apparently much more useful than vanilla SAT.

One tidy application, which would make a great longer blog post,
is how the problem of choosing versions for software dependencies
reduces to SAT.
Specifically, if software follows [semver](https://semver.org/),
and if your requirements can specify ranges of allowable versions
(e.g., `>= 2.0.4` or `<= 5.6.0`) for each dependency (and each dependency
specifies its own version requirements),
then you can set up a SAT solver to decide what versions work,
or it may report there is no legal installation
due to inconsistent requirements.
The caveat here is that this is often slow.
Though many package managers use SAT today,
the Go programming language took what I think is a magnificent approach.
In this [series of articles](https://research.swtch.com/vgo),
they study the dependency resolution problem in depth,
they morally _indict_ versioning systems
for needing something as complex as a SAT solver to function,
and then they redesign so as not to need SAT. Jump to
[this article](https://research.swtch.com/vgo-mvs), section "Theory",
for the mathematical punchline.
To me, this is an inspiring victory for good design principles.
It also emphasizes that,
while a math topic can have an application,
it might be better off not to exercise it.
Something about a tree falling in a forest.

There was another fascinating application of SAT pointed out to me,
which was the design of [physical lock-and-key systems](https://codingnest.com/modern-sat-solvers-fast-neat-and-underused-part-2-of-n/),
where some keys can open more locks than others.
Imagine a building where employees can only open their office doors,
but janitorial staff can open everyone's doors, etc.
The requirements of such a scheme
on the shape of the locks and keys
can apparently be translated into SAT.
I found a [Github project](https://github.com/master-keying/mks)
that implements this.
I emailed the author, and he suggested that,
indeed, industrial key companies use SAT-based techniques,
and he pointed me to his [dissertation](https://github.com/cernoch/mks-dis/blob/master/LockChartSolvingWeb.pdf),
which I haven't read in detail.

Many people also reported SAT/SMT applications in security and reverse engineering,
such as this [blog post](https://0xec.blogspot.com/2016/04/reversing-petya-ransomware-with.html)
that cracks a bitcoin ransomware.
And many PL-type folks made me question my sanity,
because apparently everyone uses SAT/SMT for software verification,
automated test generation (I'm suspicious of this one),[^unit]
automated code writing ("synthesis"),[^synthesis]
and automated bug detection,
none of which I had ever seen done in a practical setting at scale.
One that seems very close is a formally-verified voting system [ElectionGuard](https://blogs.microsoft.com/on-the-issues/2020/02/17/wisconsin-electionguard-polls/)
that was used in a local Wisconsin school board election
alongside paper ballots
(disclaimer: a friend of mine worked on ElectionGuard).
Sydney Gibson also [claims](https://twitter.com/sydgibs/status/1303159907118710784)
that most of the HTTPS stack was verified using SMT in a language that compiles to C,
and that the verified implementation is in Firefox in production. I would love to hear from anyone who can confirm this.

The parts of mathematics that inspire me most
rely on the tight exchange of ideas between theory and practice.
When mathematicians oversell their work,
either for reasons coming from the soul,
or cruder demands for attention or profit,
the relationship between theory and practice is corrupted.
Trust is betrayed, and made harder to rebuild.
While I won't give up on mathematics any time soon,
my relationship with _academic_ mathematics is tarnished.
The benefit of the doubt is gone.
I feel jaded and disaffected.
I hope that will pass some day.

P.S. I also wanted to talk about category theory
as an example of a misleadingly advertised topic,
but this article was getting too long.
Let me know if you want to hear my thoughts on that.

[^maxcut]: I have not heard of a convincing application of max-cut to a
  real-world problem.

[^linearize]: I wasn't quite sure what he meant by this, whether they are
  duplicitous or honest in their digression from
  what is supposed to be the key feature of SDP.

[^unit]: You'd think if you could automatically generate high-quality tests for
  Java, Google (which employs literally thousands of engineers writing Java all
  day) would evangelize the hell out of it and save millions of dollars per
  year.

[^synthesis]: I saw a [promising graphics
  demo](https://www.anishathalye.com/2019/12/12/constraint-based-graphic-design/)
  on this by Anish Athalye, though his claim that it's much easier than TikZ is
  probably because he wrote it. Every tool you build yourself seems easy to use.
