---
title: Influncer War 0
subtitle: 

# Date published
date: 2024-08-02

# Date updated
lastmod: '2024-08-02T11:46:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

authors:
  - admin
---

Here we consider the most basic setting. There are n articles {{< math >}}$ x_{1}, \hdots, x_{n} ${{< /math >}} in a 2-dimensional space. There are two players, Big and Little, with target locations, {{< math >}}$ B ${{< /math >}} and {{< math >}}$ L ${{< /math >}}, respectively. Each of them will choose a article from the set to incluence the victim, simultaneously. The victim learns by averarging their reports. Name the article chosen by Big {{< math >}}$ b $ {{< /math >}}, the article chosen by Little {{< math >}}$ l $ {{< /math >}}, and the victim's opinion {{< math >}}$ v $ {{< /math >}}. Then, {{< math >}}$$ v = \frac{b+l}{2} $${{< /math >}}. Big will want to minimize {{< math >}}$$ |v-B| $${{< /math >}}. Similarly, Little wishes to minimize {{< math >}}$$ |v-S| $${{< /math >}}.

In general, a general-sum game may not have a pure Nash equilibrium (NE), but our game here is a potential game. By running best-response dynamics, we can get a pure NE.