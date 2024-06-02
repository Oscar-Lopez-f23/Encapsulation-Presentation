- What is encapsulation
	- Definition: putting state and the behavior operating on that state together in a single unit.
	- Encapsulation helps in hiding the internal state of an object and exposing only the 
	  necessary functionalities

- Benefits of it / why its important and Software Design Principles:
	- Pillars: the 4 pillars of OOP enhance development by promoting good practices. They help create flexible, simplified, secure, modular, and reusable code. Together, these principles make development faster, more maintainable, and extensible, ultimately leading to more efficient and effective software.
	- Modularity: 
			- reusability: Since each unit is designed to perform a specific task, it can be easily integrated into other parts of the program without requiring significant modifications. This reduces the need to write new code for common functionalities.
			- maintainability: easier to update and fix, as changes can be made to individual modules without affecting the broader system.
			- testability: Since logic operating on state is isolated more specific tasks can be tested. This makes it easier to identify and fix defects within specific modules.
			- readability: Encapsulation breaks down complex functionality into smaller, more manageable pieces. Each module has a clear and specific purpose, which makes it easier for developers to understand what the code does. Well-defined interfaces between modules also improve comprehension by clearly showing how different parts of the system interact.
	- abstraction: 
			- Hides complexity: code is smaller and hides unnecessary details therefore easier to read and manage
			- Data hiding: Focuses specifically on restricting access to the internal state of an object.
	- defensive:
			- easier refactoring: modules are smaller and focus on specific tasks, meaning refactoring typically involves changes only within the module without affecting the broader system.
			- Separation of Concerns: SoC is achieved by encapsulating information inside a unit of code that has a well-defined interface which leads to a clearer and more organized system structure. This protects aspects or "concerns" within the application model
			- Security: prevents unauthorized access to sensitive data, ensuring that only designated methods can modify it. This isolation not only enhances security but also allows for fewer, more robust unit tests focused on the encapsulated logic. By encapsulating logic and data we are also stopping unsafe actions to be done.
			- Controlled Access: Encapsulation allows controlled access to the object's data. This control is enforced through methods that validate or restrict how the data can be modified.
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

- Misc: 
	- web apps vs mobile/desktop: explain how state management in web apps is not as demanding
	 in web apps compared to mobile/desktop

- IRL examples:
	- SRP
	- CQS (mention why Im not covering CQRS)
	- Strategy
	- behavioral patterns

- Heuristics && code smells: 
	- coupling/cohesion
	- association, composition and aggregation
	- Data hiding: Ensures data integrity and prevents unauthorized access and modification. Achieved through access control like private, protected, and public specifiers.
	- variable and function encap
	- look for left right code
	- Modules using internal state can be broken down into their own unit
	- Check for classes that have access to state outside of its own, Ask why and if its necessary
  	- Expose only necessary functionality, prevent unintended access and modification of internal state: HOW?
	- define contracts; this enforces behaviors

- How to: semi-live code sample
	- Point of sale
	- Member Variable Encapsulation
	- Function Encapsulation
	- UML before each refactor
	- USE ECS CALCULATOR CODE

- POTTS NOTES
	- what do the "gang of four" say about encapsulation?
	- how does that contrast with someone like Bertrand Meyer?
	- should I consider encapsulation when designing a solution in my day to day work?
	- perspective on this, would be Eric Evans

- Books
	- Refactoring by Martin Fowler
	- Refactoring to Patterns by Joshua Kerievsky


get academics- my representation of what the sources say
aggregation vs composition?
data hiding vs encapsulation

https://en.wikipedia.org/wiki/Separation_of_concerns#:~:text=In%20computer%20science%2C%20separation%20of,code%20of%20a%20computer%20program.
https://pwskills.com/blog/understanding-association-aggregation-composition-in-java/#:~:text=%7D-,Aggregation%20In%20Object-Oriented%20Programming,considered%20independent%20of%20the%20other.
https://stackify.com/oop-concepts-composition/#:~:text=Composition%20is%20one%20of%20the,has-a%20association%20between%20objects.
https://en.wikipedia.org/wiki/Coupling_(computer_programming)#:~:text=In%20software%20engineering%2C%20coupling%20is,Coupling%20and%20cohesion
https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/tutorials/oop
https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)
https://medium.com/@CodeWithHonor/c-encapsulation-6b59be896312#:~:text=Encapsulation%20is%20a%20fundamental%20concept%20in%20object-oriented%20programming%20(OOP,public%20%2C%20private%20%2C%20and%20protected%20.
