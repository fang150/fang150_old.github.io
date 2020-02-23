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
Given function $$f: X \mapsto Y$$ and $$n$$ number of sample points, $$(x_1,y_1),\dots,(x_n,y_n)$$ sampled *i.i.d.* from distribution $$P(X,Y)$$, for each $$(x_i,y_i)$$, we want to find the counterfactual example $$(x^c_i,y^c_i)$$ such that,

1. $$d(x^c_i,x_i) \leq \epsilon $$, for some $$d(\cdot,\cdot)$$
2. $$f(x^c_i)=y^c_i$$, where $$y_i \neq y^c_i$$.

This can be done by solving the following optimization probblem:

$$ \arg\min_{x'_i}   \mathcal{L}(f(x'_i),y^c_i) +d(x_i,x'_i) $$


### Choice of Distance Measure

* Squared Euclidean Distance : 

\begin{align}  d(x_i,x^c_i) = \sum^d_{k=1} (x_{i,k} - x^c_{i,k})^2 \end{align}
* Scaled Squared Euclidean Distance :

\begin{align}  d(x_i,x^c_i) = \sum^d_{k=1} \frac{(x_{i,k} - x^c_{i,k})^2}{std_k(x)} \end{align}

* Scaled L1 Norm :

\begin{align}  d(x_i,x^c_i) = \sum^d_{k=1} \frac{|x_{i,k} - x^c_{i,k}|}{MAP_k} \quad \text{where,} 
 \end{align} 
\begin{align}  {MAP_k} = median_j (|x_{j,k}  -median_l(x_{l,k})|)
 \end{align} 

## Empirical Results

### LSAT Dataset
* prediction output : student's first-year average grade.
* features :  race, grade-point average prior to law school, and law
school entrance exam scores.


### Counterfactual Question
*“What would have to be changed to give a predicted score of 0?”*

### Squared Euclidean Distance Results

![Adversarial Example (FGSM)](/images/unnormalized_L2.png )
*(Counterfactual Examples generated using Squared Euclidean Distance. [Img Src.](https://arxiv.org/pdf/1711.00399.pdf) )*


### Scaled Squared Euclidean Distance Results

![Adversarial Example (FGSM)](/images/normalized_L2.png )
*(Counterfactual Examples generated using Scaled Squared Euclidean Distance. [Img Src.](https://arxiv.org/pdf/1711.00399.pdf) )*

### Scaled L1 Norm Results
![Adversarial Example (FGSM)](/images/normalized_L1.png )
*(Counterfactual Examples generated using Squared L1 Norm. [Img Src.](https://arxiv.org/pdf/1711.00399.pdf) )*


* Person 1: If your LSAT was 34.0, you would have an
average predicted score (0).
* Person 2: If your LSAT was 32.4, you would have an
average predicted score (0).
* Person 3: If your LSAT was 33.5, and you were ‘white’,
you would have an average predicted score (0).
* Person 4: If your LSAT was 35.8, and you were ‘white’,
you would have an average predicted score (0).
* Person 5: If your LSAT was 34.9, you would have an
average predicted score (0).



## Feasibility of Counterfactual Examples [Source](https://arxiv.org/pdf/1912.03277.pdf)

### Structural Causal Model

A causal model is a triple $$M= <U,V,F>$$ such that $$U$$ is a set model, and $$F$$ is a set of functions that determine the value of each $$v_i \in V$$


## References

* [Counterfactual Explanations without Opening the Black Box: Automated Decisions and the GDPR](https://arxiv.org/pdf/1711.00399.pdf)
* [Explaining and Harnessing Adversarial Examples](https://arxiv.org/pdf/1412.6572.pdf)