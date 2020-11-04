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
