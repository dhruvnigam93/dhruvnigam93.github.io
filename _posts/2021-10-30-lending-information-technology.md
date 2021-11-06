---
layout: post
title: "On information, power and money lending"
date: 2021-10-30
---

On paper, the objective of credit risk management is deceptively simple.
>>“Don’t give money to people who may not be able to pay you back.”

In other words, avoid people whose probability of default (the event of a borrower not paying back) is high. The higher this probability, the higher the risk.

Ideally one would want the probability of default to be close to zero, but there are very few borrowers like that(even the government of India has a significantly non-zero probability of default[1]). There may be customers with a reasonably low probability of default (e.g. salaried high-ranking government employees who have a high and steady monthly income), but the competition to lend to these customers would be higher. A new-age fintech company would probably not be able to compete with the private and public banks and the larger NBFCs that would already be hounding these customers[2]. So you need to choose a segment of customers who would be comfortable taking loans from you on the terms that you offer them (typically a higher interest rate than the aforementioned entities). And you hope that a few of them will have a low enough risk(i.e. low probability of default) for you to feel comfortable. 

Within this chosen segment, say you can give loans to 20 out of every 100 customers that apply to you because only they fit the risk profile you are comfortable with. The approval rate is at 20%. For a lender, the revenue is the interest income received over and above the principal amount that is lent. So all the revenue comes from the interest paid by the 20 customers who got the loan. The expenses, on the other hand, are incurred on all 100 customers that were acquired and processed through the risk-assessment machinery. So, in 80/100 cases, there were only expenses made, no revenue generated. It’s suddenly tempting to increase the 20% approval rate. But doing this,ceteris paribus would mean lending to people who have a higher risk than one would be comfortable with. This is the fundamental tension that lies at the core of every lending institution. This tension is supposed to balance two conflicting but equally essential objectives - Take risks to make money, but not too much. We can call this the short-term profit vs risk tradeoff[3].

Consequently, assessing risk on a per loan-application basis and determining which 20 borrowers out of the 100 who apply to get a loan, is a critical process for lenders. It is essentially an exercise in predicting the future. Based on the information available about the present, lenders try to predict whether a customer would be able and willing to pay them back if given a loan. Like in any endeavor which involves prediction, errors are concomitant. Specifically, in this context, there are 2 kinds of errors -

* False negatives -  reject someone who is low risk
* False positives - approve a loan to someone who is very risky

False negatives lead to missed opportunities to lend to credit-worthy customers. False positives materialize as defaults by risky borrowers who we deemed creditworthy. Another truism about predictions is that they tend to get better when more information is available[4]. In this specific context, if we make more information available (Eg. phone bill records from telecom companies, SMS data from phones, professional history from Linkedin), decisions will get better. The lenders will benefit by having lower risk because of the improvement in the quality of decisions they make leading to fewer errors. Creditworthy borrowers will face less rejection. Another upside of more information being available to lenders is that it enables them to cater to borrowers, who were previously inaccessible due to a lack of a footprint on the conventional information channels. Think of an entrepreneur who previously sold handmade handicraft products to brick and mortar stores for cash, but now sells them on online platforms like Amazon and Etsy with each transaction having an immutable digital record. A lender can now ask for his/her bank statement or digital invoices from platforms to assess creditworthiness, which was previously very difficult.

The rise of digital payments because of UPI and demonetization, the movement of India’s physical economy to digital platforms(Amazon, Udaan, Flipkart, etc.), and the rollout of GST, following which certain businesses have to digitally file a record of all their sales/purchase transactions every month, have all flooded the SME lending ecosystem with easily accessible information. This is arguably the most important factor explaining the rise of fintech startups in the SME lending space in the last few years. 

The formal SME credit gap was always huge in India. The current hypothesis is that given the advancements in technology, particularly pertaining to access and processing of information, we will be able to drastically reduce it. Whether the hypothesis translates to reality is anyone's guess, but it is highly likely that with the amount of capital and talent pursuing this very objective, there will be a lot of exciting things happening in this space over the next few years.


[1] The market prices in a certain probability of default for each government which are implied by the price it pays to insure the debt to said government. https://pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/ctryprem.html

[2] Traditionally credit worthy customers are served well via current institutions. The reason is two fold. First, as incumbents, these institutions already have relationships and trust of these customers. Second, because of their relatively mature set up, these institutions can themselves raise money cheaper than new entrants, enabling them to lend at lower rates, attracting customers.

[3] The reasons why this trade off is short term is because in the long term, the costs of taking high risks materialise when risky customers start to default and start to affect the long term profit. However, in the short term, when the risk has not materialised and everyone is still paying back on time, an illusion of high profit is created.

[4] Assuming that the information itself is predictive on its own. Adding irrelevant information to the prediction process can actually lead to worse decisions.

Thanks to Ishan Anand, Sahul Nath and Parth Nigam for their feedback.
