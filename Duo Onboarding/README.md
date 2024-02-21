This collection is designed to help perform some of the initial onboarding processes for a new Duo client account. The collection includes requests for creating an account, updating settings, creating integrations, creating and applying policies, enrolling users, and more. For more insight into the specific requirements and usage of each collection of requests, please refer to documentation found within each folder.

## Account Setup
- Create Account (name the account)
- Modify Edition
- Modify Settings
- Modify Custom Branding
- Modify Custom Messaging

## Application Management
- Create Integration

## User Enrollment
- Create Group
- Enroll Users

## Policy Management
- Retrieve Global Policy
- Update Global Policy
- Apply Policy

## User Management
- Retrieve enrollment status
- Assign enrolled users to group

## Clean Up
- Clear Variables
  - This request cleans up all of the created global variables

## 🚀 Getting started with this collection
Note: If you haven't already, head over the Accounts API collection and set up the necessary prerequisites. Once you've completed the prerequisites, please follow the steps below.

1. **Navigate to Duo Onboarding > Variables**, and input the desired account name under the `newChildAccount` collection variable. Keep the format as `["New Child Account"]` and only replace the text within the double quotes and brackets. Example: `["Block Buster"]`
2. **(Optional)**: We've built in a capability that allows you to enroll a CSV list of users. The CSV list should contain two column headers: 'username' and 'email', followed by the respective username and email address of each user you wish to enroll. To define this in the workspace, navigate to Duo Onboarding > Variables, and input the CSV list to the `usersCsv` variable.
3. **Each request within the collection has its own parameter and configuration requirements**. Please ensure to define these according to your needs before executing each request. For detailed information on what is required, refer to the documentation provided in the corresponding folder of each section, and/or the relevant Duo API documentation.
4. **Once you've defined the configuration according to your requirements**, it's best to run the requests in sequential order via the Collection Runner, however, these requests can be run individually. Please note, however, that some requests depend on other requests to be run beforehand. Consult the Request Dependency Matrix for further insight.

## 🔍 Variable Reference
Below is a list of variables defined and used within this collection. Some variables are dynamically generated during API calls, while others need to be manually configured.

- **`accounts_api_ikey`**: Your Accounts API Integration Key. This needs to be manually set in the global variables.
- **`accounts_api_skey`**: Your Accounts API Secret Key. This needs to be manually set in the global variables.
- **`accounts_api_host`**: Your Accounts API Hostname. This needs to be manually set in the global variables.
- **`newChildAccount`**: Defines the name of the new Duo account.
- **`usersCsv`**: Defines a CSV list for user enrollment, containing 'username' and 'email' for each entry.

## ⚙️ Request Dependency Matrix
This table provides an overview of the various requests within this collection. It outlines each request, its purpose, and any dependent requests it may rely on for successful execution.

| Request                  | Description                                                                 | Dependencies                  |
|--------------------------|-----------------------------------------------------------------------------|-------------------------------|
| Create Account           | Creates a new Duo customer account                                          | None                          |
| Modify Edition           | Sets the effective Duo edition for a child account                         | Create Account                |
| Modify Settings          | Change global Duo settings                                                  | Create Account                |
| Modify Custom Branding   | Change effective custom branding settings                                   | Create Account                |
| Modify Custom Messaging  | Updates current custom messaging settings, shown to users in the Universal Prompt | Create Account          |
| Create Integration A/B   | Creates a new integration. The new integration key and secret key are randomly generated and returned in the response | Create Account       |
| Create Group             | Create a new group                                                          | Create Account                |
| Enroll Users             | Enroll a user with username and email address and send them an enrollment email that expires after valid_secs seconds | Create Account    |
| Retrieve Global Policy   | Retrieve a complete set of all policies. Includes all policy section data for each policy. | Create Account             |
| Update Global Policy     | Change an existing policy's name, add or remove policy sections, or update keys/values for the policy with the specified policy_key | Create Account, Retrieve Global Policy |
| Create Policy A/B        | Creates a new custom policy with the name specified in the parameters       | Create Account, Create Integration A/B |
| Retrieve Enrollment Status| Retrieves user enrollment status (`Retrieve Users > is_enrolled: true or false`) | Create Account, Enroll Users |
| Assign Enrolled Users to Group | Associate a group with ID `group_id` with the user with ID `user_id`       | Create Account, Retrieve Enrollment Status |

