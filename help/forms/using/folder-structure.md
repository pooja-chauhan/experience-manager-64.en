---
title: Understanding the folder structure
seo-title: Understanding the folder structure
description: How to understand the folder structure of AEM Forms workspace source code to customize.
seo-description: How to understand the folder structure of AEM Forms workspace source code to customize.
uuid: 7cfd3eab-7b2f-4c99-8bba-9f89e4115e44
contentOwner: robhagat
content-type: reference
products: SG_EXPERIENCEMANAGER/6.4/FORMS
topic-tags: forms-workspace
discoiquuid: 4d0f5064-a936-4545-b2c1-19f76d77e87d
index: y
internal: n
snippet: y
---

# Understanding the folder structure{#understanding-the-folder-structure}

AEM Forms workspace components are designed on MVC architecture using Backbone. Each component has a file for:

* Model, that contains business logic.
* Template, that is an HTML file containing interface controls.
* View, that acts as a Controller class to Template.

The assets for all the components are placed in the folder structure described below. To access the assets, log in to CRXDE Lite and browse to `/libs/ws/js/runtime/`.

**models** Contains backbone models.

**views** Contains backbone views.

**templates** Contains only the HTML templates for the components.

**routes** Contains universal routes. Templates folder inside routes contains the HTML code and the references to the components.

**services** Contains service interface to call Adobe Experience Manager server APIs on REST endpoint.

**util** Contains generic utilities usable by multiple components.

[**Contact Support**](https://www.adobe.com/account/sign-in.supportportal.html)