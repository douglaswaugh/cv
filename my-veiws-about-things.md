my views about things
===

tdd
---

### advantages

* change the way you think from what the code does to how the code is consumed.  
* has a specific refactor step to encourage thought about the design.  
* means the code you write has high test coverage and is always easy to test.
* can inform your design descisions

  One recent example is the AccessControl.  My initail idea was to I wanted to be able to test the behaviour of the AccessControl, whose responsibility it was to add the Access-Control-White-List, or not, under various circumstances.  The list of allowed origins was long and I didn't want to have to duplicate each of the behaviour tests for each of the origins.  

### disadvantages

* Test maintenance can be a problem if the tests are written poorly. 
* Can make too many design decisions up-front if you start extracting classes too early.
* Can make refactoring difficult if the tests are over-specified

### alternatives

* could do a lot of manual testing, but this becomes prohibitive as the application becomes more complex.  
* could just write unit tests after the fact, but this means you miss the refactoring step and you might write code that is hard to test.

### things that I used to do that I no longer do

arrange act assert comments
one assert per test
too much coupling to concrete instances in tests
asserting on properties returned from stubs

### things I do that I didn't used to do

listening to the tests
keep the tests focused on exactly the thing that you want to test, that you want to show you're testing

xp
---

### advantages

I like many of

### disadvantages

### alternatives

## Object Oriented Programming

I think my OO has improved dramatically improved since I started really paying attention to the abstractions that I am creating.  I try and increase cohesion and reduce

I think I understand what people (Alan Kay) says about the way that objects communicate being more important than how the objects do the things they're asked.  Although I think it's implicit that you have to work out what each object knows about in order to work out how they communicate.

### late binding/early binding

As I delve deeper in to OO I realise how restrictive and verbose statically typed languages can be.  I've been doing a little bit of Ruby recently, and I'm enjoying it.  No longer need to define interfaces (although still a good idea to test that objects conform to interfaces, including test doubles, to keep your test code inline with your production code)

## functional

## testing strategy/acceptance testing/bdd

page flow
page
integration
unit tests

page object model

## things that I changed at WTG

first unit tests written
first automated deployments

## things that I changed at energyhelpline

full continuous integration pipeline
automated deployments using octopus
constant agent for changed
got improvements included in regular work as cards on the board

## rest

### benefits

decouple the server from the client

## cqrs/event sourcing

### benefits

cqrs benefits are around scaling.  splitting the read and the write means you can optimise both individually.  mainly in collaborative domains where multiple users are working on top of the same set of logical data.
event sourcing decouple aggregates/modules/bounded contexts.  also benefits around not losing state over time.  I also find having an event sourced domain model makes it quite easy to reason about.  We have event based tests and I find it easier to spot bugs by just reading some of the tests.

### disadvantages

in our event sourcing implementation we used a lot of reflection, which can seem like magic if you don't know or trust what it's doing.  makes it quite difficult to debug.

refactoring your aggregates can be a bit annoying, as events are stored as

### alternatives

### ddd

### benefits

help developers and business communicate.  also I like the ideas for bounded contexts.  in other words, you can put a boundary around some applications or services and not worry about what happens outside of it.  this reduces the problem space.  the opposite would be to try and create a ubiquitous language for the entire organisation.  seems quite similar to the advice David West gives in the book on Object Thinking that I'm currently reading.

best used when you have domain experts.  sounds flippant, but if you don't have domain experts you probably don't need to apply DDD.3

### disadvantages

people think that applying the patterns means that you're doing DDD.  it's true that using repositories, etc might help you persist your model.

because only one aggregate should be updated in each transaction, there is a tendency to make the aggregates too big, although there are strategies to avoid big aggregates like referencing aggregates by ID

## why do I want to go contracting?

exposure to lots of different projects and lots of different developers.  I'd like to set my own consultancy up and contracting seems a good place to start.
