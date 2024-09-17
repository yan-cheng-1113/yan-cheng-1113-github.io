---
title: Influncer War 1.0
subtitle: Averaging with punishment

# Date published
date: 2024-09-010

# Date updated
lastmod: '2024-09-10T15:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: true

authors:
  - admin
---

Let us revisit the naive model where the victim simply takes the average of influencers' reports and give it a small upgrade. This time, we include {{< math >}}$ n ${{< /math >}} influcencers with targets {{< math >}}$ t_{1}, ..., t_{n} ${{< /math >}}. These targets are common knowledge. At the beginning of the game, influencer {{< math >}}$ i ${{< /math >}} will draw a sample {{< math >}}$ z_{i} ${{< /math >}}, which is private to itself, from a probability distribution {{< math >}}$ N(\mu, \sigma^{2}) ${{< /math >}} given by the environment. The victim, after collecting all the reports, generate opinion {{< math >}}$ v = f(x_{1:n}, t_{1:n}) ${{< /math >}}. And influencer {{< math >}}$ i ${{< /math >}} incurs loss {{< math >}}$ (v-t_{i})^{2} ${{< /math >}}.

The victim does not want to receive any biased reports. Hence, it decides to use the following {{< math >}}$ f ${{< /math >}}: {{< math >}}$$ f(x_{1:n}, t_{1:n})=\hat{x} + \left(\hat{x}_{-i^\star} - x_{i^\star}\right)^\top \dfrac{\hat{x}_{-i^\star} - t_{i^\star}}{\left\|\hat{x}_{-i^\star} - t_{i^\star}\right\|} \dfrac{\hat{x}_{-i^\star} - x_{i^\star}}{\left\|\hat{x}_{-i^\star} - x_{i^\star}\right\|} \varepsilon $${{< /math >}}
Where, {{< math >}}$$ i^\star = \argmax_{i} \left(\hat{x}_{-i} - x_{i}\right)^\top \dfrac{\hat{x}_{-i} - t_{i}}{\left\|\hat{x}_{-i} - t_{i}\right\|} $${{< /math >}}
And {{< math >}}$ \hat{x} ${{< /math >}} represents the average of all reports; {{< math >}}$ \hat{x}_{-i} ${{< /math >}} represents the average of all reports excluding {{< math >}}$ x_{i} ${{< /math >}}.

Here, {{< math >}}$ i^\star ${{< /math >}} denotes the biggest "cheater" in the game, which is the agent that deviates the most from its peers in a direction that is favorable to itself. This particular {{< math >}}$ f ${{< /math >}} excludes the biggest "cheating" influncer's report and moves {{< math >}}$ v ${{< /math >}} in the direction that harms the interest of this cheating agent. 

In this game, when {{< math >}}$ \varepsilon > \frac{1}{n} ${{< /math >}}, influencers can reach a strict Nash Equilibrium by reporting the same point. The game can also converge at a state where influencers try to cheat, but not that much so that they do not become the biggest cheater. Here are some examples of agents' behaviors under BRD:
<figure>
  <img src="sigma=0.png" alt="sig=0"/>
  <figcaption>The game with N(1,0) as the distribution</figcaption>
</figure>

<figure>
  <img src="N(1,1).png" alt="N(1,1)"/>
  <figcaption>The game with N(1,1) as the distribution and agents have targets at -30, -10, 5, 20, 40</figcaption>
</figure>