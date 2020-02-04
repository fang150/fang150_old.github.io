---
title: "Proof by Contradiction"
date: 2020-02-04
tags: [math]
categories: [foundation]
excerpt: "Idea of proof by contradiction."
mathjax: "true"
---


## Truth Table For "If...., then...."

| A | B | If A, then B |
|:--------|:-------:|--------:|
| T   | T   | T   |
| T   | F   | F   |
|----
| F   | T   | T   |
| F   | F   | T   |
|=====
{: rules="groups"}


## Pattern

We want to proof "If A then B"

1. Assume A and ~B (A is True and B is False)
2. Derive (A is True and B is False) to a contradiction.
    1. Possibly contradicting to original assumptions
    2. or contradicting to facts, e.g. 2>1
3. We then proof "If A then B" by contradiction


## Reason

1. The proposition "If A then B" is False only when A = True and B = False
2. Under condition either 1. or 2. , we have the conclusion that  (A = True and B = False) is False and the complement of (A = True and B = False) always leads to "If A, then B" is True.
3. Thus, we then proof "If A then B" by contradiction. That is, (A $$\cap$$ ~B = $$\phi$$ ).