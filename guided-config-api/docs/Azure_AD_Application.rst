========================================================================
Guided Configuration API : Azure AD Application
========================================================================

The Azure AD Application provides simplified secure access and single sign-on for IaaS and on-premise applications that use legacy authentication protocols, such as Kerberos and header-based authentication by instantiating an Azure AD application template. It setups BIG-IP APM as a SAML service provider and Azure AD as an Identity Provider. Integrating with BIG-IP APM provides centralized access to your applications and lets you leverage all the benefits that Azure AD offers.

Using Guided Configuration API, you can create the following objects for Azure AD Application:

* SAML SP Service
* Virtual Server
* Endpoint checks 
* Additional Checks
* Client and Server SSL profiles
* Pool
* SSO
* HTTP headers
* Session management for access profile

When you view your API created configuration for the first time, the configured applications display only the basic view's properties. To view advanced properties where applicable, enable the :guilabel:`Advanced Settings` slide button.

Supported Application Templates
--------------------------------

Azure AD Application currently supports the following Application Templates:

+-------------------------------------------------------------------------+--------------------------------------+
|                           Template Name                                 |            Template ID               |
+=========================================================================+======================================+
| F5 BIG-IP APM Azure AD integration                                      | 12f0b63d-efe6-4c9c-92ed-8b3f043b87a7 |
+-------------------------------------------------------------------------+--------------------------------------+
| Oracle PeopleSoft - Protected by F5 Networks BIG-IP APM                 | df7c8334-0ca8-4af4-bbcb-7bc79571c34a |
+-------------------------------------------------------------------------+--------------------------------------+
| SAP ERP Central Component (ECC) - Protected by F5 Networks BIG-IP APM   | e5619fca-f634-460b-b9d5-b308adfb075c |
+-------------------------------------------------------------------------+--------------------------------------+
| Oracle E-Business Suite - Protected by F5 Networks BIG-IP APM           | 19055112-9f0c-4d96-a3c1-fe7a32a2823e |
+-------------------------------------------------------------------------+--------------------------------------+
| JD Edwards - Protected by F5 Networks BIG-IP APM                        | 426a3a5e-5c8b-4e83-ad56-0b15f74e84dd |
+-------------------------------------------------------------------------+--------------------------------------+

Required Permissions and Application Registration
-------------------------------------------------

Before you begin, follow the steps below to register the app and request permissions: 

1. In Azure AD, create a service application under your organization's tenant directory using App Registration.
2. Register the App as Azure AD only single-tenant.
3. Request permissions for Microsoft Graph APIs and assign the following permissions to the application:

   * Application.Read.All
   * Application.ReadWrite.All
   * Application.ReadWrite.OwnedBy
   * Directory.Read.All
   * Group.Read.All
   * IdentityRiskyUser.Read.All
   * Policy.Read.All
   * Policy.ReadWrite.ApplicationConfiguration
   * Policy.ReadWrite.ConditionalAccess
   * User.Read.All

4. Grant admin consent for your organization's directory.
5. Copy the Client ID, Client Secret, and Tenant ID and add them to the Azure AD Application configuration.
   
Refer `Quickstart: Configure a client application to access web APIs <https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis>`_ for more information.


GC API Reference
-----------------

For Guided Configuration API and Schema Reference, click `Guided Configuration API v1.0 <https://clouddocs.f5networks.net/products/agc-api/1.0/apidocs.html>`_.