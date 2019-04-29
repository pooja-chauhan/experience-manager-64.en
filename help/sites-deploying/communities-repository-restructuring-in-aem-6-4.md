---
title: Repository Restructuring for AEM Communities in 6.4
seo-title: Repository Restructuring for AEM Communities in 6.4
description: Learn how to make the necessary changes in order to migrate to the new repository structure in AEM 6.4 for Communities.
seo-description: Learn how to make the necessary changes in order to migrate to the new repository structure in AEM 6.4 for Communities.
uuid: d161655f-4074-44a7-8d69-38e80934c58b
products: SG_EXPERIENCEMANAGER/6.4/SITES
content-type: reference
topic-tags: repo_restructuring
discoiquuid: 7383265b-0ed4-4ea7-b741-0a417d187bdd
---

# Repository Restructuring for AEM Communities in 6.4{#repository-restructuring-for-aem-communities-in}

As described on the parent [Repository Restructuring in AEM 6.4](/help/sites-deploying/repository-restructuring.md) page, customers upgrading to AEM 6.4 should use this page to assess the work effort associated with repository changes impacting the AEM Communities Solution. Some changes require work effort during the AEM 6.4 upgrade process, while others can be deferred until a 6.5 upgrade.

**With 6.4 Upgrade**

* [E-mail Notification Templates](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#e-mail-notification-templates)
* [Subscription Configurations](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#subscription-configurations)

**Prior to 6.5 Upgrade**

* [Badging Configurations](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#badging-configurations)
* [Classic Communities Console Designs](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#classic-communities-console-designs)
* [Facebook Social Login Configurations](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#facebook-social-login-configurations)
* [Language Options Configurations](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#language-options-configurations)  

* [Pinterest Social Login Configurations](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#pinterest-social-login-configurations)
* [Scoring Configurations](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#scoring-configurations)
* [Twitter Social Login Configurations](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#twitter-social-login-configurations)
* [Misc](/help/sites-deploying/communities-repository-restructuring-in-aem-6-4.md#misc)

## With 6.4 Upgrade {#with-upgrade}

### E-mail Notification Templates {#e-mail-notification-templates}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/community/notifications</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><span class="code">/libs/settings/community/notifications</span></td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td><p>Manual migration ia needed if you want to move to new path under "<span class="code">/apps/settings</span>". You can use the Granite Configuration Manager to perform the migration.</p> <p>You can perform the migration by setting the property <span class="code">mergeList</span> to <span class="code">true</span> on the "<span class="code">/libs/settings/community/subscriptions</span>" node and add an <span class="code">nt:unstructured</span> child node.</p> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

### Subscription Configurations {#subscription-configurations}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/community/subscriptions</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><span class="code">/libs/settings/community/subscriptions</span></td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td><p>Manual migration ia needed if you want to move to new path under "<span class="code">/apps/settings</span>". You can use the Granite Configuration Manager to perform the migration.</p> <p>You can perform the migration by setting the property <span class="code">mergeList</span> to <span class="code">true</span> on the "<span class="code">/libs/settings/community/subscriptions</span>" node and add an <span class="code">nt:unstructured</span> child node.</p> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

### Watchwords Configurations {#watchwords-configurations}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td>/etc/watchwords</td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td>/libs/community/watchwords</td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td>A Lazy Migration task is available to clean up the Communities Configurations.<br /> <p>The Task moves watchwords from <span class="code">/etc/watchwords</span> to <span class="code">/conf/global/settings/community/watchwords</span>.</p> <p>If customized watchwords are stored in SCM, then they should be deployed to <span class="code">/apps/settings/...</span> and you must ensure that there is not an overlaying <span class="code">/conf/global/settings/...</span> configuration that would take precedence.</p> <p>Migration task removes <span class="code">/etc</span> locations.</p> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

## Prior to 6.5 Upgrade {#prior-to-upgrade}

### Badging Configurations {#badging-configurations}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/community/badging</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><p><strong>Badge Rules:</strong></p> <p><span class="code">/libs/settings/community/badging</span></p> <p><strong>Badge Images:</strong></p> <p>For default images: <span class="code">/etc/community/badging/images are moved to /libs/community/badging/images</span></p> <p>For custom images: <span class="code">/content/community/badging/images</span></p> <p> </p> </td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td><p>Manual Migration is required.</p> <p>If your instance has customized the badging/scoring rules, there is no automated way to place all the rules under a bucket. Need customer inputs on which conf bucket (global or sitespecific) you want to use for your site.</p> <p>No UI available to configure the badging and scoring for a site.</p> <p>To align with new repository structure:</p> 
    <ol> 
     <li>Create a site context bucket using the <strong>Configuration Browser</strong> under <strong>Tools</strong></li> 
     <li>Go to the Site root</li> 
     <li>Set <span class="code">cq:confproperty</span> to the bucket path where you want to store all your settings. The same can be set via the site <strong>Edit Wizard - Set cloud config input</strong>.</li> 
     <li>Move relevant badging rules and scoring rules from <span class="code">/etc/community/*</span> to the site context bucket created in the previous step.</li> 
     <li>Adjust badging Rules and scoring Rules properties on site root to have relative references to new rule locations. 
      <ol> 
       <li>For example, if the poperty for <span class="code">cq:conf = /conf/we-retail</span>, then <span class="code">badgingRules [] = community/badging/rules</span> if rules are now moved to this new bucket.</li> 
      </ol> </li> 
     <li>Similarly, adjust the references to scoring rules in a badging rule node to have a relativepath.</li> 
    </ol> <p> </p> <p>Finally, clean up by removing the resource <span class="code">/etc/community/badging</span></p> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

### Classic Communities Console Designs {#classic-communities-console-designs}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/designs/social/console</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><p><span class="code">/libs/settings/wcm/designs/social/console</span></p> <p><span class="code">/apps/settings/wcm/designs/social/console</span></p> </td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td>N/A</td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

### Facebook Social Login Configurations {#facebook-social-login-configurations}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/cloudservices/facebookconnect</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><p><code class="code">/conf/global/settings/cloudconfigs/facebookconnect
       </code></p> <p><span class="code">/conf/&lt;tenant&gt;/settings/cloudconfigs/facebookconnect</span></p> <p> </p> </td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td><p>Any new Facebook Cloud Configurations must be migrated to the New Location.</p> 
    <ol> 
     <li>Migrate existing configurations in the Previous Location to the New Location.
      <ol> 
       <li>Manually recreate new Facebook Social Login Configurations via the AEM authoring UI at <strong>Tools &gt; Cloud Services &gt; Facebook Social Login Configuration</strong>.<br /> or <br /> </li> 
       <li>Copy any new Facebook Cloud Configurations from Previous Location to the appropriate New Location, under <span class="code">/conf/global or /conf/&lt;tenant&gt;</span>.</li> 
      </ol> </li> 
     <li>Update any AEM Communities Site root to reference the new Facebook Social Login Configuration by setting the <span class="code">[cq:Page]/jcr:content@cq:conf</span> property to the absolute path in the New Location.</li> 
     <li>Disassociate the legacy Facebook Connect Cloud Service from any AEM Communities site roots updated to reference the New Location.</li> 
    </ol> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

### Language Options Configurations {#language-options-configurations}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/social/config/languageOpts</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><span class="code">/libs/social/translation/languageOpts</span></td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

### Pinterest Social Login Configurations {#pinterest-social-login-configurations}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/cloudservices/pinterestconnect</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><p><code class="code">/conf/global/settings/cloudconfigs/pinterestconnect
       </code></p> <p><span class="code">/conf/&lt;tenant&gt;/settings/cloudconfigs/pinterestconnect</span></p> <p> </p> </td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td><p>Any new Pinterest Cloud Configurations must be migrated to the New Location.</p> 
    <ol> 
     <li>Migrate existing configurations in the Previous Location to the New Location.
      <ol> 
       <li>Manually recreate new Pinterest Social Login Configurations via the AEM authoring UI at <strong>Tools &gt; Cloud Services &gt; Pinterest Social Login Configuration</strong>.<br /> or</li> 
       <li>Copy any new Pinterest Cloud Configurations from Previous Location to the appropriate New Location under <span class="code">/conf/global or /conf/&lt;tenant&gt;</span>.</li> 
      </ol> </li> 
     <li>Update any AEM Communities Site root to reference the new Pinterest Social Login Configuration by settings the <span class="code">[cq:Page]/jcr:content@cq:conf</span> property to the absolute path in the New Location.</li> 
     <li>Disassociate the legacy Pinterest Connect Cloud Service from any AEM Communities site roots updated to reference the New Location.</li> 
    </ol> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

### Scoring Configurations {#scoring-configurations}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/community/scoring</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><span class="code">/libs/settings/community/scoring</span></td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td><p>To align with new repository structure, scoring rules can be stored in <span class="code">/apps/settings/</span> or /<span class="code">conf/.../settings</span></p> 
    <ol> 
     <li>For <span class="code">/apps/settings</span>, this would act as global or default rules managed in SCM.</li> 
    </ol> <p>Create context-aware configs in <span class="code">/conf/</span> by using CRXDELite:</p> 
    <ol> 
     <li>Create the configs in the desired <span class="code">/conf/.../settings</span> location<br /> </li> 
     <li>Communities site must have the <span class="code">cq:conf </span>property property set.
      <ol> 
       <li>If no <span class="code">cq:conf</span> is set, scoring rules would be directly read from the given path for property '<span class="code">scoringRules</span>' at the site's root node, for example: <span class="code">/content/we-retail/us/en/community/jcr:content</span></li> 
      </ol> </li> 
    </ol> <p>Cleanup: Remove the resource <span class="code">/etc/community/scoring</span></p> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

### Twitter Social Login Configurations {#twitter-social-login-configurations}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/cloudservices/twitterconnect</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><p><code class="code">/conf/global/settings/cloudconfigs/twitterconnect
       </code></p> <p><span class="code">/conf/&lt;tenant&gt;/settings/cloudconfigs/twitterconnect</span></p> <p> </p> </td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td><p>Any new Twitter Cloud Configurations must be migrated to the New Location.</p> 
    <ol> 
     <li>Migrate existing configurations in the Previous Location to the New Location.
      <ol> 
       <li>Manually recreate new Twitter Social Login Configurations via the AEM authoring UI at <strong>Tools &gt; Cloud Services &gt; Twitter Social Login Configuration</strong>.<br /> or <br /> </li> 
       <li>Copy any new Twitter Cloud Configurations from Previous Location to the appropriate New Location, under <span class="code">/conf/global or /conf/&lt;tenant&gt;</span>.</li> 
      </ol> </li> 
     <li>Update any AEM Communities Site root to reference the new Twitter Social Login Configuration by setting the <span class="code">[cq:Page]/jcr:content@cq:conf</span> property to the absolute path in the New Location.</li> 
     <li>Disassociate the legacy Twitter Connect Cloud Service from any AEM Communities site roots updated to reference the New Location.</li> 
    </ol> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>N/A<br /> </td> 
  </tr>
 </tbody>
</table>

### Misc {#misc}

<table> 
 <tbody>
  <tr>
   <td><strong>Previous location</strong></td> 
   <td><span class="code">/etc/community/templates</span></td> 
  </tr>
  <tr>
   <td><strong>New location(s)</strong></td> 
   <td><span class="code">/libs/settings/community/templates</span></td> 
  </tr>
  <tr>
   <td><strong>Restructuring guidance</strong></td> 
   <td><p>Adobe has provided a migration utility at:</p> <p><a href="https://github.com/Adobe-Marketing-Cloud/aem-communities-ugc-migration/tree/master/bundles/communities-template-migration">https://github.com/Adobe-Marketing-Cloud/aem-communities-ugc-migration/tree/master/bundles/communities-template-migration</a></p> </td> 
  </tr>
  <tr>
   <td><strong>Notes</strong></td> 
   <td>The existing custom templates would move to <span class="code">/conf/global/settings/community/template/&lt;groups/sites/functions&gt;</span></td> 
  </tr>
 </tbody>
</table>
