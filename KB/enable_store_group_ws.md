TC metrics in source and preferred currency (Basic Use Case)
---

**Problem**
---

- Seller centre reports the numbers in the store currency
- AMs want to look at the revenue metrics in store currency

**Current state**
- data team is using a third party currency conversion service and do the currency conversion with the currency rates on the day the data created
- data team maintains the amount fields in the account preferred currency

**Enable currency in the Store Group**
---

1. Let's not allow changing the account preferred currency in TC 
2. Enable currency selection while creating the store group 
3. Note: currency selection contains only the following 
     1. account preferred currency 
     2. if all the stores selected are from the same country, then seller can choose the option to see the metrics for this store group in source currency
     3. if the store group has stores from different countries, then do not show any other currency; leave them with the account's preferred currency

**Enable Store Group in workspace**
---
1. Enable store group in the new workspace 
   1. Ecommerce Workspace
      1. GMV/order_sold_amount in both source and preferred currencies are maintained.
   2. Marketing Workspace - Onsite Ads 
      1. Ad spend (amount spent) and Ad revenue (conversions) are maintained in preferred currency
      2. Can the data team make the source fields available?
   3. Marketing Workspace - Offsite Ads 
      1. The ad channel and the storefront are running at different currencies.
      2. Ads channel is linked to storefront
      3. Can the data team make the amount fields available in 
         1. account preferred currency
         2. source currency
         3. storefront currency if the storefront currency and the ad channel currency are different
   4. Insights and Recommendations
      1. amount fields in the insights and recommendations are available in account preferred currency
      2. can the data team make the amount fields available in the following 
         1. account preferred currency
         2. source currency
         3. storefront currency if the storefront currency and the ad channel are different
 
TC metrics in any currency  (Advanced Use Case)
---       
   Option 1 (more accurate) - data layer
   ---
   - can cover in data warehouse tables or views 
   - hence the conversion happens using the rates on the data created time

   Option 2 (near accurate) - application layer
   ---
   - after db query 
   - apply the current days conversion rate on the aggregated values /daily values 
