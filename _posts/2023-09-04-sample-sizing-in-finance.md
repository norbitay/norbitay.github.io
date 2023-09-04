---
title: Probability and Sample Size in Finance
layout: post
post-image: "samplesizefinance.jpeg"
description:
tags:
- Probability 
- Sample Size 
---

Probability is not a straightforward and intuitive subject; biases can easily lead to misjudgment in many scenarios. My recent reading about cognitive biases in probability raises some interesting questions.

If a hospital on average delivers ten birth a day, what is the probability of having less than or equal to four boys? I quickly calculated the probability, which is the sum of each probability less than or equal to four (equation 1). The probability of having four or fewer boys is approximately a 37% (assuming the likelihood of having boys and girls are equal).

$$
P(x≤4) = \sum_{i=0}^x \binom{n}{x_i} \times p^{x_i} \times (1-p)^{(n-x_i)}  \tag{1}
$$

Suppose the hospital delivers 1000 births each day. What is the probability of having 400 or fewer boys? The ratio is the same as four out of ten, should not the probability is the same or at least very similar? The correct answer is no. The probability of having 400 or fewer boys out of 1000 births is infinitesimally small. Sample size matters and the probability needs to be evaluated in a light of it.

The same probability theory applies in evaluating a money manger’s performance. Consider two money managers, Alex and Blair, offering you trades assuming at fair value. Alex has three profitable trades out of twelve and Blair has five profitable trades out of twenty. 

<table>
    <tr>
        <th></th>
        <th>Profitable Trades</th>
        <th>Losing Trades</th>
    </tr>
    <tr>
        <th>Alex</th>
        <td>3</td>
        <td>9</td>
    </tr>
    <tr>
        <th>Blair</th>
        <td>5</td>
        <td>15</td>
    </tr>

</table>
 
Both money managers seemed to be equally bad at trading with profitable trades that are less than 50% despite the trades assumed to be fairly priced. Without factoring in the sample size, we might have intuitively thought both Alex and Blair have the same performance, making a profit on three out of twelve and five out of twenty, respectively. Are Alex and Blair really equally bad such that they should consider a career change, or one is better than another in the perspective of probability? Let’s consider the sample size. 

We assume that the trades are fairly priced, so the probability of profiting or losing is 50/50. The probability of Alex resulting in three or fewer profitable trades out of twelve is 7.29%, which is the sum of each exact probability below:

$$
P(x=3) = \binom{12}{3} \times 0.5^{3} \times (1-0.5)^{(12-3)} = 5.37\%\\

P(x=2) = \binom{12}{2} \times 0.5^{2} \times (1-0.5)^{(12-2)} = 1.61\%\\

P(x=1) = \binom{12}{1} \times 0.5^{1} \times (1-0.5)^{(12-1)} = 0.29\%\\

P(x=0) = \binom{12}{0} \times 0.5^{0} \times (1-0.5)^{(12-0)} = 0.02\%\\
$$

The probability of Blair offering five or fewer profitable trades out of twenty is 2.07%, which is the sum of each exact probability as below and it is substantially lower compared to Alex’s three or fewer profitable trades (7.29%).

$$
P(x=5) = \binom{20}{5} \times 0.5^{5} \times (1-0.5)^{(20-5)} = 1.48\%\\

P(x=4) = \binom{20}{4} \times 0.5^{4} \times (1-0.5)^{(20-4)} = 0.46\%\\

P(x=3) = \binom{20}{3} \times 0.5^{3} \times (1-0.5)^{(20-3)} = 0.11\%\\

P(x=2) = \binom{20}{2} \times 0.5^{2} \times (1-0.5)^{(20-2)} = 0.02\%\\

P(x=1) = \binom{20}{1} \times 0.5^{1} \times (1-0.5)^{(20-1)} = 0.00\%\\

P(x=0) = \binom{20}{0} \times 0.5^{0} \times (1-0.5)^{(20-0)} = 0.00\%\\
$$

It is notably more likely for Alex to have three or fewer profitable trades out of twelve relatives to Blair to select five or fewer profitable trades out of twenty. In another words, Blair may not be a great trader but Blair’s overall performance beats Alex’s when we consider the sample size. Just like in the birth rate of boys, ignoring sample size easily leads to incorrect or incomplete conclusions.
