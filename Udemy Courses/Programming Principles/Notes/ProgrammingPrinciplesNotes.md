# There *are only two hard things in Computer Science*: cache invalidation and naming things. -- Phil Karlton

* ## Cache Invalidation
  
  * Try to limit as much as possible.
  
  * Favor computation rather than caching the value.

* ## Naming Things:
  
  * Long variable names are good if they properly explain what the thing does.
  
  * Methods should be verbs.
  
  * Classes should be nouns.
  
  * Stay away from namings like "manager" to instead of something like "player".
  
  * Ask for a second opinion when needed, the name may be obvious from a outside perspective.

# Spaghetti Code

* **Definition:** Code that is coupled with other pieces of code, one change could cause unrelated changes that should be mutually exclusive.
  
  * Code should have as little coupling as possible, only view what is needed.
  
  * Changes to other code should be minor if they happen rather than drastic.

* **DO NOTS:**
  
  * Static Variables / Global State: Can cause al instances to be affected since it's not bound to a single instance.
    
    * If it's constant, that's not a issue.
    
    * It causes bugs since if it's public it could be modified by outside code.
    
    * Poor Unit Testability.
    
    * Code Comprehension, the proper usages of the variable during the present and in the future usage.
    
    * Multitreading
    
    * When you need two or more of it

* High Cohesion / Loose Coupling:
  
  * You should have the elements of a class be limited to itself (i.e. eveything in a class relies on outside references as much as possible in favor of logic in its own class)
    
    * ```cs
      public class HighCohesionCharacter : MonoBehaviour, IAttackable
      {
          [SerializeField] Animator animator;
          [SerializeField] AudioSource audioSource;
          [SerializeField] AudioClip shout;
          float health = 100f;
      
          public void TakeHit()
          {
              animator.SetTrigger("KnockBack");
              audioSource.PlayOneShot(shout);
              health -= 10;
          }
      
      }
      ```
      
      ```
      
      ```

* You should have as few outside references / coupling to outside code as changes in one will cause other changes in other code/logic to be explicitly or implicilty changed.
  
  * ```cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;
    
    public class LooselyCoupledEnemy : MonoBehaviour
    {
        public void Attack(IAttackable target)
        {
            target.TakeHit();
        }
    }
    
    public interface IAttackable
    {
        void TakeHit();
    }
    ```

# Composition over Inheritance

* Not a hard rule to disregard inheritance, but try to use as little as possible.

* Composition allows more freedoms on how classes can be implemented.

* Inheritance forces all descendants to possibly have logic that it doesn't need or has to override.

# Law of Demeter

* Definition: Principle of least knowledge, classes should have to talk to immediate classes. 
  
  * You only ask for objects you directly need to operate on.
    
    * ```cs
      # Bad
      enemy.GetCurrentTarget().GetHealthComponent().DoDamage();
      # Good
      enemy.DoDamageToCurrentTarget();
      ```
  
  * A friend of a friend is a stranger.

# 10 Coding Commandments

1. Thy code shall read like English without comments.

2. Thou shalt take the time to name things well.

3. Thy classes shall do one thing (and functions too).

4. Thou shalt use as little state as possible.

5. Thou shalt not refactor before the 3rd repetition.

6. Thou shalt not use Static and Global State.

7. Thy classes shall be Highly Cohesive.

8. Thy classes shall be Loosely Coupled.

9. Thou shalt use Composition over Inheritance.

10. Thou shalt follow the Law of Demeter.

# Solid Principles

* **Single Responsibility Principle** - A class should only have one reason to change.

* **Open-Closed Principle** - "Open for extension, but closed for modification"
  
  * Interfaces, Abstract Classes
  
  * Usage: Strategy Pattern (Change on Runtime)

* **Liskov Substitution Principle** - "Subclasses should be substitutable for their base class"
  
  * Breaks when -> Client uses a "Square" class that inherits from "Rectangle", since a square has equal height and width, the client may try to make them different and be confused that they are the same.

* **Interface Segregation Principle** - "Many client specific interfaces are better than one general purpose interface"
  
  * Take/Use only what you need.
  
  * Health component implements
    
    * IhealthDisplay for UI
    
    * IDamageable for combat code
  
  * Have a interface inherit from another instead of adding onto an existing and having the class inherit from it.

* **Depenpendecy Inversion Principle** - "Depend upon Abstractons. Donot depend on concretions"
  
  * Ability to switch out concrete implementations like with the Strategy Pattern
