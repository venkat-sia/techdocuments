# Notification Server
---

Problem
---
 - The current inbuilt notification server does not have the following capabilities
   - digest notifications
   - schedule a delayed notifications
   - cancel a triggered notification
 - The inbuilt notification infrastructure has to be regularly maintained and update to match the state of art notification

Novu
---
  - https://novu.co/
  - Open-source notification infrastructure
  - User's timezone awareness is another prominent feature


## Requirement 1 - Digest Notifications

   - A digest notification is a notification that consolidates information from several notifications into one and delivers that notification to the end user instead of several separate messages.
   - Example 
     - Order(s) created for the last one hour
     - Recommendation(s) created for the last one day after we create the recommendations real-time
   - https://docs.novu.co/guides/how-to-add-digest-to-email-notifications/

 ## Requirement 2 - Schedule Delayed Notifications

  - The delay action awaits a specified amount of time before moving on to trigger the following steps of the workflow.
  - Example 
    - After the user signs up and connects a store , the system schedules a one day delay notification for the user to remind him of login to check the insights and recos
  - https://docs.novu.co/platform/delay/#scheduled-delay
  
## Requirement 3 - Schedule Delayed Notifications

  -   The scheduled delay action needs to cancelled 
    - Example 
      - User logs in 2 hours after the signup and connect and checks the workspace ,then it is not required to send the login reminder 
  -   https://docs.novu.co/api/cancel-triggered-event/
 
Novu Pricing
---
  - Self-hosted 
    - it is a open source 
    - if we deploy the components in our cloud vms or kubernetes then no charge 
        <img width="904" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/0852b227-6a4f-4227-a86d-a59c9979fcfa">
  - Cloud hosted
    - the services is hosted and maintained in cloud 
    - we can reach out to sales@novu.co 
      <img width="912" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/aff6b371-fcf7-4413-8671-cab8d23a1645">

How to configure
---
  - https://web.novu.co/workflows
  - invited the following team members 
    - gowtham@graas.ai 
    - ajinkya.patil@graas.ai 
  - Please check the workflows configured after login 
  - here is the api collection to trigger and cancel a notification
  - Instant Notifications screenshots
    ---
    - <img width="951" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/02d9161a-085e-4c8e-8053-7b5269432cc2">
    - <img width="955" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/9ca9ed1f-0b75-4870-9bcb-241815c4ee32">
    - ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/2a161be9-70bf-462c-99ba-387cd8a59029)
    - ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/7a8b7893-4247-4881-8f63-966fcf0f35b1)
    - ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/ac8bac80-1c99-41c1-aa01-2b74b5e9832d)
    - <img width="765" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/a01937f8-68fb-4101-813d-a2d10922c230">

