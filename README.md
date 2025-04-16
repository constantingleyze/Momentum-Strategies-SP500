# Momentum Strategies on S&P 500 Sector Indices

This repository presents a critical and practical exploration of momentum-based investment strategies, grounded in the seminal paper by Jegadeesh and Titman (1993), *"Returns to Buying Winners and Selling Losers: Implications for Stock Market Efficiency."*

> **Reference paper:**  
> Jegadeesh, N., & Titman, S. (1993). *Returns to Buying Winners and Selling Losers: Implications for Stock Market Efficiency*. *Journal of Finance*, 48(1), 65–91.

We begin with a structured summary of the original article, highlighting its methodology, theoretical framework, and key empirical findings. This is followed by a critical analysis of the paper’s assumptions, implementation constraints, and generalizability. We address issues such as transaction costs, market impact, liquidity constraints, and the potential self-fulfilling effects that can arise when similar strategies are widely adopted, thereby reinforcing price trends beyond fundamentals.

In the second part of the project, we test momentum-based long-only and long/short strategies on the S&P 500 Sector Indices over the period 1989–2018. We replicate the core ideas of Jegadeesh and Titman while extending the analysis with new allocation rules, more realistic transaction cost models, and a broader range of configurations.

Specifically, we implement and evaluate **18 distinct strategies**, combining:

- 3 allocation types (equal-weighting, performance-based weighting, and fully directional),  
- 2 portfolio structures (long-only and long/short),  
- and 3 transaction cost regimes (none, fixed linear, dynamic tiered),  

resulting in a comprehensive and systematic comparison.

We explore several portfolio construction methods, including equal-weighting, performance-based weighting, and a fully directional strategy that adjusts allocation in response to recent market signals. We also evaluate the impact of transaction costs and assess the robustness of each approach.

**Note:** Unlike the original paper, we *do not apply the 1-week lag* between return observation and portfolio formation. While this makes our implementation closer to a real-time signal application, it may slightly overstate theoretical profitability compared to more conservative (lagged) setups.

Our findings show that while simple long-only momentum strategies remain effective under moderate frictions, long-short strategies are generally more fragile and often fail when faced with realistic implementation costs. However, our directional allocation method for long-short positioning demonstrates strong net performance despite increased volatility and cost sensitivity, suggesting that adaptivity can be a valuable feature when carefully calibrated.

In the conclusion, we suggest several extensions to improve or generalize the strategies analyzed: incorporating volatility or beta control mechanisms, introducing cash allocations in uncertain environments, applying seasonal market-timing filters, using derivative overlays for downside protection, and examining the role of leverage. These avenues aim to bridge the gap between theoretical profitability and real-world implementability.

To fully understand the rationale behind the strategic and technical choices made in the code, we strongly recommend reading **Section III.1 of the paper**, which provides a detailed description of the methodology.
