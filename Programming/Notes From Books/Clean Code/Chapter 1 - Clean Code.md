# There will be Code
* Code/Programmers won't disappear, code represents details of requirements that the machine can execute. Vague guidelines a machine/human cannot understand well enough to solve actual problem at hand.
  * But we will never eliminate necessary precision—so there will always be code.

# Bad Code
* A great company can quickly fall due to a poor code foundation that leads to a snowball effect of added features that caused more problems.
* Wading: Impeded by bad code, going through bad code and wasting time trying to understand it.
* Later Equals Never: Do it right the first time or it will never be done, and that small problem will become a bigger one.

# The Total Cost of Owning a Mess
* Productivity will drop due to bugs, and more messes will occur that will cause the system to be unrepairable.

# The Grand Redesign in the Sky
* The wish for refactoring the project may happen, but by the time it's finished by the Tiger team original members may've left, the original problem may not have been solved, and the application may need a Tiger team for itself.

# Attitude
* Don't point the finger at others, take responsability for not doing it right when it was possible for you to.
  * A Doctor should say NO to a patient who demands them to operate without washing their hands when they believe it's silly.
  * So too it is unprofessional for programmers to bend to the will of managers who don’t understand the risks of making messes.

# Fun Fact
* When hand-washing was first recommended to physicians by Ignaz Semmelweis in 1847, it was rejected on the basis that doctors were too busy and wouldn’t have time to wash their hands between patient visits.

# The Primal Cunundrum
* You will not make a deadline by going fast, you will make mistakes that slow you down.
* Keep Code as clean as possible at all times.
  * Slow and steady wins the race.

# The Art of Clean Code
* It's a skill that is learned through trial and failure, a book on art can teach you how to teach yourself through practice similar to how one writes clean code.
* Code-Sense allows an experienced programer to look at a messy module and see options/variations to make a bad module behave as it should in a clean way, defeating the mess.

# What is Clean Code?
* **Bjarne Stroustrup**, inventor of C++ and author of The C++ Programming Language:
  * Elegant - Pleasing to Read
  * Logic Stright forward where bugs are hard to hide
  * Dependencies Minimal to Maintain Easier
  * Error Handlinng used Accordingly
  * Performance close to Optional
    * Make Clean Code more enticing than those who want to do bad code practices that will cause bad performance due to it.
    * A house with broken windows shows someone doesn't care, others will not care as well; causing the house to detariate by everyone, all due to one initial broken window.
      * http://www.pragmaticprogrammer.com/booksellers/2004-12.html
  * Clean Code Does One Thing Well
    * Single Responsibility is a Core Tenant in Software Engineering for a reason.
    * Clean Code is focused, Bad Code tries to much and muddies it's pure intentions.
* **Grady Booch**, author of Object Oriented Analysis and Design with Applications
  * Clean code is simple and direct. Clean code reads like well-written prose. Clean code never obscures the designer’s intent but rather is full of crisp abstractions and straightforward lines of control.
    * Clean Code should be easy readable where you are looking at logic of what's being done rather than syntax.
    * Clean Code carry only necessary detail, not speculative.
* “Big” **Dave Thomas**, founder of OTI, godfather of the Eclipse strategy
    * Clean code can be read, and enhanced by a developer other than its original author. It has unit and acceptance tests. It has meaningful names. It provides one way rather than many ways for doing one thing. It has minimal dependencies, which are explicitly defined, and provides a clear and minimal API. Code should be literate since depending on the language, not all necessary information can be expressed clearly in code alone.
      * Others should be able to read it as well as the original author.
      * Code without tests is not clean.
      * Smaller is better, keep complexities as small as possible.
      * Readable for Humans not just Computers
* **Michael Feathers**, author of Working Effectively with Legacy Code
    * I could list all of the qualities that I notice in clean code, but there is one overarching quality that leads to all of them. Clean code always looks like it was written by someone who cares. There is nothing obvious that you can do to make it better. All of those things were thought about by the code’s author, and if you try to imagine improvements, you’re led back to where you are, sitting in appreciation of the code someone left for you—code left by someone who cares deeply about the craft.
      * Clean code is code that has been taken care of. Someone has taken the time to keep it simple and orderly. They have paid appropriate attention to details. They have cared.
* **Ron Jeffries**, author of Extreme Programming Installed and Extreme Programming Adventures in C#
  * Runs all the tests
  * Contains no duplication
    * If done over and over, than the idea is not well represented and can be expressed clearly in fewer places.
  * Expresses all the design ideas that are in the system
    * Meaningful names, they take time and often change to better represent
    * Object/Method should do one thing, it's easy with modern IDEs to extract in one method that says more what it does and submethods on how it's done.
  * Minimizes the number of entities such as classes, methods, functions, and the like
  * Abstractions are better than Implementations, Can change the actual Implementation any time you want/need to for performance or other reasons.
    * Keep from knowing unnecessary details where all you need is a black box approach to solve your problem.
  * Reduced duplication, high expressiveness, and early building of simple abstractions. That’s what makes clean code for me.
* **Ward Cunningham**, inventor of Wiki, inventor of Fit, coinventor of eXtreme Programming. Motive force behind Design Patterns. Smalltalk and OO thought leader. The godfather of all those who care about code.
  * You know you are working on clean code when each routine you read turns out to be pretty much what you expected. You can call it beautiful code when the code also makes it look like the language was made for the problem.
    * Code should be as straight forward as possible. The designer makes it look ridiculously simple like all exceptional designs.
    * Languages weren't designed for our problems, but beautiful code makes the language look like it was made for the problem. So it’s our responsibility to make the language look simple! Language bigots everywhere, beware! It is not the language that makes programs appear simple. It is the programmer that make the language appear simple!

# We are Authors
* Authors are responsible for communicating well with their readers. The next time you write a line of code, remember you are an author, writing for readers who will judge your effort.
* We often read code at a 10:1 ratio than writing new code, make it easier to read so it's easier to write.
* Make it easier to read so you can go fast in the future when you're reading your old code, or others are.
* The code you write today will be easier if the surrounding code is easy to read.

# Schools of Thought
* Not a universal definition on what Clean Code is, but similar to schools of martial arts there are similar beliefs on what the definition includes and no practice in clean code/martial art is universally right.

# Boy Scout Rule
* Leave the campground cleaner than you found it.
* A little change over time goes a long way, continous improvement is an intrinsic part of professionalism.

# Conclusion
* Experience/Practice/Trial and Error is the true teacher.
* Remember the old joke about the concert violinist who got lost on his way to a performance? He stopped an old man on the corner and asked him how to get to Carnegie Hall. The old man looked at the violinist and the violin tucked under his arm, and said: “Practice, son. Practice!”