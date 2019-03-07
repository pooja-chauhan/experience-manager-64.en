---
title: Configuring Asset Upload Restrictions
seo-title: Configuring Asset Upload Restrictions
description: Learn how to configure Adobe Experience Manager (AEM) Assets to restrict the type of assets (files) that users can upload.
seo-description: Learn how to configure Adobe Experience Manager (AEM) Assets to restrict the type of assets (files) that users can upload.
uuid: be7c5168-9b26-4546-8711-45a617fd0b33
contentOwner: Chiradeep Majumdar
products: SG_EXPERIENCEMANAGER/6.4/ASSETS
topic-tags: administering
content-type: reference
discoiquuid: 265b2dae-fded-45b5-af29-212fd4462a8e
index: y
internal: n
snippet: y
---

# Configuring Asset Upload Restrictions{#configuring-asset-upload-restrictions}

You can configure Adobe Experience Manager (AEM) Assets to restrict the type of assets (files) that users can upload. This feature helps you eliminate the possibility of users uploading assets in an undesired format or uploading any malicious files. The `Day CQ DAM Asset Upload Restriction` service enables you to control the type of files that users can upload. By default, AEM Assets allows users to upload assets of all MIME types. However, you can configure the service to restrict users to upload files of specific MIME types only.

1. Go to *http://&lt;server&gt;:&lt;port&gt;/system/console/configMgr* to open the Configuration Manager web console.
1. Open the **Day CQ DAM Asset Upload Restriction** service in Edit mode. By default, the **Allow all MIME** option is selected, which allows users to upload files of all MIME types.

   ![](assets/chlimage_1-378.png)

1. To restrict users to upload files of certain MIME types only, unselect the **Allow all MIME** option and specify allowed MIME types in the **Allowed Asset MIMEs (regex)** fields using regular expressions.

   ![](assets/chlimage_1-379.png)

1. Click/tap **Save** to save the changes. If you specify MIME-strings for allowed MIME types, the upload operation fails for any asset with MIME type that doesn’t match the configured MIME strings in these fields.
