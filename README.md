# Crowdfund-Analysis

![image](https://user-images.githubusercontent.com/106030704/231515744-fd8f93cc-8355-4bb6-9a8a-2a21ab29ed8d.png)
Author: Jake Sherman

## Business Case

In 2016 the Jobs Act passed which empowered issuers to raise money from retail or non-accredited investors. 90% of startups fail to secure venture funding and so raising money via Reg CF or Reg A has become a viable alternative.  When offering securities to the public, the greatest question issuers will face is "will there be appetite from the public"?

While many issuers are successful in communicating their message to the public and securing funding, others are not as fortunate.  Offering these securities to the public can be an expensive endeavour, with Reg A offerings costing up to 400k.  Knowing which companies will be successful ahead of their fundraising launch would be valuable information.

## Objective

Using data from funding portals, we are going to create a linear regression and build a few models (decision trees, random forest, and KNN) to see if we can predict which offerings will be successful. Success will be defined as raising at least 500k. The process for Reg A and CF is very similar so we will make reg CF the focus of our model because there is much more data to review and these tend to be a much less expensive offering to launch.

## EDA

The average fundraise is just over $300k while the median is $86k.  The data is right skewed, in this case meaning the there are many unsuccessful raises and a few very successful raises that are elevating the mean way about the median.  A successful raise is defined as raising at least 500k.  Only 13.7% of raises are successful.

Real Estate and Construction is the industry with the highest average amount raised.
![image](https://user-images.githubusercontent.com/106030704/226997011-d148b49f-2680-4c1d-9c6a-ae6424b2cc59.png)

Preferred Equity offerings had the highest average amount raised.
![image](https://user-images.githubusercontent.com/106030704/226997475-4ec0db63-5336-4e57-9b33-502cfe3ca856.png)

Companies with a higher market cap tended to raise better.  Investors prefer to see a company establish itself a bit more before investing.
![image](https://user-images.githubusercontent.com/106030704/226997378-0fff6996-9837-4d25-947d-f9d0a6ec633d.png)

## Modeling

As we will only be investing in a select few offerings, we need to make sure we get our investments right.  In this case we are prioritizing precision over recall.

Decision Tree Precision 63.5% after hyptertuning with smote.

![image](https://user-images.githubusercontent.com/106030704/226997650-8e0227d9-86d8-4fe5-8a55-6d7030182e2c.png)

Random Forest Classifier had a precision of 69%

![image](https://user-images.githubusercontent.com/106030704/226999023-728d69f3-c826-496b-a16a-26ba1371cc93.png)

## Findings

Valuation/Cap and annual revenue were the most important features in determining if there was going to be a successful offering.
![image](https://user-images.githubusercontent.com/106030704/226998562-4ad6c672-0dfa-49b3-a325-b77223759cad.png)

Given that only 13.7% of offerings are successful, investing would be a risky endevour.  A precision closer to 90% would have been ideal in order to risk captial.  A precision of 69% is a start, but we likely will need more data such as marketing budgets, cash reserves, net income, and experience of senior leadership.

## Recommendations

We want to focus our investment:
1. Real Estate and Construction Industry
2. Revenue generating companies (not pre-rev) with a $20-$25M valuation
3. Utilize a preferred equity offering structure
4. Set the minimum investment to $500

## For More Information

contact Jake Sherman at jsherman918@yahoo.com

## Repository Structure

├── Companies Search Export (1).csv
├── Crowdfund Analysis.ipynb
├── Crowdfunding Analysis.pdf
├── README.md
