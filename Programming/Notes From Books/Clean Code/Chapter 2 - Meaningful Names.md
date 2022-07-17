# Use Intention Revealing Names
* It takes time at start for proper names, but saves more time during lifespan of project.
* Should reveal purpose in name **NOT IN A COMMENT**
* It doesn't make the logic less complex, but increases the understandability to who is reading it.

# Avoid Disinformation
* Abbreviations that already exist can cause confusion if used.
* Calling something in a abstract way like list when it isn't is bad information.
* Names that look almost identical can cause problems.
* Inconsistant spelling and symbols that look like others can cause problems, better to rename

# Make meaningful Distinctions
* Having klasses to satisfy compiler leads to confusion.
* Number series naming is too abstract. a1, a2...
* Noise/Common used words leads to unintended assumption, make it clear uniquely when possible.
  * ProductInfo and ProductData mean the same even though that is not the intention.
* Variable names shouldn't have the type in the name, it should be obvious.
  * When would Name be a number?
  * Cases could occur where Customer and CustomerObject exists.
* Distinquishable names allow the reader to know the difference it offers.

# Use Pronounceable Names
* Can't discuss it outloud without sounding like an idiot.
  * Tolerating it can be funny when in on joke, but will give headaches for those not in on joke.

# Use Searchable Names
* Variable names with numbers or symbols can cause searchability through things like GREP difficulty.
* Longer names trump shorter names, and any searchable name trumps a constant in code.
* Bob's personal option is that single word variable names should exist with local variables in short methods
  * **The length of a name should correspond to the size of its scope.**

# Avoid Encodings
* Hungarian Notation: An identifier naming convention in computer programming, in which the name of a variable or function indicates its intention or kind, and in some dialects its type.
  * It serves no purpose in modern languages where typing is done by the compiler where programmers do not need a crutch to have the type of variable in the name.
    * The name won't be changed explicitly unless they change it when changing the type.
* Member Prefixes
  * IDEs handle coloring to make it obvious, no need in modern age to do m_variableBla.
* Interfaces and Implentations:
  * Using leading "I" will mark as interface but is unneeded and ruins abstraction on what you're giving the user.
    * (My personal view, against this belief)
* Avoid Mental Mapping
  * Using i,j,k as counters are traditional, but cause confusion when attempted outside of traditional conventions.
    * Use longer variable names for you to read, not the computer. **clarity is king**
* Class Names
  * Should be noun or noun phrase, should not be a verb.
* Method Names
  * Should be a verb or verb phrase.
  * Getters/Setters/is should be used accordingly.
  * Using static factory methods instead of overloaded constructors can give more clarity on params usages.
* Don't be Cute (Say what you mean. Mean what you say.)
  * If others aren't in on the joke, it won't be fun for them trying to understand the big picture.
    * whack should be kill, eatMyShorts should be abort, ect.
* Pick One Word per Concept
  * Use one word for something that retrieves instead of using all (fetch, retrieve, get) in different methods but similar logic.
    * Having controller/manager/driver in same codebase, what's the difference?
  * Function names should be able to stand alone on what they do, not have to rely on doc or param names.
  * A consistent lexicon is a great boon to the programmers who must use your code.
* Don't Pun
  * Avoid using the same word for two purposes. Using the same term for two different ideas is essentially a pun.
  * Don't use a word that doesn't do the intended intention.
    * Add should be used where there are multiple inputs and a output, not added to name for consistancy if the method doesn't do the first purpose (insert or append would be better).
  * KISS -> Keep it simple stupid
* Use Solution Domain Names
  * Domain names like for CS like "JobQueue" are OK, but shouldn't draw from the Problem Domain when possible when not needed as programmer may have to reach out with customer on questions.
* Use Problem Domain Names when Solution Domain Names Aren't Enough
  * At least the programmer who maintains your code can ask a domain expert what it means.
  * The code that has more to do with problem domain concepts should have names drawn from the problem domain.
* Add Meaningful Context
  * Refactor logic into meaningful helper method/classes can save headache than large/ambiguous methods.
  * Prefixes might be a good idea in scenarios where variables are overloaded with terms like "state" in both definitions.
* Don’t Add Gratuitous Context
  * Shorter names are generally better than longer ones, so long as they are clear. Add no more context to a name than is necessary.

# Final Words
* Not a easy skill, learned from experience.
* Should not feel ashamed when adding a commit to change a name, should be accepted with proper critique like any other code change.
* Refactoring tools are avaliable with your IDE, use them.