---
title: "Counterfactual Explanations"
date: 2020-02-15
tags: [Causality]
categories: [literature review]
excerpt: "Idea of Counterfactual Explanations."
mathjax: "true"
---


## Counterfactual Explanations


*"You were denied a loan because your annual income was £30,000. If your income had been £45,000, you would have been offered a loan."*


[They](https://arxiv.org/pdf/1711.00399.pdf) define Counterfactual Explanations as statements taking the form:

*"Score p was returned because variables V had values (v1,v2,...) associated with them. If V instead had values (v1',v2',...), and all other variables had remained constant, score p' would have been returned."*

## Adversarial Examples versus Counterfactual Examples


### Adversarial Example
* $$x_{adv}=x+\epsilon \times\text{sign(} \nabla f_{x}(x,y)\text{  )}$$
* Invisible to human eyes (see the Figure below.). 

![Adversarial Example (FGSM)](/images/adv_example.png )
*(Adversarial Example generated using FGSM method. [Img Src.](https://arxiv.org/pdf/1412.6572.pdf) )*

### Counterfactual Example

* $$x_{c}=x+v$$, where $$v$$ only modifies few variables to $$x$$. 


## Problem Formulation
Given function $$f: X \mapsto Y$$ and $$n$$ number of sample points, $$(x_1,y_1),\dots,(x_n,y_n)$$ sampled *i.i.d.* from distribution$$P(X,Y)$$, for each sample point $$(x_i,y_i)$$, we want to find the counterfactual example $$(x^c_i,y^c_i)$$ where $$d(x^c_i,x_i)$$ such that $$f(x^c_i)=y^c_i$$ and $$y_i \neq y^c_i$$.



## References

* [Counterfactual Explanations without Opening the Black Box: Automated Decisions and the GDPR](https://arxiv.org/pdf/1711.00399.pdf)
* [Explaining and Harnessing Adversarial Examples](https://arxiv.org/pdf/1412.6572.pdf)