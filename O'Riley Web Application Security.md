# O'Riley Web Application Security

## History

#### 1950s - Telephone

* **Tone Dialing**: Phones switched from manual operators to audio frequencies mapped to each button that was interpreted by a automated machine to numbers for routing calls. This allowed only one operator to oversee hundreds of calls instead of a one-to-one call ratio.
* **Phreaking** (Phone + Freaking): An early type of hacker specializing in breaking or manipulating telephone networks. Early usage was tied to manipulating tone dialing by using devices to emit identical sound frequencies. Possible the term comes from "Audio Frequency" since it occurred during the transition time with AT&T's original tone dialing system.
  * **2600 HZ Tone**: Tone used by AT&T to mark that a call had ended (admin command), allowing the call to continue and not be marked by the systems on how long the call actually was (logged call as ended even though it went going)
    * Joe Engressia was a little boy who had a whistler that was identical to the tone, discovery by accident and abused it to show off to his friends.
    * John Draper, friend of Joe, discovered that a cereal toy produced the same sound as Joe's whistle. Knowledge of these techniques allowed others to match audio frequencies to abuse AT&T's known flaw.
  * **Blue Box**: Hardware device that played a 2600 HZ Signal, invented by Steve Wozniak and sold by Steve Jobs early in their lives. 
  * Usages
    * Tamper with pay phones
    * Prevent billing cycles from starting without a 2600 hz signal
    * emulate military's communcation signals
    * fake caller ID
* Design standpoint: The engineers knew about this "admin feature" and thought that normal people would not discover. This was the "Best Case Scenario", and a learning point in that you must always consider the "Worst-Case Scenario" when designing complex systems.

#### 1960s - Telephone (Anti-Phreaking Technology, Circa 1960)

**Duel Tone Multifrequency Signaling** (DTMF / Touch Dials): Each button is tied to two specific audio frequencies via row/column instead of a single frequency like the original invented by Bell Systems. Instead of Phreakers being able to mimic a simple sound, a complex sound made by multiple instruments was much more difficult to mimic (such as voice/Whistle).

* **Malicious Actor**: A entity that is partially or wholly responsible for an incident that impacts, or has the potential to impact -- an organization's security; such as a Phisher.
* **Dual Tone**: The two sounds generated each time by the new technology via ROW and COLUMN for safer security.
  * Used as standard by International Telecommunication Union (ITU)
  * Used by Cable TV to specify commercial break / for telephones.
* Design standpoint: Eventually duplicated, but much more harder to crack than the initial. Complex systems can be engineered to be more difficult to abuse if proper planning is involved in conception. 
* Eventually switching centers moved from analog to digital, eliminating almost all phreaking usages.