# Awesome GHC Talks

A collection of talks and conferences about Haskell

## Effects

### A Series of Unfortunate Effects – Robert M. Avram

[Video](https://www.youtube.com/watch?v=y5jZnMImbMY)

Involved libraries: N/A

The very essence of functional programming relies on a fairly simple premise:
write side-effectless programs, so that you can reason about them equationally.
Side-effects however are predominant in every program that... well, does
something useful. In light of this, the modelling of effects in functional
programs has become a fairly active domain of study. From stacked effects,
to horizontal ones; from transformers to free monads and so on. Every
effect model, though joyfully they may seem, have some rather unfortunate
consequences. 

In this talk, I'd like to share with you some of these effect
models and exemplify both their joyful and unfortunate nature.

### Effects for Less – Alexis King

[Video](https://www.youtube.com/watch?v=0jI-AlWEwYI)

Involved libraries:

- [`eff`](https://github.com/hasura/eff)

(No video description available)

## Lazy Evaluation

### Thunks, Sharing, Laziness: The Haskell Heap Visualized – Joachim Breitner

[Video](https://www.youtube.com/watch?v=I4lnCG18TaY)

Involved libraries:

- [`ghc-vis`](https://hackage.haskell.org/package/ghc-vis)

Haskell is a high-level, declarative language that frees you from worrying about
how your programs are actually executed, and that is a good thing. Nevertheless,
it can be quite useful to know how things work under the hood.

In his talk, our guest speaker Joachim takes you on a tour to the heap of a
running Haskell program, where you’ll get to see the shape of data types,
observe sharing and laziness, distinguish infinite and cyclic data structures,
and watch a lazy tree grow as a recursive function gets memoized.

### Being lazy without being bloated – Edsko de Vries

[Video](https://www.youtube.com/watch?v=7t6wt7ByBWg)

Involved libraries:

- [`nothunks`](https://hackage.haskell.org/package/nothunks)

Laziness is one of Haskell's most distinctive features. It is one of the two
features of functional programming that "Why Functional Programming Matters"
identifies as key to modularity, but it is also one of the most frequently cited
features of Haskell that programmers would perhaps like to change. One reason
for this ambivalence is that laziness can give rise to space leaks, which can
sometimes be fiendishly difficult to debug.

In this talk we will present a new library called `nothunks` which can be used
to test for the absence of unexpected thunks in long-lived data; when an
unexpected thunk is found, a "stack trace" is returned identifying precisely
where the thunk is ("the second coordinate of a pair in a map in a list in type
T"). In combination with QuickCheck, this can be used to test that an API does
not create any thunks when it shouldn't and thunks that are created are easily
identified and fixed. Whilst it doesn't of course fix all space leaks, it can
help avoid a significant proportion of space leaks due to excessive laziness.
