# **eConnect 20.1.0**
## **Add-ons**

## **Enterprise Edition**


## **Magento Commerce**




# Table of Contents

- [**Environment Details**](#environment-details)
- [**Standard Features**](#environment-details)
- [**Add-ons**](#add-ons)
- [**Highlights**](#highlights)
- [**eConnect-base v2.0.0**](#econnect-base-v2.0.0)
- [**IDM**](#idm)	
- [**JIRA References**](#jira-references)	
- [**GitHub Links**](#github-links)	
- [**Documentation**](#documentation)	
- [**Point of Contact**](#documentation)


# **Environment Details**

| _ **Software Name** _ | _ **Version** _ |
| --- | --- |
| Magento Commerce | 2.3.4 |
| PHP version | 7.2.2x |
| RabbitMQ | 3.8.3 |
| Infor M3 (ST) | 13.4 |
| Infor M3 (MT) | 16.1 |
| ION Desk | 12.0.0 |


# **Standard Features**

All the standard functionalities of core eConnect are supported in v20.1.0, which include the following:
- Product Addition
- Product Synchronization
- Customer Price Synchronization
- Inventory Synchronization
- Customer Registration
- Customer Addition
- Customer Synchronization
- Order Creation
- Order Synchronization
- Shipment Synchronization
- Invoice History
- Order History
- Initial Load

# **Add-ons**

The following add-ons are also available for eConnect for M3 v20.1.0 Enterprise Edition
- Sales Representative v3.1.0
- Material Plan v4.0.0
- Multi-warehouse v4.0.0
- Order Edit v3.1.0
- Configurable Order Grid v2.5.0
- IDM v3.0.0
- RMA v4.0.0
- Gift Card v2.5.0

# **Highlights**

With 20.1.0, the part of eConnect functionality dealing with connectivity to eLink and Infor OS has been moved out of eConnect extension into a new extension named eConnect-base. From 20.1.0 onward, eConnect will depend on eConnect-base extension. For further details on eConnect-base, refer here.

**eConnect-base v2.0.0**

- It provides the connectivity to eLink and/or Infor systems with the use of a generic function which decides whether to call the eLink / ION APIs based on the M3 Connection Protocol chosen in the backend
- Acts as the communication layer for RabbitMQ Message consumption
- Acts as a core module for 
	- eConnect
	- IDM
	- Supplier Portal
- eConnect add-ons depend on both eConnect-base and eConnect
- eConnect and its Add-ons works only with eConnect-base configured
- IDM can now work without eConnect

# **IDM**

IDM has a new section called Mapping.

Attribute Key refers to M3_AttributeKey Name of IDM Document Type and the Custom key is the one we name it for our reference which we will use in code to retrieve M3_AttributeKey mapped here.
M3_AttributeKeys chosen for Upload Document type may vary for the Single Tenant and Multi-Tenant environment. Since we have to use those M3_Attribute keys in our code for Upload functionality, we now map it to a common custom key.
So, instead of changing M3_AttributeKeys in code for ST & MT, updating the mapping section in the backend is enough.
