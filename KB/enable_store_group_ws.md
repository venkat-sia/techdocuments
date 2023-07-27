Turbocharger metrics in source and preferred currency (Basic Use Case)
---

**Problem**
---

- Seller centre reports the numbers in the store currency
- AMs want to look at the revenue metrics in the store currency

**Current state**
- data team is using a third-party currency conversion service and does the currency conversion with the currency rates on the day the data (amount field) created
- data team maintains the amount fields in the account's preferred currency

**Enable currency in the Store Group**
---

1. Let's not allow changing the account preferred currency in Turbocharger 
2. Enable currency selection while creating the store group 
3. Note: currency selection contains only the following 
     1. account preferred currency 
     2. if all the stores selected are from the same country, then the seller can choose the option to see the metrics for this store group in the store currency
     3. if the store group has stores across different countries, then do not show any other currency; leave them with the account's preferred currency

**Enable Store Group in workspace**
---
1. Enable store group in the new workspace 
   1. E-commerce Workspace
      1. GMV/order_sold_amount in both store and preferred currencies are maintained.
   2. Marketing Workspace - Onsite Ads 
      1. Ad spend (amount spent) and Ad revenue (conversions) are maintained in the preferred currency
      2. Can the data team make the new set of amount fields in the store currency?
   3. Marketing Workspace - Offsite Ads 
      1. when the ad channel (FB/google ads) and storefront (lazada-my) run in different currencies.
      2. Ads channel is linked to the storefront
      3. Can the data team make the amount fields available in the following
         1. account preferred currency
         2. ad channel's currency
         3. storefront currency, if the storefront currency and the ad channel currency are different
   4. Insights and Recommendations
      1. amount fields in the insights and recommendations are available in the account's preferred currency
      2. can the data team make the amount fields available in the following 
         1. account preferred currency
         2. ad channel's currency 
         3. storefront currency 
 
TC metrics in any currency/supported currencies  (Advanced Use Case)
---       
   Option 1  - data layer
   ---
   - can we cover data warehouse tables or views ?
          - maintain the list of supported currencies 
          - the pipeline design and transformation does the currency conversions 
   - hence the conversion happens using the rates on the data created time
   - this option would be more accurate and High-performing.

   Option 2 - application layer
   ---
   - after the DB query 
   - apply the current day's conversion rate on the aggregated values /daily values
   - less accurate and performant
