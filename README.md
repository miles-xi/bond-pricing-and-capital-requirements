# bond-pricing-and-capital-requirements

### Executive Summary

In this report, we analyzed a dataset of 6262 corporate bonds traded in the US on May 31, 2024, and 10 features including price, maturity, treasury spread, offering date, principal, interest frequency, coupon rate, rating, and security level. We re-priced these bonds using the Canadian yield curve on the same day and the yield curve on January 13, 2025, to analyze the effect of the interest rate on bond prices. To get accurate risk-free rates at different points in time, we interpolated the yield curves using quadratic interpolation. For coupon payment dates, we listed the dates between the transaction date and the maturity using the interval determined by interest frequency. We then discounted future coupon payments and the principal using the risk-free rates plus the spread at each payment date, getting the present value of the bonds. Results show that 80.93% of bonds achieved higher prices, with an average price increase of $1.18, under the Canadian yield curve which was approximately 1.39% lower than the U.S.  Bonds were valued even higher on January 13, 2025, when the short-term interest rate had dramatically decreased, resulting in an average price difference of $5.04. 

We concluded that a Canadian investor subject to Canadian interest rates would invest in U.S. bonds because domestic rates were lower than those abroad and money flows to wherever there are high returns. In other words, a Canadian investor would consider U.S. bonds underpriced when they discount using the Canadian rates.

Under banking regulations, banks are required to set aside economic capital for risk management. For a portfolio of bonds, the risk is credit risk. Thus we computed the capital requirements and provision for this portfolio. We first derived risk components according to the OSFI capital adequacy guideline using the Foundation Internal Rating Based (F-IRB) approach. Specifically, the Probability of Default (PD) was simulated using the log-normal distribution, and LGD was mapped from the seniority of the bonds. We then applied the capital requirement equation to individual bonds to get the capital requirements, which were then aggregated to the portfolio level. The provision was calculated similarly.

We analyzed the distribution of the capital requirement and the provision using descriptive statistics. We found that for $100 exposure to a portfolio of bonds, the bank needs to set aside $9.82 ~ $9.93 as economic capital, and $0.46 ~ $0.48 as provision. We further analyzed each rating’s contribution to the total capital requirement. CC bonds contributed the most: for $1 exposure to them, $0.64 was an unexpected loss and thus needed to be set aside as regulatory capital. This result is useful for regulatory compliance, capital budgeting, and portfolio performance measurement. 

### License and Usage Terms
This repository and its contents are © 2025 Miles Xi. All rights reserved.

You are welcome to: <br>
• View and use the code and materials directly via this GitHub repository <br>
• Use the code for educational or non-commercial personal projects, as long as you do so through GitHub

However, you may not: <br>
• Rehost, mirror, or redistribute this repository or any part of its content on third-party websites or platforms <br>
• Use any automated means (e.g., scraping tools or bots) to copy or mirror the repository or its contents elsewhere

Unauthorized redistribution or rehosting is strictly prohibited. Please contact me for permission if needed.
