I've pasted in most of the codebase, so you can have a good look at it and figure out how to design things.  your mission is to take what I've written above and think hard about how to approach it. 
At this phase we're not settling on a single design, we're looking at our choices. so enumerate all of the real questions/decisions, and for each one make a list of options, and then identify huhs+pros+cons of each option, and then, based on weighing the tradeoffs, give a recommendation? (or two recommendations like "if X do Y, if not-X do Z")





I feel like there are a few other choices we missed though.  can you highlight them and do the same pros/cons process?





and also ask me any further questions I should answer before I have you generate a megaprompt to see if we can get a coder LLM to implement a bunch of this at once.






we're going to implement this on multiple branches:
1.  
2.  

and have one instance each of claude code or cursor plug away at each of those.

So: write both of those prompts. be VERY detailed, highlighting each design choice. only what you write below will be shared with the coder LLM, so make sure to include everything it will need, and copy/quote any sections that it needs to have verbatim.  and they don't have any of the context that you have (except they can look at the codebase).

where there's stuff that is at the interface between the two, you should figure out right now what it should look like so you can tell each half how to implement its end.


maybe add something to the effect of ""




something about TDD, about generating the list of test-cases
