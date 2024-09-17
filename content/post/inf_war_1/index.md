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

Let us revisit the naive model where the victims simply takes the average of influencers' reports and add some batches to it. This time, we include {{< math >}}$ n ${{< /math >}} influcencers with targets {{< math >}}$ t_{1}, \hdot, t_{n} ${{< /math >}}. These targets are common knowledge. At the beginning of the game, influencer {{< math >}}$ i ${{< /math >}} will draw a sample {{< math >}}$ z_{i} ${{< /math >}}, which is private to itself, from a probability distribution {{< math >}}$ N(\mu, \sigma^{2}) ${{< /math >}} given by the environment. The victim, after collecting all the reports, generate opinion {{< math >}}$ v = f(x_{1:n}, t_{1:n}) ${{< /math >}}. And influencer {{< math >}}$ i ${{< /math >}} incurs loss {{< math >}}$ (v-t_{i})^{2} ${{< /math >}}.

The victim does not want to receive any biased reports. Hence, it decides to use the following {{< math >}}$ f ${{< /math >}}: {{< math >}}$$ \hat{x} + \displaystyle\max\left\{0, \left(\hat{x}_{-i^\star} - x_{i^\star}\right)^\top \dfrac{\hat{x}_{-i^\star} - t_{i^\star}}{\left\|\hat{x}_{-i^\star} - t_{i^\star}\right\|}\right\} \dfrac{\hat{x}_{-i^\star} - x_{i^\star}}{\left\|\hat{x}_{-i^\star} - x_{i^\star}\right\|} \varepsilon $${{< /math >}}