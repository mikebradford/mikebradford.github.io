---
published: true
title: Agile, Go to Market planning, and Business Cases. A case study
layout: post
---
I believe that existing/legacy business processes are not aligned with Agile.

To me Agile is about effectiveness and conventional business processes are about efficiency.

## Agile can increase effectiveness and ROI
Agile enables the business to test assumptions, as part of the investment (i.e delivery) process, enabling investment to be re-allocated depending if this would provide a better rate of return.

A great metaphor of how this works is provided by Reinertsen [here](http://reinertsenassociates.com/the-four-impostors-success-failure-knowledge-creation-and-learning/). As well as criticising the mis-leading label of failure it provides a very nice example of how incremental investment can maximise the ROI.

##This is easier in theory than practice.
I work in mobile and on a lot of new products, as well as some cash cows. Everyone is keen to use an Agile product delivery process, but not so keen to change the business processes to match. 

One area this affects is how we prioritise development and markets. The common question being do we prioritise rolling out the product or feature to large or small mobile markets first.

## Prioritisation based on Revenue and Cost.
When I first had to make this call, I prioritised based on revenue. This seems very sensible, especially as it optimises the business case. This meant that we always prioritised the largest mobile market first.

We worked with a customer, also Agile, on a project who prioritised based on cost/development resource. Their bottleneck was development, so they targeted markets requiring the least custom development first.

For the project in question we were both wrong (using 20/20 hindsight). We should have targeted markets that would have allowed us to get quicker feedback, and be able to adapt based on the feedback.

However if I try and share this learning with my peers, that prioritisation based on revenue isnt always the best choice, I get a lot of push back. 

Considering why I see two reasons
1. Not only is it counter intuitive on a personal level
2. It would also worsen the business case financial metrics of [NPV](https://en.wikipedia.org/wiki/Net_present_value) and [IRR](https://en.wikipedia.org/wiki/Internal_rate_of_return)

## Alternatives

Two agile alternatives are [Cost of Delay](http://blackswanfarming.com/cost-of-delay/) and [WSJF](http://www.scaledagileframework.com/wsjf/) 

Cost of Delay is interesting, because it factors in the missed revenue and how long it takes to deliver. This often provides a more compelling case to deliver quicker, even if it costs more, or if it delivers less revenue in the long term. (As an aside it also demonstrates the economic benefit of increased flow efficiency, even if resource costs increase) 

WSJF is the prioritisation method in SaFE. At it's core it is based on Cost of Delay, but includes some additional factors, such estimates of whether the feature is _Time Critical_ or _Reduces Risk or Enables Opportunity_.

I was curious if these methods would be useful to demonstrate the financial benefits of prioritising in an Agile fashion.

# A Case Study based on a real example

We are launching a new product using Mobile Operator APIs. 
The nature of the market means that we need to be able to sign up sufficient operators in a country to be able to cover most of the mobile subscribers. (lets say 75%).

We have two countries lined up.
### Redland 
has a huge market, spread across 4 main operators and a number of smaller MVNOs.
This means that we need to integrate with all 4 main operators to launch. However each Mobile Operator still has more subscribers than most small countries.

###Blueland 
is a lot smaller (2.5% the size of Red), but has a single dominant operator which controls 75% of the market. 

My experience tells me that we should try and launch this new service with Blueland first. With only one operator connection needed this would be a lot quicker, with less dependencies.

However _conventional_ thinking would be to launch Redland first, since this is where all the revenue is.

So let's run these different models and see what they say.

So here is the base assumptions.
##Costs
Each Mobile Operator implementation is idenitical with the same implementation cost (6 figures), up front fee (6 figures), and duration (3 months). 

This means that implementing Redland is 4x the cost and duration as implementing Blueland.

##Revenue
Revenue forecast is proportional to the number of mobile subscribers, with a projected revenue/month/subscriber. 
We will ignore the adoption curve to simplify the model, with the assumption that the impact would be proportionally the same for both markets

##Risk
This isn't quantified as part of the normal business case. However lets quantify it for this project. This would be a whole topic & model in itself, but lets use the following assumptions
1. Sourcing success/risk. This is the risk associated with obtaining the contract with the MNO. 
Assumed to be 90% likely to succeed (i.e. 10% risk of failure)
2. Implemention Success/Risk. This is the risk associated with implementing the technology.
Assumed to be 99% likely to succeed (i.e. 1% risk of failure)
3. Product/Market Success. This is the risk that the business idea doesn't work.
This is often the biggest risk with a new product. However in this case lets assume that we have a great idea that is 75% likely to work (i.e. only 25% likely to fail)

##Calculating the Result.
I made a google spreadsheet to do the grunt work [here](https://docs.google.com/spreadsheets/d/1dl0yItv9d6xSe2VIBfivuKigAJo6FOS6JlSduoASK_8/edit?usp=sharing).

##The Results
### Revenue and Cost
Redland generates 38x the revenue of Blueland, at 4x the cost

### NPV
Based on the NPV calculation over 3 years, then Redland should be launched first then Blueland since
1. Redland First NPV = $41.2M
2. Blueland First NPV = $34.9M
Delivering $6.2M more value after 3 years.

### IRR
Based on the IRR calculation over 3 years then Redland should be launched first since
1. Redland First IRR = 140%
2. Blueland First IRR = 122%
Delivering 18% better Return.

### Cost of Delay
Using Cost of Delay then Redland is still the winner.
1. Redland CoD = $317k
2. Blueland CoD = $33k
Redland wins by 9x & $283k

### WSJF
Now this model can include the Risk. There are no clear rules AFAIK on how to map this. In this case I have factored in the ratio of the risk between the two countries. Redland is still the winner.
1. Redland WSJF = 10.0
2. Blueland WSJF = 3.6
Redland wins by 2.75x

###Financial Risk
I was also curious about the Financial Risk for each option was. Assuming that we cancel the project after the implementation based on the results from the first country. what would be the exposure?
I calculated this as the sunk cost x likelihood of failure for each market.
In this one case Blueland is the winner.
1. Redland first. Financial Risk = $738k
2. Blueland first. Financial Risk = $116k
Since Blueland is so much cheaper to implement, it means that it costs us a lot less to prove the business model.

##Conclusions
1. Traditional Business Case models do not encourage us to schedule in a non-Agile Way, as they don't factor in risk 
2. Alternative __Agile__ models still encourage us to schedule in a non-Agile way in this case. This is because, whilst some do factor in risk, they dont consider the total risk exposure, just the relative exposure.
3. It is only when we evaluate the financial risk that we see the financial benefit of scheduling in an 'Agile' way.

##Recommendation
Add financial risk calculations to Business Case. This means that risks are seriously debated, and encourages the scheduling of releases to minimise financial risk, as well optimise potential revenue.

## Also see
[IT Risk Manager Post](https://theitriskmanager.wordpress.com/2015/04/13/risk-adjusted-roi-of-agile-waterfall-a-simple-example/)