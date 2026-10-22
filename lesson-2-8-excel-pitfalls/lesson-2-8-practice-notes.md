## Audits Checks You ran

I ran audit checks on dashboard, sales_2024, returns, customer_segments, marketing_spend, and the A/B Test analysis.

I checked if all ids are not auto-converted by checking if there any numbers in any of the relevant columns.

I checked for hidden data using "Go To Special" -> Visible cells only.

I checked for floating points by add all value in the column to see if there any values that have run-on decimals

## One issue you found on your own

The pivot chart for marketing spend by channel had variants causing data to be misleading.

On tab customer_segments, the column first_order_date has been formatted into the number version of dates

## Whast questions your peer asked and how you answered

“Does the hidden-rows issue change the Dashboard numbers?”
The total gross_avenue between the hidden rows is 1,888.74 with return per unit about 51.97 with 18 units. 

“How much spend was affected by the channel variants?”
The channel "Email" was affected and cause it spend to be divided in nearly in half

“How many SKUs were converted, and which ones?”
The SKUs that were converted were ones that simliar to dates
To find the one that were converted I used =SUMPRODUCT(--ISNUMBER())



## The structure of your final data quality memo

1. What I checked. Brief description of the audits run.
2. What I found. Numbered list of issues, with severity and impact.
3. What I fixed. What's already corrected in the current workbook.
4. What's still pending. What requires Beatrix's input or a follow-up engagement.
5. What I'd want for next time. 

## AI Critque Exchange

AI message: 

Main issues I fixed or flagged

Missing results: The memo lists checks on KPIs, pivot ranges, lifetime_value and spend floating points, Returns hidden rows, and the A/B rerun, but never says what they found. A reader can’t tell “clean” from “forgot to report.” I added a line asking you to state a result for each.
Unclear statuses: The SKU conversions in Sales_2024 appear under “Found” but not under “Fixed” or “Pending.” I added a pending item asking whether they were fixed or are still open.

Hidden rows: Counts and contents aren’t given. Without those, the stakeholder can’t decide whether to keep or remove them, so I reworded it as “decision needed.”

Overstated claim: “Use ROUND() to prevent floating points” overstated what ROUND does. It removes drift in the stored value but doesn’t change how Excel represents decimals. I narrowed the wording.

Understated fixes: The channel_clean change fixes the pivot but not the source column, and the short-date format is a display fix because the values were already date serials. Both are now said plainly.

Customer_segments check: The memo says you checked it for SKU conversions, but the sampled columns have customer_id, not SKU.
Returns check: “Decimal points or missing values in return_reason” probably means refund_amount, since that’s where the missing values were found. I also corrected the Returns heading in “What I found.”

Typos and wording: I fixed lifttime_value, refound_amount and “if we can the values,” and replaced “variants of rows” with “variant labels.” “CSU exports” is flagged as a possible “CSV.”


I accepted typo and wording, and double-chccked on the customer-segments
