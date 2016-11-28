# Tricks in Coq

Some tips, tricks, and features in Coq that are hard to discover.

* `pattern` tactic
* `lazymatch` for better error messages
* `Search` vernacular variants
* `deex` tactic
* `::=` to re-define Ltac
* `learn` approach - see [Clément's thesis](http://pit-claudel.fr/clement/MSc/#org036d20e)
* tactics in terms
  * `ltac:(eauto)` for argument to proof
* `unshelve` tactical, especially useful with an eapply - good example use case is constructing an object by refinement where the obligations end up being your proofs with the values as evars, when you wanted to construct the values by proof
* `Search s -Learnt` for a search of local hypotheses excluding Learnt
* `unfold "+"` works
* `destruct matches` tactic
* maximally inserted implicit arguments are implicit even when for identifier alone (eg, `nil` is defined to include the implicit list element type)
* maximally inserted arguments can be defined differently for different numbers of arguments - undocumented but [`eq_refl` provides an example](https://github.com/coq/coq/blob/trunk/theories/Init/Logic.v#L290-L291)