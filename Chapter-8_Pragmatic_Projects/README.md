###### It's All Writing

`The palest ink is better than the best memory`

- Developers don't usually give much thought to documentation
- At best it is an unforunate necessity; at work it is treated as a low-priority task in the hope that management will forget about it at the end of the project

- Should embrace documentation as an integral part of the overall development process
- Writing documentation can be easier by not duplicating effort or wasting time, and by keeping documentation close at hand - in the code itself, it possible

- Want to treat code and documentation as two views of the same model
- Want to apply `all` of the pragmatic principles to documentation as well as to code

`Treat English as Just Another Programming Language`

###### Ruthless Testing

- Developers tend ot test gently, subconsciously knowing where the code will break and avoiding the weak spots
- Should instead be `driven` to find our bugs `now`

`Test Early. Test Often. Test Automatically`

- Want to start testing as soon as we have code
- Tiny problems of becoming large problems pretty fast

- Teams that use automated tests have a much better chance of success
- Tests that run with every build are much more effective

- The earlier a bug is found, the cheaper it is to rememdy
- `Code a little, test a little`

- A good project may well have `more` test code than production code
- The time it takes to produce this test code is well worth the effort
- It ends up being cheaper in the long run, and you actually stand a chance of producing a product with close to zero defects

- Knowing that you've passed the tests gives you a high degree of confidence that a piece of code is actually `done`

######## What to Test

- Several major types of software testing that you need to perform:

    * Unit testing
    * Integration testing
    * Validation and verificiation
    * Resource exhaustion, errors, and recovery
    * Performance testing
    * Usability testing

- Not a complete list, more specialized projects will require various other types of testing as well

########## Unit Test

- A unit test is code that exercises a module
- Unit testing is the foundation of all the other forms of testing
- If the parts don't work by themselves, they probably won't work well together
- All of the modules you are using must pass their own unit tests before you can proceed

- Once all pertinent modules have passed their individual tests, you're ready for the next stage

########## Integration Testing

- `Integration Testing` shows that all the major subsystems that make up the project work and play well with each other
- W/ good contracts in place and well tested, any integration issues can be detected easily
- Otherwise, integration becomes a common place for bugs
- Often the single largest source of bugs in the system

- Really just an extension of unit testing - only now you're testing how entire subsystems honor their contracts


########## Validation and Verification

- As soon as you have a UI or prototype, you need to answer an important question: the users told you what they wanted, but is it what they need

- Does it meet the functional requirements of the system?
- A bug-free system that answers the wrong question isn't very useful
- Be conscious of end user access patterns and how they differ from developer test data

########## Resource Exhaustion, Errors, and Recovery

- Need to discover how it will behave under real-world conditions
- Few limits your code may encounter include
    * Memory
    * Disk space
    * CPU bandwidth
    * Wall-clock time
    * Disk bandwidth
    * Network bandwidth
    * Color palette
    * Video resolution

- When the system does fail, will it fail gracefully?
- Will it try to save its state and prevent loss of work

Page 282