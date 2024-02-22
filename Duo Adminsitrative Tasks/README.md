# Duo Adminstrative Tasks

In this collection, we've included a number of requests to address some common MSP use cases.
**Note:** Be sure to refer to the Duo Accounts API and Duo Admin API [Parent] collections, and ensure the Accounts API and Admin request credentials have been populated in the global variables before continuing. If you do not populate the variables as defined in those two collections, some requests in this collection will not work properly.

🚀 **Getting familiar with this collection**

- **Bypass Users:** The requests in this folder allow pulling a list of users in Bypass status across all sub-accounts and, if desired, setting those users to Active status.
  - **Get Users in Bypass status:** Pulls the full list of users in Bypass status across all child accounts and stores the users in the `bypassUserList` global variable.
  - **Set users in Bypass status to Active status:** Iterates over that list of users in the `bypassUserList`, and sends individual calls to each account to set these users to 'Active' status.
  - **Note:** The sequence of requests is comprehensive. If you have users you wish to maintain in 'Bypass' status, they should be removed from the `bypassUserList` global variable before running the 'Set Users in Bypass status to Active' request.

- **Cost Report:** The "Cost Report" comprises multiple requests designed to provide a detailed breakdown of your current Duo usage, including the total number of users, the associated edition (Essentials, Advantage, Premier), and the corresponding costs. It provides both a console-friendly table and a CSV report of each client's Duo usage.
  - **Important Note:** The Duo Admin API doesn't offer a method to retrieve the edition of the parent account natively, so to work around this, we have added a collection variable `parent_account_edition` that must be manually set to the edition of the parent account. It must be one of:
    - Duo Essentials
    - Duo Advantage
    - Duo Premier

- **Policy Management:** The request in this folder updates the global policy for each Duo child account using the list of account IDs in `duoChildAccounts`.
  - **Update Policy Section Data:** Navigate to the Body tab of the 'Update Global Policy' request and modify the policy section data to align with your desired security policies. See Policy Section Data.
  - **Update Global Policy:** Execute the 'Update Global Policy' request. This process iterates over each ID in your `duoChildAccounts`, applying the newly configured global policy settings to all your Duo child accounts.

- **Universal Prompt:** The requests in this folder automate the updating of in-scope applications to the Universal Prompt across the full list of child accounts. It involves two key steps:
  - **Retrieve V4 Integrations:** This step iterates over the list of child account IDs to identify and collect applications eligible for the Universal Prompt update. These applications are stored in a variable (`universal_prompt_ikeys`), mapped by account ID, account name, and integration keys.
  - **Enable Universal Prompt:** The next step takes the identified integration keys and activates the Universal Prompt for these applications on the target accounts.
