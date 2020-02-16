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

*"One of the more challenging aspects of Adversarial Perturbations
is that these small perturbations of an image are barely human perceptible,
but result in drastically different classifier responses. Informally, this
appears to happen because the newly generated images do not lie in the
“space of real-images,” but slightly outside it. This phenomenon serves
as an important reminder that when computing counterfactuals by
searching for a close possible world, it is at least as important that the
solution found comes from a “possible world” as it is that it is close to the
starting example. "*


### Adversarial Example
* $$x_{adv}=x+\epsilon \times\text{sign(} \nabla f_{x}(x,y)\text{  )}$$
* Invisible to human eyes (see the Figure below.). 

![Adversarial Example (FGSM)](/images/adv_example.png )
*(Adversarial Example generated using FGSM method. [Img Src.](https://arxiv.org/pdf/1412.6572.pdf) )*

### Counterfactual Example

* $$x_{c}=x+v$$, where we desire $$v$$ only changes few variables to $$x$$.


## References

* [Counterfactual Explanations without Opening the Black Box: Automated Decisions and the GDPR](https://arxiv.org/pdf/1711.00399.pdf)
* [Explaining and Harnessing Adversarial Examples](https://arxiv.org/pdf/1412.6572.pdf)