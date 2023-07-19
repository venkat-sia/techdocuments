# GRaaS Brand

## Product Listing / Sync (Import Inventory) / Edit Listing

1. if the brand exists in the inventory / product listing, then
2. **check if there is a graas brand available in brand_mapping (yet to push live)** update the brand id as graas brand id in the product listing and product master
3. else create new brand in the brand mapping 
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

4.update the brand id created as graas_brand_id in the inventory and product master 


## Order Polling (yet to enable the flag in live)
1. check if the SKU (product master) has the graas brand, if it exists then insert graas brand id into the respective order item

## Batch Job to populate the orders with GRaaS Brand (yet to develop)
2. On-demand or a cron job to populate the GRaaS Brand into the order item from product master/ inventory


## Product Master (yet to develop)(seller can enter or edit the brand name)
1. the seller/AM enters the brand name or select the graas brand from the drop-down for the product (seller SKU)
2. create a new graas brand id or update the existing graas brand id into the product master for the product 