# Duo-MSP-API-Playground

The Duo MSP API Playground is a centralized [Postman](https://postman.com) workspace for managing and interacting with Duo client accounts through the power of the Duo API. It is equipped with a variety of ready-to-use API requests and collections to help streamline a range of Duo tasks, such as account creation, application management, data retrieval, policy creation, log retrieval, and more.
You don't need to be an expert in Duo or APIs to make the most of this workspace. However, a basic understanding of Duo concepts is beneficial. If you encounter any uncertainties or wish to deepen your knowledge about specific API requests, parameters, rate limiting, etc., the Duo API documentation is your best resource. Our aim is to furnish partners with tools and resourcess to help enhance their Duo operations, and scale and expand their Duo usage.

* [Admin API](https://duo.com/docs/adminapi)
* [Accounts API](https://duo.com/docs/accountsapi)
* [Accounts API with Admin API](https://duo.com/docs/accountsapi#using-accounts-api-with-admin-api)
* [Auth API](https://duo.com/docs/authapi)


🚀 Use Cases

This workspace is organized into different collections tailored for specific use cases:
* Duo Accounts API: Enables customers to programmatically create, delete, and manage individual Duo customer accounts. New Duo accounts created using the Accounts API are subaccounts of the account where the Accounts API application exists, creating a "parent" and "child" account relationship.
* Duo Accounts API with Admin API: Used to interact with child accout objects via the Accounts API. You'll be able to fetch data from a number of Duo endpoints, e.g. Users, Groups, Integrations, Policies, Authentication Logs and more.
* Duo Admin API [Parent]: Facilitates interaction with the parent accont via the Admin API.
* Duo Admin API [Child]: Faciliates interaction with a specific Duo child account via the Admin API.
* Duo Auth API [Child]: Faciliates interaction with a specific Duo child account via the Auth API.
* Duo Onboarding: Contains a variety of requests to help streamline, operationalize and automate onboarding new Duo client accounts.
* Duo Administrative Tasks: Consists of various request combinations for tasks such as retrieving bypassed users across child accounts, assigning policies en masse, or pulling a Duo usage cost report.

NOTE: Each collection has unique configuration and paramater requirements. For detailed guidance on setup and usage, please consult the relevant collection specific documentation.

🚩 Disclaimer
We're excited you're exploring the Duo MSP API Playground. This tool is intended to be a valuable asset for MSPs and other organizations using Duo in a multi-tenant capacity, facilitating effective API interactions. However, it's important to note that this workspace is offered AS IS. It is not officially supported by Cisco or Duo, and its use is subject to the user's discretion.
While designed to be as user-friendly and self-service as possible, we acknowledge that users may have questions or face challenges. We encourage you to explore, learn, and troubleshoot independently, as our team's capacity to offer support is currently limited. We also promote a community-driven approach, inviting users of the workspace to share their enhancements, insights, and knowledge with others in the MSP community.
Thank you for your understanding and collaboration. We hope this workspace significantly contributes to the advancement of your Duo operations.



