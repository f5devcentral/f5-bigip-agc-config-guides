.. _BIG-IP AGC config guides:

***************
F5 BIG-IP Access Guided Configuration
***************

Overview
########

Access Guided Configuration (AGC) provides simple, workflow-driven configuration templates that guide you through setting up a particular use case on the BIG-IP system. Each template requests minimal input and provides contextual help to assist users during setup. These configurations can be further edited, adding more components and apps, using the Guided Configuration interface.

This document includes on the following:

#. Guided Configuration API
#. Configuration guides for SAML Templates
 * SAML IdP Connector
 * SAML SaaS Applications

Guided Configuration API
########################

The Guided Configuration API is designed to deploy and manage template-driven configurations on the BIG-IP system using REST API. These templates are currently created using Guided Configurations workflows in the Access Policy Manager on the BIG-IP system. Guided Configuration API v1.0 now allows you to use API to create, update, or delete configurations and its associated objects for the following use cases:

* API Protection
* Azure AD Application

The APIs require input properties similar to those provided in the Guided Configuration interface. Once the configuration is created using APIs, it can be viewed in :menuselection:`Access -> Guided Configuration`. You can make additional modifications using the Guided Configuration interface or by using Guided Configuration REST APIs. All updates or deletions made using API are reflected in the
BIG-IP and the Guided Configuration UI.

.. toctree::
   :maxdepth: 1
   :titlesonly:
   :includehidden:
   :hidden:
   :caption: Guided Configuration API
   :glob:

   guided-config-api/*

Configuration guides for SAML Templates
#################################################

Federation category in AGC includes the following use cases requiring support for SAML.

* :guilabel:`SAML Service Provider`: Allows you to configure BIG-IP as SAML Service Provider with optional Single Sign On. 
* :guilabel:`SAML Identity Provider for Applications`: Allows you to configure BIG-IP as SAML Identity Provider for your applications, including SaaS apps such as Office 365 and Salesforce.

Follow the steps below to configure a use case with Access Guided Configurations.

#. Logon to the BIG-IP user interface and click :menuselection:`Access -> Guided Configuration`.
#. Select the :guilabel:`Federation` category.
#. Follow the instructions in on-line help to create a configuration for a specific Federation use case. If you are configuring

 - SAML Service Provider: Select a template method for Identity Provider and refer to the SAML IdP Connector configuration guide specific to the vendor.
 - SAML Identity Provider for Applications: Select a template method for Saas Applications and refer to the SAML SaaS Applications configuration guide specific to the application. 

SAML IDP Connector
******************

.. toctree::
   :maxdepth: 1
   :titlesonly:
   :includehidden:
   :collapse: True
   :hidden:
   :caption: SAML IDP Connector
   :glob:

   saml-idp-connector/*

BIG-IP as SAML Service Provider can work with different vendor-specific identity providers. SAML IdP Connector configuration guide describes the settings for a specific external identity provider.

SAML SaaS Applications
**********************

.. toctree::
   :maxdepth: 1
   :titlesonly:
   :includehidden:
   :collapse: True
   :hidden:
   :caption: SAML SAAS Applications
   :glob:

   saml-saas-applications/*

BIG-IP as SAML Identity Provider can work with different enterprise or cloud applications. SAML SaaS Applications configuration guide describes the settings for a specific application.
