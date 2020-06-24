# Clojure Katas - Data Driven APIs (ClojureNorth 2020 Workshop)

In recent years, there’s been a wave of new Clojure libraries written with “data driven” APIs. Be it routing, database-querying, or composing systems - problems that were once solved with string-, function- or macro-based DSLs are now being re-solved in a new “style” that’s somewhat unique to Clojure. What does it mean to be ‘data driven’? Is it just a fad? Is it only for libraries?

In the first hour, we will do a brief explanation of data-driven APIs, and then participants will be tasked with designing data-driven APIs for some prepared problems. In the second hour, we will review and discuss the various solutions.

(Since we’re focusing on design rather than implementation, this workshop should be accessible to Clojurians of all levels).

1st Hour:
 - introduce “data-driven” apis
 - introduce design problems
 - participants work on design problems

2nd Hour:
 - participants submit their solutions for critique
 - review and discussion of solutions


## Your Design Task

1. You will be designing a data-driven DSL to solve some problem.

   Choose one of the problems from [this list](./problems.md).

   We recommend choosing a problem domain that you are at least somewhat familiar with (to better understand how your DSL might be used in practice).

   If you've thought of some other problem that you'd like to design a data-driven API for, go ahead!


2. Take a moment to scan through the [list of reflection questions](./evaluating-notations.md) to get an idea of some of the characteristics that you might want to keep in mind while working on your design.

3. Now the hard part: design a data-driven Clojure DSL for your chosen problem.

   You don't have to implement the actual library! Just sketch out what the syntax and workflow might be for using the library.

   Many of the suggested problems already have some existing declarative languages (which isn't data-driven), but, many of these languages are quite general and complex (and maybe even turing-complete) -- your design does *not* need to match them 1:1 in features, feel free to focus on a subset of functionality or just use the existing languages as inspiration/"prior art".

   Your solution doesn't have to be 100% "data-driven": there may certainly be parts of your design where allowing for arbitrary code is the best solution.

   We recommend you start your design work by choosing a few specific sample use-cases to design for.

   The end goal is to come up with a mock README for your library, featuring an explanation of what it does and examples of how to use it. See [the template](./template.md)

3. After you are done your design (or time is running out), take a moment to reflect on your design using [these questions](./evaluating-notations.md). Perhaps add some notes to you README if you find some of these questions make you identify something particularly good or bad about your design.

4. If you'd like to have your design potentially discussed in Part 2 of the workshop, push your README to GitHub and add a link to [the spreadsheet](https://docs.google.com/spreadsheets/d/1F7TGID104-ayVhOT47RV3fCLHpvAaeOGZScIKdvG9-8/edit?usp=sharing).

