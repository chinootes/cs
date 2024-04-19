---
id: j8ia7hmunnn41deiodneeg2
title: Abstract Class as Stepping Stone
desc: ''
updated: 1708265430316
created: 1708263551868
---

## From my own experience

I once had to implement a scenario, where there are different kinds of resources or configurations all sharing a similar structure and behavior with a little difference in some fields. But mostly the functionality would be same for all these resources.

I went with abstract class as the base for these classes, since these were [[paradigm.oo.tags.same-same-but-different classes]].

Even though I was using [[arch.design.oo.use cases for.abstract class.providing flexible behavior for related classes]] and also [[arch.design.oo.use cases for.abstract class.helper]], a little. If I went with implementing a third class as a utility to be consumed in all these classes, I would have more useless code for initializing these objects and calling the methods instead of the logic. Hence, I decided to go with the Abstract class.

As the code and requirements evolved, I made the base class as concrete and more dynamic. I now only had to use a child class for very specific scenarios. But that might change too.

Sometimes on this journey towards perfection, [[philosophy.bad code can lead to good code]].

## Another beautiful excerpt from [Nigel Thorne's answer to How to Unit Test Abstract Classes?](https://stackoverflow.com/a/2947823/14318926)

>Update 2 : Abstract Classes as a stepping stone (2014/06/12)
>
>I had a situation the other day where I used abstract, so I'd like to explore why.
>
>We have a standard format for our configuration files. This particular tool has 3 configuration files all in that format. I wanted a strongly typed class for each setting file so, through dependency injection, a class could ask for the settings it cared about.
>
>I implemented this by having an abstract base class that knows how to parse the settings files formats and derived classes that exposed those same methods, but encapsulated the location of the settings file.
>
>I could have written a "SettingsFileParser" that the 3 classes wrapped, and then delegated through to the base class to expose the data access methods. I chose not to do this yet as it would lead to 3 derived classes with more delegation code in them than anything else.
>
>However... as this code evolves and the consumers of each of these settings classes become clearer. Each settings users will ask for some settings and transform them in some way (as settings are text they may wrap them in objects of convert them to numbers etc.). As this happens I will start to extract this logic into data manipulation methods and push them back onto the strongly typed settings classes. This will lead to a higher level interface for each set of settings, that is eventually no longer aware it's dealing with 'settings'.
>
>At this point the strongly typed settings classes will no longer need the "getter" methods that expose the underlying 'settings' implementation.
>
>At that point I would no longer want their public interface to include the settings accessor methods; so I will change this class to encapsulate a settings parser class instead of derive from it.
>
>The Abstract class is therefore: a way for me to avoid delegation code at the moment, and a marker in the code to remind me to change the design later. I may never get to it, so it may live a good while... only the code can tell.
>
>I find this to be true with any rule... like "no static methods" or "no private methods". They indicate a smell in the code... and that's good. It keeps you looking for the abstraction that you have missed... and lets you carry on providing value to your customer in the mean time.
>
>I imagine rules like this one defining a landscape, where maintainable code lives in the valleys. As you add new behaviour, it's like rain landing on your code. Initially you put it wherever it lands.. then you refactor to allow the forces of good design to push the behaviour around until it all ends up in the valleys.

## References

[Nigel Thorne's answer to How to Unit Test Abstract Classes?](https://stackoverflow.com/a/2947823/14318926)

