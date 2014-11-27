Three Things are Hard in IT
===========================

Throughout my two years in the software engineering industry, I've come to understand that there are just some things, which always will be hard in IT.

1. Naming
2. Caching
3. Remembering

# Naming

When developing, I usually get an idea that I need a specific component/class/system/variable to do some job for me. I start getting a pretty good picture in my head of what it should do, which other components that should depend on it, and which components that the new component should consume. However I don’t know what to call it.  
In this situation, usually one of the following applies:

1. My idea sucks, because my unnamed component is supposed to do multiple things. This is bad because it violates the single responsibility principle. Don’t know it? Google it.
2. I am not realizing that my unnamed component is actually just a part of an existing, well-defined programming pattern. Potentially because I am not aware of the pattern. In these cases factories could become “creators”/”generators”/”initializers” and singletons might become “managers”/“handlers” and whatnot.
3. Least likely: I just invented a whole new programming pattern, and therefore naming is, justifiably, hard.

Putting it in other words: my idea probably sucks, or my knowledge of patterns is lacking.

# Caching

The only reason to use a cache in front of a system is because of insufficient resources in that system. Hence a cache is a workaround of the real problem: insufficient resources. And workarounds are bad. But we keep using them. \</rant\>

The main reason caching is hard is because of the nature of caching. Caches should be transparent. The consumer should, ideally, not experience any different behaviour because of the cache. Herein lies the fundamental problem.  
We have to decide at least:

* If not all, then which resources should be cached
* for how long

These two things sounds incredibly easy to answer, but it quickly becomes hard as soon as I start to think about the consumers of the system. What kind of use-cases will they have? Do they need "real-time" data? How many consumers will there be simultaneously?  
Boiling it down, configuring a cache is a process of guesstimating how much performance is needed. Not only now, but also in the future.

The next set of problems are those for the consumer. Since the cache should be transparent, the developer who is implementing the consumer might (most likely) not realize that the system is cached. Is this really a problem, you might ask, since the cache shouldn’t change the behaviour of the system? It might be, because the consumer might need to use the system in ways which the developer of the cached system did not intend for. Therefore assumptions which the developer who implemented the cache made might not be valid anymore. That is the real problem.  
The developer who is implementing the consumer might start to dig in the code of the cached system, searching for bugs which he thinks must exist, simply because he is using the system in ways which the developers of the cached systems couldn’t have foreseen would be needed.

To put it bluntly: caching only works if good assumptions are made. And assumptions are the mother of all screwups.

# Remembering

When I first started to talk about the three hard things in IT the third thing wasn't remembering, but as I simply cannot remember what it was (and all good things comes in threes) I've decided that remembering itself must be the third.  
AFAIK most people spend much time re-reading code - including code which we have written ourselves. What if we simply could remember what we wrote? We can’t. Because remembering code is, and probably always will be, hard.


