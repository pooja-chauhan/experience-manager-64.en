---
title: Elastic Path
seo-title: Elastic Path
description: Learn how to deploy eCommerce with Elastic Path.
seo-description: Learn how to deploy eCommerce with Elastic Path.
uuid: 273f8a59-0e20-4763-91f5-d5cb2f77f631
contentOwner: Guillaume Carlino
products: SG_EXPERIENCEMANAGER/6.4/SITES
topic-tags: e-commerce
content-type: reference
discoiquuid: 744ca5b7-ff5a-415a-9f88-cde90f7a1dcb
pagetitle: Deploying eCommerce with Elastic Path
index: y
internal: n
snippet: y
---

# Elastic Path{#elastic-path}

Deploying the necessary eCommerce packages provides the full functionality of the eCommerce framework, together with a reference implementation of eCommerce functionality as provided with Elastic Path implementation (including a demonstration catalog).

This catalog is available under the English (US) branch ( `/content/geometrixx-outdoors/en_US`) of the Geometrixx Outdoors site.

>[!NOTE]
>
>This page contains links to the [Elastic Path website](http://www.elasticpath.com/). Certain areas need an account for full access.

### Installation of eCommerce with Elastic Path {#installation-of-ecommerce-with-elastic-path}

To install AEM with an Elastic Path integration configuration (using the demonstration catalog, Geometrixx Outdoors), the basic steps are:

1. [Install AEM](../../../sites/deploying/using/deploy.md) and any other pre-requisite packages (see [https://docs.elasticpath.com/display/EP611DEV/System+Requirements](https://docs.elasticpath.com/display/EP611DEV/System+Requirements) for details).
1. Install the latest demonstration content packages using the [Package Manager](../../../sites/administering/using/package-manager.md#packagemanager) in the following order:

    1. `ep-cortex-java-bindings`
    1. `ep-aem-integration`
    1. `cq-geometrixx-ep-content`

1. [Author](../../../sites/authoring/using/page-authoring.md) any supplementary pages that you need in AEM.

>[!NOTE]
>
>To be able to find and download those packages and the matching Elastic Path Commerce demo server, please [contact Elastic Path](http://www.elasticpath.com/company/contact-us).
>
>For additional details on Elastic Path for Adobe Marketing Cloud, please see [http://cms-developers.elasticpath.com](http://cms-developers.elasticpath.com).

If Elastic Path is running on any other machine or server (as recommended for Production):

1. Navigate to [http://localhost:4502/system/console/configMgr](http://localhost:4502/system/console/configMgr).
1. Open `com.elasticpath.web.config.EPConfigurationHandler`.
1. Update the `cortex.url` to point to that machine in which Elastic Path is running.

   ![](assets/chlimage_1-108.png)

>[!CAUTION]
>
>Use of the Elastic Path server requires a separate Elastic Path license.
