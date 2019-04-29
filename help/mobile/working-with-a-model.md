---
title: Working with Models
seo-title: Working with Models
description: null
seo-description: null
uuid: e593b5cf-5b28-4910-b9e3-ebed2381f6d7
contentOwner: Jyotika Syal
content-type: reference
discoiquuid: 2d956042-56d4-4f84-a0e3-e72ce204340a
noindex: true
redirecttarget: /content/help/en/experience-manager/6-4/mobile/using/administer-mobile-apps
---

# Working with Models{#working-with-models}

>[!NOTE]
>
>Adobe recommends using the SPA Editor for projects that require single page application framework-based client-side rendering (e.g. React). [Learn more](/help/sites-developing/spa-overview.md).

A model describes a type of content and denotes what will be information will be available to the native application. This section explains the creation of new models.

>[!CAUTION]
>
>**Prerequisites for creating a model**
>
>Models can only be created under nodes that have been enabled by the Configuration Browser. The Configuration Browser also allows permissions to be defined so different users may only have access to the creation of models under certain configurations.
>
>See, **Enabling Data Models** in ** [Administering Content Services](/help/mobile/developing-content-services.md)** for detailed steps.

1.

## Creating a Model {#creating-a-model}

>[!NOTE]
>
>To get started creating models a model type must exist. A model type defines the default state for each model created from it as well as the data types available to that model.

Once you have defined the configurations in the Configuration Browser, you can create and manage your models in the application dashborad. The following steps describe the model creation flow:

1. Navigate to the Models console and choose the configuration.

   ![](assets/chlimage_1.png)

1. Click **Create** to create a new model.
1. Choose the type of template: **Entity Group** or **Primitives Types Model**. Click **Next**.

   ![](assets/chlimage_1-1.png)

1. Enter the **Model Title** and **Description**. Click **Create** to create a model.

   ![](assets/chlimage_1-2.png)

   >[!NOTE]
   >
   >Once you create a model, click **Done** to open the **Data Model Editor **to add the data types and set properties to the editor.

   If you created your model using the Entity Group as the template, you will only view options such as Properties, Copy and Delete for that created model.

   ![](assets/chlimage_1-3.png)

   If you created your model using the **Primitives Model Type** as the template, you will only view options such as Edit, Properties, Copy and Delete for that created model.

   ![](assets/chlimage_1-4.png)

1. If you choose the template as **Primitive Models type**, click **Edit** to add the data types using the **Data Model Editor**.

   ![](assets/chlimage_1-5.png)

   Or, if you are using the **Entity Template** for your model, then click on view properties to upload an image or get more information on the defined model.

   ![](assets/chlimage_1-6.png)

   >[!NOTE]
   >
   >Alternatively, you can create your own custom models. See Models in Repository to create your own models and define data types.

## Managing a Model {#managing-a-model}

Managing a model involves viewing properties, editing, and deleting a model.

**Viewing a Model** The following steps are required for reading/viewing a model:

1. Navigate to the Model Console
1. Select the model from the list by clicking on its icon
1. Choose **Properties** from the toolbar icons
1. Click **Save & Close** or **Save** when done

**Editing a Model** The following steps are required for editing a model:

1. Navigate to the Model Console
1. Select the model from the list by clicking on its icon
1. Choose **Edit** from the toolbar icons to open the **Data Model Editor**.

1. Make changes to the model
1. Click **Save** when done

>[!NOTE]
>
>You can only edit a **Primitive Model Type**.

**Reading a Model** The following steps are required for editing a model:

1. Navigate to the Model Console
1. Select the model from the list by clicking on its icon
1. Choose **Properties** from the toolbar icons
1. Make changes to the model
1. Click Save when done

**Deleting a Model** The following steps are required for deleting a model:

1. Navigate to the Model Console
1. Select the model from the list by clicking on its icon
1. Click Delete

Deleting a model will not delete entities generated from that model.

### Additional Resources {#additional-resources}

Once you learn how to create models as an author, see

* [Spaces and Entities](/help/mobile/spaces-and-entities.md)
* [Developing Models](/help/mobile/models-in-repository.md)
* [Content Delivery and Rendering](/help/mobile/rendering-and-delivery.md)
