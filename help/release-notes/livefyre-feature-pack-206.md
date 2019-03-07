---
title: Livefyre Feature Pack 2.0.6 Release Notes
seo-title: Livefyre Feature Pack 2.0.6 Release Notes
description: null
seo-description: null
uuid: 389a1926-1539-43ce-ba88-6db37241cebd
contentOwner: alba
discoiquuid: 69eaafcf-e98e-49f1-837f-48beca60fd5d
index: y
internal: n
snippet: y
---

# Livefyre Feature Pack 2.0.6 Release Notes{#livefyre-feature-pack-release-notes}

## Release Information {#release-information}

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody>
  <tr>
   <td>Products</td> 
   <td>Livefyre Feature Pack 2.0.6</td> 
  </tr>
  <tr>
   <td>Version</td> 
   <td>2.0.6</td> 
  </tr>
  <tr>
   <td>Type</td> 
   <td>Feature release</td> 
  </tr>
  <tr>
   <td>Date</td> 
   <td>August 31, 2018</td> 
  </tr>
  <tr>
   <td>Download URL<br /> </td> 
   <td>Contact your administrator</td> 
  </tr>
  <tr>
   <td>Compatibility (*)</td> 
   <td>AEM 6.4 SP1, 6.4, 6.3 GA, and 6.2 SP1</td> 
  </tr>
  <tr>
   <td>Description</td> 
   <td>This package allows you to integrate Livefyre's industry-leading curation capabilities with your AEM instance, allowing you to publish valuable user-generated content (UGC) from social networks to your site in minutes.</td> 
  </tr>
 </tbody>
</table>

## What is included in Livefyre Feature Pack 2.0.6 {#what-is-included-in-livefyre-feature-pack}

This package integrates Livefyre's industry leading curation capabilities with your AEM instance, allowing you to publish valuable user-generated content (UGC) from social networks to your site in minutes. There are 3 different components to this package:

**Import UGC Content into AEM Assets**

* Import Twitter and Instagram user-generated content (UGC) from Livefyre Studio to AEM Assets using the UGC Importer.
* Access your Livefyre Library.
* Search real-time on Twitter and Instagram using Livefyre Social Search.
* Manage Rights on the UGC.

**Add Livefyre Components to AEM Sites or Communities**

* Instantly build and customize dynamic and engaging experiences using a suite of Social Components including Maps, Galleries, and Media Walls.
* Publish UGC in AEM Sites or Communities.

**Import Product Catalogs into Livefyre with AEM Commerce**

* Seamlessly integrate your existing product catalogue into Livefyre to drive user engagement and conversion in your sites, as well as delivering shoppable UGC experiences.
* Edit or delete items in your AEM Commerce Product Catalog and automatically update changes in Livefyre.

For help with installation, see [Integrating with Livefyre](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html).

### Additional Release Information {#additional-release-information}

Due to updates affecting the aggregation of content from Instagram non-business user accounts, we can no longer post comments on your behalf or automatically check for replies from the author. [Click here to find out more](https://developers.facebook.com/blog/post/2018/04/04/facebook-api-platform-product-changes/).

>[!NOTE]
>
>Livefyre Feature Pack 2.0.6 does not support AEM Classic UI.

#### New feature or improvement {#new-feature-or-improvement}

* Added the ability to search UGC before setting up rights request social accounts in Livefyre. You must setup social accounts to request rights, or override the rights request if you own the content. 
* Instagram and Twitter [UGC rights request workflow](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) has been updated to comply with latest APIs.
* Rights status and appropriate actions are now displayed on the rights request screen.

#### Bug fixes {#bug-fixes}

* Fixed an issue where deleting a social account in Livefyre Studio used for rights request caused an error when loading the UGC library in AEM. 
* Fixed an issue where asset count in Livefyre studio did not match asset count in the AEM UGC library. 
* Fixed an issue in the UGC library where filtered results displayed after the filter options were reset. 
* Fixed an issue with AEM Commerce where call-to-action buttons redirected users to the incorrect URL. 
* Fixed an issue in AEM Sites where dragging and dropping multiple components into the parsys placeholder caused it to disappear. 
* Fixed an issue where disabled social accounts were available to select from when sending a rights request.
* Fixed an issue where dragging and dropping UGC from Assets into Sites produced an error.
* Fixed an issue where dragging and dropping Chat and Liveblog components into Sites did not create the App.
* Fixed an issue where the Comment App produced an error when users attempted to comment. 
* Fixed an issue where adding the Livefyre Media Wall App to a site created an extra node in the Java Content Repository.
* Fixed an issue causing page breaks and console errors in Instagram UGC search.
* Fixed an issue where Instagram user icons were generating API errors in Assets. 
* Fixed an issue where the Reviews app was being added to a site with no predefined format. 
* Fixed an issue with Touch UI functionality and inline editing.
* Fixed an issue causing an error when importing certain Instagram image assets.
* Fixed an issue where the Livefyre HTTP Client in AEM did not support proxy configuration.
