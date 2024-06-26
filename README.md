Plan
- What is encapsulation
	- Definition: putting state and the behavior operating on that state together in a single unit.
	- Encapsulation helps in hiding the internal state of an object and exposing only the necessary functionalities

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
			- Cyclomatic complexity: program is easier to understand, cuts down the ammount of decisions made in a method/class (The precise number to use as a limit, however, remains somewhat controversial. The original limit of 10 as proposed by McCabe has significant supporting evidence, but limits as high as 15 have been used successfully as well. Limits over 10 should be reserved for projects that have several operational advantages over typical projects, for example experienced staff, formal design, a modern programming language, structured programming, code walkthroughs, and a comprehensive test plan. In other words, an organization can pick a complexity limit greater than 10, but only if it is sure it knows what it is doing and is willing to devote the additional testing effort required by more complex modules.")

- Misc: 
	- web apps vs mobile/desktop: explain how state management is not as demanding in web apps compared to mobile/desktop
	- GOF: Favor Composition over inheritance. Program to Interfaces, not implementations. Strive for loosely coupled designs between objects that interact - Head first design patterns

- IRL examples:
	- SRP: SRP leads to more isolated, understandable, and maintainable code by ensuring that each class is focused on a single aspect of the system’s functionality
	- CQS: command query sepparation states that every method should either be a command that performs an action or a query that returns data to the caller, but not both. commands modify state but does not return value while query is the opposite. There is CQRS but that focuses on separating these actions which is why i wont cover it for encapsulation. An easy example of CQS is the default get;set;
	- behavioral patterns: design patterns that identify common communication patterns among objects. By doing so, these patterns increase flexibility in carrying out communication.
		- Strategy: hides details of the implementation
		- Specification: a specification is an encapsulation of logic in a reusable form,
		- Command pattern: design pattern in which an object is used to encapsulate all information needed to perform an action or trigger an event at a later time
	- structural patterns : design patterns that ease the design by identifying a simple way to realize relationships among entities. Patterns like Adapter, Facade, and Mediator are specifically designed to improve encapsulation by providing a simplified interface to complex subsystems.

- Heuristics: 
	- coupling/cohesion: Coupling in programming refers to how classes are connected, and cohesion is the degree to which the elements inside a module belong together in other words how closely related and focused the responsibilities are. We want low coupling so that classes are not too dependant on others as a change to one class can cause a number of changes to another, and high cohesion so we have all related code in one place. Anything that resembles some sort of God class, or a class that does more than one of the things below is not cohesive:
		- Access data located on a disk, database or network
		- Deserialises the data to an object
		- Displays the data to the user
		- Gets an input from the user to perform an operation on the data
		- Persists the changes back to the data
	- heap vs stack: if a value is passed by reference from another module we are editing another classes internal state. Everything in c# is actually passed by value but classes are reference types so their reference is passed by value, but variables passed with the ref or out keyword are passed by reference. b/c the classes reference is passed by value its properties are vulnerable to changes if not readonly but if the receiving method assings the object parameter to a new instance, the original instance passed in from the caller wont be modified.
	- Kerievsky's Encapsulate Subclasses with Creation Methods: hide implementation details
	- composition and aggregation
	- Data hiding: Ensures data integrity and prevents unauthorized access and modification. Achieved through access control like private, protected, and public specifiers.
	- class, variable and function encap
	- look for left right code
	- Modules using internal state can be broken down into their own unit
	- Check for classes that have access to state outside of its own, Ask why and if its necessary
  	- Expose only necessary functionality, prevent unintended access and modification of internal state: HOW?
	- define contracts; this enforces behaviors

- Heuristics Examples:
	- coupling: 2 classes, ShoppingCart and PaymentProcessor, if the Payment Processor class depends on shopping cart any changes done to shopping cart might mean that Payment Processor needs to change as well so we introduce a contract that payment processor can use instead of shopping cart. shopping cart can implement it so that the paymnet processor does not care who the consumer is as long as they follow the contracts rules.
	- cohesion: our payment processor shouldn't be responsible for saving the data to the database as it already has run operations on the shopping cart data to pay for the order. this job should be part of a repository who's contract is injected to the payment processor keeping coupling low
	- ref types: avoid using ref/out keyword and if passing a class make its properties readonly.
	- Kerievsky encapsulate subclasses: show kerievskys example in refactoring to patterns page 15
	- 

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

https://www.youtube.com/watch?v=JHGkaShoyNs
https://github.com/abhinavkorpal/awesome-computer-science-EBook/tree/master
https://en.wikipedia.org/wiki/Behavioral_pattern
https://en.wikipedia.org/wiki/Structural_pattern
https://www.eventstore.com/blog/transcript-of-greg-youngs-talk-at-code-on-the-beach-2014-cqrs-and-event-sourcing
https://en.wikipedia.org/wiki/Separation_of_concerns#:~:text=In%20computer%20science%2C%20separation%20of,code%20of%20a%20computer%20program.
https://pwskills.com/blog/understanding-association-aggregation-composition-in-java/#:~:text=%7D-,Aggregation%20In%20Object-Oriented%20Programming,considered%20independent%20of%20the%20other.
https://stackify.com/oop-concepts-composition/#:~:text=Composition%20is%20one%20of%20the,has-a%20association%20between%20objects.
https://en.wikipedia.org/wiki/Coupling_(computer_programming)#:~:text=In%20software%20engineering%2C%20coupling%20is,Coupling%20and%20cohesion
https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/tutorials/oop
https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)
https://en.wikipedia.org/wiki/Specification_pattern
https://medium.com/@CodeWithHonor/c-encapsulation-6b59be896312#:~:text=Encapsulation%20is%20a%20fundamental%20concept%20in%20object-oriented%20programming%20(OOP,public%20%2C%20private%20%2C%20and%20protected%20.
https://benscabbia.co.uk/programming/high-cohesion-low-coupling-and-strong-encapsulation
