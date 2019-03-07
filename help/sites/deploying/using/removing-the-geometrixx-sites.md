---
title: Removing the Geometrixx Sites
seo-title: Removing the Geometrixx Sites
description: Learn how to remove the sample Geometrixx content.
seo-description: Learn how to remove the sample Geometrixx content.
uuid: 87f4e84a-9094-4136-856c-be99a0b5c68d
contentOwner: User
products: SG_EXPERIENCEMANAGER/6.4/SITES
content-type: reference
discoiquuid: 8896640f-40d2-47b8-a7a2-41ac596c8514
index: y
internal: n
snippet: y
---

# Removing the Geometrixx Sites{#removing-the-geometrixx-sites}

AEM comes with a set of sample Geometrixx websites. You can remove this sample content through the **Package Manager**.

The individual geometrixx-related packages are:

* `cq-geometrixx-outdoors-ugc-pkg-*<version>*.zip`
* `cq-geometrixx-pkg-*<version>*.zip`
* `cq-content-mac-*<version>*.zip`
* `cq-geometrixx-login-pkg-*<version>*.zip`
* `cq-geometrixx-users-pkg-*<version>*.zip`
* `cq-geometrixx-workflow-pkg-*<version>*.zip`
* `cq-geometrixx-outdoors-pkg-*<version>*.zip`
* `cq-geometrixx-commons-pkg-*<version>*.zip`
* `cq-geometrixx-media-pkg-*<version>*.zip`

To remove an individual package, simple click **Uninstall** on that package.

There is also a super-package:

* `cq-geometrixx-all-pkg-5.6.12.zip`

This package includes all the above individual packages. To remove all the geometrixx-related content at once, click **Uninstall** on this package. The super-package will go into the uninstalled state, and all the individual packages will disappear from the package manager view.

You have now an "empty" AEM instance without any demonstration sites.

>[!NOTE]
>
>When upgrading, geometrixx sites are automatically re-installed. You may need to remove geometrixx web sites after upgrading if you do not want these samples.
