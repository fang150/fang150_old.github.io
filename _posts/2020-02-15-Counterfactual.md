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

## Adversarial Perturbations and Counterfactual Explanations

### Adversarial Example
* $$x_{adv}=x+\epsilon \times\text{sign(} \nabla f_{x}(x,y)\text{  )}$$
* Invisible to human eyes (see the Figure below.). 

![Adversarial Example (FGSM)](/images/adv_example.png )
*(Adversarial Example generated using FGSM method. [Img Src.](https://arxiv.org/pdf/1412.6572.pdf) )*

## References

* [Counterfactual Explanations without Opening the Black Box: Automated Decisions and the GDPR](https://arxiv.org/pdf/1711.00399.pdf)
* [Explaining and Harnessing Adversarial Examples](https://arxiv.org/pdf/1412.6572.pdf)