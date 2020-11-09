# Book Notes

# 1. Rediscovering Simplicity

When you were new to programming you wrote simple code. Although you may not have appreciated it at the time, this was a great strength. Since then, you’ve learned new skills, tackled harder problems, and produced increasingly complex solutions. Experience has taught you that most code will someday change, and you’ve begun to craft it in anticipation of that day. Complexity seems both natural and inevitable.

Where you once optimized code for understandability, you now focus on its changeability. Your code is less concrete but more abstract—you’ve made it initially harder to understand in hopes that it will ultimately be easier to maintain.

The basic promise of Object-Oriented Design (OOD):  if you’re willing to accept increases in the complexity of your code along some dimensions, you’ll be rewarded with decreases in complexity along others. 

OOD doesn’t claim to be free; it merely asserts that its benefits outweigh its costs.

Design decisions inevitably involve trade-offs. There’s always a cost. For example, if you’ve duplicated a bit of code in many places, the Don’t Repeat Yourself (DRY) principle tells you to extract the duplication into a single common method and then invoke this new method in place of the old code.

DRY is a great idea, but that doesn’t mean it’s free. The price you pay for DRYing out code is that the invoker of the new method no longer knows the result, only the message it should send. If you’re willing to pay this price, that is, you are willing to be ignorant of the actual behavior, the reward you reap is that when the behavior changes, you need alter your code in only one place. The argument that OOD makes is that this bargain will save you money.

Each of these design choices has costs, and it only makes sense to pay these costs if you also accrue some offsetting benefits. Design is thus about picking the right abstractions. If you choose well, your code will be expressive, understandable and flexible, and everyone will love both it and you. However, if you get the abstractions wrong, your code will be convoluted, confusing, and costly, and your programming peers will hate you.

Unfortunately, abstractions are hard, and even with the best of intentions, it’s easy to get them wrong. 

Well-meaning programmers tend to over-anticipate abstractions, inferring them prematurely from incomplete information. Early abstractions are often not quite right, and therefore they create a catch-22.

You should not reach for abstractions, but instead, you should resist them until they absolutely insist upon being created.


## Tests

All tests ontains three parts:

- **Setup** Create the specific environment required for the test. 
- **Do** Perform the action to be tested.
- **Verify** Confirm the result is as expected.


## Understanding Transformations

In the "Transformation Priority Premise" (a blog post that you are urged to scan), Martin defines transformations as "simple operations that change the behavior of code." Not only does he describe a set of transformations that move code from more specific to more generic, he arranges these transformations in "priority" order, from simpler to more complex. 

He asserts that **when a problem can be solved with any one of several transformations, the transformation with the highest priority is simplest and therefore best.**


As was stated in the previous section, as tests get more specific, code should become more generic. Code becomes more generic by becoming more abstract. 

One way to make code more abstract is to DRY it out, that is, to extract duplicate bits of code into a single method, to give that method a name, and then to refer to the code by this new name. DRYing out code removes the duplication and thus reduces its overall size.

As you’ve seen, when working towards Shameless Green, it makes sense sometimes to eliminate duplication and other times to retain it. The Shameless Green solution is optimized to be straightforward and intention-revealing, and it doesn’t much concern itself with changeability or future maintenance. The goal is to use green to maximize your understanding of the problem and to unearth all available information before committing to abstractions.


## Case(Switch) vs If/Else

Use of if / elsif implies that each subsequent condition varies in a meaningful way. Because elsif is often used to test wildly different conditions, future readers will feel obliged to closely
examine each one. 

In contrast, use of case implies that every condition checks for equality against an explicit value. While it’s true that the when clause supports more complicated operations, the form above is most common and is the one your readers will expect. Readers of case statements expect conditions to be fundamentally the same.

## The Horizontal Path

Following the horizontal path means writing code to produce every kind of verse before diverging onto tangents to DRY out small bits of code that the verses have in common. The goal is to quickly maximize the number of whole examples before extracting abstractions from their parts.


Code longs to be as ignorant as possible. 


In Chapter 28 of Test-Driven Development by Example, Kent Beck describes different ways to make tests pass. Three of his "Green Bar Patterns" are:

- Fake It ("Til You Make It") 
- Obvious Implementation 
- Triangulate



[More Notes](https://medium.com/extreme-programming/notes-from-99-bottles-of-oop-5c902afd3948)
