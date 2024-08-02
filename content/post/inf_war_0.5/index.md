---
title: Influncer War 0.5
subtitle: When Gaussian kicks in

# Date published
date: 2024-08-02

# Date updated
lastmod: '2024-08-02T15:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: true

authors:
  - admin
---

We consider a slightly more sophisticated cognitive model than simply taking the average of Big and Small. Our victim has become more rational; it does not want to accept information that is too extreme or biased. Moreover, it also has its own idea before the game starts, which is represented by {{< math >}}$ x_{0} ${{< /math >}}. Let us also transform the dicrete space of [Influencer War 0](https://yan-cheng-1113.github.io/yan-cheng-1113-github.io/post/inf_war_0/) into a continuous one.

Given reports {{< math >}}$ x_{b} ${{< /math >}} and {{< math >}}$ x_{s} ${{< /math >}} from Big and Small, the victim chooses {{< math >}}$ \sigma_{g} ${{< /math >}} and {{< math >}}$ \sigma_{s} ${{< /math >}}, then it calculates {{< math >}}$$ g_{b}=e^{-\frac{(x_{b}-x_{0})^{2}}{2\sigma^{2}_{b}}} \\ g_{s}=e^{-\frac{(x_{s}-x_{0})^{2}}{2\sigma^{2}_{s}}} $${{< /math >}} Here, {{< math >}}$ g_{b} ${{< /math >}} and {{< math >}}$ g_{s} ${{< /math >}} represent "how much the victim trusts Big and Small based on the articles they picked". The victim updates its opinion by calculating {{< math >}}$$ v=\frac{x_{0}+x_{b}\cdot g_{b} + x_{s}\cdot g_{s}}{1+g_{b}+g_{s}} $${{< /math >}}


We ran best-response dynamics using the 1-d verison of the game. Here we showcase one of the games:
<figure>
  <img src="sd_10.png" alt="sd_10"/>
  <figcaption>Game development with victim's prior at 0, B at 50, S at -50, and SD=10 for both players.</figcaption>
</figure>
The game converges at Big choosing {{< math >}}$ 10 ${{< /math >}} and Small choosing {{< math >}}$ -10 ${{< /math >}}, suggesting that the converging points of the game seem to be closely related to the standard deviation {{< math >}}$ \sigma ${{< /math >}}. We fixed other parameters and ran more best-response simulations with different {{< math >}}$ \sigma ${{< /math >}}, here are the results :
<figure>
  <img src="table1.jpg" alt="table1"/>
</figure>
In the table, {{< math >}}$ x^{\dagger}_{1} ${{< /math >}} and {{< math >}}$ x^{\dagger}_{2} ${{< /math >}} represent {{< math >}}$ B ${{< /math >}} and {{< math >}}$ S ${{< /math >}}, respectively. {{< math >}}$ s_{1} ${{< /math >}} is {{< math >}}$ \sigma_{b} ${{< /math >}} and {{< math >}}$ s_{2} ${{< /math >}} is {{< math >}}$ \sigma_{s} ${{< /math >}}. We can observe that when the same standard deviation is applied, the convergence of the game is dominated by this value.

It is not yet clear whether the game under this setting, when extended to {{< math >}}$ n ${{< /math >}} players, is still a potential game. 
