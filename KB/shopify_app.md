Graas – Growth as a Service Shopify app
---

### Shopify Connect Current State
- **Connect**
	+ The connect page requires the seller to do the manual steps documented here https://turbocharger.graas.ai/connector/help/Connector-shopify.html
		* The following has to be manually entered in the TC connect page
			- API Key
			- Secret Key
			- Access Token
- **Enable Shopify tracker**
    + Once connected, the tracker has to be installed manually on the Shopify site
		* then click Enable Shopify Tracker on the Connect page
          ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/71046b9f-4837-4785-ab94-241c8a12b9e1)
- **Shopify sellers don't know about Turbocharger**
   + Our sales team finds the prospective Shopify sellers for TC 
		

### Graas – Growth as a Service Shopify ap
- **Connect flow is streamlined**
	+ Sellers log in to their store (example: https://admin.shopify.com/store/testgraas007/)
		![image](https://github.com/venkat-sia/techdocuments/assets/79962203/98635130-3633-4a9a-8c11-95aabd90fd07) 
 	+ Graas app is in pilot mode and kept as an unlisted app; hence you can't find it under Add apps
	+ Please install it from  the app's App Store listing page, that is, to open our site  https://apps.shopify.com/graas in the browser
        ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/c1379563-6480-460a-949a-a67928b8a053)
		![image](https://github.com/venkat-sia/techdocuments/assets/79962203/28425e2f-de2c-4b97-978b-0835427c190e)
  	+ The user will be redirected to the turbocharger login or sign-up page
        ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/4b50a03e-13a0-4013-a09a-1e01e3c24fa4)
    + If the seller is an existing customer of Turbocharger, then they can log in using their username and password, and the seller will be taken to the Connect page
        ![image](https://github.com/venkat-sia/techdocuments/assets/79962203/5ce7e70f-fb14-46cd-a210-4dfaa1cfec67)
	
    + If the seller is NOT an existing customer of Turbocharger, then they can sign up, and the seller will be taken to the Connect page

 - **Next steps**
     + **Shopify sellers to find the Turbocharger from the app store**
	     - onboard new sellers using the https://apps.shopify.com/graas
	     - switch from an unlisted app to a listed app. Hence it will be visible under "Add apps."
     + **Streamline the tracker installation**
	     - implement the pixel APIs webhooks
	     - enable single data pipeline for tracker
	     - enhance the app to register the pixel API and auto-install the call-back function to listen to pixel events
 
     + **Pixel API console log**
       - npm deploy <app name>
       - javascript function gets injected into the seller's store?
       - installation connect flow 
         - any additional scopes 
         - any other steps to register the seller to listen pixel api events?
       - we don't change anything in the app setup
         - do we need to resubmit for approval? **NO , not required**
