# Evaluating

- In what ways is the data-driven syntax better than a custom string syntax? In what ways is it worse?

- In what ways is it better than a "fluent design" (using functions and macros)? In what ways is it worse?

- How easy is it to programmatically compose parts of a program into a working whole?

- How easy is it to read vs. write vs. modify?

- Is there an "escape valve" to allow users to do something in a custom way?

- How well would the syntax "scale" with a larger problem?

- After part of the syntax is learned, how easy is the rest to guess?

- Is there any possible ambiguity between components of a program?


## Cognitive Dimensions of Notations

Below we've adapted several questions from Thomas Green's 'Cognitive Dimensions of Notations' a set of design principles for notations.


### Viscosity

- How easy is it to make changes?

- Do small changes in one place require changes in many others?

- Are there particular changes that are more difficult to make?


### Diffuseness

- How verbose is the syntax?

- What sort of things might take more space to describe?

- Would it be longer or shorter to do with a general purpose language?


### Hard Mental Operations

- How much 'cognitive load' does this syntax require of the user?

- How many degrees-of-freedom are there in the syntax? If you had to write a parser, how complex would it be?

- How complex is the mental-model of the underlying "machine"?


### Error Proneness

- To what extent does the syntax influence the likelihood of the user making a mistake?

- What is the most likely mistake a user might make with the syntax?


### Closeness of Mapping

- How closely does the syntax correspond to the problem domain?

- How much effort does it take to translate a problem to fit within the syntax?


### Role Expressiveness

- When reading the syntax, is it easy to tell what role each part of the syntax plays in the solution as a whole?

- Are there some parts of the syntax more difficult to intepret?


### Hidden Dependencies

- If some parts of the syntax are related to others (ex. a change to one requires a change to the other), are those dependencies visible?


### Progressive Evaluation

- How easy is it to get feedback on an incomplete program? (ie. Is it possible to try out a partially-completed version of a program, and compose it in stages?)


### Premature Commitment

- In practice, does the syntax impose a certain order in how it is used?

- Does the syntax force you to think ahead and make certain decisions in advance?


### Consistency

- Are there places in the syntax where some things ought to be similar but the syntax makes them different?


### Abstraction Management

- Does the syntax make it possible to encapsulate details through new abstractions?


### Visibility and Juxtaposability

- How easy is it to compare different programs in the syntax and spot differences?


### More re: Cognitive Dimensions

 - https://en.wikipedia.org/wiki/Cognitive_dimensions_of_notations
 - https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.22.1477
 - https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.13.2023
 - https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.33.7804
