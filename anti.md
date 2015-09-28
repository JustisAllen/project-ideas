# Anti project


## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Some runners (and similarly cyclists, hikers, and swimmers) like to save routes so they don't have to memorize
each path (i.e., where to turn) and corresponding distance.
The ability to reference saved routes saves effort and brain power
and is particularly convenient when choosing a route based on distance.
Today, apps/sites like [Runkeeper] allow users to trace a route on a map,
and then the app/site saves the route and calculates the distance.
This method is a good solution to the problem, and I think an argument can be made that this route creation system is itself a DSL,
but I think a more traditional DSL with more conventional syntax would not be/have been an appropriate solution to the problem.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

I think a more traditional, 'human-readable' DSL would _not_ be appropriate because,
assuming the user is interfacing with a file rather than a map,
there would need to be some way to represent 'actual space' like streets;
but I'm not convinced that conventional syntax offers a natural and simple way to represent relational points in space.


### Why you?
_What excites you about this idea? How did you come up with it?_

I hit a 'running peak' last semester, and this semester I'd like to revisit and surpass that peak.
I'm not quite starting from scratch, but (especially since it's Summer still) I'm not ready to go out
and run as far as I was willing and able to last semester;
so I'm building up my mileage gradually. I'll often decide what distance I want to run before I start,
then browse my repository of routes, and choose one that matches the intended distance.
I was content with my experience in creating the routes,
but the perfectionist in me wished that the routes could be more precise
than a rough trace&mdash;hence I (briefly) considered a language.


### Domain
_Describe the project's domain in five words._

Route Mapping


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

In a more traditional DSL, the user might specify the points in space by giving coordinates or referring to actual street names,
though street names would limit the potential of the language;
however, neither of these options seem particularly good to me.
Coordinates seem too impersonal and devoid of meaning,
and while I recognize that we can give meaning to the coordinates by assigning them to named variables,
using several assignments in a file to enhance the meaning of the coordinates is much less than ideal&mdash;especially
considering that there will likely be variables that are only used in a single route.
Street names, on the other hand, would be more readable; my concern here
is that the user would have to be very precise and verbose
with the names of the streets to avoid conflicts in the case where there are multiple streets with the same name.
I'd imagine coding in such a rigid language would be irritating.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, the points in space are properly connected to form a route,
and an image of the connected route is produced along with the computed distance of the route. If the points have an order, there shouldn't be any issue in creating an image or computing the distance; but if the user only indicates a single point, that could be an error along with anything syntax-related, any of which can be communicated on the command line.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It _should_ be easy to create a route based on real locations,
ideally possible to map on non-street locations (i.e., mountain trails),
and impossible to perform any sort of conventional computation.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I mentioned [Runkeeper] above, and I'd guess there are probably some other route-mapping applications,
but I'd be surprised to learn that any of them use a traditional language schema. Runkeeper's application for saving routes works well: it basically let's you use a bunch of lines to form your route, which give you a good estimate of the distance and a good visually representation of the route. To address my perfectionist wants, they might add the ability to curve the lines to reflect the desired arc. (I also just realized that Runkeep uses [Mapbox] for its mapping application.)


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

If there is a decent, conventional, language-based solution, I think there would be a significant amount of time given to finding it and figuring out a friendly interface.


### Scope
_How big an idea is this? How ambitious is this project?_


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_


[Runkeeper]: https://runkeeper.com
[Mapbox]: https://www.mapbox.com/
