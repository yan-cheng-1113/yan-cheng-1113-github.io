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

We consider a slightly more sophisticated cognitive model than simply taking the average of Big and Small. Our victim has become more rational; it does not want to accept information that is too extreme or biased. Moreover, it also has its own idea before the game starts, which is represented by {{< math >}}$ x_{0} ${{< /math >}}. Let us also transform the dicrete space of [Influencer War 0](https://yan-cheng-1113.github.io/yan-cheng-1113-github.io/post/inf_war_0/) into a continuous line.

Given reports {{< math >}}$ x_{b} ${{< /math >}} and {{< math >}}$ x_{s} ${{< /math >}} from Big and Small, the victim calculates {{< math >}}$$ g_{b}=e^{-\frac{(x_{b}-x_{0})^{2}}{2\sigma^{2}}},\\ g_{s}=e^{-\frac{(x_{s}-x_{0})^{2}}{2\sigma^{2}}} $${{< /math >}} Here, {{< math >}}$ g_{b} ${{< /math >}} and {{< math >}}$ g_{s} ${{< /math >}} represent "how much the victim trusts Big and Small". The victim updates its opinion by calculating {{< math >}}$$ v=\frac{x_{0}+x_{b}\cdot g_{b} + x_{s}\cdot g_{s}}{1+g_{b}+g_{s}} $${{< /math >}}
