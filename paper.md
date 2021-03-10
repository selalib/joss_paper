---
title: 'SeLaLib: A modular library for kinetic and gyrokinetic simulations of plasmas in fusion energy devices by semi-Lagrangian or particle-in-cell methods.'
tags:
  - fortran
  - fusion
  - plasma
  - vlasov
  - particle-in-cell
  - semi-lagrangian
authors:
  - name: Author1^[Custom footnotes for e.g. denoting who the corresponding author is can be included like this.]
    orcid: 0000-0003-0872-7098
    affiliation: "1, 2" # (Multiple affiliations must be quoted)
  - name: Author Without ORCID
    affiliation: 2
  - name: Author with no affiliation
    affiliation: 3
affiliations:
 - name: Université de Strasbourg
   index: 1
 - name: Institution Name
   index: 2
 - name: Independent Researcher
   index: 3
date: 9 Mars 2020
bibliography: paper.bib

# Optional fields if submitting to a AAS journal too, see this blog post:
# https://blog.joss.theoj.org/2018/12/a-new-collaboration-with-aas-publishing
aas-doi: 10.3847/xxxxx <- update this with the DOI from AAS once you know it.
aas-journal: Astrophysical Journal <- The name of the AAS journal.
---

# Summary

The SeLaLib software library is a modular library for kinetic and
gyrokinetic simulations of plasmas in fusion energy devices by
semi-Lagrangian or particle-in-cell methods.

SeLaLib contains a collection of individual building blocks for the
parallel simulation of the Vlasov equations and the gyrokinetic equation
either based on semi-Lagrangian schemes or particle methods. Besides
numerical algorithms the library provides low-level utilities,
input-output modules as well as parallelization strategies. Moreover, a
collection of simulations for typical test cases with various
discretization schemes supplements the library.

# Statement of need

The SeLaLib project arose from the need of researchers to develop
numerical methods with simplified test cases while also having
independently tested modules that would facilitate gradual changes in
existing production code. While originally envisioned to be specialized
on the semi-lagrangian method, the abstractions that we have built can
be used with other types of approaches, such as particle-in-cell.

# Mathematics

- Vlasov equation:
$$
\partial_t f(t,\mathbf{x},\mathbf{v}) + \mathbf{v}\nabla_{\mathbf{x}} f(t,\mathbf{x},\mathbf{v}) + \frac{q}{m} \mathbf{E}(t,\mathbf{x}) \nabla_{\mathbf{v}} f(t,\mathbf{x},\mathbf{v}) = 0
$$

$$-\Delta \phi(t,\mathbf{x}) =  1- \rho(t, \mathbf{x})$$

- Vlasov--Maxwell

$$\begin{aligned}
    &&\partial_t f(t,x,\mathbf{v}) + v_1 \partial_{x_1} f(t,x,\mathbf{v}) + \mathbf{E}(t, x) \cdot \nabla_{\mathbf{v}} f(t, x, \mathbf{v}) + B v_2 \partial_{v_1} f(t,x,\mathbf{v}) - B v_1 \partial_{v_2} f(t,x,\mathbf{v}) = 0, \\
    && \partial_t B(t,x) = - \partial_{x_1} E_2, \\
    && \partial_t E_2 = - \partial_{x_1} B - \int_{\mathsf{R}^1} v_2 f(t, x, \mathbf{v}) \, \mathrm{d}v,\\
    && \partial_t E_1 = - \int_{\mathsf{R}^1} v_1 f(t, x, \mathbf{v}) \, \mathrm{d}v.\end{aligned}$$

- Guiding center

$$\partial_t f(t,r,\theta) - \frac{\partial_{\theta}\Phi(r, \theta)}{r} \partial_r f(t,r,\theta) +  \frac{\partial_{r}\Phi}{r} \partial_{\theta} f  = 0.$$

# Citations

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

If you want to cite a software repository URL (e.g. something on GitHub without a preferred
citation) then you can do it with the example BibTeX entry below for @fidgit.

For a quick reference, the following citation commands can be used:
- `@author:2001`  ->  "Author et al. (2001)"
- `[@author:2001]` -> "(Author et al., 2001)"
- `[@author1:2001; @author2:2001]` -> "(Author1 et al., 2001; Author2 et al., 2002)"

# Figures

Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
and referenced from text using \autoref{fig:example}.

Figure sizes can be customized by adding an optional second parameter:
![Caption for example figure.](figure.png){ width=20% }

# Acknowledgements

Much of `SeLaLib` was implemented by Edwin Chacon-Golcher while he was supported by Inria through the AdT (Aide au développement technologique) selalib of the center Nancy-Grand Est.
We acknowledge contributions from Aliou Diouf, Samuel Santis and Raphael Blanchard while funded also by Inria.


# References
