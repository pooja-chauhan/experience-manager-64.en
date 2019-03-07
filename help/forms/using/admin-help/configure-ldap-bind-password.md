---
title: Configure the LDAP bind password
seo-title: Configure the LDAP bind password
description: Learn how to configure the bind password field before you import the configuration file into another system. 
seo-description: Learn how to configure the bind password field before you import the configuration file into another system. 
uuid: 465c9068-ec65-4801-8a9a-d99e856afe6b
contentOwner: admin
content-type: reference
geptopics: SG_AEMFORMS/categories/configuring_user_management
products: SG_EXPERIENCEMANAGER/6.4/FORMS
discoiquuid: cfcea199-2075-4c22-b41c-420ee8314ae8
index: y
internal: n
snippet: y
---

# Configure the LDAP bind password{#configure-the-ldap-bind-password}

To avoid security risks, the bind password field in the exported configuration file (config.xml) is not configured. Before you import the configuration file into another system, ensure that you configure this password. This password overrides an existing password that is stored in the database. A null password does not override an existing non-null password value.

1. In administration console, click Settings &gt; User Management &gt; Configuration &gt; Import And Export Configuration Files.
1. To export the current configuration setting to a file, click Export and save the configuration file in another location.
1. In the file, locate the `Domains` > *[Your domain name]* > `DirectoryConfigs` > `LDAPGroupConfig` node. Here is an example:

   ```as3
    <node name="LDAPGroupConfig"> 
        <map> 
            <entry key="bindanonymously" value="false" />  
            <entry key="basedn" value="dc=corp,dc=adobe,dc=com" />  
            <entry key="batchSize" value="200" />  
            <entry key="binduser" value="cn=Directory Manager" />  
            <entry key="bindpassword" value="" /> 
        </map>
   ```

   Type a value for `bindpassword` and save your changes.

1. In the file, locate the `Domains` > *[Your domain name]* > `DirectoryConfigs` > `LDAPGroupConfig` > `LDAPUserConfig` node. Here is an example:

   ```as3
    <node name="LDAPUserConfig"> 
        <map> 
            <entry key="bindanonymously" value="false" />  
            <entry key="batchSize" value="200" />  
            <entry key="basedn" value="dc=corp,dc=adobe,dc=com" />  
            <entry key="bindpassword" value="" /> 
            <entry key="binduser" value="cn=Directory Manager" />  
        </map>
   ```

   Type a value for `bindpassword` and save your changes.

1. To import the updated file, in User Management, click Configuration &gt; Import And Export Configuration Files.
1. Click Browse to find the file, click Import, and then click OK.
