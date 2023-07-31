# Notification Server
---

Problem
---
 - The current notification server built-in lacks certain capabilities.
   - digest notifications
   - schedule delayed notifications
   - cancel a triggered notification
 - The inbuilt notification server has to be regularly maintained and updated to match the state of art notification

Novu (this is the open-source notification infrastructure available)
---
  - https://novu.co/
  - Open-source notification infrastructure
  - User's timezone awareness is another prominent feature
    <img width="829" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/e7a2b307-6e6c-4e1e-abc1-d3647396f90a">


## Requirement 1 - Digest Notifications

   - A digest notification is a notification that consolidates information from several notifications into one and delivers that notification to the end user instead of several separate messages.
   - Example 
     - Order(s) created for the last hour
     - Recommendation(s) created for the last day after we create the real-time recommendations
   - https://docs.novu.co/guides/how-to-add-digest-to-email-notifications/

 ## Requirement 2 - Schedule Delayed Notifications

  - The delay action awaits a specified amount of time before moving on to trigger the following steps of the workflow.
  - Example 
    - After the user signs up and connects to a store, the system schedules a one-day delay notification for the user to remind him to log in to check the insights and recos
  - https://docs.novu.co/platform/delay/#scheduled-delay
  
## Requirement 3 - Cancel Delayed Notifications

  -   The scheduled delay action needs to be cancelled 
    - Example 
      - User logs in 2 hours after the signup and connects and checks the workspace, then it is not required to send the login-reminder 
  -   https://docs.novu.co/api/cancel-triggered-event/
 
Novu Pricing
---
  - Self-hosted 
    - it is an open source https://github.com/novuhq/novu
    - if we deploy the components in our cloud VMs, Kubernetes, then no charge 
        <img width="904" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/0852b227-6a4f-4227-a86d-a59c9979fcfa">
    - We already hosting and running https://cube.dev/ (DAO layer) in our VMs and Kubernetes and not the cloud version
    - We can host the components and upgrade the versions regularly
    - NOVU suggests us to use the open source version if we have complicated PII security needs
        <img width="812" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/1da6fa4f-ac35-45ea-a6b4-ddfb1e465115">
  - Cloud hosted
    - the services are hosted and maintained in the cloud 
    - we can reach out to sales@novu.co 
      <img width="912" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/aff6b371-fcf7-4413-8671-cab8d23a1645">
    - https://www.crunchbase.com/organization/novu-1a6b
    <img width="559" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/f662c8fc-ffdf-43ba-90b0-323a1144d783">

How to configure
---
  - https://web.novu.co/workflows
  - invited the following team members 
    - gowtham@graas.ai 
    - ajinkya.patil@graas.ai 
  - Please check the workflows configured after login 
  - here is the API collection to trigger and cancel a notification https://github.com/venkat-sia/techdocuments/blob/main/Postman%20Collections/NOVU.postman_collection.json
  - Instant Notifications screenshots
    ---
    - <img width="951" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/02d9161a-085e-4c8e-8053-7b5269432cc2">
    - <img width="955" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/9ca9ed1f-0b75-4870-9bcb-241815c4ee32">
    - ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/2a161be9-70bf-462c-99ba-387cd8a59029)
    - ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/7a8b7893-4247-4881-8f63-966fcf0f35b1)
    - ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/ac8bac80-1c99-41c1-aa01-2b74b5e9832d)
    - <img width="765" alt="image" src="https://github.com/venkat-sia/techdocuments/assets/79962203/a01937f8-68fb-4101-813d-a2d10922c230">

