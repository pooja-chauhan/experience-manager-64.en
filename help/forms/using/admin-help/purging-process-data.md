---
title: Purging process data
seo-title: Purging process data
description: Process data that is generated when a long-lived process is invoked can become too large, resulting in lower AEM forms performance and the use of unnecessary disk space. See how you can purge process data.
seo-description: Process data that is generated when a long-lived process is invoked can become too large, resulting in lower AEM forms performance and the use of unnecessary disk space. See how you can purge process data.
uuid: e99297b8-daba-4089-9f78-69d2669c594d
contentOwner: admin
content-type: reference
geptopics: SG_AEMFORMS/categories/maintaining_the_aem_forms_database
products: SG_EXPERIENCEMANAGER/6.4/FORMS
discoiquuid: 03e134c0-f9be-45c1-9c9f-10733ef2b43f
index: y
internal: n
snippet: y
---

# Purging process data{#purging-process-data}

Process data that is generated when a long-lived process is invoked can become too large, resulting in lower AEM forms performance and the use of unnecessary disk space. It is good practice to purge process data when records are no longer necessary. AEM forms provides several means of purging process data:

* You can use administration console to perform a one-time purge of obsolete records related to long-lived processes, or to schedule regular automatic purges. (See [Purge records from the Job Manager database](../../../forms/using/admin-help/purge-records-job-manager-database.md#purge-records-from-the-job-manager-database).)
* You can use the AEM forms Java API and web service API to programmatically purge process data related to long-lived processes. (See "Purging Process Data" in [Programming with AEM forms](http://www.adobe.com/go/learn_aemforms_programming_63).)
* Use the process purge tool to purge processes based on the process name and other parameters. For details, see the process purge tool readme file, located in *[aem_forms root]*\sdk\misc\Foundation\ProcessPurgeTool\ReadMe.txt.
