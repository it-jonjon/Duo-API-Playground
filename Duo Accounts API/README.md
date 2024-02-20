This collection is designed to interact with the Duo Accounts API. The Accounts API allows a Duo parent account administrator to create, manage, and delete Duo child accounts.

🚀 Getting started with this collection

Step 1: Login to your Duo Admin Panel as an Owner of your MSP tenant, click Applications > Protect an Application and search for Accounts API in the applications list. Click Protect to the far-right to configure the application and make note of your integration key, secret key, and API hostname.

Step 2: After creating the Accounts API in the Duo Admin Panel, return to Postman and navigate to Environments > Globals, and populate the following variables with their correspoding values.
* accounts_api_ikey: Accounts API Integration Key
* accounts_api_skey: Accounts API Secret Key
* accounts_api_host: Accounts API API Hostname

You should now be able to use any request within the Duo Accounts API collection.
Within this colllection, you'll find three individual API requests:

* Retrieve Accounts: Retreives a list of child accounts and returrns their Account Name, Account ID, and API Hostname. These values are then stored as an object map in the ```duoChildAccounts``` global variable.
* Create Account: Creates a new child account beneath the parent. Requires the ```name``` paramater. Please see the Params tab to include the name of the account you'd like to create.
* Delete Account: Deletes a child account beneath the parent. Requires the ```account_id``` paramater. Please see the Params tab to include the Account ID of the account you'd like to delete. You can run the Retrieve Accounts request to get the Account ID if you don't have it already.
