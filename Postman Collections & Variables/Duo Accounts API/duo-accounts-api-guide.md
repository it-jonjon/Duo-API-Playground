# Duo Accounts API Collection

This collection enables interaction with the Duo Accounts API, facilitating the creation, management, and deletion of Duo child accounts for Duo parent account administrators.

## 🚀 Getting Started

### Step 1: Configure the Accounts API Application
1. Log in to your Duo Admin Panel as an MSP tenant Owner.
2. Navigate to `Applications > Protect an Application` and find the Accounts API in the application list.
3. Click `Protect` on the far right to configure the application. Note your integration key, secret key, and API hostname.

### Step 2: Set Up Environment Variables in Postman
1. In Postman, go to `Environments > Globals`.
2. Populate the following variables with their corresponding values:
   - `accounts_api_ikey`: Accounts API Integration Key
   - `accounts_api_skey`: Accounts API Secret Key
   - `accounts_api_host`: Accounts API Hostname

You're now ready to use the Duo Accounts API collection within Postman.

## Collection Requests

- **Retrieve Accounts**: Retrieves a list of child accounts, returning their Account Name, Account ID, and API Hostname. These details are stored as an object map in the `duoChildAccounts` global variable.
- **Create Account**: Creates a new child account. Requires the `name` parameter. Refer to the Params tab to include the desired account name.
- **Delete Account**: Deletes a specified child account. Requires the `account_id` parameter. Use the Retrieve Accounts request to obtain the Account ID if needed.

## 💡 Collection Note

The **Retrieve Accounts** request is crucial for performing other requests within this workspace. It allows Duo administrators to compile a list of all child accounts, storing the returned child account IDs and names as an object mapping in the `duoChildAccounts` global variable. This variable facilitates mass operations across multiple Duo child accounts and is utilized in various requests within this collection and others, including the Admin API and Duo Onboarding collections, enhancing the management efficiency of child accounts.

