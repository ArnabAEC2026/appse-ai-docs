---
title: "BigCommerce B2B"
slug: /app-integrations/bigcommerceb2b
---

BigCommerce is a powerful e-commerce solution which also offers a dedicated B2B Edition with advanced features tailored for wholesale and business-to-business operations, enabling companies to manage complex pricing structures, customer groups, company accounts, and bulk ordering efficiently. appse ai lets you seamlessly connect with your BigCommerce B2B account to automate key processes such as order management, company management, quote synchronization, and invoice updates—helping streamline operations and enhance efficiency through intelligent, automated workflows.

---

## Setup Credential

Follow the steps below to quickly set up your credential.

### Required Fields

The following fields are required to authenticate your BigCommerce account:

| Field      | Description                                  |
| ---------- | -------------------------------------------- |
| Store Hash | Unique identifier for your BigCommerce store |
| API Token  | Token used to authenticate API requests      |

### Step-by-Step Guide

#### 1. Find Your Store Hash

- Log in to your BigCommerce admin dashboard.
- In your browser's address bar, you will see a URL like:  
   `https://store-abc123.mybigcommerce.com/manage/dashboard`

<img src="/img/credentials/bigcommerce-b2b/bigcommerce-cred-store-hash.png" alt="APPSeAI BigCommerce Store Hash" width="700"/>

- The value after `store-` is your **Store Hash**.  
   Example: `abc123`

#### 2. Generate Your Access Token

- Navigate to **Settings** → **Store-level API accounts** → Click **Create API Account**.

<img src="/img/credentials/bigcommerce-b2b/bigcommerce-cred-access-token-1.png" alt="APPSeAI BigCommerce Store Level API Accounts" width="700"/>

<img src="/img/credentials/bigcommerce-b2b/bigcommerce-cred-access-token-2.png" alt="APPSeAI BigCommerce Store Create API Account" width="700"/>

- Enter a **Name** and select the required **OAuth scopes**.

Here is a recommended table for the required OAuth scopes:

| OAuth Scope                                  | Access    |
| -------------------------------------------- | --------- |
| Content                                      | None      |
| Checkout Content                             | None      |
| Customers                                    | modify    |
| Customers login                              | None      |
| Information & settings                       | None      |
| Marketing                                    | None      |
| Orders                                       | modify    |
| Order transactions                           | modify    |
| Create payments                              | create    |
| Get Payment methods                          | read-only |
| Stored Payment Instruments                   | None      |
| Products                                     | modify    |
| Themes                                       | None      |
| Carts                                        | None      |
| Checkouts                                    | None      |
| Sites & routes                               | None      |
| Channel settings                             | None      |
| Channel listings                             | None      |
| Storefront API tokens                        | None      |
| Storefront API customer impersonation tokens | None      |
| Store Locations                              | modify    |
| Store Inventory                              | modify    |
| Fulfillment Methods                          | modify    |
| Order Fulfillment                            | modify    |
| Metafield Ownership                          | None      |
| Metafields Access                            | full      |
| B2B Edition                                  | modify    |

:::info
Make sure the B2B Edition scope is checked. It is mandatory for accessing B2B features of BigCommerce.
:::

<img src="/img/credentials/bigcommerce-b2b/scope.png" alt="APPSeAI BigCommerce B2B Api Scope" width="700"/>

- Click **Save** to generate the token.

<img src="/img/credentials/bigcommerce-b2b/bigcommerce-cred-access-token-3.png" alt="APPSeAI BigCommerce B2B Save API" width="700"/>

- Copy and securely store the **Access Token** — it will not be shown again.

<img src="/img/credentials/bigcommerce-b2b/bigcommerce-cred-access-token-4.png" alt="APPSeAI BigCommerce B2B Access Token" width="700"/>

You will now have your **Access Token** for use within the APPSe AI platform.

### Test Your Credential

Once both **Store Hash** and **API Token** are entered into the credential form, use the **Save** button to store your configurations.

<img src="/img/credentials/bigcommerce-b2b/save-cred.png" alt="APPSeAI BigCommerce B2B Save Credentails" width="700"/>

- If successful, your BigCommerce B2B integration will be ready to use.
- If unsuccessful, try the following solutions:
  - Ensure your Store Hash and token are correct and that the scopes are properly set.
  - Ensure that your API token has the required scope for the Customers endpoint. Missing or insufficient permissions may result in authentication or data access errors. Refer to the OAuth scope recommendation table above.

---

### Triggers and Actions

## BigCommerce B2B Integration

### Overview
This file documents all available actions and triggers for integrating with BigCommerce B2B platform, enabling automation and seamless data synchronization between systems.

### Triggers
- **Order Created**: Initiates workflow when a new B2B order is placed
- **Order Updated**: Activates workflow when an existing order is modified
- **Customer Created**: Triggers workflow when a new B2B customer account is registered
- **Customer Updated**: Initiates workflow when customer information is changed
- **Product Updated**: Activates workflow when product details or inventory changes

### Actions
- **Create Order**: Generates a new B2B order in BigCommerce
- **Update Order**: Modifies existing order details or status
- **Create Customer**: Registers a new B2B customer account
- **Update Customer**: Modifies customer profile information
- **Get Products**: Retrieves product catalog and details
- **Update Inventory**: Syncs product stock levels
Here is a list of all the actions and triggers available for BigCommerce B2B:

---

### New Companies Created

**New Companies Created** trigger is used to fetch newly created company records from Shopify based on a specified time and limit.

#### Select Credentials and Action Events
<img src="" width="700" />

Click on **Continue** button.

---------------------------

#### Configuration

| Field | Description |
|------|-------------|
| Fetch Data Since | Specify the date and time to fetch new company records. (e.g., "01/04/2024 05:58") |
| Limit | Define the number of records to retrieve. (e.g., "10" or "1") |

> **Note:** Fetch Data Since is mandatory. Limit can be adjusted based on how many records you want to retrieve.

Click on **Continue**, then **Run** node.

-------------------------

#### Example Configuration
<img src="" width="700" />
<img src="" width="700" />

-------------------------

#### Result

```json


## Support

Need help? Contact our support team at hello@appse.ai
