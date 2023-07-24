# GRaaS Brand

## Product Listing / Sync (Import Inventory) / Edit Listing

- if a brand name exists in the inventory / product listing and no graasBrandID available, then
- **check if there is a graasBrandID available in brand_mapping for the brand name(yet to push live)** 
- if graasBrandID exists in brand_mapping then update the graasBrandID in the inventory and product master
- else create graasBrandID in the brand mapping 
```
{
    "_id" : ObjectId("6436cc9db71bb17e293dee06"),
    "brandName" : "olivia burton",
    "brandNames" : [ 
        "olivia burton",
        "Olivia Burton"
        "olivia_burton"
    ],
    "lemmatizedBrandName" : "olivia burton",
    "brandNameMapping" : [ 
        {
            "name" : "olivia_burton",
            "marketplace" : "lazada-SG"
        }
    ],
    "timeLastUpdated" : NumberLong(1681313035)
}
```
- then update the graasBrandID  in the inventory and product master 
- Note: the graas brand name will be the brand name from the inventory 

## Creating / updating graasBrandID through admin for a product (yet to develop)
- develop a page in the admin to create / edit the graasBrandID for a product (product master)
- support bulk import
  - choose from graas brand names 
  - create a new brand name
    - **check if there is a graasBrandID available in brand_mapping for the brand name(yet to push live)** 
    - if graasBrandID exists in brand_mapping then update the graasBrandID in the inventory and product master
    - else create graasBrandID in the brand mapping 
    - then update the graasBrandID  in the inventory and product master


## Order Polling (yet to enable the flag in live)
- check if the SKU (product master) has the graasBrandID 
  - if it exists then insert graasBrandID into the respective order item

## Batch Job to populate the orders with GRaaS Brand (yet to develop)
- On-demand or a cron job to populate the graasBrandID into the order item from product master/ inventory

## Admin can change the brand name globally for any graasBrandID (yet to develop)
- develop an admin page hence the super user can change the brand name of a graasBrandID globally

## Account admin can change the  brand name for a graasBrandID only for their account  (yet to develop)
- maintain the brand name at the account level which overrides the default one at global TC level
  ``` 
     {
       merhcantID:"AABSO",
        [ 
          {
            graas_brand_id:"",
            brandName:""
          }
        ]
     }
  ```
