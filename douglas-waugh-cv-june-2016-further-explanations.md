# extensions from cv

## easy to understand code

short methods, names that make sense, good abstractions, conform to coding standards of the team, maintain architectural integrity, highly cohesive
in the tests make it clear what the test is testing by hiding irrelevant details

## easy to change code

loosely coupled using dependency injection and composition over inheritance, good abstractions, high cohesion

## deliver highest value first

break work down into small units that deliver value as a horizontal slice, ask business to prioritise the features, work on one feature at a time, keep working on feature until it's deployed

## 'three amigos'

concept from the theory of constraints developed by Eliyahu Goldratt, he says in a system with bottlenecks, identify the bottleneck and move the quality control in front the bottleneck identified, this reduces waste to the minimum.  in practice this is just about making sure that everyone is on the same page regarding the piece of work to be delivered

## test driven development

red - green - refactor.  obviously helps with making sure your code does what you think it does today and in the future.  it also helps you design the API of the objects under test because you always have to think from the point of view of the clients of that object.  the act of testing forces you to think about what you are writing.  tests can also help to validate your design. a common problem is that the object under test has many dependencies some of which aren't relevant to your test.  this is a signal that perhaps the object should be split.  another problem might be that you have lots of very similar tests.  in this case it may be that you are missing a more general abstraction that could be tested, rather than the individual cases.

## 
