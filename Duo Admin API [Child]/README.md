This collection enables you to directly manage a specific Duo child account beneath your Duo MSP parent tenant via Duo Admin API. It offers methods to create, retrieve, update, and delete core Duo components such as users, phones, hardware tokens, admins, integrations, logs, and more.

NOTE: Before referring to steps below please see [Prerequisites](https://github.com/it-jonjon/Duo-API-Playground/blob/main/README.md#prerequisites).

## 🚀 Getting started with this collection

**Step 1:** In the Duo Admin API [Child] collection, go to the variables tab and enter the desired child account's name in the `child_account_name` variable field. This name must match exactly as it appears in the Duo Admin Panel. To confirm the correct account name, you can use the 'Retrieve Accounts' request in the Duo Accounts API collection, which provides a list of child accounts and their names.

**Step 2:** After populating `child_account_name`, navigate to the Setup Child Account folder and execute the 'Deploy Admin API' request. This request creates an Admin API integration on the target account, and populates the request credentials automatically for use.

**Step 3:** Be sure to configure any necessary or optional parameters for any particular request within this collection as specified in the Duo Admin API documentation. After setting up the environment variables and configuring parameters as needed, you're ready to utilize any request within the Duo Admin API [Child] collection.

## 💡 Collection Note

The collection performs multiple functions.

- **Duo Admin API:** This request automates the deployment of the Admin API through a series of steps. Initially, it runs "Retrieve Accounts" to retrieve the list of child accounts and identifies the specific account ID by referencing the `child_account_name` variable. Subsequently, it creates the Admin API on the identified child account via "Create Integration" and obtains the secret key required for authentication via "Retrieve Secret Key." The script stores these values as both collection variables to allow API calls to be made and also in the `child_admin_api_matrix` for future use. In subsequent requests, it checks for existing entries in the matrix to determine if the Admin API [Child] already exists for a particular account and updates the collection variables accordingly.

- **Clear Admin API Variables:** This request serves to clear the values of the collection variables related to the Admin API. It resets the `child_account_name`, `child_account_account_id`, `child_admin_api_ikey`, `child_admin_api_skey`, and `child_admin_api_host` variables to empty values. It's important to clear the variables to ensure requests are run on the correct account.

## 🔍 Variable Reference

Below is a list of variables defined within this collection. Some variables are dynamically generated during API interactions, while others need to be manually configured.

| Variable Name | Description | Scope |
|---------------|-------------|-------|
| `child_admin_api_ikey` | Your Accounts API Integration Key. This needs to be manually set in the global variables. | Global |
| `child_admin_api_skey` | Your Accounts API Secret Key. This needs to be manually set in the global variables. | Global |
| `child_admin_api_host` | Your Accounts API Hostname. This needs to be manually set in the global variables. | Global |
