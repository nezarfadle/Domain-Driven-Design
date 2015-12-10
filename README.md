# Domain Driven Design


### FLow ###
  * All the layers should sign a contract with each other via DTO's or a Concrete Class Objects
  * Application Layer will Start the Use Case ( Purchasing )
  * Instantiate the Actor who is gonna start the Use Case ( Purchaser )
  * Instantiate the Actor in a valid State ( Please give him an empty Cart )
    * ``` Customer = new Customer(new Cart()) ```
  * Use Specifications, Application and Domain Services to drive the flow 
    * ``` AuthenticationService ( Application Service ) ```
    * ``` DidThePurchaserPurchasedMoreThanThreeItems ( Specefication ) ```
    * ``` TaxCalculater ( Domain Service ) ```
  * Domain Service argument's and return's must be a Domain Objects
  * Dispatch a Domain and Application Events
  * Handle Domain and Application Events if any
  * End the Use Case 

### Bounded Contexts Types ###
* CRUD Bounded Contexts ( User Management - Product Management )
* Use Case Bounded Context ( Shopping - Invoicing )

### Folder Structure ###
---------------
#### BoundedContext ####
* Interface Layer
  * DTO’s Objects
* Application Layer
  * Actions = Use Cases
  * DTO Objects
  * Command Bus
  * Commands
  * Commands Handlers
  * Specifications ( IsItLessThanThreeMinutesSinceTheSystemSentTheTacSMS )
  * Composites Specification
  * Event Dispatcher
  * Data Mappers
  * Events
  * Services
  * Factories 
  * IUnitOfWork
  * IUnitOfWorkRepository
 
* Domain Layer
  * IAggrgateRoot - IEntity
  * Entities
  * Value Objects
  * IRepository Contracts
  * Services
  * Specifications 
  * Composites Specification
  * Events
  * Exceptions 
  * Use Events to help UnitOfWork knows about the dmain changes:
    * ` Purchaser.buy() -> Dispatch -> NewPurchaseEvent ` 

* Infrastructure Layer
  * Sessions Manager ( Temporary save the Domain State )
  * IReadOnlyRepository ( Thin Read Layer )
  * IRepository
  * Repositories
  * Mailers 
  * Cache
  * File System 

### Vocabularies ###
* Coding Standards Convention
* CQRS



