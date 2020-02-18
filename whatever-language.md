# Whatever Programming Langauge You're Using is Fine, Really.

The title for this post was inspired by [Vicki
Boykis](https://twitter.com/vboykis/status/971538313831165952).

Back in the late 2000's I was given a programming assignment to implement a
simple website and database from scratch. It was a basic blog in raw HTML,
which let you compose and publish articles. The server would store the content,
automatically add dates and author tags, and display them on the front page.
The assignment could be written in any language you wished. I cheekily chose
perl, a language often derided as so obfuscated that there's no point in having
an "obfuscated Perl" contest. The perl used a module that implemented CGI.
Essentially, the website was composed of glorified shell scripts.

To my surprise, my profressor displayed my project submission as exemplary.
Other students, many of whom chose to implement their projects in Java or C++,
remarked, "How did you make it so simple? I thought Perl was supposed to be
confusing!"

The answer is discipline. I used as few of Perl's confusing features as
possible, and kept my code simple. All it did was keep track of filepaths,
template content into html strings, and parse dictionaries from requests.  I
apply similar types of discipline in my current job using Java. I tightly
restrict my use of generics. I prefer to created named interfaces for concepts
rather than introduce long and arduous type signatures. I use AutoValue to
compensate for Java having no concept of an immutable dataclass. I limit the
craziness of my project's dependency injection graph so that each engineer can
keep it in their head.

Programs are complicated because we don't put in the time to make them simple.
It's important to make things simple because simple things last for a long
time. The more I build and maintain, the more I'm convinced that what matters
most is discipline, simplicity, and investing in the tools to make it easy to
uphold those.

Here are some principles I try to abide by, which have been told to me, or
discovered myself, or cobbled together from what I've read.

- When you start to get confused, pause and reflect on the underlying source of
  your confusion. Redesign or refactor the code so as to eliminate the
  confusion.
- In the face of a confusing use of a language feature, think about how to
  implement it if the feature did not exist. Often it will be very little extra
  work to do away with the use of that feature.
- If you don't understand why something was done a certain way, don't assume it
  was for a good reason. Ask, and challenge yourself to think of a better way.
- Do not be afraid to repeat yourself once or twice. Only think about
  abstraction and generalization once the repetition becomes a source of
  problems.
- Simple, but repeated things are better than complex brief things.  We have
  thousands of tools for searching, sorting, and filtering through simple
  repetitious things, and zero tools for automatically enlightening ourselves
  about arbitrarily complex things.
- Learn to use those tools for managing repeated simple things! Since this is
  almost always text, learn to use the bazillion tools that exists for munging
  text. Install a snippet generator so you don't have to type boilerplate.
  Learn to apply regular expressions over your codebase.
- Instill in your team the virtue of simplicity.
