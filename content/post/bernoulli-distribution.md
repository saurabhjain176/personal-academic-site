---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Bernoulli Distribution"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2020-10-26T16:53:50+01:00
lastmod: 2020-10-26T16:53:50+01:00
featured: false
draft: false
math: true
# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
In an experiment, where the possible outcome is (0,1) or (yes/no), **Bernoulli Distribution** gives a model of possible outcome. It is the discrete probability distribution of a random variable that has a probability $ p $ of having a value 1 and probability $ 1- p $ as having a value 0.

Let's consider a classic example of flipping a fair coin. Consider random variable $ c \in \{H,T\} $ which represent the result of tossing the coin. The probability of getting $ H $ is $ x = p(c = H) $ and the probability of getting $ T $ is $ 1 - x = p(c = T).$

Therefore, the probability function of this distribution over the outcomes $c \in \{H,T\}$  can be given as
$$p(c|x) = \begin{cases} x & \text{if }c=H, \\\\
1-x & \text {if }c=T.\end{cases}$$

This can also be represented as $$ p(c|x) = x^c(1 - x)^{1-c}$$  
The equation above is the **Bernoulli Distribution**.
Let's quickly check if this holds true for our flipping coin example.

Given c = 0 (HEADS),

$$p(c = 0 | x) = x^0(1 - x)^{1-0} = 1-x $$

and given c = 1 (TAILS),

$$p(c = 1 | x) = x^1(1 - x)^{1-1} = x $$

It shows that **Bernoulli Distribution** holds true for both the values.

**Usage:** Imagine that you are building a very basic classification model to detect _hate speech_ from a given text. The dependent variable of the classification is $ y \in 0, 1 $ for _NO_HATE_ and _HATE_ respectively. Now we can model the dependent variable $y$ using the **Bernoulli Distribution** as $ p(y|x) = x^y(1 - x)^{1-y}$. Note that in practical usage, $x$ can be more sophisticated activation function like _sigmoid_ or _ReLU_.


**Reference:**

1. Wikipedia - https://en.wikipedia.org/wiki/Bernoulli_distribution
