---
title: 'Literature on the Empty Domain'
date: 2019-03-19
permalink: /posts/2019-03-19-Literature-on-the-Empty-Domain
tags:
  - formal logic
  - empty domain
  - philosophical logic
---

The state of play in the empty domain, pun-intended, seems to be this: nobody has really gotten a generally satisfactory proof theory and semantics for ([non-free](https://plato.stanford.edu/entries/logic-free/)) _inclusive logic_—logic inclusive of the empty domain. I think that getting a satisfactory semantics for it stands to benefit discussions of _metaphysical nihilism_—the view that, possibly, there are no concrete entities—a priori justification for contingent claims, and of proof-theoretic and model-theoretic semantics for logic.

So in a kind of literature survey, I want to lay out the currently-available approaches to inclusive logic. The terminology 'inclusive logic' comes from Quine's 1954. My treatment here largely follows the quasi-literature survey in ([Williamson, 1999](https://onlinelibrary.wiley.com/doi/abs/10.1111/1467-8284.00140)). Since it has been twenty years (now twenty-four!), I thought that the state of play was worth reviewing again in an accessible, public-domain format.

- [Mostowski's 1951 Trick](https://www.jstor.org/stable/2266682): Interpret the value of every formula containing free variables as the empty set, and the value of all formulas without free variables as either true or false. In this case, all universally-closed formulas are true, and all existentially-closed formulas are false.
  - Motivation: Universally-closed formulas should come out vacuously true, whereas existentially-closed formulas should come out false.
    - We might also think that formulas containing free variables should come out true, since the meaning of these is seemingly odd if the empty domain is allowed. In such cases, we have a kind of vacuous quantification—quantification where the bound variable does not occur in the formula occurring within the scope of the quantifier, as in (∀x)(Fb). As vacuous quantifiers are redundant, they should not weigh on whether the formula is true or not. As such, these formulas should be counted as false in the empty domain, just as Fb is.
  - Problem: The rule of _modus ponens_ is not truth-preserving in the empty domain (as Mostowski himself pointed out). The formulas (φ∨¬φ) and (φ∨¬φ)→(∃x)(φ∨¬φ) come out true, but (∃x)(φ∨¬φ) does not. We only get _modus ponens_ in a restricted form (it is truth-preserving whenever φ and ψ share all the free variables—then we do have that φ and φ→ψ imply ψ).
- [Quine's 1954 Trick](https://www.jstor.org/stable/2268615): Mark every formula with an intial universal quantifier (∀x)(φ) as true, and mark every formula with an initial existential quantifier (∃x)(φ) as false. Apply truth-functional considerations elsewhere.
  - Motivation: for this is that universally-closed formulas should come out vacuously true, whereas existentially-closed formulas should come out false.
    - Also, we want to preserve extensionality: vacuous quantifiers (∀x)(Fb) are justified by the equivalence (∀x)(Fb)↔(∀x)(Fb∧(Fx→Fx)). And this sytem preserves extensionality (in that it preserves the vacuity of vacuous quantifiers).
  - Problem: Universally-closed contradictions (∀x)(φ∧¬φ) come out true and existentially-closed tautologies (∃x)(φ∨¬φ) come out false. But it seems that a closed tautology should be true, and a closed contradiction should be false.
- [Schneider's 1958 Trick](https://eudml.org/doc/114803): First, we define satisfaction under _limited interpretations_—interpretations of free predicate and individual variables in a given formula φ only.  Second we consider _unlimited interpretations_—interpretations of all predicate and individual variables in the language, not just those occurring in a given formula.
  - Explanation of Limited Interpretations: In limited interpretations over the empty domain, any _open_ formula comes out true because there are no assignments of their free variables to anything—there are no functions from variables to elements of the domain. As such, all open formulas are vacuously satisfied. Limited interpretations of closed formulas, in contrast, still operate in the truth-functional way, as do ones of universally-closed formulas (which are true) and of existentially-closed formulas (which are false).
  - Motivation for Limited Interpretations: In limited-interpretation satisfaction in the empty domain, we have satisfaction in the empty domain roughly as on Quine's trick. Open formulas are all valid, and we can treat quantifiers truth-functionally as on Quine's trick.
  - Problem for Limited Interpretations: The odd formulas that should not be true, like universally-closed contradictions (∀x)(φ∧¬φ), come out true, while the odd formulas that should not be false, like existentially-closed tautologies (∃x)(φ∨¬φ), come out false.
  - Explanation of Unlimited Interpretations: In unlimited interpretations, we interpret _all_ predicate and individual variables. But in the empty domain, there is no assignment for such formulas. As such, any formula is vacuously true in the empty domain under an unlimited interpretation.
  - Motivation for Unlimited Interpretations: Since logical truth is usually characterized as true in every non-empty domain, including the empty domain does not change what counts as logically true: for every formula that is true in all non-empty domains is also true in the empty domain under unlimited interpretations. So we get as universally valid, in all domains including empty ones, all formulas that are valid in non-empty domains. In this approach to empty-domain logic, we keep as logical truths formulas like (∃x)(φ∨¬φ) and (∀x)(Fx)→(∃x)(Fx), while rejecting as false formulas like (∀x)(φ∧¬φ).
  - Problem for Unlimited Interpretations: Under unlimited interpretations, formulas like φ∧¬φ and (∃x)(Fx) come out true in the empty domain (though not as true in all domains). But the first example seems like it should come out false in every domain, and the second seemingly should come out false in the empty domain (on the intended meaning of "(∃x)(Fx)"). So we preserve what we might want from non-empty domain logic, but at the cost of undermining practically any intended interpretation of truth in the empty domain (besides the deeply implausible one on which everything is true because everything is vacuous).

These are the approaches that do not rely on inner-domain and outer-domain semantics that are typical in free logic (and in semantics for quantified modal logic). These are also the alternatives that preserve compositionality—the truth-conditions of complex formulas is given recursively through the truth-conditions of their constituent formulas (so that we do not get, for instance, that φ∨¬φ is true while φ and ¬φ are both false).

I believe that covers the available approaches. I am, of course, fallible. So if you know of others that should be added to the list, let me know!