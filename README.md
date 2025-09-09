# bond-pricing-and-capital-requirements

### Executive Summary

In this report, we analyzed a dataset consisting of 6262 corporate bonds traded in the US and 10 features including price, maturity, treasury spread, offering date, principal, interest frequency, coupon rate, rating, and security level. We re-priced these bonds based on Canadian yield curve on May 31, 2024 and yield curve on January 13, 2025 to analyze the effect of the interest rate on bond prices. To get the accurate risk-free rate, we interpolated the yield curves using quadratic interpolation. We generated the coupon payment dates from the offering date to the maturity using the interval determined by interest frequency. We then discounted future coupon payments and the principal using the risk-free rates plus the spread at each date, getting the present value of bonds. Results show that 80.4% of bonds had higher prices, with an average price increase of $3.75 under the Canadian yield curve, which was approximately 1.39% lower than the U.S.  Bonds were valued even higher on January 13, 2025, before which the short-term interest rate had dramatically decreased, resulting in a further average price difference of $1.18. 

We therefore concluded that a Canadian investor subject to Canadian interest rates would invest in U.S. bonds, because domestic interest rates were lower than those abroad and money flows to wherever there are high returns. In other words, a Canadian investor would consider U.S. bonds underpriced when they discount using the Canadian rates.

Under banking regulations, banks are required to set aside regulatory capital for risk management. For a portfolio of bonds, the risk is credit risk. Thus we computed the capital requirements and provision for this portfolio. We first derived risk components according to the OSFI CAR guideline using the Foundation Internal Rating Based (F-IRB) approach. Specifically, the Probability of Default (PD) was simulated using the log-normal distribution in each rating, and LGD were mapped from seniority of the bonds. We then applied the capital requirement equation to each individual bond to get the capital requirements, which were then aggregated to the portfolio level. The provision was calculated in a similar fashion.

We analyzed the distribution of the capital requirement and the provision using descriptive statistics. We found that for $100 exposure to a portfolio of bonds, the bank needs to set aside $3.21 ~ $3.26 as capital, and $0.123 ~ $0.129 as provision. We further analyzed each rating’s contribution to the capital requirement and provision. CC bonds contributed the most: for $1 exposure to them, $0.18 was unexpected loss and $0.013 expected loss and thus needed to be set aside as regulatory capital and provision. This shows that although CC bonds have a high yield, they are likely to have low risk-adjusted return on capital (RAROC).

### Main references
1. FM 9528 Banking Analytics lecture slides
2. [OSFI CAR Guideline Chap 5: Credit Risk – Internal Ratings-Based Approach](https://www.osfi-bsif.gc.ca/en/guidance/guidance-library/capital-adequacy-requirements-car-2024-chapter-5-credit-risk-internal-ratings-based-approach)


### License and Usage Terms
This repository and its contents are © 2025 Miles Xi. All rights reserved.

You are welcome to: <br>
• View and use the code and materials directly via this GitHub repository <br>
• Use the code for educational or non-commercial personal projects, as long as you do so through GitHub

However, you may not: <br>
• Rehost, mirror, or redistribute this repository or any part of its content on third-party websites or platforms <br>
• Use any automated means (e.g., scraping tools or bots) to copy or mirror the repository or its contents elsewhere

Unauthorized redistribution or rehosting is strictly prohibited. Please contact me for permission if needed.
