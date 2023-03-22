# Crowdfund-Analysis
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
![image](https://user-images.githubusercontent.com/106030704/226978184-9b124bff-3645-4c29-bde7-a55633441114.png)

Companies with a higher market cap tended to raise better.  Investors prefer to see a company establish itself a bit more before investing.
![image](https://user-images.githubusercontent.com/106030704/226988448-90e6f86e-e524-4bef-a2d8-1e65fe678f68.png)

## Modeling

As we will only be investing in a select few offerings, we need to make sure we get our investments right.  In this case we are prioritizing precision over recall.

Decision Tree Precision 63.5% after hyptertuning with smote.
![image](https://user-images.githubusercontent.com/106030704/226989879-c256b07e-33a6-441e-9a44-2ffe4f35a9da.png)
![image](https://user-images.githubusercontent.com/106030704/226990168-2dcd621b-fb36-4ff1-87b4-43d9dada11a4.png)

Random Forest Classifier had a precision of 69%
![image](https://user-images.githubusercontent.com/106030704/226991130-a19509f4-49da-4814-9959-b7fd5787bc6d.png)

## Findings

Valuation/Cap and annual revenue were the most important features in determining if there was going to be a successful offering.
![image](https://user-images.githubusercontent.com/106030704/226991458-62b8d623-265d-42ca-95f8-8abff7a4c09e.png)

Given that only 13.7% of offerings are successful, investing would be a risky endevour.  A precision closer to 90% would have been ideal in order to risk captial.  A precision of 69% is a start, but we likely will need more data such as marketing budgets, cash reserves, net income, and experience of senior leadership.
