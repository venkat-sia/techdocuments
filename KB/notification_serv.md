# Notification Server
---

## Requirement 1 - Digest Notifications

  * Publisher - Order Management Server
  * Reciever - Seller
  * Message - Order 34578346785 created on 15-07-2023 13:00:00

  * Publisher - Order Management Server
  * Reciever - Seller
  * Message - Order 23453245 created on 15-07-2023 13:10:00

  collects multiple notifications, aggregates them into a single message, and delivers it to the subscriber.
  https://docs.novu.co/guides/how-to-add-digest-to-email-notifications/

  * Publisher - Order Management Server
  * Reciever - Seller
  * Message - Orders 34578346785,23453245 created between 13:00:00 and 14:00:00

## Requirement 2 - Schedule Delayed Notifications

  * Publisher - Account Management Server (15-07-2023 13:20:00)
  * Reciever - Seller
  * Message - (16-07-2023 13:20:00) Your data is ready please login to check the insights created
  https://docs.novu.co/platform/delay/#scheduled-delay

## Requirement 3 - Schedule Delayed Notifications

  * Publisher - Account Management Server (15-07-2023 15:20:00)
  * Reciever - Seller
  * Message - User has logged in and checked analyze
  
  this should cancel any active pending login notifications
   https://docs.novu.co/api/cancel-triggered-event/