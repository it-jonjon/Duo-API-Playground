In this collection, we've included a number of requests to address some common MSP use cases.

NOTE: Before referring to steps below please see [Prerequisites](https://github.com/it-jonjon/Duo-API-Playground/blob/main/README.md#prerequisites).

## 🚀 Getting familiar with this Collection

### Bypass Users

The requests in this folder allow pulling a list of users in Bypass status across all sub-accounts and, if desired, setting those users to Active status.

- **Get Users in Bypass status:** Pulls the full list of users in Bypass status across all child accounts and stores the users in the `bypassUserList` global variable.
- **Set users in Bypass status to Active status:** Iterates over the list of users in the `bypassUserList`, and sends individual calls to each account to set these users to 'Active' status.

**Note:** The sequence of requests is comprehensive. If you have users you wish to maintain in 'Bypass' status, they should be removed from the `bypassUserList` global variable before running the 'Set Users in Bypass status to Active' request.

### Cost Report

The "Cost Report" comprises multiple requests designed to provide a detailed breakdown of your current Duo usage, including the total number of users, the associated edition (Essentials, Advantage, Premier), and the corresponding costs. It provides both a console-friendly table and a CSV report of each client's Duo usage.

**Important Note:** The Duo Admin API doesn't offer a method to retrieve the edition of the parent account natively, so to work around this, we have added a collection variable `parent_account_edition` that must be manually set to the edition of the parent account. It must be one of:

- Duo Essentials
- Duo Advantage
- Duo Premier

Before starting, ensure that the edition name is spelled correctly in the collection variable. If an edition name is misspelled or missing, the function will not run successfully.

### Push Phish Simulator

This collection enables Duo administrators to conduct a phishing test using Duo Push or Phone Call on a select user group. By simulating authentication requests, it helps administrators assess whether users can distinguish and approve only legitimate authentication attempts.
