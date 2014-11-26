Three Things are Hard in IT
===========================

Throughout my two years in the software engineering industry, I've come to understand that there are just some things, which always will be hard in IT.

# Naming

When developing, I usually get an idea that I need a specific component/class/system/variable to do some job for me. I start getting a pretty good picture in my head of what it should do, which other components that should depend on it, and which components that the new component should consume. However I don’t know what to call it.  
In this situation, usually one of the following applies:

1. My idea sucks, because my unnamed component is supposed to do multiple things. This is bad because it violates the single responsibility principle. Don’t know it? Google it.
2. I am not realizing that my unnamed component is actually just a part of an existing, well-defined programming pattern. Potentially because I am not aware of the pattern. In these cases factories could become “creators”/”generators”/”initializers” and singletons might become “managers”/“handlers” and whatnot.
3. Least likely: I just invented a whole new programming pattern, and therefore naming is, justifiably, hard.

Putting it in other words: my idea probably sucks, or my knowledge/experience is lacking.

# Caching

The only reason to use a cache in front of a system is because of insufficient resources in that system. Hence a cache is a workaround of the real problem: insufficient resources. And workarounds are bad. But we keep using them. </rant>  
The main reason caching is hard is because of the nature of caching. Caches should be transparent. The consumer should  (usually) not experience any different behaviour because of the cache. Herein lies the fundamental problem.

# Remembering

When I first started to talk about the three hard things in IT the third thing wasn't remembering, but as I simply cannot remember what it was I've finally decided that remembering itself must be the third.  
AFAIK most people spend much time re-reading code - including code which we have written ourselves. What if we simply could remember what we wrote? We can’t. Because remembering code is, and probably always will be, hard.
