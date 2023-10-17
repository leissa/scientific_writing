# Scientific Writing

## General Remarks

* Keep an eye on your terminology
* Use the same word for the same thing
    * Don't try to be inventive
* Don't make statements without proof, experimental validation or citation
* Never use a term that is not common computer science knowledge or explicitly defined
* Make sure any term you define is only used **after** it has been defined
* Avoid forward references,
    * Build a dependency graph of your terms/contents before and derive a partial order from it
* Try to design your thesis in a top-down fashion, explain things in a top-down fashion
* Try to Prepare the reader for the upcoming section/paragraph
    * Influence the readers mindset in the right direction

## Style

* Every sentence should be necessary
* Have one idea per sentence or paragraph and one topic per section.
* Have a straightforward, logical organization.
    `\paragraph`, example sections (see below), etc. are your friends.
* Use short words.
* Prefer simple words.
* Use short sentences with simple structure.

    Bad:
    > The object under consideration is displaced horizontally.

    Good:
    > The ball moves sideways.
* Keep paragraphs short.
* Avoid buzzwords, clichés, and slang.
* Avoid excess, in length or style.
* Omit unnecessary material.
* Be specific, not vague or abstract.

* Use examples.
    * Use dedicated example blocks:
        > **Example 3.5.** With this algorithm we obtain Listing 3.2 from Listing 3.1.
    * Often an informative example is just a few words:
        > Special cases, such as the empty set, need to be handled separately.

* Every story needs a hero (prefer active over passive voice)!

    Bad:
    > The loop is unrolled four times.

    By whom? The programmer, the compiler, some cool programming technique?

    Good:
    > The compiler unrolls the loop four times.

    Bad:
    > The following theorem can now be proved.

    Better:
    > We now prove the following theorem.

    * "We" (the authors/the author and the reader) is usually a better alternative than passive voice but often there is even a better subject:

        Bad:
        > X is simplified to Y, as Rule R is triggered.

        Better:
        > We apply Rule R to simplify X to Y.

        Even better (only makes sense when using inference rules etc.):
        > Rule R triggers and simplifies X to Y.

* Please stop overusing "can"!

    Either you do something or not.

    Bad:
    > We can then generate LLVM code.

    Okay, does this mean you actually *do* emit LLVM code or is this something you could theoretically do but haven't implemented yet?

    Good:
    > Then, the compiler emits LLVM code.

    Bad:
    > We can express this relation in the following code.

    Better:
    > We express this relation in the following code.

    Even better:
    > The following code expresses this relation.

* Don't judge:

    Bad:
    > The benchmark shows a tremendous speedup.

    Good:
    > The benchmark shows a significant speedup of 20%-40%.

    Bad:
    >The problem can be solved with the following simple algorithm.

    Use active voice, remove "can", and whether the algorithm is simple or not is something the reader has to decide on their own:

    Good:
    > The following algorithm solves this problem.

* Don't start a sentence with math or code.

    Bad:
    > m denotes the mass.

    Good:
    > In Newton's laws of motion, m denotes the mass.

    Bad:
    > rec recurses over the graph.

    Good:
    > The function rec recurses over the graph.

* Make sure that a sentence makes sense, if you elide citations (`\citet`/`\textcite` is your friend):

    Bad:
    > As [23] points out ...

    Good:
    > AS Dijkstra [23] points out ...

* Good figures are a lot of work but often way better and clearer than complicated text that nobody understands.
* Only use pseudo-code, if you **really** need to bring a certain point across such as arguing about the asymptotic runtime.
    * Prefer math (inference rules, mathematical functions, ...) over pseudo-code.
    * Often it is better to just show a stripped-down version of the real code.
    * Sometimes it's better to run through an example with accompanying figures.

* Break these rules if there is a good reason to do so.

## Further Resources

* ["How to write a great research paper"](https://www.microsoft.com/en-us/research/academic-program/write-great-research-paper/)
    by *Simon Peyton Jones*
* ["Mathematical Writing"](https://jmlr.csail.mit.edu/reviewing-papers/knuth_mathematical_writing.pdf)
    by *Donald E. Knuth*, *Tracy Larrabee*, and *Paul M. Roberts*
* ["Writing for Computer Science"](https://link.springer.com/book/10.1007/978-1-4471-6639-9)
    by *Justin Zobel*
* [ How to Write Papers So People Can Read Them ](https://www.youtube.com/watch?v=L_6xoMjFr70)
    by *Derek Dreyer*
* [How to Have Your Abstract Rejected](http://www.sigplan.org/Resources/Advice/VanLeunen-Lipton/)
    by *Mary-Claire van Leunen*, and *Richard Lipton*
* [Advice to Authors of Extended Abstracts](http://www.sigplan.org/Resources/Advice/Pugh/)
    by *William Pugh*
* [What it's like to be a POPL referee; or how to write an extended abstract so that it is more likely to be accepted](https://dl.acm.org/doi/10.1145/14947.14955)
    by *Mark Wegman*
