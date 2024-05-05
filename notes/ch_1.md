# Chapter 1

## Goals:
- Learn basic boolean algebra
- understand that everthing is boolean math underneath the hood
- Understand HDL language/setup
- Implement all of the gates listed in the chapter

## 1.1 Boolean Algebra
In common parlance, we say something is either true or false. This is represented as a *boolean*. This true or false relationship is the fundamental building block of all of computer science.

We represent *true* and *false* as 1 and 0 respectively. 

### Boolean Operators
While we have boolean values, we need to be able to do more than just have values. We need to be able to do things with them. We call such 'functions' operators.

The basic functions are called 'and', 'or' and 'not'.

These are represented in different ways. Two viable sets of notation are shown below:

| Operator | Book Notation   | Mathematical Notation   |
|----------|-----------------|--------------------|
| And      | $$ x \cdot y $$ | $$ x \land y $$ |
| Or       | $$ x + y $$ |          $$ x \lor y $$          |
| Not      |  $$ \overline{x}$$               |      $$ \lnot x$$               |

Fair enough. So now we have 2 ways to write this. But realisitically, this is not what this chapter is about. At the end of the day, this is called *Nand2Tetris*. So what is *Nand*?

If you guessed *not and*, you are correct. And Nor is *not or*.
| Operator | Book Notation   |
|----------|-----------------|
| Nand      | $$ \overline{x \cdot y} $$ |
| Nor      | $$ \overline{x + y} $$ |

So why did the author's choose nand? Because logically, every single boolean function can be realized with only boolean functions. What's the rationale here? 

Intuitively, from a high level, if you're able to get the basic operators from a nand gate, shouldn't you be able to buld everything else?

TODO: get this proof in line Appendix 1

### Boolean functions
At a very simple level, a boolean function is the application of some combination of boolean operators that result in some sort of function. There are two ways to visualize a boolean function. 

1. Truth Tables
1. Boolean Expressions

They are both equivalent. But here we can start to see the power/complexity of these operations as we grow them.

### List of boolean functions and Truth Table

| English | Notation |   |   |   |   |
|---------|----------|---|---|---|---|
| Constant 0     |    0     | 0 | 0 | 0 | 0 |
| Constant 1       |    1     | 1 | 1 | 1 | 1 |
| x       |   x      | 0  | 0 | 1 | 1 |
| y       |   y      |  0 |  1 | 0 | 1  |
| x and y | $$ x \cdot y $$ | 0 | 0 | 0| 1|
| x or y | $$ x + y$$ | 0 | 1 | 1 | 1|
| not x| $$\overline{x}$$ | 1 | 1| 0|0|
| not y| $$\overline{y}$$ | 1 | 0| 1| 0|
|xor| $$x\cdot \overline{y} + \overline{x} \cdot y$$ | 0| 1 | 1 | 0 |
|nor | $$ \overline{x + y} $$ | 1 | 0 | 0| 0|
|Nand| $$\overline{x\cdot y}$$ | 1 | 1| 1| 0|
| Equivalence| $$ x\cdot y + \overline{x} \cdot \overline{y}$$| 1| 0 | 0| 1|
| If x then y| $$\overline{x} + y $$| 1 | 1 | 0| 1|
|If y then x | $$x+ \overline{y} $$ | 1 | 0| 1| 0|

Key things here, conditionals aren't as intuitive. The rest are just logical completions of what is already known.

So given any gboolean expression, we can construct the corresponding truth table. The truth table is convenient for describing the state while the boolean expression is a convenient formalism for realising this in silicon. Maybe a clearer way -- a convenient formalism for realising this in code.

## Logic gates
A gate is a physical devise that implements a boolean function. It's a dated construct/concept as today most ocmputers use electricity rather than physical gates to realize the logic they're tyring to implement. However, for initial/individual understanding, it helps to think that they are in silicon. *Gate* and *chip* are used interchangeably. We prefer to use the word gate for simpler versions of *chips*.

## Primitive and composite gates
A primitive gate is one of the simple boolean funcitons. A composite gate is some combination of the boolean functions. Said another way, every single composite gate is formed with primitive gates.

An interface, much like a software interface, is the overarching behavior of a given chip while the implementation of the given chip is some combination of chips and gates.

### Unnecessary tidbits but cool to know
- Claude Shannon's 1937 paper is considered the most important M.Sc thesis in c.s. where he used boolean algebra to analyze the abstract behavior of logic gates.
