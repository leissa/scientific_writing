# Scientific Writing

## General Philosophy

* Optimize for reader comprehension, not for displaying sophistication.

  * The reader should never need to guess:

    * what a term means,
    * why something matters,
    * or how a section connects to the previous one.

* Scientific writing is not a puzzle game.

  * The goal is not to impress the reader with unnecessary complexity.
  * The goal is to communicate ideas precisely and efficiently.

* Every sentence should be necessary.

* Break these rules if there is a good reason to do so.

---

# Structure and Organization

## Organize Top-Down

* Design your thesis and explanations in a top-down fashion.

  * Present the big picture before the details.
  * Explain why something matters before explaining how it works.

* Prepare the reader for the next section, paragraph, or idea.

  * Guide the reader's expectations and attention.

* Keep each sentence, paragraph, and section focused on a single main idea.

* Organize material in a straightforward and logical way.

  * `\paragraph`, example sections, etc. are your friends.

## Dependencies and Ordering

* Build a dependency graph of your terms and contents before writing.

  * Derive a partial order from it.

* Avoid unnecessary forward references.

  * Readers should rarely need information from later sections to understand the current discussion.

## Introductions and Abstracts

* The introduction should answer:

  * What problem is being solved?
  * Why does it matter?
  * Why is it difficult?
  * What is the key idea?
  * What are the main results?

* An abstract should:

  * state the problem,
  * summarize the approach,
  * and present the main result.

---

# Terminology and Notation

## Terminology

* Keep an eye on your terminology.

  * Use the same word for the same thing.
  * Avoid introducing multiple names for the same concept.
  * Don't try to be inventive.

* Define specialized or potentially ambiguous terminology before relying on it.

  * Make sure any term you define is only used **after** it has been defined.

* Distinguish clearly between:

  * observations,
  * hypotheses,
  * implementation details,
  * and proven results.

* State assumptions and limitations explicitly.

  * Readers should know when a claim does not apply.

## Notation

* Reuse standard notation whenever possible.

  * Custom notation has a cognitive cost.

* Introduce notation gradually.

  * Avoid presenting multiple new symbols, terms, or abstractions at once.

* Before presenting a formal definition:

  * explain the intuition,
  * explain the purpose,
  * and provide a small example when possible.

---

# Style

## Keep Things Simple

* Prefer simple, direct language.

  * Use short words and simple sentence structures when possible.

  Bad:

  > The object under consideration is displaced horizontally.

  Good:

  > The ball moves sideways.

* Keep paragraphs short.

* Avoid buzzwords, clichés, and slang.

* Avoid excess, in length or style.

* Omit unnecessary material.

* Be specific, not vague or abstract.

* Don't show off.

## Use Examples

* Use examples.

  * Use dedicated example blocks:

    > **Example 3.5.** With this algorithm we obtain Listing 3.2 from Listing 3.1.

  * Often an informative example is just a few words:

    > Special cases, such as the empty set, need to be handled separately.

---

# Agency, Precision, and Claims

## Every Story Needs a Hero

* Prefer active over passive voice.

  Bad:

  > The loop is unrolled four times.

  By whom? The programmer, the compiler, some cool programming technique?

  Good:

  > The compiler unrolls the loop four times.

  Bad:

  > The following theorem can now be proved.

  Better:

  > We now prove the following theorem.

  * "We" (the authors/the author and the reader) is usually a better alternative than passive voice, but often there is an even better subject:

    Bad:

    > X is simplified to Y, as Rule R is triggered.

    Better:

    > We apply Rule R to simplify X to Y.

    Even better (only makes sense when using inference rules etc.):

    > Rule R triggers and simplifies X to Y.

## Please Stop Overusing "Can"

* In scientific writing, "can" is often unnecessary noise.

  Entire theses read like speculative fiction:

  > We can now define...
  >
  > We can then observe...
  >
  > We can use...
  >
  > We can state...

  Wonderful. Humanity *can* colonize Mars too. Did you actually do the thing or not?

  Bad:

  > We can then generate LLVM code.

  Does the compiler actually emit LLVM code or is this merely a theoretical possibility?

  Good:

  > Then, the compiler emits LLVM code.

  Bad:

  > We can express this relation in the following code.

  Better:

  > We express this relation in the following code.

  Even better:

  > The following code expresses this relation.

  * Bottom line: Use modal verbs ("can", "may", "could") precisely.

    * Distinguish between:

      * implemented behavior,
      * theoretical capability,
      * and future work.

## Don't Judge

* Whether a speedup is great or tremendous is a matter of opinion:

  Bad:

  > The benchmark shows a tremendous speedup.

  Good:

  > The benchmark shows a significant speedup of 20%-40%.

* Whether something is simple is a matter of opinion at best and borderline offensive if the reader does not understand it at worst:

  Bad:

  > The problem can be solved with the following simple algorithm.

  Good:

  > The following algorithm solves this problem.
  
* For the same reasons avoid: "obviously" "trivially" and "clearly"

---

# Technical Writing Details

## Sentences and References

* Don't start a sentence with math or code.

  Bad:

  > m denotes the mass.

  Good:

  > In Newton's laws of motion, m denotes the mass.

  Bad:

  > rec recurses over the graph.

  Good:

  > The function rec recurses over the graph.

* Make sure that a sentence still makes sense if citations are elided (`\citet`/`\textcite` are your friends).

  Bad:

  > As [23] points out ...

  Good:

  > As Dijkstra [23] points out ...

## Figures and Pseudo-Code

* A good figure is often clearer than a long textual explanation.

  * Invest time in figures.

* Only use pseudo-code if you really need to bring a certain point across, such as arguing about asymptotic runtime.

  * Prefer math (inference rules, mathematical functions, ...) over pseudo-code.
  * Often it is better to show a stripped-down version of the real code.
  * Sometimes it is better to walk through an example accompanied by figures.

---

# Further Resources

* ["How to write a great research paper"](https://www.microsoft.com/en-us/research/academic-program/write-great-research-paper/)
  by *Simon Peyton Jones*

* ["Mathematical Writing"](https://jmlr.csail.mit.edu/reviewing-papers/knuth_mathematical_writing.pdf)
  by *Donald E. Knuth*, *Tracy Larrabee*, and *Paul M. Roberts*

* ["Writing for Computer Science"](https://link.springer.com/book/10.1007/978-1-4471-6639-9)
  by *Justin Zobel*

* ["How to Write Papers So People Can Read Them"](https://www.youtube.com/watch?v=L_6xoMjFr70)
  by *Derek Dreyer*

* ["How to Have Your Abstract Rejected"](http://www.sigplan.org/Resources/Advice/VanLeunen-Lipton/)
  by *Mary-Claire van Leunen* and *Richard Lipton*

* ["Advice to Authors of Extended Abstracts"](http://www.sigplan.org/Resources/Advice/Pugh/)
  by *William Pugh*

* ["What it's like to be a POPL referee; or how to write an extended abstract so that it is more likely to be accepted"](https://dl.acm.org/doi/10.1145/14947.14955)
  by *Mark Wegman*
