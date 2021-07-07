.. _BIG-IP AGC config guides:

***************
F5 BIG-IP Access Guided Configuration
***************

Overview
########

Access Guided Configuration (AGC) provides simple, workflow-driven configuration templates that guide you through setting up a particular use case on the BIG-IP system. Each template requests minimal input and provides contextual help to assist users during setup. These configurations can be further edited, adding more components and apps, using the Guided Configuration interface.

This document includes the following:

#. Guided Configuration API
#. Configuration guides for SAML Templates

   - SAML IdP Connector

   - SAML SaaS Applications

Guided Configuration API
########################

The Guided Configuration API is designed to deploy and manage template-driven configurations on the BIG-IP system using REST API. These templates are currently created using Guided Configurations workflows in the Access Policy Manager on the BIG-IP system. Guided Configuration API v1.0 allows you to use API to create, update, or delete configurations and their associated objects for API Protection Proxy and Azure AD Application use cases. 

Guided Configuration API requires input properties similar to those provided in the Guided Configuration interface. Once the configuration is created using APIs, you can view it in :menuselection:`Access -> Guided Configuration`. You can make additional modifications using the Guided Configuration interface or by using Guided Configuration APIs. All updates or deletions made using API are reflected in the BIG-IP system and the Guided Configuration UI.

.. toctree::
   :titlesonly:
   :includehidden:
   :maxdepth: 2

   guided-config-api/guided-config-api

Configuration guides for SAML Templates
#################################################

Federation category in AGC includes the following use cases requiring support for SAML:

* :guilabel:`SAML Service Provider`: Allows you to configure the BIG-IP system as SAML Service Provider with optional Single Sign-On. 
  
* :guilabel:`SAML Identity Provider for Applications`: Allows you to configure the BIG-IP system as SAML Identity Provider for your applications, including SaaS apps such as Office 365 and Salesforce.

SAML IDP Connector
******************

BIG-IP as SAML Service Provider can work with different vendor-specific identity providers. SAML IdP Connector configuration guide describes the settings for a specific external identity provider.

.. toctree::
   :titlesonly:
   :includehidden:
   :maxdepth: 2

   saml-idp-connector/idp-connector-configGuide

SAML SaaS Applications
**********************

BIG-IP as SAML Identity Provider can work with different enterprise or cloud applications. SAML SaaS Applications configuration guide describes the settings for a specific application.

.. toctree::
   :titlesonly:
   :includehidden:
   :maxdepth: 2

   saml-saas-applications/saas-application-configGuide

