# Small

* Should be as small as possible, should be parts that lead to the next piece of logic soundly like a story.

# Blocks and Indenting

* If/Else/While statements should be one line long, having a function call for the logic gives meaning on what's happening.
* Functions shouldn't have nested structures?

# Do One Thing

* So, another way to know that a function is doing more than “one thing” is if you can extract another function from it with a name that is not merely a restatement of its implementation
* One Level of Abstraction per Function, move it to another function if levels of complexity are intermixed.

# Reading Code from Top to Bottom: The Stepdown Rule

* Functions should do one thing. Doing so they should be able to go through each abstraction like a step from a to b and so forth among each level of abstraction.

# Switch Statements

* My general rule for switch statements is that they can be tolerated if they appear only once, are used to create polymorphic objects, and are hidden behind an inheritance relationship so that the rest of the system can’t see them. This cannot always be done, but at least you can try to follow this principal.

# Use Descriptive Names

* The smaller and more focused a function is, the easier it is to choose a descriptive name.
* A long descriptive name is better than a short enigmatic name. A long descriptive name is better than a long descriptive comment.
* Take as long as you need to make/change, use one of those IDEs and experiment with different names until you find one that is as descriptive as you can make it.
* **BE CONSISTANT**, doing so will give you "Pretty much what you expected".

# Arguements

* One input argument is the next best thing to no arguments.
* The more you have, the more complex it is to test/understand.

# Common Monadic Forms (One Param)

* Single param functions that return a boolean based on param or transforms it into a value should be used in consistant context.
* Choose names that make distinction clear.
* Single param no return methods are "Events" to alter something, use with care with clear intention in naming.
* Avoid functions that don't follow these forms.

# Flag Arguments

* Passing a boolean into a funtion is bad as it implies that the true/false doesn't correspond to Single Responsibility.
  * Split into seperate methods if possible.

# Dyadic Functions (Two param)

* Has it's usages like with params that correspond to each other like coordinates, but try to stick to one param.

# Triads

* The issues of ordering, pausing, and ignoring are more than doubled when reading each param.

# Argument Objects

* Wraping params that fit together into own class simplifies complexities when reducing amount of code, and overall understanding relationship between parameters.

# Argument Lists

* **DO NOT MAKE METHODS MORE THAN THREE PARAMS**

# Verbs and Keywords

* Verb/Verb-Noun Pair for a mono param method is clear to reader on purpose.
* Keyword Form - Adding the names of arguments in function name mitigates issue with param order.

# Have No Side Effects

* Should do one thing, shouldn't modify the param unless that's the one thing. Checking a password should return a boolean, not do anything when it's true/false.
* If you must have temporal coupling, be explicit in the name of function "checkPasswordAndInitializeSession", but that violates the "Do one thing".

# Output Arguments

* Anything that forces you to check the function signature is equivalent to a double-take. It’s a cognitive break and should be avoided.
* In general output arguments should be avoided. If your function must change the state of something, have it change the state of its owning object.

# Command Query Separation

* Do not have a function that does something and returns if it actually did it, better to split it into a method that says if it can, and another that does it when it can.

# Prefer Exceptions to Returning Error Codes

* If you use exceptions instead of returned error codes, then the error processing code can be separated from the happy path code.

# Extract Try/Catch Blocks

* This provides a nice separation that makes the code easier to understand and modify.

# Error Handling Is One Thing

* Try should be the first line in a method that has a try/catch block and nothing else.

# The Error.java Dependency Magnet

* When you use exceptions rather than error codes, then new exceptions are derivatives of the exception class. They can be added without forcing any recompilation or redeployment.

# Don't Repeat Yourself

* It would appear that since the invention of the subroutine, innovations in software development have been an ongoing attempt to eliminate duplication from our source code.

# Structured Programming

* Edsger Dijkstra’s rules of structured programming: hould only be one return statement in a function, no break or continue statements in a loop, and never, ever, any goto statements.
  * This isn't beneficial with small functions, it is OK to have multiple return/break/continue to express than single entry/exit.

# How Do You Write Functions Like This?

* Functions start messy, and should be refactored to meet guidelines. They aren't written perfect from start.

# Conclusion

* Program is a system, Functions are the verbs of that language, and classes are the nouns.
* The art of programming is, and has always been, the art of language design.
* Master programmers think of systems as stories to be told rather than programs to be written.
* This chapter has been about the mechanics of writing functions well. If you follow the rules herein, your functions will be short, well named, and nicely organized. But never forget that your real goal is to tell the story of the system, and that the functions you write need to fit cleanly together into a clear and precise language to help you with that telling.