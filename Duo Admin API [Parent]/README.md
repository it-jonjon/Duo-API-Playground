This collection is designed to interact with the MSP parent account via the Duo Admin API. The API has methods for creating, retrieving, updating, and deleting the core objects in Duo's system: users, phones, hardware tokens, admins, and integrations.
If you are unfamiliar with the Duo Admin API, its endpoints, and any of the required parameters, please refer to the corresponding Duo Admin API section in the documentation.

## 🚀 Getting started with this collection

1. **Login to your Duo Admin Panel**, click Applications > Protect an Application and locate the entry for Admin API in the applications list. Click Protect to the far-right to configure the application and make note of your integration key, secret key, and API hostname.
2. **Determine the permissions** you want to grant to this Admin API application, and specify which permissions you would like to grant in the Duo Admin Panel. **NOTE:** If you would like to use the entire list of requests in this collection, enable all permissions on the Admin API integrations page.
3. **After creating the Admin API**, navigate to Environments > Globals in Postman, and populate the following variables with their corresponding values:
   - `parent_admin_api_ikey`: Your Admin API Integration Key
   - `parent_admin_api_skey`: Your Admin API Secret Key
   - `parent_admin_api_host`: Your Admin API Hostname
4. **Navigate to a request** that you'd like to make and configure any required or optional parameters for that endpoint as outlined in the Duo Admin API documentation.

After populating the necessary environment variables, and configuring any required/optional parameters, you should now be able to use any request within the Duo Admin API collection.

## 🔍 Variable Reference

Below is a list of variables defined within this collection. Some variables are dynamically generated during API interactions, while others need to be manually configured.

| Variable Name         | Description                             | Scope |
|-----------------------|-----------------------------------------|-------|
| `parent_admin_api_ikey` | Your Admin API Integration Key. This needs to be manually set in the global variables. | Global |
| `parent_admin_api_skey` | Your Admin API Secret Key. This needs to be manually set in the global variables. | Global |
| `parent_admin_api_host` | Your Admin API Hostname. This needs to be manually set in the global variables. | Global |
