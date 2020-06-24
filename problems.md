### Argument Parsing

Thanks to [GraalVM](https://youtu.be/topKYJgv6qA) and tools like [Babashka](https://github.com/borkdude/babashka) and [native-image](https://github.com/taylorwood/clj.native-image), Clojure is now a viable langauge for writing commandline programs.

One of the needs of almost every commandline program is to handle commandline arguments, which is easy enough for adhoc programs, but doing it comprehensively is not exactly trivial (or at least, tedious).

What might a data-driven library for defining and parsing commandline arguments look like?

You might want to support boolean flags, single value arguments, list arguments, and more?  For example:  `./program -l -p 8080 -d /usr/logs -g a,b,c,d,e`

What would the extracted data look like?

Could this library generate man-docs as well?

...and provide feedback to a user for minor mistakes? (as with [spell-spec](https://github.com/bhauman/spell-spec))

...and do type coercion?

You might want to have your design make use of [spec](https://clojure.org/guides/spec), [spec-tools](https://github.com/metosin/spec-tools/blob/master/docs/02_data_specs.md) or [malli](https://github.com/metosin/malli/)


### ACL on Data Structures

Proper access-control is central to many web applications. Often, it's sufficient to model which users (or roles) have access to which resources. What might this look like in a declarative data-driven way?

In some applications, the access-control is more nuanced: different users might have different access to certain fields on certain resources (for example, on AirBnB, the location of a rental is approximate, but once you've booked that rental, it's exact). What might a data-driven way of defining per-field ACLs look like? How might it be used to 'filter' data-structures?


### End-to-End Testing (Selenium, etc.)

End-to-end tests are incredibly valuable at avoiding regressions in web applications, but, they're often tedious to write and maintain.

Existing APIs such as [Selenium](https://en.wikipedia.org/wiki/Selenium_(software)), [Puppeteer](https://developers.google.com/web/tools/puppeteer) and [Capybara](https://github.com/teamcapybara/capybara) are "fluent DSLs", giving you the full power of your programming language. But, since 90% of E2E tests consist of similar actions (visit url, click button 'x', check for value 'y', etc.), perhaps a data-driven syntax could be useful?


### BDD Testing (Gherkin)

Gherkin is a language used for writing BDD test cases. What might it look like as a data-driven Clojure DSL?

Resources
- [Gherkin on Wikipedia](https://en.wikipedia.org/wiki/Cucumber_(software)#Gherkin_language)
- [Gherkin Docs](https://cucumber.io/docs/gherkin/reference/)


### Software Build Automation (rake, make)

Rake is a language used to describe tasks and dependencies in the context of software build automation. It mixes a declarative DSL (defining tasks and dependencies) with imperative aspects (the task code itself). What might this look like as a data-driven Clojure DSL?

Resources
- [Rake on Wikpedia](https://en.wikipedia.org/wiki/Rake_(software))
- [Martin Fowler's Intro to Rake](https://martinfowler.com/articles/rake.html)


### DevOps (Ansible, Dockerfiles, etc.)

Several DSLs exist for declarative system configuration ([Ansible](https://en.wikipedia.org/wiki/Ansible_(software)), [Chef](https://en.wikipedia.org/wiki/Chef_(software)), [Terraform](https://en.wikipedia.org/wiki/Terraform_(software))). Various other components of the DevOps ecosystem also rely on declarative DSLs (ex. [Dockerfiles](https://docs.docker.com/engine/reference/builder/)).

Some of these might already be data-driven (Ansible uses YAML), but is this a good idea? Would using EDN be better?

Is there some problem within this space that would be particularly suited for a data-driven approach?


### Describing Language Grammars (Instaparse)

[Instaparse](https://github.com/engelberg/instaparse) is an existing Clojure library for describing context-free grammars, but it uses an [EBNF](https://en.wikipedia.org/wiki/Extended_Backus%E2%80%93Naur_form) based custom-string syntax. What might it look like if it was data-driven?


### Extracting Data from Text (AWK)

AWK is a language for extracting and manipulating data from text files. What might an AWK-like library look like as a data-driven Clojure DSL?

Resources
- [AWK on Wikipedia](https://en.wikipedia.org/wiki/AWK)


### Data Structure Transformations (XSLT)

XSLT is a language for describing transformations of XML documents in XML syntax.

Perhaps, it'd be possible to create a similar language for transforming EDN documents in EDN?

Resources
 - [XSLT on Wikipedia](https://en.wikipedia.org/wiki/XSLT)


### Describing Graphs (DOT / GraphViz)

DOT is a language used for describing graphs (the nodes-and-vertices kind, not the bar-chart kind). Tools like GraphViz consume DOT files and use various algorithms to render the graphs.

What would a data-driven Clojure version of DOT look like?

Resources
- [DOT on Wikipedia](https://en.wikipedia.org/wiki/DOT_(graph_description_language))
- [Lots of Examples](http://graphviz.org/gallery/)


### ERD Diagrams

ERD diagrams are useful for communicating data schemas. ERDs are essentially graphs, so, a syntax similar to DOT (see above) might be appropriate, but... because ERDs are a more limited domain, it might allow for a simpler syntax.


### Board Games

Chess and Go have notations for describing the moves of a game. What would these look like as EDN? Or, what might these look like for your favorite board game? Or, card games in general? Or, board games in general?

Resources
  - [Portable Game Notation](https://en.wikipedia.org/wiki/Portable_Game_Notation)
  - [Smart Game Format](https://en.wikipedia.org/wiki/Smart_Game_Format)


### Modeling Physical Systems (Modelica)

Modelica is a language used to model complex systems, such as the electrical and mechanical subsystems of a car. Modelica lets you define components (such as a "resistor") with input and output "pins", define equations that related the various inputs and outs (ex. `V = IR`), and then hook up and simulate a network of components. It can also be used to model System Dynamics.

Perhaps by choosing a specific subdomain (ex. electrical circuits, or [system dynamics](https://en.wikipedia.org/wiki/System_dynamics)) it can reduce the scope of your design.

Resources
  - [Modelica by Example (Book)](https://book.xogeny.com/)
  - [Modelica on Wikipedia](https://en.wikipedia.org/wiki/Modelica)



### Modeling Discrete Processes (Simul8)

Discrete event simulation is used to model the flow of work throughout a process, such as in assembly lines, hospitals, supply chains, etc.

The building blocks of these simulations are pretty standard and are likely amenable to a declarative syntax.

Resources
  - [Simul8 on Wikipedia](https://en.wikipedia.org/wiki/Simul8)


### Mathematical Notation

Clojure's existing syntax allows for writing functions to convert inputs -> outputs, but they are not true 'equations'. Clojure's syntax allows for defining specific computations (ex. weight, height => BMI), but aren't transparent enough to derive alternative calculations (ex. BMI, height => weight).

How could we represent mathematical formulae in Clojure to allow for easy human and programmatic generation and manipulation, to perhaps be used...
  - within a symbolic manipulation system (as in [Maple](https://en.wikipedia.org/wiki/Maple_(software)), [Mathematica](https://en.wikipedia.org/wiki/Wolfram_Mathematica), or [SageMath](https://en.wikipedia.org/wiki/SageMath))
  - within a simulation systems (like [Modelica](https://en.wikipedia.org/wiki/Modelica))
  - to convert to other formats (ex. [latex](https://en.wikipedia.org/wiki/TeX#Mathematical_example))


### Chemical Formulas

Like with math, chemists have [their own notations and standards](https://en.wikipedia.org/wiki/International_Chemical_Identifier) for representing chemical formulas. How might we represent chemical formulas as a Clojure data-driven DSL? (Perhaps, to feed into a system for [balancing chemical equations](https://www.webqc.org/balance.php)).

Or... instead of formulas, what about representing [molecular structures](https://en.wikipedia.org/wiki/Structural_formula), for the purpose of manipulating and then generating diagrams (ex. skeletal diagrams, Lewis dot diagrams, etc.)? These are graphs, so, perhaps a solution might look similar to the DOT syntax (see above), but because it's a more limited domain, you can make the syntax less general. [Chemical Markup Language](http://www.xml-cml.org/documentation/index.html) might be a good place to look for inspiration.


### Musical Notation

[Modern staff notation](https://en.wikipedia.org/wiki/Musical_notation#Modern_staff_notation) isn't the only form of music notation; different subsets of music have their own notations, such as [percussion notation](https://en.wikipedia.org/wiki/Percussion_notation) and [tablatures](https://en.wikipedia.org/wiki/Tablature).

Several ways of representing music for programmatic use already exist, but, could Clojure's EDN be of any use?

Uses might include: live coding music, programmatic composition and/or manipulation of songs, etc.

Resources
 - [Overtone](http://overtone.github.io/)
 - [ABC Notation](https://en.wikipedia.org/wiki/ABC_notation)
 - [LilyPond](https://en.wikipedia.org/wiki/LilyPond)
 - [MusicXML](https://en.wikipedia.org/wiki/MusicXML)

