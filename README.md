# Duo-API-Playground

[![published](https://static.production.devnetcloud.com/codeexchange/assets/images/devnet-published.svg)](https://developer.cisco.com/codeexchange/github/repo/it-jonjon/Duo-API-Playground)

[![Duo API Playground](url-to-thumbnail-image)]([https://app.vidcast.io/share/embed/5ed27a58-3a8c-4aa2-8ce3-836fe086ef43](https://app.vidcast.io/share/5ed27a58-3a8c-4aa2-8ce3-836fe086ef43))


The Duo API Playground is a centralized [Postman](https://postman.com) workspace for managing and interacting with Duo accounts through the power of the Duo API. It is equipped with a variety of ready-to-use API requests and collections to help streamline a range of Duo tasks, such as account creation, application management, data retrieval, policy creation, log retrieval, and more.
You don't need to be an expert in Duo or APIs to make the most of this workspace. However, a basic understanding of Duo concepts is beneficial. If you encounter any uncertainties or wish to deepen your knowledge about specific API requests, parameters, rate limiting, etc., the Duo API documentation is your best resource. The aim is to furnish Cisco Duo customers and partners with tools and resourcess to help enhance their Duo operations, and scale and expand their Duo usage.

* [Admin API](https://duo.com/docs/adminapi)
* [Accounts API](https://duo.com/docs/accountsapi)
* [Accounts API with Admin API](https://duo.com/docs/accountsapi#using-accounts-api-with-admin-api)
* [Auth API](https://duo.com/docs/authapi)


## 🚀 Use Cases

This workspace is organized into different collections tailored for specific use cases:
* **Duo Accounts API**: Enables multi-tenant Duo customers to programmatically create, delete, and manage individual Duo customer accounts. New Duo accounts created using the Accounts API are subaccounts of the account where the Accounts API application exists, creating a "parent" and "child" account relationship.
* **Duo Accounts API with Admin API**: Enables multi-tenant Duo customers to interact with child accout objects via the Accounts API. You'll be able to fetch data from a number of Duo endpoints, e.g. Users, Groups, Integrations, Policies, Authentication Logs and more.
* **Duo Admin API [Parent]**: Facilitates interaction with the parent accont via the Admin API.
* **Duo Admin API [Child]**: Faciliates interaction with a specific Duo child account via the Admin API.
* **Duo Auth API [Child]**: Faciliates interaction with a specific Duo child account via the Auth API.
* **Duo Onboarding**: Contains a variety of requests to help streamline, operationalize and automate onboarding new Duo client accounts.
* **Duo Administrative Tasks**: Consists of various request combinations for tasks such as retrieving bypassed users across child accounts, assigning policies en masse, or pulling a Duo usage cost report.

NOTE: Each collection has unique configuration and parameter requirements. For detailed guidance on setup and usage, please consult the relevant collection specific documentation.


## Prerequisites

1. Sign up for a [Postman](https://www.postman.com/) account if necessary.
2. Download and install the [Postman Client](https://www.getpostman.com/apps).
3. Open Postman and create a new [Workspace](https://learning.postman.com/docs/getting-started/first-steps/creating-your-first-workspace/) in Postman.
4. Download each collection JSON file and the global variables file from the [Postman Collections & Variables](https://github.com/it-jonjon/Duo-API-Playground/tree/2144d8871a1fa10a760bcfcecc7bf7d1641ad2c6/Postman%20Collections%20%26%20Variables) folder in this repository.
    - Note: If you would like to avoid downloading each JSON file individually, navigate to the Duo API Playground main page and [download the entire repository](https://docs.github.com/en/repositories/working-with-files/using-files/downloading-source-code-archives).
5. Import each collection JSON file and the global variables JSON file into Postman. [Import data into Postman](https://learning.postman.com/docs/getting-started/importing-and-exporting/importing-data/).
6. Login to your [Duo Admin Panel](https://admin.duosecurity.com/) and create an [Accounts API](https://duo.com/docs/accountsapi#first-steps) and an [Admin API](https://duo.com/docs/adminapi#first-steps) integration.
    - Note: Enable all available permissions for the Admin API.
7. Return to Postman and navigate to [Environments > Globals](https://learning.postman.com/docs/sending-requests/variables/variables/#variable-scopes), and populate the following variables with their corresponding values:
    - `accounts_api_ikey`: Accounts API Integration Key
    - `accounts_api_skey`: Accounts API Secret Key
    - `accounts_api_host`: Accounts API API Hostname
    - `parent_admin_api_ikey`: Admin API Integration Key
    - `parent_admin_api_skey`: Admin API Secret Key
    - `parent_admin_api_host`: Admin API API Hostname



   

## 🚩 Disclaimer
I'm  excited you're exploring the Duo API Playground. This tool is intended to be a valuable asset for MSPs and other organizations using Duo in a multi-tenant capacity, facilitating effective API interactions. However, it's important to note that this workspace is offered AS IS. It is not officially supported by Cisco or Duo, and its use is subject to the user's discretion.
While designed to be as user-friendly and self-service as possible, I acknowledge that users may have questions or face challenges. I encourage you to explore, learn, and troubleshoot independently, as our team's capacity to offer support is currently limited. I also promote a community-driven approach, inviting users of the workspace to share their enhancements, insights, and knowledge with others in the MSP and broder Cisco community.

Thank you for your understanding and collaboration. I hope this workspace significantly contributes to the advancement of your Duo operations.



