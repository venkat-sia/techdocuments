## Automate Inventory Polling for any channel (Shopify,shopee)

`The data team wants the daily update on the inventory for recommendations and insights`


### 1. UI and batch server
		Enable the start date and end date for inventory polling for that channel
### 2. Channel Server
		Enable the start date and end date for inventory polling in the channel server
### 3. Connect
		At the time of connecting store, Please set the lastInventoryPollingTime as 1 year ago
### 4. Create Shopify Inventory Polling job (one day once) (bookkeeping batch, k8s job) which will
		1. Iterate all the channel's merchants / or merchant list provided in the main program argument 
		2. Read the db 
		3. Take the lastInventoryPollingTime as start date
		4. Set the end date as current date
		5. Call the batch API with start date and end date
		6. Once the inventories are polled successfully, please update lastInventoryPollingTime as current time.

