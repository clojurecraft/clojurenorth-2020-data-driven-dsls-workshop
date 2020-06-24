


 ### Modeling Physical Systems (Modelica)

 Modelica is a language used to model complex systems, such as the electrical and mechanical subsystems of a car. Modelica lets you define components (such as a "resistor") with input and output "pins", define equations that related the various inputs and outs (ex. `V = IR`), and then hook up and simulate a network of components.

 Resources
  - [Modelica by Example (Book)](https://book.xogeny.com/)
  - [Modelica on Wikipedia](https://en.wikipedia.org/wiki/Modelica)


### System Dynamics

 representing System Dynamics (stocks and flows)
    https://en.wikipedia.org/wiki/System_dynamics


### Mathematical Notation

https://en.wikipedia.org/wiki/TeX#Mathematical_example

for generating, manipulating and then..
      … converting for use in latex
              … converting for use in a symbolic math system (Maple, Mathematica)


### Gherkin

Gherkin is a language used for writing BDD test cases.

Resources
- [Gherkin on Wikipedia](https://en.wikipedia.org/wiki/Cucumber_(software)#Gherkin_language)
- [Gherkin Docs](https://cucumber.io/docs/gherkin/reference/)


### Describing Language Grammars (Instaparse)

[Instaparse](https://github.com/engelberg/instaparse) is an existing Clojure library for describing context-free grammars, but it uses an [EBNF](https://en.wikipedia.org/wiki/Extended_Backus%E2%80%93Naur_form) based custom-string syntax. What might it look like if it was data-driven?


### Musical Notation

  Percussion notation: https://en.wikipedia.org/wiki/Percussion_notation
  Tabs: https://en.wikipedia.org/wiki/Tablature
  Modern staff notation: https://en.wikipedia.org/wiki/Musical_notation#Modern_staff_notation

https://en.wikipedia.org/wiki/ABC_notation
https://en.wikipedia.org/wiki/LilyPond
https://en.wikipedia.org/wiki/MusicXML




### Dockerfiles


### Describing Graphs (DOT / GraphViz)

DOT is a language used for describing graphs (the nodes-and-vertices kind, not the bar-chart kind). Tools like GraphViz consume DOT files and use various algorithms to render the graphs.

Resources
- [DOT on Wikipedia](https://en.wikipedia.org/wiki/DOT_(graph_description_language))
- [Lots of Examples](http://graphviz.org/gallery/)


### rake

Rake is a language used to describe tasks and dependencies in the context of software build automation.

define tasks, with optional multiple dependencies

Resources
- [Rake on Wikpedia](https://en.wikipedia.org/wiki/Rake_(software))
- [Martin Fowler's Intro to Rake](https://martinfowler.com/articles/rake.html)


### AWK

AWK is a language for extracting and manipulating data from text files.

Resources
- [AWK on Wikipedia](https://en.wikipedia.org/wiki/AWK)


### XSLT... for EDN?

XSLT is a language for describing transformations of XML documents in XML syntax.

Perhaps, it'd be possible to create a similar language for transforming EDN documents in EDN?

Resources
 - (XSLT on Wikipedia)[https://en.wikipedia.org/wiki/XSLT]


### Board Games

https://en.wikipedia.org/wiki/Portable_Game_Notation
https://en.wikipedia.org/wiki/Smart_Game_Format


### ERD Diagrams

Like DOT, but, just for ERD diagrams. (A more limited domain might allow for a simpler syntax)


### Argument Parsing

“data driven ‘spec’ for what a commandline can take in”,
    What would the extracted data look like?

`./program -l -p 8080 -d /usr/logs -g a,b,c,d,e`


### ACL on Data Structures

Representing ACL rules on certain fields (to then be used to ‘filter’ data structures)


### Finite-State Machines
  https://en.wikipedia.org/wiki/Finite-state_machine




### End-to-End Testing

declarative format to run E2E tests

can do so w/ full support of language
but, since the domain is pretty limited (visit url, click button 'x', check for value 'y', etc.), could a data-driven syntax work?


https://github.com/teamcapybara/capybara
https://en.wikipedia.org/wiki/Selenium_(software)
https://developers.google.com/web/tools/puppeteer


### Chemical Formulas

Representing chemical formulas, so they can be balanced

https://www.webqc.org/balance.php

https://en.wikipedia.org/wiki/International_Chemical_Identifier


### Chemical Structural Formulas

Representing the molecular structure of a complex compound, for the purpose of then generating a diagram (one or more of: skeletal diagram, Lewis dot diagram, etc.)

https://en.wikipedia.org/wiki/Structural_formula

(perhaps similar to DOT, but, because it's an even more limited domain, you can make the language less general)

https://en.wikipedia.org/wiki/International_Chemical_Identifier

http://www.xml-cml.org/documentation/index.html


### Board Games

https://en.wikipedia.org/wiki/Portable_Game_Notation
https://en.wikipedia.org/wiki/Smart_Game_Format

