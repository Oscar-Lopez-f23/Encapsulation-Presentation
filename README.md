# Encapsulation Presentation Plan

Plan
- What is encapsulation
	- Definition: putting state and the behavior operating on that state together in a single unit.
	- Encapsulation helps in hiding the internal state of an object and exposing only the 
	  necessary functionalities
- Benefits of it / why its important and Software Design Principles:
	- Security: prevent access to sensitive data
	- SOLID: follows solid principles, why, and how following SOLID principles can lead to encap
	- Modularity: reusability, maintainability and testability, readability
	- abstraction: hides complexity
	- Cyclomatic complexity: program is easier to understand, cuts down the ammount of
		decisions made in a method/class (The precise number to use as a limit, however,
 remains somewhat controversial. The original limit of 10 as proposed by McCabe has significant
 supporting evidence, but limits as high as 15 have been used successfully as well. Limits over
 10 should be reserved for projects that have several operational advantages over typical projects,
 for example experienced staff, formal design, a modern programming language, structured programming,
 code walkthroughs, and a comprehensive test plan.
 In other words, an organization can pick a complexity limit greater than 10, but only if it is sure
 it knows what it is doing and is willing to devote the additional testing effort required by more
 complex modules.")

	- easier refactoring
	- defensive
	- Pillars
- IRL examples:
	- behavioral patterns
	- CQS (mention why Im not covering CQRS)
	- Strategy
- Heuristics && code smells: 
	- coupling/cohesion
	- variable and function encap
	- look for left right code
	- Modules using internal state can be broken down into their own unit
	- Check for classes that have access to state outside of its own, Ask why and if its necessary
  	- Expose only necessary functionality, 
		prevent unintended access and modification of internal state: HOW?
	- define contracts; this enforces behaviors
- How to: semi-live code sample
	- Point of sale
	- Member Variable Encapsulation
	- Function Encapsulation
	- USE ECS CALCULATOR CODE


- POTTS NOTES
	- what do the "gang of four" say about encapsulation?
	- how does that contrast with someone like Bertrand Meyer?
	- should I consider encapsulation when designing a solution in my day to day work?

https://en.wikipedia.org/wiki/Coupling_(computer_programming)#:~:text=In%20software%20engineering%2C%20coupling%20is,Coupling%20and%20cohesion
https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/tutorials/oop
https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)
https://medium.com/@CodeWithHonor/c-encapsulation-6b59be896312#:~:text=Encapsulation%20is%20a%20fundamental%20concept%20in%20object-oriented%20programming%20(OOP,public%20%2C%20private%20%2C%20and%20protected%20.
