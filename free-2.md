# Free project 2


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Sometimes people want to download all of a certain type of content from a webpage
(e.g., pictures for storage, or text to analyze word frequency),
but there doesn't seem to be a simple way to retrieve these data.
I'm not really certain who would want to download web content in this fashion,
but I think researchers and tech-savvy people might be interested in doing it from time to time.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A language seems appropriate so that users can specify what content to download (e.g., only images, text, or links).


### Why you?
_What excites you about this idea? How did you come up with it?_

I'm honestly not nearly as excited about this idea as the other one,
but I definitely think that this is something that should be fairly easy for people to do,
and&mdash;maybe my googling skills just aren't up to par, and admittedly I didn't try _too_ hard,
but&mdash;I'm amazed that I didn't find anything that seems to serve this purpose.
My friend Savannah gave me this idea; she mentioned that it seems really complicated to download
specific elements of a webpage.


### Domain
_Describe the project's domain in five words._

Web Content Selection and Download


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

I believe [jQuery] is a popular library that already provides a simple platform for selecting specific web content
(and if I'm not mistaken, the realm of web content selection is fairly big).
Since there is already an existing framework for content selection,
we probably don't want to reinvent the wheel for that portion of the language specification,
but instead build upon it to allow the user to download the selected content to a file.
As [Downloadify] does, it might be sufficient to simply add a `download` method
and include some way to specify a file name and destination.
But in essence, it seems like making the language an extension of something like jQuery
might be best to utilize a pre-existing content selection language.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, the computer looks up the specified web page(s),
and downloads the specified content to a file. The downloaded content would probably be static,
so the user probably couldn't interact with it besides viewing it
or putting it through some other program to process it.
Errors might occur if there's a bad internet connection
or if the desired webpage does not exist. I think the errors can be communicated on the command line,
but it might be beneficial to have the errors in the file where the content is expected to be.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to download specific content from a website,
possible to download an entire website, and impossible to perform any sort of conventional computation.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

As I mentioned above, I believe [jQuery] and some other languages handle web content selection,
but jQuery doesn't seem to support saving the content to a file.
[Downloadify] seems to support some sort of downloading in combination with jQuery,
but either it doesn't provide the functionality I've described,
or the requirements or implementation is much different than I think it should be
to cleanly solve the proposed problem&mdash;though, as I mentioned, the syntax seems fairly nice.
I would think it does, but I also don't know whether jQuery supports selection across an entire website,
which I think is a feature the proposed language should have.


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Since I'd think most of the work goes into the selector,
I don't think the downloading feature would require very much implementation;
so I'd say ~20% of the time would be spent engaging in the language aspects.


### Scope
_How big an idea is this? How ambitious is this project?_

The idea doesn't seem too big or ambitious, so I think it's reasonable to expect completion
of the project along with a moderate amount of attention given to error and warning messages.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

**Benefits**
* Seems reasonable to expect completion by the semester's end, which allows time to develop a well-rounded yet brief language

**Drawbacks**
* Small language likely means that not a lot of tradeoffs will be considered.


[jQuery]: https://en.wikipedia.org/wiki/JQuery
[Downloadify]: https://github.com/dcneiner/Downloadify
