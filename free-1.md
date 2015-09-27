# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Trying to understand someone else's code&mdash;especially at a large scale&mdash;can be an intimidating, difficult, and overwhelming task,
even if the person trying to digest the code is an experienced programmer:
having to read and distinguish keywords in raw source code can be tiring, even if the code is well-commented.
Documentation can help this process, but words on a page aren't always the best way to express an idea.
To address this problem, I propose designing a language that translates code into flowcharts,
which would offer a more visually-appealing representation of code.
Not only would this solution help anyone (i.e., programmers and non-programmers alike) in understanding code,
but it could also reduce the effort necessary to produce 'good' documentation,
and (perhaps optimistically) force programmers to write more high level and well-commented/documented code.
One really cool potential result would be that people could use skeleton code in the language in which they intend to work
(and with which, therefore, they _are probably_, or at least _probably should_, be familiar)
to generate high level flowcharts that express the intended algorithm.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

1. The programmer will likely not want every implementation detail to leak into the flowcharts,
so there should be some way to indicate what _should_ appear on the flowcharts.

2. There should be as few barriers as possible to using this tool,
so I think allowing users to simply add code or annotations to the working code would be ideal.


### Why you?
_What excites you about this idea? How did you come up with it?_

I really like the idea of making algorithms represented in code more accessible.
I myself tend to favor and think in visualizations, and I think it would be a lot easier to explain code to someone
if I could easily transform my code into a flowchart. During my internship over the summer,
I wrote a document that details the design of my project, and in that document,
I created a flowchart to represent how I decided to handle one of the more complex parts of the project
because a flowchart seemed fitting for the task. I also think documentation is _super_ important,
so it's very appealing to me to create tools that ameliorate the documentation process
and compel others to put more effort toward it.


### Domain
_Describe the project's domain in five words._

Code Documentation and Visualization


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

Again, I'd like the code to feel as much like the underlying language as possible
so that there's not too much of a learning curve and to minimize the barriers
that might cause one to avoid using the tool. To that end,
my initial thoughts go to [Javadoc] annotations and [Doxygen] comments,
which use minimal indicators in the code to denote something.
I'm leaning toward comments for the syntax because I think they will be less offensive and confusing than a Java-style annotation.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, the marked up file is parsed, and one or more flowcharts are created based on the markings.
I think it would be really cool if users could interact with the generated flowcharts:
for instance, one of the blocks that indicates some sort of helper function
can be clicked to reveal the helper function's algorithm in the form of another flowchart.
If the proposed language is mostly text replacement, the synax _is_ based on comments,
and the flowchart structure largely comes from the code, then I don't foresee a need for very many errors;
however, I think errors _can_ be communicated on the command line.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to generate flowcharts that illustrate some code,
possible to generate the flowcharts without the actual code being written
and ideally to add comments to the flowcharts,
but pretty much impossible to do any sort of conventional computation.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

The first DSL in the domain that I found goes by [code2flow] and is designed to make flowchart creation easy;
however, the language is separate from any established language, so it doesn't suit my ideal.
Another language that is actually very on par with my idea is [Flowgen].
It's on GitHub, and it's even associated with a [paper][Flowgen Paper]!
Flowgen works for C++ and addresses the need pretty well.
For the most part, I really appreciate the syntax (It uses comments!);
however, it's not finished, the flowcharts aren't very pretty, I don't like how it does subroutine-linking,
and I'm not convinced the provided interface is as simple as it could be.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I'd say maybe 20-30% of their time would be spent on engaging in the language aspects. Some questions that remain to be answered:

* Should code structures be opt-in or opt-out in the flowchart?
..* Based on this decision, what does it look like to opt in or out, say, an `if` statement?
* What language should be used to generate the flowchart?
..* What effect do potential languages have on the processing logic?


### Scope
_How big an idea is this? How ambitious is this project?_

I think the idea has potential to grow, but I think one could successfully see multiple meaningful iterations
before the semester's end.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

**Benefits**
* Well-scoped
* Have to consider adapting the proposed DSL to the language for which it's designed (considering both this language's syntax and style)
* Have to consider complexity of flowchart creation language
* Potential to extend or modify an existing language

**Drawbacks**
* There is an existing, though incomplete, language that addresses the need fairly well.


[Javadoc]: https://en.wikipedia.org/wiki/Javadoc
[Doxygen]: https://en.wikipedia.org/wiki/Doxygen
[code2flow]: http://code2flow.com/
[Flowgen]: http://jlopezvi.github.io/Flowgen/index.html
[Flowgen Paper]: http://arxiv.org/pdf/1405.3240.pdf
