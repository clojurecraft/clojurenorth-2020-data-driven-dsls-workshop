




Pick one of the below.

give some examples of how you would use it.


- The task is *not* to implement the system, it is just to design the data-driven API.

- You do not have to implement the entire language, just use the existing language as inspiration.


We recommend choosing a problem domain that you are at least somewhat familiar with (to better understand how your syntax might be used in practice).

If you have some other problem domain you'd like to design a data-driven API for, go ahead!



 ### Modelica (modeling physical systems)

 Modelica is a language used to model complex systems, such as the electrical and mechanical subsystems of a car. Modelica lets you define components (such as a "resistor") with input and output "pins", define equations that related the various inputs and outs (ex. `V = IR`), and then hook up and simulate a network of components.

 Resources
  - [Modelica by Example (Book)](https://book.xogeny.com/)
  - [Modelica on Wikipedia](https://en.wikipedia.org/wiki/Modelica)


### Gherkin

Gherkin is a language used for writing BDD test cases.

Resources
- [Gherkin on Wikpedia](https://en.wikipedia.org/wiki/Cucumber_(software)#Gherkin_language)
- [Gherkin Docs](https://cucumber.io/docs/gherkin/reference/)


### Describing Language Grammars (Instaparse)

[Instaparse](https://github.com/engelberg/instaparse) is an existing Clojure library for describing context-free grammars, but it uses an [EBNF](https://en.wikipedia.org/wiki/Extended_Backus%E2%80%93Naur_form) based custom-string syntax. What might it look like if it was data-driven?


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
- [Rake on Wikipedia](https://en.wikipedia.org/wiki/Rake_(software))
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
