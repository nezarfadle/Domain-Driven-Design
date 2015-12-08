# Domain Driven Design


### FLow ###
  * Application Layer will Start the Use Case ( Purchasing )
  * Instantiate the Actor who is gonna start the use Case ( Purchaser )
  * Instantiate the Actor in a valid State ( Please give him an empty Cart )
    * ``` Customer = new Customer(new Cart()) ```
  * Use Specifications and Domain Services to drive the flow 
    * DidTheCsutomerPurchasedMoreThanThreeItems ( Specefication )
    * TaxCalculater ( Service )
  * Domain Service argument's and return's must be a Domain Objects
  * Dispatch Domain Events and Give the flow control back to the Application Layer
  * End the Use Case 

### Bounded Contexts Types ###
CRUD Bounded Contexts ( User Management - Products Management )
Use Case Bounded Context ( Shopping - Invoicing )

Folder Structure
BoundedContext
Interface Layer
DTO’s Objects
Application Layer
Actions = Use Cases
DTO Objects
Commands
Command Bus
Commands Handlers
Unit Of Works
Event Dispatcher
Data Mappers
Events
Services
Factories 
IUnitOfWork
IUnitOfWorkRepository
Domain Layer
IAggrgateRoot - IEntity
Entities
Value Objects
IRepository Contracts
Services
Specifications 
Composites Specification
Events
Exceptions 
Infrastructure Layer
Sessions Manager ( Temporary save the Domain State )
IReadOnlyRepository ( Thin Read Layer )
IRepository
Repositories
Mailers 
Cache
File System 





